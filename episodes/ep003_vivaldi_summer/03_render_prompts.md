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
· 이 화의 그림 규칙: **유리 안쪽(실내)은 선을 거의 쓰지 않고 비운다.**
  유리 너머(창밖 한여름)만 해칭을 촘촘히 해서 뜨겁게 보이게 한다.
· 프레임: 컷 가장자리에 손으로 그린 테두리선을 두를 것.
· 금지: 3D, 사실적인 피부, 일본 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경,
        로고·브랜드명, 장면에 없는 상징물.
· 비율: 4:5 (1080×1350)
· 3장부터는 직전에 만든 그림의 인물과 선 스타일을 그대로 이어갈 것.
· 각 장의 카메라 거리가 다르다. 지정된 구도를 그대로 지킬 것.

=== 지금 만들 것 ===
[2장 · 컷1]
행동: 한여름 오후, 더위를 피해 들어온 루아가 창가 자리에 앉는다. 앉는 동작에 어깨의 가방끈이 팔꿈치까지 흘러내린다.
구도: 공간 와이드숏 / 카메라 거리 와이드 — 실내 전체가 보이고 루아는 그 안에 있다.
배경: 높은 층고, 흰 타일 벽, 큰 창으로 들어오는 흰 햇빛. 실내는 선을 적게 써서 서늘하고 조용해 보이게.
      위쪽 여백을 넓게 남겨 층고를 살린다.
표정: 생각 중.
이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
"밖이 너무 더워서 들어왔다. 앉자마자 비발디의 여름, 느린 악장을 틀었다."

=== 아래는 이후 순서. 지금 만들지 말 것 ===

[3장 · 컷2]
행동: 이어폰을 낀 채 듣고 있다. 무언가를 처음 알아채는 순간, 눈이 아주 조금 움직인다.
구도: 얼굴 일부 — 귀와 이어폰, 눈 아래까지만 / 카메라 거리 클로즈업.
배경: 흐린 밝은 면만. 이 컷에서는 실내도 창밖도 보이지 않는다 — 소리 안에만 있다.
표정: 고민 중.
넣을 글자 — 상단: "선율은 느린데 그 아래에서 뭐가 계속 낮게 깔려 있다."
             하단에 작게: "이거 원래 있었나?"

[4장 · 컷3]
행동: 고개를 들어 창밖을 본다. 아스팔트 위로 아지랑이가 올라오고, 사람들은 그늘 쪽으로만 붙어 걷고,
      가로수 잎은 하나도 안 움직인다. 한여름 대낮이 그대로 있다.
구도: 캐릭터 시점 — 루아가 보는 창밖. 화면 아래쪽에 유리와 컵 윗부분만 걸친다 / 카메라 거리 중경.
      루아의 얼굴은 보이지 않는다.
배경: **유리 안쪽은 선을 거의 비우고, 유리 너머만 해칭으로 빽빽하고 뜨겁게.**
      사람들은 얼굴 없는 실루엣으로만. 잎은 하나도 흔들리지 않게 그린다.
이미지 안에 글자를 넣지 마. (무대사 컷)

[5장 · 컷4]
행동: 창밖에서 눈을 떼지 않은 채 옆모습. 옅은 미소. 이어폰 줄에 손이 올라가 있다.
구도: 옆모습 / 카메라 거리 중경(허리 위).
배경: 창빛과 유리만. 여백 크게.
표정: 옅은 미소.
넣을 글자 — 상단: "밖은 아까부터 계속 저러고 있었다. 아, 안 들리던 게 아니라 안 듣고 있었구나."
             하단에 작게: "이 사람한테도 여름은 이랬겠지."

[6장 · 여운]
행동: 테이블 위. 다 식은 커피컵을 쥔 손. 팔꿈치엔 아까 흘러내린 가방끈이 그대로 걸려 있다.
구도: 손 디테일 — 컵과 손, 가방끈 끝 / 카메라 거리 디테일. 얼굴은 프레임 밖.
배경: 테이블 표면과 컵 아랫부분만. 여백 크게. 컵에 로고 금지.
넣을 글자 — 상단 여백에: "커피가 다 식을 때까지 그 부분만 계속 들었다."
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
· Episode-specific rule: **leave the interior side of the glass almost empty of linework.**
  Only what is beyond the glass (the midsummer street) gets dense hatching, so it reads as hot.
· Frame: draw a hand-drawn border/outline around the edge of each panel.
· Avoid: 3D, realistic skin, Japanese anime style, glossy webtoon coloring, gradients,
  complex backgrounds, logos or brand names, symbolic objects not in the scene.
· Aspect ratio: 4:5 (1080x1350)
· From panel 3 onward, carry over the character and line style of the previous image.
· Each panel uses a different camera distance. Follow the specified composition exactly.

