# [ep003] 쉬는 악장인 줄 알았는데 — 이미지 렌더링 지시서

> **프롬프트 우선순위** (`brand/06_IMAGE_RULE.md`) — 각 컷은 콘티의 장면(보이는 행동)에서 시작한다.
> **본편 컷(2~6장)에 에피소드 제목·컷 번호·다른 컷 문구를 넣지 않는다.** 제목은 표지에만.
> **로고·워드마크 금지** — 컵·간판·앞치마·휴대폰 화면 전부 무지. 공간의 생김새로만 카페를 식별한다.
> 따옴표 안 문구는 `02_storyboard.md`의 「이미지에 들어가는 글자」 표와 글자 하나까지 같아야 한다.

# 0. 표지(1장) — 실사 배경 콜라주

## 실행 순서 (4단계)
1. **블루보틀 실내 사진**을 준비한다 (높은 층고, 흰 타일, 큰 창, 한낮의 흰빛).
   ※ 사진에 **간판·컵의 로고가 찍혔으면 잘라내거나 지운다**
2. 아래 캐릭터 컷아웃 프롬프트로 **배경 없는 캐릭터만** 생성 (character_sheet.png 첨부)
3. 사진 위에 배치, 흰 테두리를 살려 스티커처럼. **원근과 빛을 맞춘다** — 창빛이 옆에서 오게
4. 제목 "쉬는 악장인 줄 알았는데"를 손글씨 폰트로 **상단**에 얹는다. 캐릭터는 우하단 — **겹치지 않게**

> 표지 장면은 컷1에 실제로 나오는 장면이다. 상징적 장면을 새로 만들지 않았다.

