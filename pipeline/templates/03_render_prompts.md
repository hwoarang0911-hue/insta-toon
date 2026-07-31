# [epNNN] 제목 — 이미지 렌더링 지시서

6장 각각에 대해 나노바나나(Gemini)용과 GPT용 프롬프트를 모두 제공한다.
사용자는 도구를 골라 해당 프롬프트만 복사해 쓰면 된다.

> ## ⚠️ 프롬프트 안의 한글 문구 = 이미지에 그려질 글자
> 따옴표 안 문구는 `02_storyboard.md`의 **「이미지에 들어가는 글자」 표와
> 글자 하나까지 같아야 한다.** 콘티 대사가 바뀌면 이 파일도 즉시 따라간다.
> 프롬프트를 쓰기 전에 그 표를 먼저 열어 대조한다.

# 0. 표지(1장) — 실사 배경 콜라주 (예외 워크플로)

> **표지만 다른 5장과 만드는 방식이 다르다.** 배경은 실제 사진, 캐릭터는 손그림 컷아웃을 합성한다.
> 컷1~4·여운(2~6장)은 아래 「🚀 한 번에 전달하기」로 넘어간다.
> (`brand/03_DRAWING_STYLE.md` 표지 예외, `brand/06_IMAGE_RULE.md` 표지 합성 절차 참고)

## 실행 순서 (4단계)
1. 에피소드 실제 장소의 사진을 준비한다 (직접 촬영 또는 출처가 분명한 사진)
2. 아래 캐릭터 컷아웃 프롬프트로 **배경 없는 캐릭터만** 생성 (character_sheet.png 첨부)
3. 사진 편집 툴(캔바, 미리캔버스, 포토샵 등)에서 사진 위에 캐릭터 컷아웃을 배치, 흰 테두리를 살려 스티커처럼 보이게 한다
4. 표지 문구를 손글씨 느낌 폰트로 얹는다: "(표지 문구)"

### 캐릭터 컷아웃 프롬프트 — 한국어판 (Gemini/나노바나나)
```
첨부한 캐릭터 시트의 루아를 그대로 유지해서 그려줘.
[포즈·표정 묘사 — 콘티의 표지 장면 참고]
배경은 순백색으로, 캐릭터만 오려내기 쉽게 그려줘. 배경 요소는 아무것도 넣지 마.
스타일: 손으로 그린 만년필 펜 스케치, 불규칙한 선, 흑백, 해칭 음영.
금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 그라데이션, 배경 요소 일체.
정사각형 1:1 비율.
```

### 캐릭터 컷아웃 프롬프트 — 영어판 (ChatGPT)
```
Keep the exact same character (Lua) from the attached character sheet:
a Korean woman in her mid-20s, shoulder-length wavy black hair,
tiny dot eyes, calm minimal expression, plain long-sleeve top and wide pants.
Pose/expression: [scene description translated from the storyboard's cover panel]
Background: pure flat white, nothing else — the character must be easy to cut out cleanly.
Style: hand-drawn fountain pen sketch, irregular wobbly ink lines,
black and white, hatching for shade.
Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, gradients, any background elements.
Square 1:1 aspect ratio.
```

---

# 🚀 한 번에 전달하기 (컷1~4 + 여운 · 2~6장)

> **매 화 반드시 작성한다.** 사용자가 이미지 AI에 한 번 붙여넣어 나머지 5장을 뽑는 실물이다.
> 링크·외부 참조 없이 **이것만으로 완결**되어야 한다 (캐릭터 스펙·그림체·금지·비율 포함).
> 표지(1장)는 여기 포함되지 않는다 — 위 0번 워크플로로 별도 제작한다.

## 실행 순서 (3단계)
1. 이미지 생성 AI에 **`assets/character_sheet.png` 첨부**
2. 아래 통합 프롬프트를 **통째로 복사해 붙여넣기** (도구에 맞는 언어판)
3. 컷1(2장)이 나오면 **그 이미지를 첨부하고 "다음 장"** → 여운(6장)까지 반복