=== GENERATE PANEL 2 ONLY. THE REST COME LATER ===
[Panel 2 · cut 1]
Action: a midsummer afternoon. Escaping the heat, Lua sits down at a window table. As she sits,
  her bag strap slides off her shoulder down to her elbow.
Composition: wide establishing shot / camera distance WIDE — the whole room is visible and she
  is inside it.
Background: high ceiling, white tiled walls, large windows with flat white daylight. Keep the
  interior sparse in linework so it reads cool and quiet. Leave generous space at the top.
Expression: thoughtful.
Render this Korean text large, in neat handwriting style:
"밖이 너무 더워서 들어왔다. 앉자마자 비발디의 여름, 느린 악장을 틀었다."

=== BELOW: LATER PANELS. DO NOT GENERATE YET ===

[Panel 3 · cut 2]
Action: she is listening through her earphones. At the moment she first notices something, her
  eyes shift very slightly.
Composition: partial face — only her ear, the earphone, and down to just below her eyes /
  camera distance CLOSE-UP.
Background: only a blurred bright plane. Neither the room nor the street is visible here —
  she is inside the sound.
Expression: pondering.
Text — top: "선율은 느린데 그 아래에서 뭐가 계속 낮게 깔려 있다."
       small, bottom: "이거 원래 있었나?"

[Panel 4 · cut 3]
Action: she looks up and out the window. Heat shimmer rises off the asphalt, people walk hugging
  the shade, and not one leaf on the street trees is moving. The midsummer afternoon is simply there.
Composition: her point of view — the street through the glass, with only the glass and the top of
  her cup entering the bottom of the frame / camera distance MEDIUM. Her face is not visible.
Background: **keep the interior side of the glass nearly empty of linework; give only what is
  beyond the glass dense, hot hatching.** People are faceless silhouettes. No leaf moves.
Do not render any text in this image. (silent panel)

[Panel 5 · cut 4]
Action: still not taking her eyes off the window, seen in profile, a faint smile, one hand
  raised to the earphone cord.
Composition: side profile / camera distance MEDIUM (waist up).
Background: only window light and glass. Generous negative space.
Expression: faint smile.
Text — top: "밖은 아까부터 계속 저러고 있었다. 아, 안 들리던 게 아니라 안 듣고 있었구나."
       small, bottom: "이 사람한테도 여름은 이랬겠지."

[Panel 6 · closing]
Action: the tabletop. A hand around a cup of coffee gone cold. The bag strap is still hanging at
  her elbow where it slid earlier.
Composition: hand detail — the cup, the hand, the end of the strap / camera distance DETAIL.
  Her face is out of frame.
Background: only the table surface and the base of the cup. Generous negative space. No logo on the cup.
Text — in the top margin: "커피가 다 식을 때까지 그 부분만 계속 들었다."
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
- 네거티브: "3D, 사실적 피부, 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경, 로고·브랜드명, 에피소드 제목·컷 번호, 장면에 없는 상징물"

---

## 2장 — 컷1 (와이드)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 세부 외형은 그 시트가 기준이다.
> 행동: 한여름 오후, 더위를 피해 들어온 루아가 창가 자리에 앉는다.
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
> Action: a midsummer afternoon. Escaping the heat, Lua sits down at a window table. As she sits,
> her bag strap slides off her shoulder down to her elbow.
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

