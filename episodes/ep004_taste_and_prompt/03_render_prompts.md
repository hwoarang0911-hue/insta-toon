# [ep004] 커서만 십 분째 — 이미지 렌더링 지시서

> **프롬프트 우선순위** (`brand/06_IMAGE_RULE.md`) — 각 컷은 콘티의 `visible_action`에서 시작한다.
> **본편 컷(2~6장)에 에피소드 제목·컷 번호·다른 컷 문구를 넣지 않는다.** 제목은 표지에만.
> **화면 속 UI에 실제 서비스명·로고를 넣지 않는다.**
> 따옴표 안 문구는 `02_storyboard.md`의 「이미지에 들어가는 글자」 표와 글자 하나까지 같아야 한다.

# 0. 표지(1장) — 실사 배경 콜라주

## 실행 순서 (4단계)
1. **밤중 책상 사진**을 준비한다 (모니터 빛만 있는 어두운 방). 화면에 실제 서비스 UI가 찍혔으면 지운다
2. 아래 캐릭터 컷아웃 프롬프트로 **배경 없는 캐릭터만** 생성 (character_sheet.png 첨부)
3. 사진 위에 배치, 흰 테두리를 살려 스티커처럼. **원근과 빛을 맞춘다** — 모니터 빛이 얼굴 쪽에서 오게
4. 제목 "커서만 십 분째"를 손글씨 폰트로 **좌상단**에 얹는다. 캐릭터는 우측 — **겹치지 않게**

> 표지 장면은 컷1에 실제로 나오는 장면이다. 상징적 장면을 새로 만들지 않았다.

