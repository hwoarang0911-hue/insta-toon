# [ep002] 물을 그린 피아니스트 — 이미지 렌더링 지시서

# 🚀 한 번에 전달하기

## 실행 순서 (3단계)
1. 이미지 생성 AI 대화창에 **`assets/character_sheet.png`를 첨부**한다
2. 아래 통합 프롬프트를 **통째로 복사해서 붙여넣는다** (도구에 맞는 언어판 선택)
3. 1장이 나오면 **그 이미지를 첨부하고 "다음 장"**이라고 한다 → 6장까지 반복
   *(직전 컷 첨부가 그림체 일관성의 핵심이라 이 단계만은 손으로 해야 한다)*

---

## (A) 통합 프롬프트 — 한국어판 · Gemini / 나노바나나용

> 한글 텍스트를 이미지에 직접 넣는 데 강하다. 이쪽을 우선 권장.

```
인스타툰 6장을 순서대로 만들어줘. 한 번에 한 장씩, 1장부터 6장까지.
내가 "다음 장"이라고 하면 다음 컷으로 넘어가.

[모든 장에 공통 적용]
· 캐릭터: 20대 한국 여성. 어깨에 닿는 검은 웨이브 단발, 작은 점 같은 눈,
  담백한 표정, 무지 긴팔 상의와 통 넓은 바지, 각진 토트백.
  첨부한 캐릭터 시트의 인물을 그대로 유지할 것.
· 그림체: 손으로 그린 만년필 펜 스케치. 선이 불규칙하고 굵기가 일정하지 않다.
  흑백, 오프화이트 종이 배경, 음영은 해칭(빗금)으로만.
  배경은 미니멀하게, 여백을 많이 남긴다.
· 금지: 3D, 사실적인 피부, 일본 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경.
· 비율: 정사각형 1:1
· 각 장에 지정된 한글 텍스트를 이미지 안에 손글씨 느낌으로 정확히 넣을 것.
· 2장부터는 직전에 만든 그림의 인물과 선 스타일을 그대로 이어갈 것.

[1장 · 표지]
이어폰을 낀 여성의 상반신 클로즈업. 고개를 살짝 기울여 아래를 내려다본다.
화면 하단 1/4에 잔잔한 물결 선 몇 줄, 그 사이에 작은 음표 두세 개.
넣을 글자 — 상단 제목: "물을 그린 피아니스트"

[2장]
해질녘 한강. 걷다 멈춘 여성이 강가 난간에 살짝 기대어 물을 내려다본다.
이어폰, 어깨에 토트백. 강은 화면 하단 절반, 하늘은 넓게.
강 건너 도시 스카이라인은 아주 가는 선으로 멀리 희미하게.
넣을 글자 — 상단 내레이션:
"퇴근길에 그냥 노들섬에서 내렸다.
듣고 있던 피아노가 자꾸 물소리처럼 들렸다."

[3장]
이어폰을 끼고 걷는 여성의 옆모습(허리 위).
이어폰에서 흘러나온 선율 한 줄이 왼쪽에서 오른쪽으로 길게 이어지며 모양이 변한다:
낮게 가라앉는 수평의 물결 → 가운데에서 잘게 반짝이는 물방울들 →
끝에서 위로 솟는 가는 물줄기 하나. 사람 초상이나 라벨 없이 선의 변화만으로.
넣을 글자 — 상단 내레이션:
"리스트가 쓴 곡에는 물에 대한 이야기가 유난히 많다.
호수도 있고, 샘도 있고, 분수도 있다."
하단에 작게: "그런데 이상하게 하나도 안 비슷하다. 왜 다 다르게 들리지?"

[4장]
문득 고개를 들어 강을 바라보는 여성(허리 위, 강과 마주 보는 구도).
강 수면의 결이 왼쪽에서 오른쪽으로 계속 달라진다:
왼쪽은 가로로 긴 해칭선의 잔잔한 물결, 가운데는 바람이 지나간 자국처럼
비스듬한 짧은 해칭, 오른쪽은 짧고 촘촘한 해칭으로 빛에 잘게 반짝임.
3장에서 그린 선율의 변화와 같은 리듬으로 그려서 두 컷이 겹쳐 보이게 할 것.
넣을 글자 — 상단 내레이션:
"그러다 문득 고개를 들었는데, 강이 아까랑 좀 달라 보였다.
바람이 한 번씩 불 때마다 물빛이 계속 바뀌고 있었다."

[5장]
강을 바라보는 여성의 옆모습(허리 위), 옅은 미소.
수면은 여전히 결이 살아 움직이는 채로. 배경은 강과 하늘만, 여백 크게.
넣을 글자 — 상단 내레이션:
"아, 물은 원래 계속 다른 거구나.
같은 강이어도 볼 때마다 다르다."
하단에 작게: "그 사람도 이렇게 오래 앉아서 물을 봤겠지."

[6장 · 여운]
멀리서 본 강가. 난간에 기대 물을 보는 여성의 작은 뒷모습.
해가 거의 저문 하늘에 별 하나. 물결 선은 아주 잔잔하게 최소한으로.
인물과 난간은 화면 하단 1/3에 작게, 나머지는 넓은 여백(화면의 60% 이상).
넣을 글자 — 상단 여백: "해가 다 질 때까지 그냥 좀 더 서 있었다."
```

