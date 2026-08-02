# [ep005] 낮도 밤도 아닌 노래 — 이미지 렌더링 지시서

> **프롬프트 우선순위** (`brand/06_IMAGE_RULE.md`) — 각 컷은 콘티의 장면(보이는 행동)에서 시작한다.
> **본편 컷(2~6장)에 에피소드 제목·컷 번호·다른 컷 문구를 넣지 않는다.** 제목은 표지에만.
> **로고·워드마크 금지** — 놀이터 기구·휴대폰 화면 전부 무지.
> 따옴표 안 문구는 `02_storyboard.md`의 「이미지에 들어가는 글자」 표와 글자 하나까지 같아야 한다.

# 0. 표지(1장) — 실사 배경 콜라주

## 실행 순서 (4단계)
1. **동네 놀이터 사진**을 준비한다 (그네, 트인 하늘, 노을~보라 하늘빛).
   ※ 사진에 브랜드·상표가 찍혔으면 잘라내거나 지운다
2. 아래 캐릭터 컷아웃 프롬프트로 **배경 없는 캐릭터만** 생성 (character_sheet.png 첨부)
3. 사진 위에 배치, 흰 테두리를 살려 스티커처럼. **원근과 빛을 맞춘다** — 하늘빛이 위에서 오게
4. 제목 "낮도 밤도 아닌 노래"를 손글씨 폰트로 **상단**에 얹는다. 캐릭터는 우하단 — **겹치지 않게**

> 표지 장면은 컷3에 실제로 나오는 장면(하늘을 올려다보는 자세)이다. 상징적 장면을 새로 만들지 않았다.

### 캐릭터 컷아웃 — 한국어판 (Gemini/나노바나나)
```
첨부한 캐릭터 시트의 루아를 그대로 유지해서 그려줘. 캐릭터 시트가 외형의 기준이다.
행동: 상반신. 그네에 앉아 이어폰을 낀 채 고개를 들어 하늘을 올려다보고 있다(생각 중).
캐릭터가 화면에서 작아지지 않게, 작은 화면에서도 형태가 뚜렷이 보이는 크기로.
배경은 순백색(#ffffff), 캐릭터만 오려내기 쉽게. 배경 요소는 아무것도 넣지 마.
스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 해칭 음영.
의상·소지품에 로고나 브랜드명을 넣지 마.
금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 그라데이션, 배경 요소 일체, 로고·워드마크.
4:5 비율(1080×1350).
```

### 캐릭터 컷아웃 — 영어판 (ChatGPT)
```
Keep the exact same character (Lua) from the attached character sheet — it is the source of
truth for her appearance: a Korean woman in her mid-20s, shoulder-length wavy black hair,
tiny dot eyes, calm minimal expression, plain long-sleeve top and wide pants.
Action: upper body, seated on a swing, wearing earphones, looking up at the sky, thoughtful.
Keep her large enough to read clearly on a small (mobile) screen.
Background: pure flat white (#ffffff), nothing else — she must be easy to cut out cleanly.
Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white, hatching.
No logos or brand names on clothing or accessories.
Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, gradients, background elements, logos.
4:5 aspect ratio (1080x1350).
```

---

# 🚀 한 번에 전달하기 (컷1~4 + 여운 · 2~6장)

1. 이미지 생성 AI에 **`assets/character_sheet.png` 첨부**
2. 아래 통합 프롬프트를 **통째로 복사해 붙여넣기**
3. 컷1(2장)이 나오면 **그 이미지를 첨부하고 "다음 장"** → 여운(6장)까지 반복

## (A) 통합 프롬프트 — 한국어판 · Gemini / 나노바나나용