### 캐릭터 컷아웃 — 한국어판 (Gemini/나노바나나)
```
첨부한 캐릭터 시트의 루아를 그대로 유지해서 그려줘. 캐릭터 시트가 외형의 기준이다.
행동: 상반신. 책상 앞에 앉아 키보드 위에 손만 올려둔 채 화면 쪽을 보고 있다(생각 중).
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
Action: upper body, seated at a desk with her hands resting on the keyboard, looking at the
screen (thoughtful expression).
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
  담백한 표정, 무지 긴팔 상의와 통 넓은 바지. 첨부한 캐릭터 시트의 인물을 그대로 유지할 것.
· 무대: 밤 11시, 루아의 방 책상. 방 불은 꺼져 있고 모니터 빛만 있다.
  화면 속 UI에 실제 서비스 이름이나 로고를 넣지 마. 화면 요소는 단순한 네모와 선으로만.
· 캐릭터 크기: 화면에서 작아지지 않게. 작은 화면에서도 형태가 뚜렷이 보이는 크기로.
· 그림체: 손으로 그린 만년필 펜 스케치. 선은 두껍고 불규칙하다.
  흑백, 배경색은 흰색(#ffffff), 음영은 해칭(빗금)으로만. 배경 묘사는 짧게.
· 이 화의 그림 규칙: 방은 거의 비우고, 모니터 주변만 밝게. 어둠은 넓은 여백으로 처리한다
  (검게 칠하지 말고 선을 비워서 어둡게 보이게 한다).
· 프레임: 컷 가장자리에 손으로 그린 테두리선을 두를 것.
· 금지: 3D, 사실적인 피부, 일본 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경,
        로고·브랜드명, 장면에 없는 상징물.
· 비율: 4:5 (1080×1350)
· 3장부터는 직전에 만든 그림의 인물과 선 스타일을 그대로 이어갈 것.
· 각 장의 카메라 거리가 전부 다르다. 지정된 구도를 그대로 지킬 것.

=== 지금 만들 것 ===
[2장 · 컷1]
행동: 어두운 방 책상 앞. 모니터에 빈 입력창과 깜빡이는 커서만 있다.
      루아는 키보드 위에 손만 올려둔 채 가만히 있다.
구도: 공간 와이드숏 / 카메라 거리 와이드 — 방 전체가 어둡고 모니터 주변만 밝다.
배경: 책상, 의자, 책상 옆에 엽서꽂이가 작게 보인다, 꺼진 방 조명.
표정: 생각 중.
이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘: "뭐 만들지."

=== 아래는 이후 순서. 지금 만들지 말 것 ===

[3장 · 컷2]
행동: 화면에 결과 이미지 여러 장이 떠 있다. 손은 마우스에서 떨어져 있고 그냥 보고만 있다.
구도: 어깨너머 — 루아의 어깨 너머로 본 모니터 화면 / 카메라 거리 중경. 뒤통수와 어깨만 보인다.
배경: 화면 속 결과물은 네모 몇 개로만 그린다. 실제 이미지나 서비스 UI를 그리지 마.
이미지 안에 글자를 넣지 마. (무대사 컷)

[4장 · 컷3]
행동: 의자를 옆으로 돌린다. 책상 아래에서 발이 천천히 흔들린다.
구도: 바닥 가까이에서 보는 구도 — 책상 아래, 의자 다리와 흔들리는 발 / 카메라 거리 디테일.
       얼굴은 보이지 않는다.
배경: 바닥, 의자 바퀴, 전선 한 줄.
이미지 안에 글자를 넣지 마. (무대사 컷)

[5장 · 컷4]
행동: 책상 옆 엽서꽂이에서 엽서 한 장을 뽑아 든다. 손끝으로 가장자리를 만진다.
구도: 손 디테일 — 엽서를 쥔 두 손 / 카메라 거리 디테일. 얼굴은 프레임 밖.
배경: 엽서꽂이 가장자리와 책상 표면만. 엽서 그림은 단순한 선 몇 개로.
이미지 안에 다음 한글 텍스트를 넣어줘: "아, 이건 좀 좋다."

[6장 · 여운]
행동: 모니터 옆에 엽서가 붙어 있다. 화면의 입력창은 그대로 비어 있고 커서만 깜빡인다.
구도: 위에서 내려다보는 구도 — 책상 위 전체 / 카메라 거리 중경. 인물은 없다.
배경: 모니터, 붙인 엽서, 키보드, 빈 입력창. 여백을 화면의 60% 이상.
이미지 안에 글자를 넣지 마. (무대사 컷)
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
  calm minimal expression, plain long-sleeve top, wide-leg pants. Keep the exact same character
  as the attached character sheet — it is the source of truth for her appearance.
· Setting: 11pm, Lua's desk in her room. The room light is off; only the monitor is lit.
  Put no real service name or logo in the on-screen UI — render screen elements as plain
  rectangles and lines only.
· Character size: keep her large enough to read clearly on a small (mobile) screen.
· Style: hand-drawn fountain pen sketch. Thick, irregular, wobbly ink lines. Black and white
  on a pure white (#ffffff) background. Shading only through hatching. Background kept brief.
· Episode-specific rule: leave the room almost empty and keep only the area around the monitor
  detailed. Render darkness as open negative space — do not fill it with black.
· Frame: draw a hand-drawn border/outline around the edge of each panel.
· Avoid: 3D, realistic skin, Japanese anime style, glossy webtoon coloring, gradients,
  complex backgrounds, logos or brand names, symbolic objects not in the scene.
· Aspect ratio: 4:5 (1080x1350)
· From panel 3 onward, carry over the character and line style of the previous image.
· Every panel uses a DIFFERENT camera distance. Follow the specified composition exactly.

=== GENERATE PANEL 2 ONLY. THE REST COME LATER ===
[Panel 2 · cut 1]
Action: a dark room, at the desk. The monitor shows an empty input box with a blinking cursor.
  Lua sits still, hands resting on the keyboard.
Composition: wide establishing shot / camera distance WIDE — the room is dark and only the
  area around the monitor is lit.
Background: desk, chair, a small postcard holder beside the desk, the room light off.
Expression: thoughtful.
Render this Korean text large, in neat handwriting style: "뭐 만들지."

=== BELOW: LATER PANELS. DO NOT GENERATE YET ===

[Panel 3 · cut 2]
Action: several generated images are now on screen. Her hand has left the mouse; she is just
  looking at them.
Composition: over the shoulder — the monitor seen past her shoulder / camera distance MEDIUM.
  Only the back of her head and her shoulders are visible.
Background: render the on-screen results as a few plain rectangles only. Do not draw real
  images or any service UI.
Do not render any text in this image. (silent panel)

[Panel 4 · cut 3]
Action: she swivels the chair sideways. Under the desk, her foot swings slowly.
Composition: low angle near the floor — under the desk, the chair legs and her swinging foot /
  camera distance DETAIL. Her face is not visible.
Background: floor, a chair caster, one cable.
Do not render any text in this image. (silent panel)

[Panel 5 · cut 4]
Action: she pulls a single postcard from the holder beside the desk and holds it, running a
  fingertip along its edge.
Composition: hand detail — both hands holding the postcard / camera distance DETAIL.
  Her face is out of frame.
Background: only the edge of the holder and the desk surface. Draw the postcard's picture as
  a few simple lines.
Render this Korean text: "아, 이건 좀 좋다."

[Panel 6 · closing]
Action: the postcard is now stuck beside the monitor. On screen, the input box is still empty
  with the cursor blinking.
Composition: looking down from above — the whole desktop / camera distance MEDIUM. No character.
Background: monitor, the stuck postcard, keyboard, the empty input box. Negative space covers
  60%+ of the frame.
Do not render any text in this image. (silent panel)
```