---

## (B) 통합 프롬프트 — 영어판 · ChatGPT용

> 한글이 깨지면 텍스트 없이 생성한 뒤 아래 「후보정용 글자표」로 얹는다.

```
Create a 6-panel Instagram comic, one panel at a time, in order from 1 to 6.
Wait for me to say "next" before moving to the following panel.

[Apply to every panel]
· Character: a Korean woman in her mid-20s. Shoulder-length wavy black hair,
  tiny dot eyes, calm minimal expression, plain long-sleeve top, wide-leg pants,
  a boxy tote bag. Keep the exact same character as the attached character sheet.
· Style: hand-drawn fountain pen sketch. Irregular, wobbly ink lines of uneven
  weight. Black and white on off-white paper. Shading only through hatching.
  Minimal background, generous negative space.
· Avoid: 3D, realistic skin, Japanese anime style, glossy webtoon coloring,
  gradients, complex backgrounds.
· Aspect ratio: square 1:1
· Render the Korean text specified for each panel inside the image, in neat
  handwriting style, exactly as written.
· From panel 2 onward, carry over the character and line style of the previous image.

[Panel 1 · Cover]
Close-up of the woman's upper body wearing earphones, head slightly tilted,
gazing downward. Gentle water ripple lines fill the bottom quarter of the frame,
with two or three small music notes among them.
Text — title at top: "물을 그린 피아니스트"

[Panel 2]
Han River at dusk. She has stopped mid-walk, leaning lightly on the riverside
railing, looking down at the water. Earphones, tote bag on her shoulder.
The river fills the bottom half, wide sky above. A faint, thin-lined city
skyline sits far across the water.
Text — narration at top:
"퇴근길에 그냥 노들섬에서 내렸다.
듣고 있던 피아노가 자꾸 물소리처럼 들렸다."

[Panel 3]
Side view of her from the waist up, walking with earphones on.
A single melodic line flows out of her earphone and stretches from left to right,
transforming as it goes: low calm horizontal ripples → small sparkling droplets
in the middle → one thin jet of water rising at the end.
No portraits, no labels — express it only through the changing line.
Text — narration at top:
"리스트가 쓴 곡에는 물에 대한 이야기가 유난히 많다.
호수도 있고, 샘도 있고, 분수도 있다."
Small text at bottom: "그런데 이상하게 하나도 안 비슷하다. 왜 다 다르게 들리지?"

[Panel 4]
She has just looked up, facing the river (waist up).
The river's surface texture keeps changing from left to right within the frame:
calm horizontal ripples in long hatching on the left, short diagonal hatching
like a trace of wind in the middle, short dense hatching sparkling with light
on the right. Match this rhythm to the melodic line from panel 3 so the two
panels visually echo each other.
Text — narration at top:
"그러다 문득 고개를 들었는데, 강이 아까랑 좀 달라 보였다.
바람이 한 번씩 불 때마다 물빛이 계속 바뀌고 있었다."

[Panel 5]
Side view of her from the waist up, gazing at the river, a faint soft smile.
The water still shows its shifting texture. Background is only river and sky,
with large negative space.
Text — narration at top:
"아, 물은 원래 계속 다른 거구나.
같은 강이어도 볼 때마다 다르다."
Small text at bottom: "그 사람도 이렇게 오래 앉아서 물을 봤겠지."

[Panel 6 · Closing]
The riverside seen from afar. Her small figure from behind, leaning on the
railing, looking at the water. The sky nearly dark, one star. Minimal, very calm
ripple lines. She and the railing stay small in the bottom third; the rest is
open negative space (over 60% of the frame).
Text — in the upper space: "해가 다 질 때까지 그냥 좀 더 서 있었다."
```

---

## (C) 링크로 전달하려면

**현재 이 저장소는 private이라 외부 AI가 링크를 읽지 못한다.** 쓰려면 둘 중 하나:

