# [ep002] 물을 그린 피아니스트 — 이미지 렌더링 지시서

# 0. 표지(1장) — 실사 배경 콜라주 (예외 워크플로)

> **표지만 다른 5장과 만드는 방식이 다르다.** 배경은 실제 사진, 캐릭터는 손그림 컷아웃을 합성한다.
> 컷1~4·여운(2~6장)은 아래 「🚀 한 번에 전달하기」로 넘어간다.
> (`brand/03_DRAWING_STYLE.md` 표지 예외, `brand/06_IMAGE_RULE.md` 표지 합성 절차 참고)

## 실행 순서 (4단계)
1. **해질녘 노들섬·한강 사진**을 준비한다 (직접 촬영 또는 출처가 분명한 사진)
2. 아래 캐릭터 컷아웃 프롬프트로 **배경 없는 캐릭터만** 생성 (character_sheet.png 첨부)
3. 사진 편집 툴(캔바, 미리캔버스, 포토샵 등)에서 사진 위에 캐릭터 컷아웃을 배치, 흰 테두리를 살려 스티커처럼 보이게 한다
4. 표지 문구를 손글씨 느낌 폰트로 얹는다: "물을 그린 피아니스트"

### 캐릭터 컷아웃 프롬프트 — 한국어판 (Gemini/나노바나나)
```
첨부한 캐릭터 시트의 루아를 그대로 유지해서 그려줘. 캐릭터 시트가 외형의 기준이다.
상반신. 이어폰을 낀 채 고개를 살짝 기울여 아래를 내려다보는 표정(생각 중).
캐릭터가 화면에서 작아지지 않게, 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로 그려줘.
배경은 순백색(#ffffff)으로, 캐릭터만 오려내기 쉽게 그려줘. 배경 요소는 아무것도 넣지 마.
스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 해칭 음영.
소지품(토트백 등)에 로고나 브랜드명을 넣지 마.
금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 그라데이션, 배경 요소 일체, 로고·워드마크.
4:5 비율(1080×1350).
```

### 캐릭터 컷아웃 프롬프트 — 영어판 (ChatGPT)
```
Keep the exact same character (Lua) from the attached character sheet — it is the source of
truth for her appearance:
a Korean woman in her mid-20s, shoulder-length wavy black hair,
tiny dot eyes, calm minimal expression, plain long-sleeve top and wide pants.
Pose/expression: upper body, wearing earphones, head tilted slightly, gazing downward
(thoughtful expression).
Keep the character large enough to read clearly on a small (mobile) screen — do not draw her too small.
Background: pure flat white (#ffffff), nothing else — the character must be easy to cut out cleanly.
Style: hand-drawn fountain pen sketch, thick and irregular wobbly ink lines,
black and white, hatching for shade.
No logos or brand names on any accessory (tote bag, etc).
Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, gradients, any background elements, logos/wordmarks.
4:5 aspect ratio (1080x1350).
```

---

# 🚀 한 번에 전달하기 (컷1~4 + 여운 · 2~6장)

> 표지(1장)는 여기 포함되지 않는다 — 위 0번 워크플로로 별도 제작한다.

## 실행 순서 (3단계)
1. 이미지 생성 AI 대화창에 **`assets/character_sheet.png`를 첨부**한다
2. 아래 통합 프롬프트를 **통째로 복사해서 붙여넣는다** (도구에 맞는 언어판 선택)
3. 컷1(2장)이 나오면 **그 이미지를 첨부하고 "다음 장"**이라고 한다 → 여운(6장)까지 반복
   *(직전 컷 첨부가 그림체 일관성의 핵심이라 이 단계만은 손으로 해야 한다)*

> **첫 장이 나오면 확인할 것**: 한 이미지에 장면이 하나만 있어야 한다.
> 여러 컷이 격자로 한 장에 다 들어갔다면 이렇게 다시 말한다 —
> `"한 이미지에 한 장면만. 격자로 합치지 말고 컷1만 다시 만들어줘."`

---

## (A) 통합 프롬프트 — 한국어판 · Gemini / 나노바나나용

> 한글 텍스트를 이미지에 직접 넣는 데 강하다. 이쪽을 우선 권장.

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
  담백한 표정, 무지 긴팔 상의와 통 넓은 바지, 각진 토트백(로고·브랜드명 없음).
  첨부한 캐릭터 시트의 인물을 그대로 유지할 것 — 세부 외형은 그 시트가 기준이다.