## (C) 후보정용 글자표
한글이 깨지면 텍스트 없이 생성 후 `02_storyboard.md`의 「이미지에 들어가는 글자」 표 기준으로 손글씨 폰트 삽입.
**컷2·컷3·여운은 원래 무대사다** — 글자를 넣지 않는다.

---
---

# 컷별 상세 프롬프트

## 공통 준비물
- 참조 1: `assets/character_sheet.png` — **모든 컷에 첨부**
- 참조 2: 직전에 생성한 컷 이미지 — **3장부터 첨부**

## 스타일 고정 문구
- 한국어: "손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게, 컷 가장자리에 테두리선, 4:5 비율"
- 영어: "hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white, pure white (#ffffff) background, hatching for shade, minimal background description, hand-drawn panel border, 4:5 aspect ratio"
- 네거티브: "3D, 사실적 피부, 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경, 로고·브랜드명, 에피소드 제목·컷 번호, 장면에 없는 상징물"

---

## 2장 — 컷1 (와이드)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 세부 외형은 그 시트가 기준이다.
> 행동: 어두운 방 책상 앞. 모니터에 빈 입력창과 깜빡이는 커서만 있다.
>       루아는 키보드 위에 손만 올려둔 채 가만히 있다.
> 구도: 공간 와이드숏. 카메라 거리는 와이드 — 방 전체가 어둡고 모니터 주변만 밝다.
> 배경: 책상, 의자, 책상 옆에 엽서꽂이가 작게 보인다, 꺼진 방 조명.
>       어둠은 검게 칠하지 말고 선을 비워서 표현해줘.
> 표정: 생각 중.
> 화면 속 UI에 실제 서비스 이름이나 로고를 넣지 마. 입력창은 단순한 네모와 선으로만.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘: "뭐 만들지."
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
> Action: a dark room, at the desk. The monitor shows an empty input box with a blinking
> cursor. Lua sits still, hands resting on the keyboard.
> Composition: wide establishing shot / camera distance WIDE — the room is dark and only the
> area around the monitor is lit.
> Background: desk, chair, a small postcard holder beside the desk, the room light off.
> Render darkness as open negative space, not filled black.
> Expression: thoughtful.
> Put no real service name or logo in the UI — the input box is plain rectangles and lines.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text large, in neat handwriting style: "뭐 만들지."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, episode titles, panel numbers.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 3장 — 컷2 (중경 · 어깨너머 · 무대사)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(2장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 화면에 결과 이미지 여러 장이 떠 있다. 손은 마우스에서 떨어져 있고 그냥 보고만 있다.
> 구도: 어깨너머 — 루아의 어깨 너머로 본 모니터 화면. 카메라 거리는 중경.
>       뒤통수와 어깨만 보인다. 얼굴은 보이지 않는다.
> 배경: 화면 속 결과물은 네모 몇 개로만. 실제 이미지나 서비스 UI를 그리지 마.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> **이미지 안에 글자를 넣지 마.**
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명, 글자 일체.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png + 직전 컷(2장)
> ```
> Keep the exact same character (Lua) from the attached character sheet. Carry over the line
> style of the previous panel.
> Action: several generated images are now on screen. Her hand has left the mouse; she is just
> looking at them.
> Composition: over the shoulder — the monitor seen past her shoulder / camera distance MEDIUM.
> Only the back of her head and her shoulders are visible. Her face is not visible.
> Background: render the on-screen results as a few plain rectangles only. Do not draw real
> images or any service UI.
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

## 4장 — 컷3 (디테일 · 바닥 가까이 · 무대사)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(3장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 의자를 옆으로 돌린다. 책상 아래에서 발이 천천히 흔들린다.
> 구도: 바닥 가까이에서 보는 구도 — 책상 아래, 의자 다리와 흔들리는 발.
>       카메라 거리는 디테일. **얼굴은 보이지 않는다. 발과 의자 다리 위주.**
> 배경: 바닥, 의자 바퀴, 전선 한 줄. 그 외에는 비운다.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> **이미지 안에 글자를 넣지 마.**
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 신발·의자의 로고, 글자 일체.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png + 직전 컷(3장)
> ```
> Keep the exact same character (Lua) from the attached character sheet. Carry over the line
> style of the previous panel.
> Action: she swivels the chair sideways. Under the desk, her foot swings slowly.
> Composition: low angle near the floor — under the desk, the chair legs and her swinging foot /
> camera distance DETAIL. **Her face is not visible. Focus on the foot and chair legs.**
> Background: floor, a chair caster, one cable. Leave the rest empty.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> **Do not render any text in this image.**
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos on the shoe or chair, any text.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 5장 — 컷4 (디테일 · 손)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(4장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 책상 옆 엽서꽂이에서 엽서 한 장을 뽑아 든다. 손끝으로 엽서 가장자리를 만진다.
> 구도: 손 디테일 — 엽서를 쥔 두 손. 카메라 거리는 디테일. **얼굴은 프레임 밖.**
> 배경: 엽서꽂이 가장자리와 책상 표면만. 엽서 그림은 단순한 선 몇 개로만 (구체적 그림 금지).
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘: "아, 이건 좀 좋다."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 엽서 속 로고·브랜드명, 에피소드 제목.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png + 직전 컷(4장)
> ```
> Keep the exact same character (Lua) from the attached character sheet. Carry over the line
> style of the previous panel.
> Action: she pulls a single postcard from the holder beside the desk and holds it, running a
> fingertip along its edge.
> Composition: hand detail — both hands holding the postcard / camera distance DETAIL.
> **Her face is out of frame.**
> Background: only the edge of the holder and the desk surface. Draw the postcard's picture as
> a few simple lines — no specific illustration.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text large, in neat handwriting style: "아, 이건 좀 좋다."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names on the postcard, episode titles.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 6장 — 여운 (중경 · 위에서 · 무대사 · 인물 없음)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(5장)
> ```
> 직전 컷의 선 스타일을 그대로 이어갈 것. (이 컷에는 인물이 나오지 않는다)
> 행동: 모니터 옆에 엽서가 붙어 있다. 화면의 입력창은 그대로 비어 있고 커서만 깜빡인다.
> 구도: 위에서 내려다보는 구도 — 책상 위 전체. 카메라 거리는 중경. **인물은 그리지 마.**
> 배경: 모니터, 붙인 엽서, 키보드, 빈 입력창. 여백을 화면의 60% 이상 남긴다.
> 새로운 상징물을 넣지 마. 장면에 있는 것만 그린다.
> 화면 속 UI에 실제 서비스 이름이나 로고를 넣지 마.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> **이미지 안에 글자를 넣지 마.**
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명, 글자 일체.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png + 직전 컷(5장)
> ```
> Carry over the line style of the previous panel. (No character appears in this panel.)
> Action: the postcard is now stuck beside the monitor. On screen, the input box is still empty
> with the cursor blinking.
> Composition: looking down from above — the whole desktop / camera distance MEDIUM.
> **Do not draw the character.**
> Background: monitor, the stuck postcard, keyboard, the empty input box. Negative space covers
> 60%+ of the frame.
> Do not add any new symbolic object — draw only what is in the scene.
> Put no real service name or logo in the on-screen UI.
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

## Stage 3 체크리스트
- [x] **각 컷 프롬프트가 콘티의 `visible_action`에서 시작하는가** — 전 컷 "행동:" / "Action:"으로 시작
- [x] 카메라 구도·거리가 콘티와 일치하는가 — 와이드/중경/디테일/디테일/중경
- [x] 생활 디테일이 프롬프트에 들어갔는가 — 컷3 전체가 흔들리는 발
- [x] **"한 장면만" 문구가 모든 컷에 있는가**
- [x] **무대사 컷에 "글자를 넣지 마" 지시가 있는가** — 컷2·컷3·여운
- [x] **본편 프롬프트에 에피소드 제목·컷 번호가 들어가지 않았는가**
- [x] 표지는 0번 실사 배경 콜라주 워크플로로 별도 작성됐는가
- [x] 컷1~4·여운 모두 character_sheet.png 첨부 지시 포함
- [x] 3장부터 직전 컷 첨부 지시 포함
- [x] 매 컷 스타일 고정 문구 + 금지 문구 포함
- [x] 화면 텍스트 원문이 따옴표로 정확히 명시됨
- [x] 배경색 흰색(#ffffff), 비율 4:5(1080×1350) 지시가 모든 컷에 있는가
- [x] 로고·브랜드명 노출 금지 지시가 있는가 (화면 UI·엽서·신발 포함)
- [x] 감정 형용사 반복·장면에 없는 상징물이 없는가
