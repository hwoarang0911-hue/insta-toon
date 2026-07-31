# [ep003] 이 곡, 진짜 여름 같아? — 이미지 렌더링 지시서

6장 각각에 대해 나노바나나(Gemini)용과 GPT용 프롬프트를 모두 제공한다.
사용자는 도구를 골라 해당 프롬프트만 복사해 쓰면 된다.

> ## ⚠️ 프롬프트 안의 한글 문구 = 이미지에 그려질 글자
> 따옴표 안 문구는 `02_storyboard.md`의 **「이미지에 들어가는 글자」 표와
> 글자 하나까지 같아야 한다.**
> 프롬프트를 쓰기 전에 그 표를 먼저 열어 대조한다.

# 0. 표지(1장) — 실사 배경 콜라주 (예외 워크플로)

> **표지만 다른 5장과 만드는 방식이 다르다.** 배경은 실제 사진, 캐릭터는 손그림 컷아웃을 합성한다.
> 컷1~4·여운(2~6장)은 아래 「🚀 한 번에 전달하기」로 넘어간다.
> (`brand/03_DRAWING_STYLE.md` 표지 예외, `brand/06_IMAGE_RULE.md` 표지 합성 절차 참고)

> **이번 화는 특정 랜드마크가 없다** (`01_storyline.md` 참고 — 노들섬 같은 실명 지명 대신 일반적인 여름날 공간으로 진행).
> 그래서 1단계 사진은 장소를 특정하지 않는다. **무겁게 가라앉은 여름 하늘, 소나기가 막 쏟아지기 시작하는 창밖·거리 풍경** 등
> 이 화의 분위기와 맞는 실제 사진이면 충분하다 (직접 촬영한 소나기 사진이 가장 좋다).

## 실행 순서 (4단계)
1. 소나기/무거운 여름 하늘 분위기의 실제 사진을 준비한다 (장소 특정 불필요 — 직접 촬영 권장)
2. 아래 캐릭터 컷아웃 프롬프트로 **배경 없는 캐릭터만** 생성 (character_sheet.png 첨부)
3. 사진 편집 툴(캔바, 미리캔버스, 포토샵 등)에서 사진 위에 캐릭터 컷아웃을 배치, 흰 테두리를 살려 스티커처럼 보이게 한다
4. 표지 문구를 손글씨 느낌 폰트로 얹는다: "이 곡, 진짜 여름 같아?"