· 캐릭터 크기: 화면에서 작아지지 않게. 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로.
· 그림체: 손으로 그린 만년필 펜 스케치. 선은 두껍고 불규칙하며 굵기가 일정하지 않다.
  흑백, 배경색은 흰색(#ffffff), 음영은 해칭(빗금)으로만.
  배경 묘사는 짧게, 최소한으로만 (표지와 달리 실사 배경 없음 — 전부 손그림 배경).
· 텍스트: 크게 — 작은 화면에서도 한 번에 읽히는 크기로.
· 프레임: 컷 가장자리에 손으로 그린 테두리선(외곽선)을 두를 것.
· 금지: 3D, 사실적인 피부, 일본 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경, 로고·브랜드명 노출.
· 비율: 4:5 (1080×1350)
· 각 장에 지정된 한글 텍스트를 이미지 안에 손글씨 느낌으로 정확히 넣을 것.
· 3장부터는 직전에 만든 그림의 인물과 선 스타일을 그대로 이어갈 것.

=== 지금 만들 것 ===
[2장 · 컷1]
해질녘 한강. 걷다 멈춘 여성이 강가 난간에 살짝 기대어 물을 내려다본다.
이어폰, 어깨에 토트백. 강은 화면 하단 절반, 하늘은 넓게.
강 건너 도시 스카이라인은 아주 가는 선으로 멀리 희미하게.
넣을 글자 — 상단 내레이션:
"퇴근길에 그냥 노들섬에서 내렸다.
듣고 있던 피아노가 자꾸 물소리처럼 들렸다."

=== 아래는 이후 순서. 지금 만들지 말 것 ===

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
  a boxy tote bag (no logo or brand name). Keep the exact same character as the
  attached character sheet — it is the source of truth for her appearance.
· Character size: keep her large enough to read clearly on a small (mobile) screen —
  do not draw her too small.
· Style: hand-drawn fountain pen sketch. Thick, irregular, wobbly ink lines of uneven
  weight. Black and white on a pure white (#ffffff) background. Shading only through
  hatching. Background description kept minimal and brief (unlike the cover, no photo
  background — every background here is hand-drawn).
· Text: large — readable at a glance on a small screen.
· Frame: draw a hand-drawn border/outline around the edge of each panel.
· Avoid: 3D, realistic skin, Japanese anime style, glossy webtoon coloring,
  gradients, complex backgrounds, logos or brand names.
· Aspect ratio: 4:5 (1080x1350)
· Render the Korean text specified for each panel inside the image, in neat
  handwriting style, exactly as written.
· From panel 3 onward, carry over the character and line style of the previous image.

=== GENERATE PANEL 2 ONLY. THE REST COME LATER ===
[Panel 2]
Han River at dusk. She has stopped mid-walk, leaning lightly on the riverside
railing, looking down at the water. Earphones, tote bag on her shoulder.
The river fills the bottom half, wide sky above. A faint, thin-lined city
skyline sits far across the water.
Text — narration at top:
"퇴근길에 그냥 노들섬에서 내렸다.
듣고 있던 피아노가 자꾸 물소리처럼 들렸다."

=== BELOW: LATER PANELS. DO NOT GENERATE YET ===

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
- 참조 2: 직전 생성 컷 — **3장부터** 첨부 (2장 컷1은 표지가 콜라주라 캐릭터 시트만 첨부)
- 스타일 참조(선택): `assets/samples/sample_4cut_bruckner_mahler.png`

---

## 1장 — 표지

> **표지는 여기서 만들지 않는다.** 실사 배경 콜라주 워크플로(문서 맨 위 **0번**)를 쓴다.
> 해질녘 노들섬·한강 사진 위에 캐릭터 컷아웃을 얹고, 문구 "물을 그린 피아니스트"를 손글씨 폰트로 삽입한다.

---

## 2장 — 컷1 (상황)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 세부 외형은 그 시트가 기준이다.
> 해질녘 노들섬. 루아가 걷다 멈춰 강가 난간에 살짝 기대어
> 한강을 내려다본다. 이어폰을 끼고 어깨에 각진 토트백.
> 강은 화면 하단 절반, 하늘은 넓게. 강 건너로 아주 가는 선의
> 도시 스카이라인이 멀리 희미하게 보인다.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 정확히 넣어줘:
> 상단 내레이션 "퇴근길에 그냥 노들섬에서 내렸다.
> 듣고 있던 피아노가 자꾸 물소리처럼 들렸다."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 해칭 음영, 배경은 강과 하늘만 짧게.
> 캐릭터와 글씨는 작은 화면에서도 잘 보이게 크게. 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png
> ```
> Keep the exact same character (Lua) from the attached character sheet — it is
> the source of truth for her appearance.
> Scene: Nodeul Island, Han River, at dusk. Lua has stopped mid-walk,
> leaning lightly on the riverside railing, looking down at the river.
> She wears earphones and carries her boxy tote bag. The river fills the
> bottom half of the frame, the sky wide above; a faint, thin-lined city
> skyline sits far across the water.
> Render Korean text in neat handwriting: narration at top
> "퇴근길에 그냥 노들섬에서 내렸다.
> 듣고 있던 피아노가 자꾸 물소리처럼 들렸다."
> Style: fountain pen sketch, thick wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching, minimal background (river and sky only),
> generous negative space.
> Keep her large enough and the text big enough to read on a small (mobile) screen.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime, glossy coloring, complex background, logos or brand names.
> 4:5 aspect ratio (1080x1350).
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
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게.
> 캐릭터와 글씨는 작은 화면에서도 잘 보이게 크게. 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명.
> 4:5 비율(1080×1350).
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
> Style: fountain pen sketch, thick wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching, minimal, generous negative space.
> Keep her large enough and the text big enough to read on a small (mobile) screen.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime, glossy coloring, complex background, logos or brand names.
> 4:5 aspect ratio (1080x1350).
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
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 수면은 해칭 방향 변화로 표현, 배경 묘사는 짧게.
> 캐릭터와 글씨는 작은 화면에서도 잘 보이게 크게. 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명.
> 4:5 비율(1080×1350).
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
> Style: fountain pen sketch, thick wobbly ink lines, black and white,
> pure white (#ffffff) background, water rendered through shifting hatching direction,
> minimal, generous negative space.
> Keep her large enough and the text big enough to read on a small (mobile) screen.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime, glossy coloring, complex background, logos or brand names.
> 4:5 aspect ratio (1080x1350).
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
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게, 여백 크게.
> 캐릭터와 글씨는 작은 화면에서도 잘 보이게 크게. 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명.
> 4:5 비율(1080×1350).
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
> Style: fountain pen sketch, thick wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching, minimal, large negative space.
> Keep her large enough and the text big enough to read on a small (mobile) screen.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime, glossy coloring, complex background, logos or brand names.
> 4:5 aspect ratio (1080x1350).
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
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 해칭 음영, 여백이 화면의 60% 이상.
> 인물은 작게 배치하되 작은 화면에서도 뒷모습 형태는 뚜렷하게. 글씨는 크게.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명.
> 4:5 비율(1080×1350).
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
> Style: fountain pen sketch, thick wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching, negative space over 60% of the frame.
> Keep her large enough and the text big enough to read on a small (mobile) screen.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime, glossy coloring, complex background, logos or brand names.
> 4:5 aspect ratio (1080x1350).
> ```

---

## Stage 3 체크리스트
- [x] 표지(1장)는 0번 실사 배경 콜라주 워크플로로 별도 작성됐는가 (나머지 5장과 다른 방식)
- [x] 컷1~4·여운(2~6장) 모두 character_sheet.png 첨부 지시 포함
- [x] 3장부터 직전 컷 첨부 지시 포함
- [x] 매 컷 스타일 고정 문구 + 금지 문구 포함
- [x] 화면 텍스트 원문이 따옴표로 정확히 명시됨
- [x] 배경색 흰색(#ffffff), 비율 4:5(1080×1350) 지시가 모든 컷에 있는가
- [x] 펜선 두껍게, 컷 외곽선, 캐릭터·텍스트 크게 지시가 있는가
- [x] 로고·브랜드명 노출 금지 지시가 있는가
- [x] 사색 우선 — 작곡가 초상·정보 라벨 없음, 선율=물의 변형과 수면의 결 변화로만 표현
- [x] 청계천 잔재 없음 — 전면 노들섬/한강 배경