---

## (A) 통합 프롬프트 — 한국어판 · Gemini / 나노바나나용

```
인스타툰의 컷1~4와 마지막 여운 장, 5장짜리를 만들 거야 (표지는 별도로 만든다). 시작 전에 중요한 규칙 두 가지.

❗ 규칙 1 — 5장을 한 이미지에 모아 그리지 마.
   각 장은 완전히 독립된 별개의 이미지다. 한 이미지 = 한 장면 하나.
   격자 배치, 콜라주, 4컷 만화식 분할, 여러 장면을 한 화면에 넣기 전부 금지.

❗ 규칙 2 — 지금은 아래 [2장 · 컷1]만 만들어.
   3~6장은 내가 "다음 장"이라고 말할 때까지 만들지 마.
   아래에 전체 목록을 미리 주는 건 그림체와 이야기 흐름을 알려주기 위해서다.

[모든 장에 공통 적용]
· 캐릭터: 20대 한국 여성. 어깨에 닿는 검은 웨이브 단발, 작은 점 같은 눈,
  담백한 표정, 무지 긴팔 상의와 통 넓은 바지, 각진 토트백.
  첨부한 캐릭터 시트의 인물을 그대로 유지할 것.
· 그림체: 손으로 그린 만년필 펜 스케치. 선이 불규칙하고 굵기가 일정하지 않다.
  흑백, 오프화이트 종이 배경, 음영은 해칭(빗금)으로만.
  배경은 미니멀하게, 여백을 많이 남긴다 (표지와 달리 실사 배경 없음 — 전부 손그림 배경).
· 금지: 3D, 사실적인 피부, 일본 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경.
· 비율: 정사각형 1:1
· 각 장에 지정된 한글 텍스트를 이미지 안에 손글씨 느낌으로 정확히 넣을 것.
· 3장부터는 직전에 만든 그림의 인물과 선 스타일을 그대로 이어갈 것.

=== 지금 만들 것 ===
[2장 · 컷1]
(장면 묘사)
넣을 글자 — "(컷1 대사)"

=== 아래는 이후 순서. 지금 만들지 말 것 ===
[3장] ~ [6장]  ← 콘티의 「이미지에 들어가는 글자」 표와 문구가 일치해야 한다
```

---

## (B) 통합 프롬프트 — 영어판 · ChatGPT용

```
I am making an Instagram comic series — panels 2 through 6 (cut1-4 plus a closing panel;
the cover panel is made separately). Two critical rules first.

IMPORTANT 1 — Do NOT combine the panels into one image.
   Each panel is a completely separate, standalone image. One image = one scene.
   No grids, no collages, no 4-panel comic layouts, no multiple scenes in one frame.

IMPORTANT 2 — Generate ONLY [Panel 2] right now.
   Do not generate panels 3-6 until I say "next".
   The full list below is given in advance only so you know the art style and story flow.

[Apply to every panel]
· Character: a Korean woman in her mid-20s. Shoulder-length wavy black hair,
  tiny dot eyes, calm minimal expression, plain long-sleeve top, wide-leg pants,
  a boxy tote bag. Keep the exact same character as the attached character sheet.
· Style: hand-drawn fountain pen sketch. Irregular, wobbly ink lines of uneven
  weight. Black and white on off-white paper. Shading only through hatching.
  Minimal background, generous negative space (unlike the cover, no photo background —
  every background here is hand-drawn).
· Avoid: 3D, realistic skin, Japanese anime style, glossy webtoon coloring,
  gradients, complex backgrounds.
· Aspect ratio: square 1:1
· Render the Korean text specified for each panel inside the image, in neat
  handwriting style, exactly as written.
· From panel 3 onward, carry over the character and line style of the previous image.

=== GENERATE PANEL 2 ONLY. THE REST COME LATER ===
[Panel 2 ~ 6]  ← 한글 문구는 원문 그대로 (번역하지 않는다)
```