```
인스타툰의 컷1~4와 마지막 여운 장, 5장짜리를 만들 거야 (표지는 별도로 만든다). 시작 전에 중요한 규칙 두 가지.

❗ 규칙 1 — 5장을 한 이미지에 모아 그리지 마.
   각 장은 완전히 독립된 별개의 이미지다. 한 이미지 = 한 장면 하나.
   격자 배치, 콜라주, 분할 화면, 여러 장면을 한 화면에 넣기 전부 금지.
   다른 컷의 문구를 넣지 마. 에피소드 제목과 컷 번호도 넣지 마.

❗ 규칙 2 — 지금은 아래 [2장 · 컷1]만 만들어.
   3~6장은 내가 "다음 장"이라고 말할 때까지 만들지 마.

[모든 장에 공통 적용]
· 캐릭터: 20대 한국 여성. 어깨에 닿는 검은 웨이브 단발, 작은 점 같은 눈,
  담백한 표정, 무지 긴팔 상의와 통 넓은 바지.
  첨부한 캐릭터 시트의 인물을 그대로 유지할 것 — 세부 외형은 그 시트가 기준이다.
· 무대: 여름 저녁, 노을이 진 직후의 동네 놀이터. 그네, 낮은 철봉, 트인 하늘.
  아무도 없이 조용하다.
  ❗ 놀이터 기구·휴대폰 화면 어디에도 브랜드 이름이나 로고를 넣지 마. 전부 무지로.
· 캐릭터 크기: 화면에서 작아지지 않게. 작은 화면에서도 형태가 뚜렷이 보이는 크기로.
· 그림체: 손으로 그린 만년필 펜 스케치. 선은 두껍고 불규칙하다.
  흑백, 배경색은 흰색(#ffffff), 음영은 해칭(빗금)으로만. 배경 묘사는 짧게.
· 이 화의 그림 규칙: **하늘색의 변화(노을빛 → 보라)를 해칭의 밀도와 톤으로만 표현한다.**
  실제 색을 칠하지 않고 흑백 해칭의 진하기로 시간의 흐름을 나타낼 것.
· 이 화의 감정 규칙: **입꼬리를 올리는 미소 표정을 어느 컷에도 그리지 마.**
  가장 감정이 큰 컷(5장)도 표정은 "집중"까지만.
· 프레임: 컷 가장자리에 손으로 그린 테두리선을 두를 것.
· 금지: 3D, 사실적인 피부, 일본 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경,
        로고·브랜드명, 장면에 없는 상징물.
· 비율: 4:5 (1080×1350)
· 3장부터는 직전에 만든 그림의 인물과 선 스타일을 그대로 이어갈 것.
· 각 장의 카메라 거리가 다르다. 지정된 구도를 그대로 지킬 것.

=== 지금 만들 것 ===
[2장 · 컷1]
행동: 저녁 산책 중 놀이터에 들른 루아가 그네에 앉는다. 사슬을 양손으로 잡고 이어폰을 낀 뒤
      재생 버튼을 누른다.
구도: 공간 와이드숏 / 카메라 거리 와이드 — 놀이터 전체와 하늘이 함께 보이고 루아는 그 안에 있다.
배경: 아무도 없는 놀이터. 하늘이 화면 위쪽 절반 이상을 차지. 노을빛이 옅게 남아 있다.
표정: 생각 중.
이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
"저녁 먹고 나와서 그냥 걷다가 놀이터에 들렀다. 그네에 앉아서 라벨의 물의 유희를 틀었다."

=== 아래는 이후 순서. 지금 만들지 말 것 ===

[3장 · 컷2]
행동: 그네에 앉아 이어폰을 듣는 루아. 다음 곡으로 넘어가는 순간, 미간이 살짝 좁아진다.
구도: 얼굴과 상반신 / 카메라 거리 미디엄. 그네 사슬을 쥔 손이 화면 하단에 살짝 걸린다.
배경: 흐린 노을빛만.
표정: 고민 중.
넣을 글자 — 상단: "그런데 다음 곡이 볼레로였다. 방금 거랑 너무 다르다. 같은 사람이 쓴 거 맞아?"

[4장 · 컷3]
행동: 고개를 든 루아가 올려다보는 하늘. 낮의 파랑도 밤의 검정도 아닌, 그 사이의 색으로
      물들어 있다.
구도: 캐릭터 시점, 하늘 위주의 원경 — 화면 아래쪽에 그네 사슬과 어깨 끝만 살짝 걸친다 /
      카메라 거리 원경. **루아의 얼굴은 보이지 않는다.**
배경: 하늘이 화면 대부분을 차지한다. 구름 몇 가닥만 가늘게, 나머지는 균일한 톤의 해칭으로
      색의 경계 없이 자연스럽게.
이미지 안에 글자를 넣지 마. (무대사 컷)

[5장 · 컷4]
행동: 여전히 하늘을 보고 있는 루아. 그네를 밀던 발이 멈춘다.
구도: 옆모습 / 카메라 거리 중경(허리 위).
배경: 하늘만, 여백 크게.
표정: 집중. **입꼬리를 올리지 않는다.**
넣을 글자 — 상단: "하늘이 어느새 파랑도 검정도 아니었다. 물의 유희도 볼레로도, 이 색 하나였구나."

[6장 · 여운]
행동: 그네에서 일어나려는 손. 손바닥에 사슬이 남긴 자국이 옅게 찍혀 있다.
구도: 손 디테일 — 손바닥과 그네 사슬 끝 / 카메라 거리 디테일. 얼굴은 프레임 밖.
배경: 그네 사슬과 손 주변만. 여백 크게.
넣을 글자 — 상단 여백에: "일어나려는데 손바닥에 사슬 자국이 남아 있었다."
```