| 방법 | 어떻게 | 비고 |
|---|---|---|
| **Secret Gist** (권장) | 위 (A) 또는 (B) 통합 프롬프트를 [gist.github.com](https://gist.github.com)에 **Secret gist**로 올리고 `Raw` 버튼의 URL을 쓴다 | 저장소는 private 유지. URL 아는 사람만 접근 |
| 저장소 public 전환 | GitHub 저장소 Settings → General → Change visibility | 브랜드 바이블·미공개 에피소드가 전부 공개된다 |

링크가 준비되면 이 지시문과 함께 전달한다:

```
다음 링크의 지시대로 인스타툰 6장을 순서대로 만들어줘.
한 번에 한 장씩, 내가 "다음 장"이라고 하면 다음 컷으로 넘어가.
2장부터는 내가 첨부하는 직전 컷의 그림체를 그대로 이어가.

<여기에 raw 링크>
```

※ 어느 방법이든 **캐릭터 시트 이미지는 직접 첨부**해야 한다. 링크로 주는 것보다 첨부가 인물 일관성에 훨씬 정확하다.

---

## (D) 후보정용 글자표

한글이 깨져 나오면 텍스트 없이 다시 생성한 뒤, `02_storyboard.md`의
**「이미지에 들어가는 글자」** 표를 기준으로 손글씨 폰트를 얹는다.
(나눔손글씨 붓, KCC은영체 등 상업용 무료 폰트 권장)

---
---

# 컷별 상세 프롬프트

> 위 통합 프롬프트로 결과가 만족스럽지 않은 컷만 아래에서 골라 다시 돌린다.

## 공통 준비물
- 참조 1: `assets/character_sheet.png` — 모든 컷에 첨부
- 참조 2: 직전 생성 컷 — 2장부터 첨부
- 스타일 참조(선택): `assets/samples/sample_4cut_bruckner_mahler.png`

---

## 1장 — 표지 (훅)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘.
> 20대 여성 루아의 상반신 클로즈업. 이어폰을 끼고 고개를 살짝 기울여
> 아래를 내려다보는 담백한 표정. 화면 하단 1/4에 잔잔한 물결 선 몇 줄,
> 물결 사이에 작은 음표 두세 개가 떠 있다.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 정확히 넣어줘:
> 상단 제목 "물을 그린 피아니스트"
> 스타일: 손으로 그린 만년필 펜 스케치, 불규칙한 선, 흑백,
> 오프화이트 배경, 해칭 음영, 미니멀한 배경, 여백 많음.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경.
> 정사각형 1:1 비율.
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png
> ```
> Keep the exact same character (Lua) from the attached character sheet:
> a Korean woman in her mid-20s, shoulder-length wavy black hair,
> tiny dot eyes, calm minimal expression, plain long-sleeve top.
> Scene: close-up of Lua's upper body wearing earphones, head slightly
> tilted, gazing downward. A few gentle horizontal water ripple lines fill
> the bottom quarter of the frame, with two or three small music notes
> floating among the ripples.
> Render this Korean text in neat handwriting style:
> title "물을 그린 피아니스트" at top.
> Style: hand-drawn fountain pen sketch, irregular wobbly ink lines,
> black and white, off-white paper background, hatching for shade,
> minimal background, generous negative space.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background.
> Square 1:1 aspect ratio.
> ```
> ※ 한글이 깨지면 텍스트 없이 생성 후 손글씨 폰트로 후삽입.

---

## 2장 — 컷1 (상황)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 1장 표지
> ```
> 첨부한 캐릭터 시트와 직전 컷의 캐릭터·그림체를 그대로 유지해서 그려줘.
> 해질녘 노들섬. 루아가 걷다 멈춰 강가 난간에 살짝 기대어
> 한강을 내려다본다. 이어폰을 끼고 어깨에 각진 토트백.
> 강은 화면 하단 절반, 하늘은 넓게. 강 건너로 아주 가는 선의
> 도시 스카이라인이 멀리 희미하게 보인다.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 정확히 넣어줘:
> 상단 내레이션 "퇴근길에 그냥 노들섬에서 내렸다.
> 듣고 있던 피아노가 자꾸 물소리처럼 들렸다."
> 스타일: 손으로 그린 만년필 펜 스케치, 불규칙한 선, 흑백,
> 오프화이트 배경, 해칭 음영, 배경은 강과 하늘만 미니멀하게, 여백 많음.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경.
> 정사각형 1:1 비율.
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png + 1장 표지
> ```
> Keep the exact same character and art style as the attached references.
> Scene: Nodeul Island, Han River, at dusk. Lua has stopped mid-walk,
> leaning lightly on the riverside railing, looking down at the river.
> She wears earphones and carries her boxy tote bag. The river fills the
> bottom half of the frame, the sky wide above; a faint, thin-lined city
> skyline sits far across the water.
> Render Korean text in neat handwriting: narration at top
> "퇴근길에 그냥 노들섬에서 내렸다.
> 듣고 있던 피아노가 자꾸 물소리처럼 들렸다."
> Style: fountain pen sketch, wobbly ink lines, black and white,
> off-white paper, hatching, minimal background (river and sky only),
> generous negative space.
> Avoid: 3D, realistic skin, anime, glossy coloring, complex background.
> Square 1:1 aspect ratio.
> ```

---

## 3장 — 컷2 (발견 · 자문자답)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 2장
> ```
> 첨부한 캐릭터 시트와 직전 컷의 캐릭터·그림체를 그대로 유지해서 그려줘.
> 이어폰을 끼고 걷는 루아의 옆모습(허리 위). 이어폰에서 흘러나온
> 선율 한 줄이 왼쪽에서 오른쪽으로 길게 이어지며 모양이 변한다:
> 처음에는 낮게 가라앉는 수평의 물결 → 가운데에서 잘게 반짝이는
> 작은 물방울들 → 끝에서 위로 솟는 가는 물줄기 하나.
> 사람 초상이나 라벨 없이, 선의 변화만으로 표현.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 정확히 넣어줘:
> 상단 내레이션 "리스트가 쓴 곡에는 물에 대한 이야기가 유난히 많다.
> 호수도 있고, 샘도 있고, 분수도 있다.",
> 하단 작게 "그런데 이상하게 하나도 안 비슷하다. 왜 다 다르게 들리지?"
> 스타일: 손으로 그린 만년필 펜 스케치, 불규칙한 선, 흑백,
> 오프화이트 배경, 해칭 음영, 미니멀, 여백 많음.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경.
> 정사각형 1:1 비율.
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png + 2장
> ```
> Keep the exact same character and art style as the attached references.
> Scene: side view of Lua from the waist up, walking with earphones on.
> A single melodic line flows out of her earphone and stretches from left
> to right across the frame, transforming as it goes: first low, calm
> horizontal ripples — then small sparkling droplets in the middle — then
> one thin jet of water rising upward at the end.
> No portraits, no labels; express it only through the changing line.
> Render Korean text in neat handwriting: narration at top
> "리스트가 쓴 곡에는 물에 대한 이야기가 유난히 많다.
> 호수도 있고, 샘도 있고, 분수도 있다.",
> small text at bottom "그런데 이상하게 하나도 안 비슷하다. 왜 다 다르게 들리지?"
> Style: fountain pen sketch, wobbly ink lines, black and white,
> off-white paper, hatching, minimal, generous negative space.
> Avoid: 3D, realistic skin, anime, glossy coloring, complex background.
> Square 1:1 aspect ratio.
> ```

---

## 4장 — 컷3 (목격)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 3장
> ```
> 첨부한 캐릭터 시트와 직전 컷의 캐릭터·그림체를 그대로 유지해서 그려줘.
> 문득 고개를 들어 강을 바라보는 루아(허리 위, 강과 마주 보는 구도).
> 화면 속 강 수면의 결이 왼쪽에서 오른쪽으로 계속 달라진다:
> 왼쪽은 가로로 긴 해칭선의 잔잔한 수평 물결, 가운데는 바람이 지나가는
> 자국처럼 비스듬한 짧은 해칭, 오른쪽은 짧고 촘촘한 해칭으로 빛에
> 잘게 반짝이는 표현. 한 화면 안에서 물의 결이 세 단계로 자연스럽게 변한다.
> 3장에서 그린 선율의 변화(물결→물방울→물줄기)와 같은 리듬으로 그려서
> 두 컷이 겹쳐 보이게 한다.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 정확히 넣어줘:
> 상단 내레이션 "그러다 문득 고개를 들었는데, 강이 아까랑 좀 달라 보였다.
> 바람이 한 번씩 불 때마다 물빛이 계속 바뀌고 있었다."
> 스타일: 손으로 그린 만년필 펜 스케치, 불규칙한 선, 흑백,
> 오프화이트 배경, 수면은 해칭 방향 변화로 표현, 미니멀, 여백 많음.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경.
> 정사각형 1:1 비율.
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png + 3장
> ```
> Keep the exact same character and art style as the attached references.
> Scene: Lua from the waist up, having just looked up, facing the river.
> The river's surface texture keeps changing from left to right within a
> single frame: the left side shows calm horizontal ripples in long
> hatching strokes, the middle shows short diagonal hatching like a trace
> of wind passing, the right side shows short, dense hatching that
> sparkles with light. The water's texture shifts naturally in three
> stages across the frame. Match this rhythm to the melodic line drawn in
> the previous-but-one panel (ripples → droplets → jet) so the two panels
> visually echo each other.
> Render Korean text in neat handwriting: narration at top
> "그러다 문득 고개를 들었는데, 강이 아까랑 좀 달라 보였다.
> 바람이 한 번씩 불 때마다 물빛이 계속 바뀌고 있었다."
> Style: fountain pen sketch, wobbly ink lines, black and white,
> off-white paper, water rendered through shifting hatching direction,
> minimal, generous negative space.
> Avoid: 3D, realistic skin, anime, glossy coloring, complex background.
> Square 1:1 aspect ratio.
> ```

---

## 5장 — 컷4 (깨달음)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 4장
> ```
> 첨부한 캐릭터 시트와 직전 컷의 캐릭터·그림체를 그대로 유지해서 그려줘.
> 강을 바라보는 루아의 옆모습(허리 위), 옅은 미소. 수면은 여전히
> 결이 살아 움직이는 채로(3장과 같은 방식의 해칭 변화).
> 배경은 강과 하늘만, 여백 크게.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 정확히 넣어줘:
> 상단 내레이션 "아, 물은 원래 계속 다른 거구나.
> 같은 강이어도 볼 때마다 다르다.",
> 하단 작게 "그 사람도 이렇게 오래 앉아서 물을 봤겠지."
> 스타일: 손으로 그린 만년필 펜 스케치, 불규칙한 선, 흑백,
> 오프화이트 배경, 해칭 음영, 미니멀, 여백 크게.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경.
> 정사각형 1:1 비율.
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png + 4장
> ```
> Keep the exact same character and art style as the attached references.
> Scene: side view of Lua from the waist up, gazing at the river, a faint
> soft smile. The water surface still shows its shifting texture (same
> hatching variation as the previous panel). Background is only river and
> sky, large negative space.
> Render Korean text in neat handwriting: narration at top
> "아, 물은 원래 계속 다른 거구나.
> 같은 강이어도 볼 때마다 다르다.",
> small text at bottom "그 사람도 이렇게 오래 앉아서 물을 봤겠지."
> Style: fountain pen sketch, wobbly ink lines, black and white,
> off-white paper, hatching, minimal, large negative space.
> Avoid: 3D, realistic skin, anime, glossy coloring, complex background.
> Square 1:1 aspect ratio.
> ```

---

## 6장 — 여운

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 5장
> ```
> 첨부한 캐릭터 시트와 직전 컷의 캐릭터·그림체를 그대로 유지해서 그려줘.
> 멀리서 본 노들섬. 난간에 기대 강을 보는 루아의 작은 뒷모습.
> 해가 완전히 저물어가는 하늘, 별 하나. 물결 선은 아주 잔잔하게 최소한으로.
> 루아와 난간은 화면 하단 1/3에 작게, 나머지는 넓은 여백.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 정확히 넣어줘:
> 상단 여백에 "해가 다 질 때까지 그냥 좀 더 서 있었다."
> 스타일: 손으로 그린 만년필 펜 스케치, 불규칙한 선, 흑백,
> 오프화이트 배경, 해칭 음영, 여백이 화면의 60% 이상.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경.
> 정사각형 1:1 비율.
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png + 5장
> ```
> Keep the exact same character and art style as the attached references.
> Scene: Nodeul Island seen from afar at dusk. Lua's small figure from
> behind, leaning on the railing, gazing at the river. The sky is nearly
> dark, one star visible. Minimal, very calm ripple lines. Lua and the
> railing stay small in the bottom third; the rest is open negative space.
> Render Korean text in neat handwriting in the upper space:
> "해가 다 질 때까지 그냥 좀 더 서 있었다."
> Style: fountain pen sketch, wobbly ink lines, black and white,
> off-white paper, hatching, negative space over 60% of the frame.
> Avoid: 3D, realistic skin, anime, glossy coloring, complex background.
> Square 1:1 aspect ratio.
> ```

---

## Stage 3 체크리스트
- [x] 6컷 모두 character_sheet.png 첨부 지시 포함
- [x] 2장부터 직전 컷 첨부 지시 포함
- [x] 매 컷 스타일 고정 문구 + 금지 문구 포함
- [x] 화면 텍스트 원문이 따옴표로 정확히 명시됨
- [x] 사색 우선 — 작곡가 초상·정보 라벨 없음, 선율=물의 변형과 수면의 결 변화로만 표현
- [x] 청계천 잔재 없음 — 전면 노들섬/한강 배경
