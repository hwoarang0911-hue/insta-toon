# [epNNN] 제목 — 스토리 콘티

> ## ⚠️ 작성 순서를 지킨다
>
> 각 컷은 **`visible_action`을 먼저 쓰고, `dialogue`는 맨 마지막에** 쓴다.
> 대사를 먼저 쓰면 그림이 대사의 삽화가 된다. 이것이 감성 에세이처럼 읽히는 첫 번째 원인이다.
>
> **1단계** — 6장 전부의 `visible_action`만 채운다
> **2단계** — 구도·카메라 거리·연결을 채운다
> **3단계** — 그래도 없으면 안 되는 컷에만 대사를 넣는다
> **4단계** — 마지막 컷 삭제 테스트
> **5단계** — `pipeline/NATURALNESS_CHECKLIST.md` 통과

> ## ⚠️ 이 문서의 대사가 **이미지 안에 그려지는 글자**다
>
> | | 어디에 들어가나 |
> |---|---|
> | **스크립트** (이 문서의 대사) | **이미지 안에 손글씨로 렌더링된다.** 그림의 일부 |
> | 캡션 (`04_caption.md`) | 이미지 밖. 인스타그램 게시글 본문에 타이핑 |
>
> **이 문서의 대사를 고치면 `03_render_prompts.md`도 반드시 함께 고친다.**
> 문서 맨 아래 「이미지에 들어가는 글자」 표가 그 기준이다.

## 이 화의 설정 (01에서 가져옴)

```yaml
primary_type:
emotion_level:
concrete_event:
life_detail:
```

**대사 예산** — 유형별 가이드(`brand/11_STORY_TYPES.md` 6장)에 따라 대사 있는 컷 __개 / 총 __문장
**무대사 컷** — 최소 1컷 (어느 컷인지 미리 정한다: ____)

---

## 1장 — 표지

> 표지는 본편과 규칙이 다르다 (`brand/05_EPISODE_TEMPLATE.md`).
> 제목은 여기서 **한 번만** 노출한다. 본편에는 제목을 넣지 않는다.

- **화면 텍스트(제목)**:
- **대표 장면**: (본편에 실제로 나오는 장면. 새로 만들지 않는다)
- **카메라**:
- **표정**: (과장하지 않는다)
- **구도 메모**: 제목 스티커와 캐릭터가 겹치지 않게

## 2장 — 컷1

```yaml
visible_action:            # 먼저 작성
character_reaction:        # 표정 4종 안에서. 얼굴이 안 보이면 "해당 없음"
composition:               # 공간 와이드숏 / 캐릭터 중경 / 사물 클로즈업 / 캐릭터 시점 / 어깨너머 / 뒷모습 / 손·발 디테일 / 빈 풍경 / 얼굴 일부 / 위에서 / 바닥 가까이
camera_distance:           # 와이드 / 중경 / 클로즈업 / 디테일
background_detail:         # 필수 배경만
continuity_from_previous:  # (컷1은 비움)
dialogue:                  # 마지막에 작성. 비우는 것이 기본
```

## 3장 — 컷2

```yaml
visible_action:
character_reaction:
composition:
camera_distance:
background_detail:
continuity_from_previous:
dialogue:
```

## 4장 — 컷3

```yaml
visible_action:
character_reaction:
composition:
camera_distance:
background_detail:
continuity_from_previous:
dialogue:
```

## 5장 — 컷4

```yaml
visible_action:
character_reaction:
composition:
camera_distance:
background_detail:
continuity_from_previous:
dialogue:
```

## 6장 — 여운

```yaml
visible_action:            # 끝난 자리. 작은 행동 / 반복 / 풍경 / 침묵 / 시선 / 사물의 상태 변화
character_reaction:
composition:               # 뒷모습·빈 풍경·디테일 권장
camera_distance:
background_detail:
continuity_from_previous:
dialogue:                  # 0이 기본
```

### 마지막 컷 삭제 테스트 (필수)

> **마지막 독백을 삭제해도 에피소드가 유지되는가?**

- [ ] 유지된다 → **삭제했다**
- [ ] 유지되지 않는다 → 독백을 복구하지 않고 **행동·사물·구도를 고쳤다**

고친 내용:

---

## 구도 점검 (5컷 기준)

| 컷 | composition | camera_distance | 대사 |
|---|---|---|---|
| 컷1 | | | |
| 컷2 | | | |
| 컷3 | | | |
| 컷4 | | | |
| 여운 | | | |

- [ ] 와이드숏 1컷 이상
- [ ] 사물 또는 손 디테일숏 1컷 이상
- [ ] 캐릭터 얼굴 전체가 보이지 않는 컷 1컷 이상
- [ ] 무대사 컷 1컷 이상
- [ ] 동일한 카메라 거리 3회 이상 연속 없음

---

## 이미지에 들어가는 글자 (렌더링용 최종본)

> `03_render_prompts.md`의 따옴표 문구는 이 표와 **글자 하나까지** 같아야 한다.
> **표지 외의 컷에는 제목·컷 번호·다른 컷 문구를 넣지 않는다.**

| 장 | 위치 | 문구 |
|---|---|---|
| 1 표지 | 제목 | |
| 2 컷1 | | |
| 3 컷2 | | |
| 4 컷3 | | |
| 5 컷4 | | |
| 6 여운 | | |

(대사가 없는 컷은 「없음」이라고 적는다 — 비워두면 누락과 구분되지 않는다)

---

## Stage 2 체크리스트
- [ ] **모든 컷의 `visible_action`을 대사보다 먼저 썼는가**
- [ ] **대사 없이도 컷 흐름이 이해되는가**
- [ ] 무대사 컷이 최소 하나 있는가
- [ ] 완결된 감성 문장이 3개 미만인가
- [ ] 그림으로 보이는 것을 대사로 반복하지 않았는가
- [ ] 경고 표현을 스캔했는가
- [ ] 생활 디테일이 어느 컷엔가 실제로 그려지는가
- [ ] 구도 점검 5항목을 통과했는가
- [ ] 컷마다 `continuity_from_previous`가 채워졌는가
- [ ] **마지막 컷 삭제 테스트를 수행했는가**
- [ ] 마지막 컷이 교훈·요약·철학적 질문이 아닌가
- [ ] 본편 컷에 제목·컷 번호·다른 컷 문구가 없는가
- [ ] 표정이 4종 안에서 해결되는가 (얼굴 안 보이는 컷 포함)
- [ ] 「이미지에 들어가는 글자」 표를 채웠는가
- [ ] **`pipeline/NATURALNESS_CHECKLIST.md`를 끝까지 통과했는가**