### 캐릭터 컷아웃 프롬프트 — 한국어판 (Gemini/나노바나나)
```
첨부한 캐릭터 시트의 루아를 그대로 유지해서 그려줘. 캐릭터 시트가 외형의 기준이다.
상반신, 이어폰이나 작은 스피커 쪽으로 살짝 고개를 기울이고 의심스러운 듯 듣고 있는 표정(생각 중).
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
Pose/expression: upper body, head tilted slightly toward her earphones or a small speaker,
listening with a doubtful, thoughtful look.
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
무더운 토요일 오후, 집 안. 선풍기 앞에 앉은 루아가 스피커로 음악을 틀어놓고 생각에 잠긴 표정.
창밖 나뭇잎이 하나도 흔들리지 않는 정지된 느낌을 배경에 옅게.
넣을 글자 — "토요일 오후, 선풍기 앞에 앉아서 비발디의 여름을 틀었다. 근데 앞부분이 생각보다 너무 조용하다."

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
A hot Saturday afternoon, indoors. Lua sits in front of a fan, playing music from a small
speaker, lost in thought. In the background, faintly, the leaves outside the window are
completely still.
Text to render — "토요일 오후, 선풍기 앞에 앉아서 비발디의 여름을 틀었다. 근데 앞부분이 생각보다 너무 조용하다."

[Panel 3 ~ 6]  ← 한글 문구는 원문 그대로 (번역하지 않는다)
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
- 한국어: "손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게, 캐릭터는 화면에서 작지 않게, 텍스트는 크게, 컷 가장자리에 테두리선, 4:5 비율"
- 영어: "hand-drawn fountain pen sketch, thick irregular wobbly ink lines, black and white, pure white (#ffffff) background, hatching for shade, minimal background description, character kept large enough for mobile screens, large text, hand-drawn panel border, 4:5 aspect ratio"
- 네거티브(금지): "3D, realistic skin, anime style, glossy webtoon coloring, gradients, complex background, logos or brand names" / "3D, 사실적 피부, 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경, 로고·브랜드명 노출 금지"

---

## 2장 — 컷1

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png
>
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 세부 외형은 그 시트가 기준이다.
> 무더운 토요일 오후, 집 안. 선풍기 앞에 앉은 루아가 스피커로 음악을 틀어놓고 생각에 잠긴 표정(생각 중).
> 창밖 나뭇잎이 하나도 흔들리지 않는 정지된 느낌을 배경에 옅게.
> 캐릭터가 화면에서 작아지지 않게, 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로 그려줘.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> "토요일 오후, 선풍기 앞에 앉아서 비발디의 여름을 틀었다. 근데 앞부분이 생각보다 너무 조용하다."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게. 컷 가장자리에 손그림 테두리선을 둘러줘.
> 소지품(토트백 등)에 로고나 브랜드명을 넣지 마.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png
>
> ```
> Keep the exact same character (Lua) from the attached character sheet — it is the
> source of truth for her appearance:
> a Korean woman in her mid-20s, shoulder-length wavy black hair,
> tiny dot eyes, calm minimal expression, plain long-sleeve top and wide pants,
> a boxy tote bag (no logo or brand name).
> Scene: a hot Saturday afternoon indoors. Lua sits in front of a fan, playing music
> from a small speaker, lost in thought (thinking expression). In the background,
> faintly, the leaves outside the window are completely still.
> Keep her large enough to read clearly on a small (mobile) screen — do not draw her too small.
> Render this Korean text large, in neat handwriting style: "토요일 오후, 선풍기 앞에 앉아서 비발디의 여름을 틀었다. 근데 앞부분이 생각보다 너무 조용하다."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines,
> black and white, pure white (#ffffff) background, hatching for shade,
> minimal background description. Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background, logos or brand names.
> 4:5 aspect ratio (1080x1350).
> ```
> ※ 한글이 깨지면 텍스트 없이 생성 후 손글씨 폰트로 후삽입.

---

## 3장 — 컷2

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(2장)
>
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 세부 외형은 그 시트가 기준이다.
> 눈을 감고 음악을 듣는 루아. 턱에 손을 얹고 골몰히 생각하는 표정(고민 중).
> 배경에는 2장과 이어지는 창문, 나뭇잎이 여전히 하나도 흔들리지 않는 모습을 넓게 보여준다 — 고요함이 계속되고 있다는 느낌.
> 캐릭터가 화면에서 작아지지 않게, 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로 그려줘.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> 상단 — "여름인데 폭풍이 갑자기 몰아친대. 3악장 전까지는 계속 이렇게 잠잠하다."
> 하단에 작게 — "근데 왜 이렇게까지 참았다가 터지지?"
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게. 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png + 직전 컷(2장)
>
> ```
> Keep the exact same character (Lua) from the attached character sheet — it is the
> source of truth for her appearance. Same outfit and line style as the previous panel.
> Scene: Lua listens to the music with her eyes closed, chin resting on her hand,
> deep in thought (pondering expression). In the background, the same window from the
> previous panel, leaves still completely motionless, shown a little wider — the stillness
> is continuing.
> Keep her large enough to read clearly on a small (mobile) screen — do not draw her too small.
> Render this Korean text large, in neat handwriting style:
> Top — "여름인데 폭풍이 갑자기 몰아친대. 3악장 전까지는 계속 이렇게 잠잠하다."
> Small, bottom — "근데 왜 이렇게까지 참았다가 터지지?"
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines,
> black and white, pure white (#ffffff) background, hatching for shade,
> minimal background description. Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background, logos or brand names.
> 4:5 aspect ratio (1080x1350).
> ```
> ※ 한글이 깨지면 텍스트 없이 생성 후 손글씨 폰트로 후삽입.

---

## 4장 — 컷3

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(3장)
>
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 세부 외형은 그 시트가 기준이다.
> 창가로 다가가 하늘을 올려다보는 루아. 눈이 살짝 커진 정도의 표정(생각 중 — 놀람은 이 이상 넘지 않는다).
> 창밖은 무겁게 가라앉은 하늘, 그리고 정말 갑자기 비가 쏟아지기 시작하는 순간. 3장에서 미동도 없던 나뭇잎이
> 이 컷에서는 비바람에 세차게 흔들리는 모습으로 — 같은 나무가 고요에서 폭발로 바뀌었다는 걸 보여준다.
> 캐릭터가 화면에서 작아지지 않게, 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로 그려줘.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> "그러다 창밖을 봤는데, 하늘이 아까부터 이상하게 무거웠다. 그리고 정말 갑자기, 비가 쏟아지기 시작했다."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게. 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png + 직전 컷(3장)
>
> ```
> Keep the exact same character (Lua) from the attached character sheet — it is the
> source of truth for her appearance. Same outfit and line style as the previous panel.
> Scene: Lua steps toward the window and looks up at the sky, her eyes just slightly
> widened (thinking expression — surprise never goes further than this). Outside, the
> sky has been sitting heavy, and rain suddenly, truly suddenly starts pouring down.
> The same leaves that were completely still in the previous panel are now whipping
> wildly in the wind and rain — showing the same tree flipping from stillness to
> outburst.
> Keep her large enough to read clearly on a small (mobile) screen — do not draw her too small.
> Render this Korean text large, in neat handwriting style:
> "그러다 창밖을 봤는데, 하늘이 아까부터 이상하게 무거웠다. 그리고 정말 갑자기, 비가 쏟아지기 시작했다."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines,
> black and white, pure white (#ffffff) background, hatching for shade,
> minimal background description. Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background, logos or brand names.
> 4:5 aspect ratio (1080x1350).
> ```
> ※ 한글이 깨지면 텍스트 없이 생성 후 손글씨 폰트로 후삽입.

---

## 5장 — 컷4

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(4장)
>
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 세부 외형은 그 시트가 기준이다.
> 창가 또는 처마 밑에서 쏟아지는 비를 바라보는 루아의 옆모습, 옅은 미소(좋아하는 순간 → 미소).
> 배경은 빗줄기와 젖은 창밖 풍경만, 여백을 크게 남긴다.
> 캐릭터가 화면에서 작아지지 않게, 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로 그려줘.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> 상단 — "아, 여름은 원래 이렇게 참다가 한 번에 쏟아지는 계절이구나."
> 하단에 작게 — "나도 가끔은 이렇게 한 번씩 쏟아내도 되는 거였을까."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게. 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png + 직전 컷(4장)
>
> ```
> Keep the exact same character (Lua) from the attached character sheet — it is the
> source of truth for her appearance. Same outfit and line style as the previous panel.
> Scene: Lua's side profile at the window or under the eaves, watching the pouring rain,
> a faint smile (a moment of enjoyment → smile). Background is only rain streaks and a
> wet view outside the window, with generous negative space.
> Keep her large enough to read clearly on a small (mobile) screen — do not draw her too small.
> Render this Korean text large, in neat handwriting style:
> Top — "아, 여름은 원래 이렇게 참다가 한 번에 쏟아지는 계절이구나."
> Small, bottom — "나도 가끔은 이렇게 한 번씩 쏟아내도 되는 거였을까."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines,
> black and white, pure white (#ffffff) background, hatching for shade,
> minimal background description. Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background, logos or brand names.
> 4:5 aspect ratio (1080x1350).
> ```
> ※ 한글이 깨지면 텍스트 없이 생성 후 손글씨 폰트로 후삽입.

---

## 6장 — 여운

### 🍌 나노바나나 (Gemini)
> **첨부**: character_sheet.png + 직전 컷(5장)
>
> ```
> 첨부한 캐릭터 시트의 캐릭터(루아)를 그대로 유지해서 그려줘. 세부 외형은 그 시트가 기준이다.
> 비가 그친 뒤, 창문을 열고 서 있는 루아의 작은 뒷모습. 원경.
> 젖은 풍경 위로 옅은 햇살 한 줄기, 빗방울 떨어지는 소품은 최소한으로. 여백이 화면의 60% 이상.
> 캐릭터는 작게 배치하되, 작은 화면에서도 뒷모습의 형태는 뚜렷이 보이는 크기를 유지해줘.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘 (상단 여백에):
> "비가 그치고, 선선한 바람이 이마를 스치고 지나갔다."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게. 컷 가장자리에 손그림 테두리선을 둘러줘.
> 금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 복잡한 배경, 로고·브랜드명.
> 4:5 비율(1080×1350).
> ```

### 🤖 GPT (이미지 생성)
> **첨부**: character_sheet.png + 직전 컷(5장)
>
> ```
> Keep the exact same character (Lua) from the attached character sheet — it is the
> source of truth for her appearance. Same outfit and line style as the previous panel.
> Scene: after the rain has stopped, Lua's small figure from behind, standing at an open
> window. Wide shot. A faint ray of sunlight over the wet scenery, raindrop details kept
> minimal. Negative space covers 60%+ of the frame.
> Keep her small in the frame, but her silhouette from behind should still read clearly
> even on a small screen.
> Render this Korean text large, in neat handwriting style, in the top margin:
> "비가 그치고, 선선한 바람이 이마를 스치고 지나갔다."
> Style: hand-drawn fountain pen sketch, thick irregular wobbly ink lines,
> black and white, pure white (#ffffff) background, hatching for shade,
> minimal background description. Draw a hand-drawn border/outline around the panel edge.
> Avoid: 3D, realistic skin, anime style, glossy webtoon coloring, complex background, logos or brand names.
> 4:5 aspect ratio (1080x1350).
> ```
> ※ 한글이 깨지면 텍스트 없이 생성 후 손글씨 폰트로 후삽입.

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