### 캐릭터 컷아웃 — 한국어판 (Gemini/나노바나나)
```
첨부한 캐릭터 시트의 루아를 그대로 유지해서 그려줘. 캐릭터 시트가 외형의 기준이다.
행동: 상반신. 창가 자리에 앉아 이어폰을 낀 채 살짝 고개를 기울이고 듣고 있다(생각 중).
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
Action: upper body, seated by the window, wearing earphones, head tilted slightly as she listens.
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
  담백한 표정, 무지 긴팔 상의와 통 넓은 바지, 각진 토트백(로고 없음).
  첨부한 캐릭터 시트의 인물을 그대로 유지할 것 — 세부 외형은 그 시트가 기준이다.
· 무대: 한여름 오후, 층고 높은 커피 전문점. 흰 타일 벽, 원목 바 카운터, 큰 창으로 들어오는 흰 햇빛.
  실내는 미니멀하고 비어 있다.
  ❗ 간판·컵·앞치마·휴대폰 화면 어디에도 브랜드 이름이나 로고를 넣지 마. 전부 무지로.
· 캐릭터 크기: 화면에서 작아지지 않게. 작은 화면에서도 형태가 뚜렷이 보이는 크기로.
· 그림체: 손으로 그린 만년필 펜 스케치. 선은 두껍고 불규칙하다.
  흑백, 배경색은 흰색(#ffffff), 음영은 해칭(빗금)으로만. 배경 묘사는 짧게.
· 이 화의 감정 규칙: **입꼬리를 올리는 미소 표정을 어느 컷에도 그리지 마.**
  가장 감정이 큰 컷(5장)도 표정은 "집중"까지만 — 눈매가 살짝 진지해지는 정도.
· 프레임: 컷 가장자리에 손으로 그린 테두리선을 두를 것.
· 금지: 3D, 사실적인 피부, 일본 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경,
        로고·브랜드명, 장면에 없는 상징물.
· 비율: 4:5 (1080×1350)
· 3장부터는 직전에 만든 그림의 인물과 선 스타일을 그대로 이어갈 것.
· 각 장의 카메라 거리가 다르다. 지정된 구도를 그대로 지킬 것.

=== 지금 만들 것 ===
[2장 · 컷1]
행동: 한여름 오후, 더위를 피해 들어온 루아가 창가 자리에 앉아 이어폰을 끼고 재생 버튼을 누른다.
      앉는 동작에 어깨의 가방끈이 팔꿈치까지 흘러내린다.
구도: 공간 와이드숏 / 카메라 거리 와이드 — 실내 전체가 보이고 루아는 그 안에 있다.
배경: 높은 층고, 흰 타일 벽, 큰 창으로 들어오는 흰 햇빛. 실내는 선을 적게 써서 서늘하고 조용해 보이게.
      위쪽 여백을 넓게 남겨 층고를 살린다.
표정: 생각 중.
이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
"밖이 너무 더워서 들어왔다. 앉자마자 비발디의 여름, 느린 악장을 틀었다."

=== 아래는 이후 순서. 지금 만들지 말 것 ===

[3장 · 컷2]
행동: 테이블 위 손끝. 듣다가 낮게 깔린 소리를 처음 알아채고, 그 박자를 따라 손끝으로
      테이블을 톡, 톡 짚어본다. **얼굴은 프레임 밖.**
구도: 손 디테일 — 손끝과 테이블 표면만 / 카메라 거리 디테일.
배경: 테이블 표면만, 나머지는 거의 여백.
넣을 글자 — 상단: "선율은 느린데 그 아래에서 뭐가 계속 낮게 깔려 있다. 손끝으로 박자를 짚어봤다."

[4장 · 컷3]
행동: 얼굴 클로즈업. 손끝으로 짚은 박자와 이어폰 속 소리가 같다는 걸 확인한 순간,
      눈이 아주 조금 커진다.
구도: 얼굴 클로즈업 — 눈과 이어폰 낀 귀까지 / 카메라 거리 클로즈업.
배경: 흐린 밝은 면만. **창밖도 카페 내부도 보여주지 않는다** — 확인은 이 얼굴 하나로 끝난다.
표정: 알아채는 순간 (눈이 살짝 커짐). 미소 아님.
이미지 안에 글자를 넣지 마. (무대사 컷)

[5장 · 컷4]
행동: 이어폰 줄에 손이 올라가 있고, 다른 손은 휴대폰 화면의 재생 바를 뒤로 미는 중.
      옆모습, 살짝 앞으로 기운 자세.
구도: 옆모습 / 카메라 거리 중경(허리 위).
배경: 창빛과 유리만. 여백 크게.
표정: 집중. **입꼬리를 올리지 않는다.**
넣을 글자 — 상단: "다시 앞으로 돌려서 들었다. 이번엔 놓치지 않았다."

[6장 · 여운]
행동: 테이블 위. 휴대폰 재생 바 옆에 놓인 손, 손끝이 아직 리듬을 짚고 있다.
      팔꿈치엔 아까 흘러내린 가방끈이 그대로 걸려 있다.
구도: 테이블 전체와 컵, 휴대폰이 함께 보이는 중경 / 카메라 거리 중경. 얼굴은 프레임 밖.
배경: 테이블 표면 전체. 여백 크게. 컵과 휴대폰에 로고 금지.
넣을 글자 — 상단 여백에: "그 부분만 세 번 더 돌려 들었다."
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
  calm minimal expression, plain long-sleeve top, wide-leg pants, a boxy tote bag (no logo).
  Keep the exact same character as the attached character sheet — it is the source of truth.
· Setting: a midsummer afternoon in a high-ceilinged specialty coffee shop. White tiled walls,
  a wooden bar counter, large windows letting in flat white daylight. The room is minimal and empty.
  ❗ Put NO brand name or logo anywhere — signage, cups, aprons, phone screen all stay blank.
· Character size: keep her large enough to read clearly on a small (mobile) screen.
· Style: hand-drawn fountain pen sketch. Thick, irregular, wobbly ink lines. Black and white
  on a pure white (#ffffff) background. Shading only through hatching. Background kept brief.
· Episode-specific rule: **do not draw a smiling expression, on any panel.**
  Even the most emotional panel (panel 5) stops at "focused" — eyes narrowing slightly, no raised
  corners of the mouth.
· Frame: draw a hand-drawn border/outline around the edge of each panel.
· Avoid: 3D, realistic skin, Japanese anime style, glossy webtoon coloring, gradients,
  complex backgrounds, logos or brand names, symbolic objects not in the scene.
· Aspect ratio: 4:5 (1080x1350)
· From panel 3 onward, carry over the character and line style of the previous image.
· Each panel uses a different camera distance. Follow the specified composition exactly.

=== GENERATE PANEL 2 ONLY. THE REST COME LATER ===
[Panel 2 · cut 1]
Action: a midsummer afternoon. Escaping the heat, Lua sits down at a window table, puts in her
  earphones, and presses play. As she sits, her bag strap slides off her shoulder down to her elbow.
Composition: wide establishing shot / camera distance WIDE — the whole room is visible and she
  is inside it.
Background: high ceiling, white tiled walls, large windows with flat white daylight. Keep the
  interior sparse in linework so it reads cool and quiet. Leave generous space at the top.
Expression: thoughtful.
Render this Korean text large, in neat handwriting style:
"밖이 너무 더워서 들어왔다. 앉자마자 비발디의 여름, 느린 악장을 틀었다."

=== BELOW: LATER PANELS. DO NOT GENERATE YET ===

[Panel 3 · cut 2]
Action: the tabletop, her fingertip. She first notices something low sitting under the melody,
  and taps the table lightly with her fingertip, following the beat. **Her face is out of frame.**
Composition: hand detail — only her fingertip and the table surface / camera distance DETAIL.
Background: only the table surface, mostly negative space.
Text — top: "선율은 느린데 그 아래에서 뭐가 계속 낮게 깔려 있다. 손끝으로 박자를 짚어봤다."

[Panel 4 · cut 3]
Action: a close-up on her face. The moment she confirms the beat her fingertip tapped matches
  the sound in her ears, her eyes widen just slightly.
Composition: close-up on her face — eyes and the earphone-wearing ear / camera distance CLOSE-UP.
Background: only a blurred bright plane. **Show neither the street nor the café interior** —
  the confirmation happens on this face alone.
Expression: the moment of noticing (eyes widen slightly). Not a smile.
Do not render any text in this image. (silent panel)

[Panel 5 · cut 4]
Action: one hand raised to the earphone cord, the other hand scrubbing the phone's playback bar
  backward. Side profile, leaning slightly forward.
Composition: side profile / camera distance MEDIUM (waist up).
Background: only window light and glass. Generous negative space.
Expression: focused. **Do not raise the corners of the mouth.**
Text — top: "다시 앞으로 돌려서 들었다. 이번엔 놓치지 않았다."

[Panel 6 · closing]
Action: the tabletop. A hand resting beside the phone's playback bar, fingertip still faintly
  tracing the rhythm. The bag strap is still hanging at her elbow where it slid earlier.
Composition: a medium shot showing the whole table, the cup, and the phone together /
  camera distance MEDIUM. Her face is out of frame.
Background: the full table surface. Generous negative space. No logo on the cup or phone.
Text — in the top margin: "그 부분만 세 번 더 돌려 들었다."
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
- 스타일 흔들림 시: `assets/samples/sample_4cut_bruckner_mahler.png` 추가 첨부

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
> 행동: 한여름 오후, 더위를 피해 들어온 루아가 창가 자리에 앉아 이어폰을 끼고 재생 버튼을 누른다.
>       앉는 동작에 어깨의 가방끈이 팔꿈치까지 흘러내린다.
> 구도: 공간 와이드숏. 카메라 거리는 와이드 — 실내 전체가 보이고 루아는 그 안에 있다.
> 배경: 층고 높은 커피 전문점. 흰 타일 벽, 원목 바 카운터, 큰 창으로 들어오는 흰 햇빛.
>       실내는 선을 적게 써서 서늘하고 조용해 보이게. 위쪽 여백을 넓게 남겨 층고를 살린다.
> 표정: 생각 중.
> 간판·컵·앞치마 어디에도 브랜드 이름이나 로고를 넣지 마. 전부 무지로.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> "밖이 너무 더워서 들어왔다. 앉자마자 비발디의 여름, 느린 악장을 틀었다."
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
> tiny dot eyes, calm minimal expression, plain long-sleeve top and wide pants, a boxy tote bag.
> Action: a midsummer afternoon. Escaping the heat, Lua sits down at a window table, puts in her
> earphones, and presses play. As she sits, her bag strap slides off her shoulder down to her elbow.
> Composition: wide establishing shot / camera distance WIDE — the whole room is visible and she
> is inside it.
> Background: a high-ceilinged coffee shop. White tiled walls, a wooden bar counter, large windows
> with flat white daylight. Keep the interior sparse in linework so it reads cool and quiet.
> Leave generous space at the top.
> Expression: thoughtful.
> Put no brand name or logo anywhere — signage, cups, aprons all stay blank.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text large, in neat handwriting style:
> "밖이 너무 더워서 들어왔다. 앉자마자 비발디의 여름, 느린 악장을 틀었다."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, episode titles, panel numbers.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 3장 — 컷2 (디테일 · 손끝 · 얼굴 안 보임)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(2장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 테이블 위, 손끝. 듣다가 낮게 깔린 소리를 처음 알아채고, 그 박자를 따라
>       손끝으로 테이블을 톡, 톡 짚어본다. **얼굴은 프레임 밖.**
> 구도: 손 디테일 — 손끝과 테이블 표면만. 카메라 거리는 디테일.
> 배경: 테이블 표면만, 나머지는 거의 여백. 손가락 동작이 리듬감 있게 보이도록.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> "선율은 느린데 그 아래에서 뭐가 계속 낮게 깔려 있다. 손끝으로 박자를 짚어봤다."
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
> Action: the tabletop, her fingertip. She first notices something low sitting under the melody,
> and taps the table lightly with her fingertip, following the beat. **Her face is out of frame.**
> Composition: hand detail — only her fingertip and the table surface / camera distance DETAIL.
> Background: only the table surface, mostly negative space. The finger motion should read
> with a sense of rhythm.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text large, in neat handwriting style:
> "선율은 느린데 그 아래에서 뭐가 계속 낮게 깔려 있다. 손끝으로 박자를 짚어봤다."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, episode titles.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 4장 — 컷3 (클로즈업 · 얼굴 · **무대사**)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(3장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 얼굴 클로즈업. 손끝으로 짚은 박자와 이어폰 속 소리가 같다는 걸 확인한 순간,
>       눈이 아주 조금 커진다.
> 구도: 얼굴 클로즈업 — 눈과 이어폰 낀 귀까지. 카메라 거리는 클로즈업.
> 배경: 흐린 밝은 면만. **창밖도 카페 내부도 보여주지 않는다** — 확인은 이 얼굴 하나로 끝난다.
> 표정: 알아채는 순간 (눈이 살짝 커짐). **미소가 아니다.**
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> **이미지 안에 글자를 넣지 마.**
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명, 글자 일체, 미소 표정.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png + 직전 컷(3장)
> ```
> Keep the exact same character (Lua) from the attached character sheet. Carry over the line
> style of the previous panel.
> Action: a close-up on her face. The moment she confirms the beat her fingertip tapped matches
> the sound in her ears, her eyes widen just slightly.
> Composition: close-up on her face — eyes and the earphone-wearing ear / camera distance CLOSE-UP.
> Background: only a blurred bright plane. **Show neither the street nor the café interior** —
> the confirmation happens on this face alone.
> Expression: the moment of noticing (eyes widen slightly). **Not a smile.**
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> **Do not render any text in this image.**
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, any text, a smiling expression.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 5장 — 컷4 (중경 · 옆모습)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(4장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 이어폰 줄에 손이 올라가 있고, 다른 손은 휴대폰 화면의 재생 바를 뒤로 미는 중.
>       옆모습, 살짝 앞으로 기운 자세.
> 구도: 옆모습, 허리 위. 카메라 거리는 중경.
> 배경: 창빛과 유리만. 여백 크게.
> 표정: 집중. **입꼬리를 올리지 않는다 — 미소가 아니다.**
> 휴대폰 화면·컵에 로고나 브랜드명을 넣지 마.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> "다시 앞으로 돌려서 들었다. 이번엔 놓치지 않았다."
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
> Action: one hand raised to the earphone cord, the other hand scrubbing the phone's playback bar
> backward. Side profile, leaning slightly forward.
> Composition: side profile, waist up / camera distance MEDIUM.
> Background: only window light and glass. Generous negative space.
> Expression: focused. **Do not raise the corners of the mouth — not a smile.**
> No logo or brand name on the phone screen or the cup.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text large, in neat handwriting style:
> "다시 앞으로 돌려서 들었다. 이번엔 놓치지 않았다."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, episode titles, a smiling expression.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 6장 — 여운 (중경 · 테이블)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(5장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 테이블 위. 휴대폰 재생 바 옆에 놓인 손, 손끝이 아직 리듬을 짚고 있다.
>       팔꿈치엔 아까 흘러내린 가방끈이 그대로 걸려 있다.
> 구도: 테이블 전체와 컵, 휴대폰이 함께 보이는 중경. 카메라 거리는 중경. **얼굴은 프레임 밖.**
> 배경: 테이블 표면 전체. 여백을 크게 남긴다.
> 컵과 휴대폰 화면에 로고나 브랜드명을 넣지 마.
> 새로운 상징물을 넣지 마. 장면에 있는 것만 그린다.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 상단 여백에 손글씨 느낌으로 크게 넣어줘:
> "그 부분만 세 번 더 돌려 들었다."
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
> Action: the tabletop. A hand resting beside the phone's playback bar, fingertip still faintly
> tracing the rhythm. The bag strap is still hanging at her elbow where it slid earlier.
> Composition: a medium shot showing the whole table, the cup, and the phone together /
> camera distance MEDIUM. **Her face is out of frame.**
> Background: the full table surface. Generous negative space.
> No logo or brand name on the cup or the phone screen.
> Do not add any new symbolic object — draw only what is in the scene.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text in the top margin, large, in neat handwriting style:
> "그 부분만 세 번 더 돌려 들었다."
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
- [x] 카메라 구도·거리가 콘티와 일치하는가 — 와이드/디테일/클로즈업/중경/중경
- [x] 생활 디테일이 프롬프트에 들어갔는가 — 가방끈 (컷1·여운)
- [x] "한 장면만" 문구가 모든 컷에 있는가
- [x] 무대사 컷에 "글자를 넣지 마" 지시가 있는가 — 컷3
- [x] 본편 프롬프트에 에피소드 제목·컷 번호가 들어가지 않았는가
- [x] 표지는 0번 실사 배경 콜라주 워크플로로 별도 작성됐는가
- [x] 컷1~4·여운 모두 character_sheet.png 첨부 지시 포함
- [x] 3장부터 직전 컷 첨부 지시 포함
- [x] **로고·브랜드명 금지 지시가 있는가** — 간판·컵·앞치마·휴대폰 화면 전부
- [x] 배경색 흰색(#ffffff), 비율 4:5(1080×1350) 지시가 모든 컷에 있는가
- [x] 감정 형용사 반복·장면에 없는 상징물이 없는가
- [x] **미소 결말·창밖 목격 금지 지시가 전 컷에 있는가** (`brand/11_STORY_TYPES.md` 17장)