## (B) 통합 프롬프트 — 영어판 · ChatGPT용

```
I am making an Instagram comic series — panels 2 through 6 (cut1-4 plus a closing panel;
the cover panel is made separately). Two critical rules first.

IMPORTANT 1 — Do NOT combine the panels into one image.
   Each panel is a completely separate, standalone image. One image = one scene.
   No grids, no collages, no split screens, no multiple moments in one frame.
   Do not include text from any other panel. No episode title, no panel numbers.

IMPORTANT 2 — Generate ONLY [Panel 2] right now.
   Do not generate panels 3-6 until I say "next".

[Apply to every panel]
· Character: a Korean woman in her mid-20s. Shoulder-length wavy black hair, tiny dot eyes,
  calm minimal expression, plain long-sleeve top, wide-leg pants.
  Keep the exact same character as the attached character sheet — it is the source of truth.
· Setting: a neighborhood playground on a summer evening, just after sunset. A swing, a low
  bar, an open sky. Nobody else is there.
  ❗ Put NO brand name or logo anywhere — playground equipment, phone screen all stay blank.
· Character size: keep her large enough to read clearly on a small (mobile) screen.
· Style: hand-drawn fountain pen sketch. Thick, irregular, wobbly ink lines. Black and white
  on a pure white (#ffffff) background. Shading only through hatching. Background kept brief.
· Episode-specific rule: **render the changing sky (afterglow → purple) only through the
  density and tone of the hatching** — no actual color, just how dark/dense the ink gets,
  to suggest the passage of time.
· Emotional rule: **do not draw a smiling expression, on any panel.**
  Even the most emotional panel (panel 5) stops at "focused."
· Frame: draw a hand-drawn border/outline around the edge of each panel.
· Avoid: 3D, realistic skin, Japanese anime style, glossy webtoon coloring, gradients,
  complex backgrounds, logos or brand names, symbolic objects not in the scene.
· Aspect ratio: 4:5 (1080x1350)
· From panel 3 onward, carry over the character and line style of the previous image.
· Each panel uses a different camera distance. Follow the specified composition exactly.

=== GENERATE PANEL 2 ONLY. THE REST COME LATER ===
[Panel 2 · cut 1]
Action: on an evening walk, Lua stops by a playground and sits on a swing. She grips the chains
  with both hands, puts in her earphones, and presses play.
Composition: wide establishing shot / camera distance WIDE — the whole playground and sky are
  visible, and she is inside it.
Background: an empty playground. The sky fills more than the top half of the frame, with a thin
  trace of sunset color left in it.
Expression: thoughtful.
Render this Korean text large, in neat handwriting style:
"저녁 먹고 나와서 그냥 걷다가 놀이터에 들렀다. 그네에 앉아서 라벨의 물의 유희를 틀었다."

=== BELOW: LATER PANELS. DO NOT GENERATE YET ===

[Panel 3 · cut 2]
Action: still on the swing, listening. The moment the track changes, her brow furrows slightly.
Composition: face and upper body / camera distance MEDIUM. Her hand gripping the swing chain
  just enters the bottom of the frame.
Background: only a hazy trace of sunset light.
Expression: pondering.
Text — top: "그런데 다음 곡이 볼레로였다. 방금 거랑 너무 다르다. 같은 사람이 쓴 거 맞아?"

[Panel 4 · cut 3]
Action: she tilts her head back and looks up at the sky — no longer daytime blue, not yet
  night's black, but somewhere between the two.
Composition: her point of view, sky-dominant, a long shot — only the swing chains and the top
  of her shoulder enter the bottom of the frame / camera distance LONG. **Her face is not visible.**
Background: the sky fills nearly the whole frame. A few thin wisps of cloud; the rest is an
  even tone of hatching with no hard edge between colors.
Do not render any text in this image. (silent panel)

[Panel 5 · cut 4]
Action: still looking up at the sky. The foot that was pushing the swing comes to a stop.
Composition: side profile / camera distance MEDIUM (waist up).
Background: only the sky. Generous negative space.
Expression: focused. **Do not raise the corners of the mouth.**
Text — top: "하늘이 어느새 파랑도 검정도 아니었다. 물의 유희도 볼레로도, 이 색 하나였구나."

[Panel 6 · closing]
Action: a hand about to push off the swing to stand up. A faint mark from the chain is
  pressed into her palm.
Composition: hand detail — her palm and the end of the swing chain / camera distance DETAIL.
  Her face is out of frame.
Background: only the swing chain and the space around the hand. Generous negative space.
Text — in the top margin: "일어나려는데 손바닥에 사슬 자국이 남아 있었다."
```