## 3장 — 컷2 (클로즈업)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(2장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 이어폰을 낀 채 듣고 있다. 무언가를 처음 알아채는 순간, 눈이 아주 조금 움직인다.
> 구도: 얼굴 일부 — 귀와 이어폰, 눈 아래까지만. 카메라 거리는 클로즈업.
> 배경: 흐린 밝은 면만. 이 컷에서는 실내도 창밖도 보이지 않는다 — 소리 안에만 있다.
> 표정: 고민 중. 놀람은 눈이 조금 움직이는 정도까지만.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> 상단 — "선율은 느린데 그 아래에서 뭐가 계속 낮게 깔려 있다."
> 하단에 작게 — "이거 원래 있었나?"
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
> Action: she is listening through her earphones. At the moment she first notices something, her
> eyes shift very slightly.
> Composition: partial face — only her ear, the earphone, and down to just below her eyes /
> camera distance CLOSE-UP.
> Background: only a blurred bright plane. Neither the room nor the street is visible here —
> she is inside the sound.
> Expression: pondering. Surprise never goes past a slight eye movement.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text large, in neat handwriting style:
> Top — "선율은 느린데 그 아래에서 뭐가 계속 낮게 깔려 있다."
> Small, bottom — "이거 원래 있었나?"
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, episode titles.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 4장 — 컷3 (중경 · 캐릭터 시점 · **무대사**)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(3장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 고개를 들어 창밖을 본다. 아스팔트 위로 아지랑이가 올라오고, 사람들은 그늘 쪽으로만 붙어 걷고,
>       가로수 잎은 하나도 안 움직인다. 한여름 대낮이 그대로 있다.
> 구도: 캐릭터 시점 — 루아가 보는 창밖을 그린다. 화면 아래쪽에 유리와 컵 윗부분만 걸친다.
>       카메라 거리는 중경. **루아의 얼굴은 보이지 않는다.**
> 배경: 이 화에서 유일하게 선이 빽빽한 컷. **유리 안쪽(실내)은 선을 거의 비우고,
>       유리 너머(창밖)만 해칭을 촘촘히 해서 뜨겁게 보이게 한다.** 사람들은 얼굴 없는 실루엣으로만.
>       잎은 하나도 흔들리지 않게 그린다.
> 간판·컵·앞치마에 브랜드 이름이나 로고를 넣지 마.
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
> Action: she looks up and out the window. Heat shimmer rises off the asphalt, people walk hugging
> the shade, and not one leaf on the street trees is moving. The midsummer afternoon is simply there.
> Composition: her point of view — the street through the glass, with only the glass and the top of
> her cup entering the bottom of the frame / camera distance MEDIUM. **Her face is not visible.**
> Background: the only densely drawn panel in this episode. **Keep the interior side of the glass
> nearly empty of linework; give only what is beyond the glass dense, hot hatching.**
> People are faceless silhouettes. No leaf moves.
> No brand name or logo on signage, cups, or aprons.
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
> 행동: 창밖에서 눈을 떼지 않은 채 옆모습. 옅은 미소. 이어폰 줄에 손이 올라가 있다.
> 구도: 옆모습, 허리 위. 카메라 거리는 중경.
> 배경: 창빛과 유리만. 여백 크게. **창밖 풍경은 이제 자세히 그리지 않는다.**
> 표정: 옅은 미소 (좋아하는 순간 → 미소). 과장하지 않는다.
> 컵에 로고나 브랜드명을 넣지 마.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> 상단 — "밖은 아까부터 계속 저러고 있었다. 아, 안 들리던 게 아니라 안 듣고 있었구나."
> 하단에 작게 — "이 사람한테도 여름은 이랬겠지."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영.
> 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명, 에피소드 제목.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT
> **첨부**: character_sheet.png + 직전 컷(4장)
> ```
> Keep the exact same character (Lua) from the attached character sheet. Carry over the line
> style of the previous panel.
> Action: still not taking her eyes off the window, seen in profile, a faint smile, one hand
> raised to the earphone cord.
> Composition: side profile, waist up / camera distance MEDIUM.
> Background: only window light and glass. Generous negative space. **Do not render the street
> outside in detail anymore.**
> Expression: a faint smile. Do not exaggerate.
> No logo or brand name on the cup.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text large, in neat handwriting style:
> Top — "밖은 아까부터 계속 저러고 있었다. 아, 안 들리던 게 아니라 안 듣고 있었구나."
> Small, bottom — "이 사람한테도 여름은 이랬겠지."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white,
> pure white (#ffffff) background, hatching for shade.
> Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background,
>        logos or brand names, episode titles.
> 4:5 aspect ratio (1080x1350).
> ```

---

## 6장 — 여운 (디테일 · 손)

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(5장)
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 직전 컷의 선 스타일을 이어갈 것.
> 행동: 테이블 위. 다 식은 커피컵을 쥔 손. 어깨에서 흘러내린 가방끈이 아직 팔꿈치에 걸려 있다.
> 구도: 손 디테일 — 컵과 손, 가방끈 끝. 카메라 거리는 디테일(가까이). **얼굴은 프레임 밖.**
> 배경: 테이블 표면과 컵 아랫부분만. 여백을 크게 남긴다.
> 컵에 로고나 브랜드명을 넣지 마.
> 새로운 상징물을 넣지 마. 장면에 있는 것만 그린다.
> 이 한 장면만 담은 독립된 이미지 하나를 만들어줘.
> 만화 격자, 콜라주, 분할 화면을 만들지 마. 다른 컷의 문구를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 상단 여백에 손글씨 느낌으로 크게 넣어줘:
> "커피가 다 식을 때까지 그 부분만 계속 들었다."
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
> Action: the tabletop. A hand around a cup of coffee gone cold. The bag strap is still hanging
> at her elbow where it slid earlier.
> Composition: hand detail — the cup, the hand, the end of the strap / camera distance DETAIL.
> **Her face is out of frame.**
> Background: only the table surface and the base of the cup. Generous negative space.
> No logo or brand name on the cup.
> Do not add any new symbolic object — draw only what is in the scene.
> Generate one standalone image containing only this single scene.
> Do not create a comic grid, collage, or split screen. Do not include text from any other panel.
> Render this Korean text in the top margin, large, in neat handwriting style:
> "커피가 다 식을 때까지 그 부분만 계속 들었다."
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
- [x] 카메라 구도·거리가 콘티와 일치하는가 — 와이드/클로즈업/중경/중경/디테일
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