---

## (C) 링크로 전달하려면

저장소가 private이면 외부 AI가 raw 링크를 읽지 못한다. 둘 중 하나를 쓴다:
- **Secret Gist** (권장): 통합 프롬프트만 gist.github.com에 Secret으로 올리고 Raw URL 사용
- 저장소 public 전환 (브랜드 문서가 전부 공개되므로 신중히)

※ 어느 방법이든 **캐릭터 시트는 직접 첨부**한다.

## (D) 후보정용 글자표
한글이 깨지면 텍스트 없이 생성 후 `02_storyboard.md`의 「이미지에 들어가는 글자」 표 기준으로 손글씨 폰트 삽입.

---
---

# 컷별 상세 프롬프트

> 통합 프롬프트로 만족스럽지 않은 컷만 아래에서 골라 다시 돌린다.
> **표지(1장)는 여기 포함되지 않는다** — 위 0번의 컷아웃 프롬프트를 쓴다. 아래는 컷1~4·여운(2~6장)만 해당.

## 공통 준비물
- 참조 1: `assets/character_sheet.png` — **모든 컷에 첨부**
- 참조 2: 직전에 생성한 컷 이미지 — **3장부터 첨부** (연속성)
- 스타일 흔들림 시: `assets/samples/sample_4cut_bruckner_mahler.png` 추가 첨부

## 스타일 고정 문구 (매 컷 프롬프트에 포함됨)
- 한국어: "손으로 그린 만년필 펜 스케치, 불규칙한 선, 흑백, 오프화이트 배경, 해칭 음영, 미니멀한 배경, 여백 많음"
- 영어: "hand-drawn fountain pen sketch, irregular wobbly ink lines, black and white, off-white paper background, hatching for shade, minimal background, generous negative space"
- 네거티브(금지): "3D, realistic skin, anime style, glossy webtoon coloring, gradients, complex background" / "3D, 사실적 피부, 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경 금지"

---

## N장 — (역할: 컷1/컷2/컷3/컷4/여운)   ← 2~6장 각각 반복

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png (+ 직전 컷)
>
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘.
> [장면 묘사 — 콘티의 장면·카메라·표정·구도를 자연어로]
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 정확히 넣어줘:
> "[화면 텍스트 원문]"
> 스타일: 손으로 그린 만년필 펜 스케치, 불규칙한 선, 흑백,
> 오프화이트 배경, 해칭 음영, 미니멀한 배경, 여백 많음.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경.
> 정사각형 1:1 비율.
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png (+ 직전 컷)
>
> ```
> Keep the exact same character (Lua) from the attached character sheet:
> a Korean woman in her mid-20s, shoulder-length wavy black hair,
> tiny dot eyes, calm minimal expression, plain long-sleeve top and wide pants.
> Scene: [장면 묘사 영어 번역 — 카메라·표정·구도 포함]
> Render this Korean text in neat handwriting style: "[화면 텍스트 원문]"
> Style: hand-drawn fountain pen sketch, irregular wobbly ink lines,
> black and white, off-white paper background, hatching for shade,
> minimal background, generous negative space.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background.
> Square 1:1 aspect ratio.
> ```
> ※ 한글이 깨지면 텍스트 없이 생성 후 손글씨 폰트로 후삽입.

---

## Stage 3 체크리스트
- [ ] 표지(1장)는 0번 실사 배경 콜라주 워크플로로 별도 작성됐는가 (나머지 5장과 다른 방식)
- [ ] 컷1~4·여운(2~6장) 모두 character_sheet.png 첨부 지시 포함
- [ ] 3장부터 직전 컷 첨부 지시 포함
- [ ] 매 컷 스타일 고정 문구 + 금지 문구 포함
- [ ] 화면 텍스트 원문이 따옴표로 정확히 명시됨
