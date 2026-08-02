# 자연스러움 검수 — 실행 절차

> **검수 기준의 원문은 `brand/11_STORY_TYPES.md` 11장이다.**
> 이 문서는 그 체크리스트를 **어떻게 돌리는지**만 정의한다. 기준을 여기에 복제하지 않는다.

> ## ⚠️ 이건 통과 게이트가 아니라 점검 도구다
> **항목을 못 맞췄다고 이야기를 깎지 않는다.** 다 쓴 뒤 한 번 훑어보는 용도다.
> 특히 아래 세 가지는 수치를 맞추려다 이야기를 망치기 쉬우니 주의한다:
> - **대사 글자수** — 사색이 살아있는 문장을 글자수 때문에 자르지 않는다
> - **무대사 컷 개수** — 개수를 채우려고 필요한 독백을 지우지 않는다
> - **삭제 테스트** — **교훈으로 확장한 문장**을 지우라는 뜻이지, 루아가 알아챈 것 자체를 지우라는 뜻이 아니다
>
> 정말 작위적일 때(관념에서 출발했거나, 마지막이 교훈이거나, 캐릭터가 작가처럼 말할 때)만 다시 쓴다.

Stage 2(콘티)를 마친 뒤 아래 순서로 훑는다.

---

## 1. 체크리스트 14항목

`brand/11_STORY_TYPES.md` **11장**의 표를 그대로 사용한다.
결과는 `02_storyboard.md`의 「검수 체크리스트 14항목」 표에 기록한다.

## 2. Naturalness Review 9항목

`brand/11_STORY_TYPES.md` **13장** 템플릿 하단의 9개 항목.
`02_storyboard.md`의 「Naturalness Review」에 기록한다.

## 3. 최종 삭제 테스트

마지막 독백을 삭제해본다. **대상은 「교훈으로 확장한 문장」이다.**

| 삭제 대상 | 남길 것 |
|---|---|
| "우리 인생도 그렇게 매일 달라지는 게 아닐까" | "아, 물은 원래 계속 다른 거구나" |
| "소중한 건 결국 이런 순간이다" | "그 사람도 이렇게 오래 앉아서 물을 봤겠지" |

- 삭제해도 이야기의 감정이 유지되면 그대로 삭제한다
- 삭제하면 전혀 이해되지 않으면 행동이나 구도를 보완한다
- **루아가 그 자리에서 알아챈 것은 삭제 대상이 아니다.** 그게 이 툰의 목적지다

## 4. 금지 패턴 스캔

`brand/11_STORY_TYPES.md` **15장** — 메시지 선행형 / 명언 제조형 / 상징 과잉형 / 반전 강박형 / 감정 과장형 / 해설 중복형

## 5. 기계 스캔

### 경고 표현 (동 문서 8장)

```bash
grep -nE "결국|어쩌면|문득|그제야|우리 모두|인생|진정한|소중한|깨았다|깨달았다|의미 있는|나다운|본질|행복이란" \
  episodes/epNNN_*/02_storyboard.md episodes/epNNN_*/04_caption.md
```

### 대사 총 글자수 (동 문서 8장 유형별 상한)

```bash
python3 - <<'EOF'
import re,sys,glob
p = sorted(glob.glob("episodes/ep*/02_storyboard.md"))[-1]
seg = open(p).read().split("## 이미지에 들어가는 글자")[1].split("\n## ")[0]
rows = re.findall(r'^\|\s*(\d[^|]*?)\s*\|\s*([^|]*?)\s*\|\s*(.*?)\s*\|$', seg, re.M)
lines = [t for n,_,t in rows if t not in ("없음","문구","") and not n.startswith("1")]
print(p)
for l in lines: print(f"  {len(l.replace(chr(60)+'br'+chr(62),''))}자  {l}")
print("총", sum(len(l) for l in lines), "자")
EOF
```

| 유형 | 상한 | 유형 | 상한 |
|---|---|---|---|
| OBSERVE | 20~40자 | CINEMA | 0~15자 |
| RELATE | 25~60자 | CULTURE | 20~50자 |
| STORY | 30~70자 | DIARY | 10~40자 |
| TASTE | 15~45자 | DEADPAN | 20~55자 |
| REFLECTION | 30~70자 | SILENCE | 0자 |

### 구도 반복 (동 문서 10장)

```bash
python3 - <<'EOF'
import re,glob
p = sorted(glob.glob("episodes/ep*/02_storyboard.md"))[-1]
d = [x.strip() for x in re.findall(r'^\|\s*(?:CUT \d|CLOSING|컷\d|여운)\s*\|[^|]*\|\s*([^|]+)\|', open(p).read(), re.M)]
print(p, "→", " → ".join(d))
run=1
for i in range(1,len(d)):
    run = run+1 if d[i]==d[i-1] else 1
    if run>=3: print("  ✗ 동일 카메라 거리 3회 연속:", d[i])
else: print("  ✓ 3회 연속 없음")
EOF
```

### 콘티 ↔ 렌더 프롬프트 문구 일치

```bash
python3 - <<'EOF'
import re,glob
ep = sorted(glob.glob("episodes/ep*/"))[-1]
seg = open(ep+"02_storyboard.md").read().split("## 이미지에 들어가는 글자")[1].split("\n## ")[0]
rp  = open(ep+"03_render_prompts.md").read()
for n,_,t in re.findall(r'^\|\s*(\d[^|]*?)\s*\|\s*([^|]*?)\s*\|\s*(.*?)\s*\|$', seg, re.M):
    if t in ("없음","문구",""): continue
    print(("OK " if t.replace("<br>"," ") in rp or t.replace("<br>","\n") in rp else "✗✗ "), n, t[:50])
EOF
```

---

## 6. 연재 로테이션 점검 (동 문서 19장)

- [ ] 동일 유형 3회 이상 연속 아님
- [ ] 사색형 연속 게시 아님
- [ ] 직전이 CULTURE면 이번은 OBSERVE 또는 RELATE
- [ ] 무대사형(SILENCE) 누적 비율 10% 이내
- [ ] 유머형 다음에 분위기가 다른 유형
- [ ] 20화 기준 권장 비율(12장)에서 크게 벗어나지 않음

```bash
grep -h "^- Type:\|primary_type:" episodes/ep*/0[12]_*.md
```

## 7. 문서 간 정합성

- [ ] 본편 컷에 **에피소드 제목·컷 번호·다른 컷의 문구**가 없는가
- [ ] 캡션이 본편 문장을 복사하지 않았는가
- [ ] 캡션이 본편의 의미를 대신 설명하지 않는가