## (C) 후보정용 글자표
한글이 깨지면 텍스트 없이 생성 후 `02_storyboard.md`의 「이미지에 들어가는 글자」 표 기준으로 손글씨 폰트 삽입.
**컷3만 무대사다** — 그 컷에는 글자를 넣지 않는다.

---
---

# 컷별 상세 프롬프트

> 통합 프롬프트로 만족스럽지 않은 컷만 아래에서 골라 다시 돌린다.
> 표지(1장)는 위 0번의 컷아웃 프롬프트를 쓴다.

## 공통 준비물
- 참조 1: `assets/character_sheet.png` — **모든 컷에 첨부**
- 참조 2: 직전에 생성한 컷 이미지 — **3장부터 첨부**

## 스타일 고정 문구
- 한국어: "손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게, 캐릭터는 화면에서 작지 않게, 컷 가장자리에 테두리선, 4:5 비율"
- 영어: "hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white, pure white (#ffffff) background, hatching for shade, minimal background description, hand-drawn panel border, 4:5 aspect ratio"
- 네거티브: "3D, 사실적 피부, 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경, 로고·브랜드명, 에피소드 제목·컷 번호, 장면에 없는 상징물, 미소 표정"

---

## 2장 — 컷1 (와이드)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 세부 외형은 그 시트가 기준이다.
> 행동: 저녁 산책 중 놀이터에 들른 루아가 그네에 앉는다. 사슬을 양손으로 잡고 이어폰을
>       낀 뒤 재생 버튼을 누른다.
> 구도: 공간 와이드숏. 카메라 거리는 와이드 — 놀이터 전체와 하늘이 함께 보이고 루아는 그 안에 있다.
> 배경: 아무도 없는 놀이터. 하늘이 화면 위쪽 절반 이상을 차지. 노을빛이 옅게 남아 있다.
> 표정: 생각 중.
> 놀이터 기구에 브랜드 이름이나 로고를 넣지 마. 전부 무지로.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> "저녁 먹고 나와서 그냥 걷다가 놀이터에 들렀다. 그네에 앉아서 라벨의 물의 유희를 틀었다."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명, 에피소드 제목, 컷 번호.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png
> ```
> Keep the exact same character (Lua) from the attached character sheet — it is the source of
> truth for her appearance: a Korean woman in her mid-20s, shoulder-length wavy black hair,
> tiny dot eyes, calm minimal expression, plain long-sleeve top and wide pants.
> Action: on an evening walk, Lua stops by a playground and sits on a swing. She grips the
> chains with both hands, puts in her earphones, and presses play.
> Composition: wide establishing shot / camera distance WIDE — the whole playground and sky
> are visible, and she is inside it.
> Background: an empty playground. The sky fills more than the top half of the frame, with a
> thin trace of sunset color left in it.
> Expression: thoughtful.
> Put no brand name or logo anywhere on the playground equipment.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text large, in neat handwriting style:
> "저녁 먹고 나와서 그냥 걷다가 놀이터에 들렀다. 그네에 앉아서 라벨의 물의 유희를 틀었다."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, episode titles, panel numbers.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 3장 — 컷2 (미디엄)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(2장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 그네에 앉아 이어폰을 듣는 루아. 다음 곡으로 넘어가는 순간, 미간이 살짝 좁아진다.
> 구도: 얼굴과 상반신. 카메라 거리는 미디엄. 그네 사슬을 쥔 손이 화면 하단에 살짝 걸린다.
> 배경: 흐린 노을빛만.
> 표정: 고민 중.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> "그런데 다음 곡이 볼레로였다. 방금 거랑 너무 다르다. 같은 사람이 쓴 거 맞아?"
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명, 에피소드 제목.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png + 직전 컷(2장)
> ```
> Keep the exact same character (Lua) from the attached character sheet. Carry over the line
> style of the previous panel.
> Action: still on the swing, listening. The moment the track changes, her brow furrows slightly.
> Composition: face and upper body / camera distance MEDIUM. Her hand gripping the swing chain
> just enters the bottom of the frame.
> Background: only a hazy trace of sunset light.
> Expression: pondering.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text large, in neat handwriting style:
> "그런데 다음 곡이 볼레로였다. 방금 거랑 너무 다르다. 같은 사람이 쓴 거 맞아?"
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, episode titles.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 4장 — 컷3 (원경 · 하늘 · **무대사**)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(3장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 고개를 든 루아가 올려다보는 하늘. 낮의 파랑도 밤의 검정도 아닌, 그 사이의 색으로
>       물들어 있다.
> 구도: 캐릭터 시점, 하늘 위주의 원경 — 화면 아래쪽에 그네 사슬과 어깨 끝만 살짝 걸친다.
>       카메라 거리는 원경. **루아의 얼굴은 보이지 않는다.**
> 배경: 하늘이 화면 대부분을 차지한다. 구름 몇 가닥만 가늘게, 나머지는 균일한 톤의 해칭으로
>       색의 경계 없이 자연스럽게. **실제 색을 칠하지 않고 해칭의 밀도로만 시간을 표현한다.**
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> **이미지 안에 글자를 넣지 마.**
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명, 글자 일체.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png + 직전 컷(3장)
> ```
> Keep the exact same character (Lua) from the attached character sheet. Carry over the line
> style of the previous panel.
> Action: she tilts her head back and looks up at the sky — no longer daytime blue, not yet
> night's black, but somewhere between the two.
> Composition: her point of view, sky-dominant, a long shot — only the swing chains and the
> top of her shoulder enter the bottom of the frame / camera distance LONG. **Her face is not
> visible.**
> Background: the sky fills nearly the whole frame. A few thin wisps of cloud; the rest is an
> even tone of hatching with no hard edge between colors. **Do not use actual color — suggest
> the passage of time only through hatching density.**
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> **Do not render any text in this image.**
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, any text.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 5장 — 컷4 (중경 · 옆모습)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(4장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 여전히 하늘을 보고 있는 루아. 그네를 밀던 발이 멈춘다.
> 구도: 옆모습, 허리 위. 카메라 거리는 중경.
> 배경: 하늘만, 여백 크게.
> 표정: 집중. **입꼬리를 올리지 않는다 — 미소가 아니다.**
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> "하늘이 어느새 파랑도 검정도 아니었다. 물의 유희도 볼레로도, 이 색 하나였구나."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명, 에피소드 제목, 미소 표정.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png + 직전 컷(4장)
> ```
> Keep the exact same character (Lua) from the attached character sheet. Carry over the line
> style of the previous panel.
> Action: still looking up at the sky. The foot that was pushing the swing comes to a stop.
> Composition: side profile, waist up / camera distance MEDIUM.
> Background: only the sky. Generous negative space.
> Expression: focused. **Do not raise the corners of the mouth — not a smile.**
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text large, in neat handwriting style:
> "하늘이 어느새 파랑도 검정도 아니었다. 물의 유희도 볼레로도, 이 색 하나였구나."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, episode titles, a smiling expression.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 6장 — 여운 (디테일 · 손)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(5장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 그네에서 일어나려는 손. 손바닥에 사슬이 남긴 자국이 옅게 찍혀 있다.
> 구도: 손 디테일 — 손바닥과 그네 사슬 끝. 카메라 거리는 디테일(가까이). **얼굴은 프레임 밖.**
> 배경: 그네 사슬과 손 주변만. 여백을 크게 남긴다.
> 새로운 상징물을 넣지 마. 장면에 있는 것만 그린다.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 상단 여백에 손글씨 느낌으로 크게 넣어줘:
> "일어나려는데 손바닥에 사슬 자국이 남아 있었다."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명, 에피소드 제목.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png + 직전 컷(5장)
> ```
> Keep the exact same character (Lua) from the attached character sheet. Carry over the line
> style of the previous panel.
> Action: a hand about to push off the swing to stand up. A faint mark from the chain is
> pressed into her palm.
> Composition: hand detail — her palm and the end of the swing chain / camera distance DETAIL.
> **Her face is out of frame.**
> Background: only the swing chain and the space around the hand. Generous negative space.
> Do not add any new symbolic object — draw only what is in the scene.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text in the top margin, large, in neat handwriting style:
> "일어나려는데 손바닥에 사슬 자국이 남아 있었다."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, episode titles.
> 4:5 aspect ratio (1080x1350).
> ```

---

## Stage 3 체크리스트
- [x] 각 컷 프롬프트가 콘티의 행동에서 시작하는가 — 전 컷 "행동:" / "Action:"으로 시작
- [x] 카메라 구도·거리가 콘티와 일치하는가 — 와이드/미디엄/원경/중경/디테일
- [x] 생활 디테일이 프롬프트에 들어갔는가 — 그네 사슬 (컷1·컷2·여운)
- [x] "한 장면만" 문구가 모든 컷에 있는가
- [x] 무대사 컷에 "글자를 넣지 마" 지시가 있는가 — 컷3
- [x] 본편 프롬프트에 에피소드 제목·컷 번호가 들어가지 않았는가
- [x] 표지는 0번 실사 배경 콜라주 워크플로로 별도 작성됐는가
- [x] 컷1~4·여운 모두 character_sheet.png 첨부 지시 포함
- [x] 3장부터 직전 컷 첨부 지시 포함
- [x] **로고·브랜드명 금지 지시가 있는가** — 놀이터 기구·휴대폰 화면 전부
- [x] 배경색 흰색(#ffffff), 비율 4:5(1080×1350) 지시가 모든 컷에 있는가
- [x] **미소 결말·창밖 목격 금지 지시가 전 컷에 있는가** (`brand/11_STORY_TYPES.md` 17장)
