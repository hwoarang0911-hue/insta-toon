# [ep003] 조용한 데가 제일 안 조용하다 — 이미지 렌더링 지시서

6장 각각에 대해 나노바나나(Gemini)용과 GPT용 프롬프트를 모두 제공한다.
사용자는 도구를 골라 해당 프롬프트만 복사해 쓰면 된다.

> ## ⚠️ 프롬프트 안의 한글 문구 = 이미지에 그려질 글자
> 따옴표 안 문구는 `02_storyboard.md`의 **「이미지에 들어가는 글자」 표와
> 글자 하나까지 같아야 한다.**
> 프롬프트를 쓰기 전에 그 표를 먼저 열어 대조한다.

> ## ⚠️ 카페 브랜드명·로고 금지
> 이 화의 무대는 홍대 길가의 미니멀한 유리창 카페다. 실제 카페 브랜드의 이름·로고·간판은
> **어떤 컷에도 넣지 않는다** (`brand/03_DRAWING_STYLE.md` 금지). 컵·창문·간판 전부 무지로 그린다.

# 0. 표지(1장) — 실사 배경 콜라주 (예외 워크플로)

> **표지만 다른 5장과 만드는 방식이 다르다.** 배경은 실제 사진, 캐릭터는 손그림 컷아웃을 합성한다.
> 컷1~4·여운(2~6장)은 아래 「🚀 한 번에 전달하기」로 넘어간다.
> (`brand/03_DRAWING_STYLE.md` 표지 예외, `brand/06_IMAGE_RULE.md` 표지 합성 절차 참고)

## 실행 순서 (4단계)
1. **비 오는 날 홍대 길가 사진**을 준비한다 (직접 촬영 권장 — 카페 유리창 너머 젖은 거리, 우산 쓴 사람들).
   ※ 사진에 실제 카페 간판·로고가 찍혔으면 잘라내거나 흐리게 지운다
2. 아래 캐릭터 컷아웃 프롬프트로 **배경 없는 캐릭터만** 생성 (character_sheet.png 첨부)
3. 사진 편집 툴(캔바, 미리캔버스, 포토샵 등)에서 사진 위에 캐릭터 컷아웃을 배치, 흰 테두리를 살려 스티커처럼 보이게 한다
4. 표지 문구를 손글씨 느낌 폰트로 얹는다: "이 곡, 조용한 데가 제일 안 조용하다"

### 캐릭터 컷아웃 프롬프트 — 한국어판 (Gemini/나노바나나)
```
첨부한 캐릭터 시트의 루아를 그대로 유지해서 그려줘. 캐릭터 시트가 외형의 기준이다.
상반신. 비를 맞아 머리끝이 살짝 젖은 상태로, 이어폰을 낀 채 옆쪽을 조용히 바라보는 표정(생각 중).
캐릭터가 화면에서 작아지지 않게, 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로 그려줘.
배경은 순백색(#ffffff)으로, 캐릭터만 오려내기 쉽게 그려줘. 배경 요소는 아무것도 넣지 마.
스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백, 해칭 음영.
소지품(토트백, 컵 등)에 로고나 브랜드명을 넣지 마.
금지: 3D, 사실적 피부, 애니풍, 웹툰 광택, 그라데이션, 배경 요소 일체, 로고·워드마크.
4:5 비율(1080×1350).
```

### 캐릭터 컷아웃 프롬프트 — 영어판 (ChatGPT)
```
Keep the exact same character (Lua) from the attached character sheet — it is the source of
truth for her appearance:
a Korean woman in her mid-20s, shoulder-length wavy black hair,
tiny dot eyes, calm minimal expression, plain long-sleeve top and wide pants.
Pose/expression: upper body, hair slightly damp from the rain, wearing earphones,
looking quietly off to one side (thoughtful expression).
Keep the character large enough to read clearly on a small (mobile) screen — do not draw her too small.
Background: pure flat white (#ffffff), nothing else — the character must be easy to cut out cleanly.
Style: hand-drawn fountain pen sketch, thick and irregular wobbly ink lines,
black and white, hatching for shade.
No logos or brand names on any accessory (tote bag, cup, etc).
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
· 무대: 홍대 길가의 큰 유리창 카페. 회색 콘크리트와 나무의 미니멀한 실내.
  카페 간판·컵·창문 어디에도 실제 브랜드 이름이나 로고를 넣지 말 것. 전부 무지로.
· 캐릭터 크기: 화면에서 작아지지 않게. 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로.
· 그림체: 손으로 그린 만년필 펜 스케치. 선은 두껍고 불규칙하며 굵기가 일정하지 않다.
  흑백, 배경색은 흰색(#ffffff), 음영은 해칭(빗금)으로만.
  배경 묘사는 짧게, 최소한으로만 (표지와 달리 실사 배경 없음 — 전부 손그림 배경).
· 이 화의 그림 규칙: 유리창을 경계로 **안쪽은 선을 거의 쓰지 않고, 바깥쪽은 빗줄기 해칭을 빽빽하게**.
  같은 화면에서 고요와 폭우가 붙어 있게 그린다.
· 텍스트: 크게 — 작은 화면에서도 한 번에 읽히는 크기로.
· 프레임: 컷 가장자리에 손으로 그린 테두리선(외곽선)을 두를 것.
· 금지: 3D, 사실적인 피부, 일본 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경, 로고·브랜드명 노출.
· 비율: 4:5 (1080×1350)
· 각 장에 지정된 한글 텍스트를 이미지 안에 손글씨 느낌으로 정확히 넣을 것.
· 3장부터는 직전에 만든 그림의 인물과 선 스타일을 그대로 이어갈 것.

=== 지금 만들 것 ===
[2장 · 컷1]
소나기. 비를 맞은 루아가 홍대 길가 카페 문을 밀고 들어선다. 어깨와 토트백이 젖어 있다.
큰 유리창, 회색 콘크리트와 나무의 미니멀한 실내. 밖은 빗줄기 해칭으로 어수선하게, 안은 선을 최소한으로.
넣을 글자 — "비를 쫄딱 맞고 홍대 길가 카페로 뛰어들었다. 이어폰에선 아직 비발디의 여름이 흐르고 있었다."

=== 아래는 이후 순서. 지금 만들지 말 것 ===
[3장 · 컷2] 창가 자리에 앉은 루아. 컵을 앞에 두고 이어폰에 귀를 기울인다. 실내는 아주 조용하다. 표정은 고민 중.
  유리창은 아직 화면 가장자리에만 걸치게.
  넣을 글자 — 상단 "자리에 앉으니 안은 조용하다. 근데 곡은 느린 악장인데 저 아래에서 뭔가 계속 웅웅거린다."
  하단에 작게 "조용한 부분인데 왜 하나도 안 편하지?"

[4장 · 컷3] 고개를 돌려 창밖을 보는 루아. 유리 한 장 너머로 퍼붓는 비, 우산 쓴 사람들, 젖은 길이 그대로 다 보인다.
  유리를 경계로 안쪽은 선이 거의 없고 바깥쪽은 빗줄기 해칭이 빽빽하게. 이 화의 가장 조용한 컷.
  넣을 글자 — "유리 한 장 너머로 비가 그대로 다 보인다. 소리만 없고 나머지는 하나도 안 사라졌다."

[5장 · 컷4] 여전히 창밖을 보는 루아의 옆모습, 옅은 미소. 컵을 두 손으로 감싸 쥐고 있다. 배경은 유리창과 빗줄기만, 여백 크게.
  넣을 글자 — 상단 "아, 조용해져도 밖은 안 사라지니까 그렇구나. 비발디는 그 조용함을 이렇게 써놨다."
  하단에 작게 "잘 썼다는 말이 이제야 무슨 뜻인지 알겠다."

[6장 · 여운] 멀리서 본 창가 자리. 이어폰을 뺀 루아의 작은 뒷모습이 창밖을 보고 있다. 원경.
  여백이 화면의 60% 이상. 유리에 맺힌 물방울 몇 개만 소품으로.
  넣을 글자 — 상단 여백에 "이어폰을 뺐다. 창밖이 계속 그 곡이었다."
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
· Setting: a minimal cafe with large street-facing windows in Hongdae, Seoul.
  Grey concrete and wood interior. Do NOT put any real brand name or logo anywhere —
  not on the signage, the cup, or the window. Everything stays blank.
· Character size: keep her large enough to read clearly on a small (mobile) screen —
  do not draw her too small.
· Style: hand-drawn fountain pen sketch. Thick, irregular, wobbly ink lines of uneven
  weight. Black and white on a pure white (#ffffff) background. Shading only through
  hatching. Background description kept minimal and brief (unlike the cover, no photo
  background — every background here is hand-drawn).
· Rule specific to this episode: use the window as a divider — **almost no linework on the
  inside, dense rain hatching on the outside.** Stillness and downpour sit side by side in
  the same frame.
· Text: large — readable at a glance on a small screen.
· Frame: draw a hand-drawn border/outline around the edge of each panel.
· Avoid: 3D, realistic skin, Japanese anime style, glossy webtoon coloring,
  gradients, complex backgrounds, logos or brand names.
· Aspect ratio: 4:5 (1080x1350)
· Render the Korean text specified for each panel inside the image, in neat
  handwriting style, exactly as written.
· From panel 3 onward, carry over the character and line style of the previous image.

=== GENERATE PANEL 2 ONLY. THE REST COME LATER ===
[Panel 2 · cut 1]
A sudden summer downpour. Lua, soaked, pushes open the door of a street-facing cafe in
Hongdae. Her shoulders and tote bag are wet. Large windows, grey concrete and wood
interior. Outside is busy with rain hatching; inside uses as little linework as possible.
Text to render — "비를 쫄딱 맞고 홍대 길가 카페로 뛰어들었다. 이어폰에선 아직 비발디의 여름이 흐르고 있었다."

=== BELOW: LATER PANELS. DO NOT GENERATE YET ===
[Panel 3 · cut 2] Lua sits at the window seat, a cup in front of her, listening closely to her
  earphones. The interior is very quiet. Pondering expression. The window only grazes the
  edge of the frame for now.
  Text — top: "자리에 앉으니 안은 조용하다. 근데 곡은 느린 악장인데 저 아래에서 뭔가 계속 웅웅거린다."
  small, bottom: "조용한 부분인데 왜 하나도 안 편하지?"

[Panel 4 · cut 3] Lua turns her head to look out the window. Through a single pane of glass,
  the pouring rain, people under umbrellas, and the soaked street are all fully visible.
  The window divides the frame: almost no linework inside, dense rain hatching outside.
  The quietest panel of the episode.
  Text — "유리 한 장 너머로 비가 그대로 다 보인다. 소리만 없고 나머지는 하나도 안 사라졌다."

[Panel 5 · cut 4] Lua's side profile, still watching out the window, a faint smile, both hands
  wrapped around the cup. Background is only the window and rain, generous negative space.
  Text — top: "아, 조용해져도 밖은 안 사라지니까 그렇구나. 비발디는 그 조용함을 이렇게 써놨다."
  small, bottom: "잘 썼다는 말이 이제야 무슨 뜻인지 알겠다."

[Panel 6 · closing] A wide shot of the window seat from a distance. Lua's small figure from
  behind, earphones now removed, still facing the window. Negative space covers 60%+ of the
  frame. Only a few droplets on the glass as props.
  Text — in the top margin: "이어폰을 뺐다. 창밖이 계속 그 곡이었다."
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
> 소나기. 비를 맞은 루아가 홍대 길가 카페 문을 밀고 들어선다. 어깨와 토트백이 젖어 있다.
> 큰 유리창, 회색 콘크리트와 나무의 미니멀한 실내. 표정은 생각 중.
> 밖은 빗줄기 해칭으로 어수선하게, 안은 선을 최소한으로 — 한 컷 안에서 밖과 안이 갈리게.
> 카페 간판·컵·창문 어디에도 실제 브랜드 이름이나 로고를 넣지 마. 전부 무지로.
> 캐릭터가 화면에서 작아지지 않게, 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로 그려줘.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> "비를 쫄딱 맞고 홍대 길가 카페로 뛰어들었다. 이어폰에선 아직 비발디의 여름이 흐르고 있었다."
> 스타일: 손으로 그린 만년필 펜 스케치, 두껍고 불규칙한 선, 흑백,
> 흰색(#ffffff) 배경, 해칭 음영, 배경 묘사는 짧게. 컷 가장자리에 손그림 테두리선을 둘러줘.
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
> Scene: a sudden summer downpour. Soaked, Lua pushes open the door of a street-facing
> cafe in Hongdae. Her shoulders and tote bag are wet. Large windows, grey concrete and
> wood minimal interior. Thoughtful expression. Outside is busy with rain hatching;
> inside uses as little linework as possible, so the frame splits into outside and inside.
> Put no real brand name or logo anywhere — signage, cup, window all stay blank.
> Keep her large enough to read clearly on a small (mobile) screen — do not draw her too small.
> Render this Korean text large, in neat handwriting style: "비를 쫄딱 맞고 홍대 길가 카페로 뛰어들었다. 이어폰에선 아직 비발디의 여름이 흐르고 있었다."
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
> 창가 자리에 앉은 루아. 컵을 앞에 두고 이어폰에 귀를 기울인다. 실내는 아주 조용하다.
> 턱에 손을 얹고 골몰히 생각하는 표정(고민 중). 유리창은 아직 화면 가장자리에만 걸치게 — 아직 밖을 제대로 보지 않았다.
> 컵에 로고나 브랜드명을 넣지 마. 무지 컵으로.
> 캐릭터가 화면에서 작아지지 않게, 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로 그려줘.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> 상단 — "자리에 앉으니 안은 조용하다. 근데 곡은 느린 악장인데 저 아래에서 뭔가 계속 웅웅거린다."
> 하단에 작게 — "조용한 부분인데 왜 하나도 안 편하지?"
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
> Scene: Lua sits at the window seat, a cup in front of her, listening closely to her
> earphones. The interior is very quiet. Chin resting on her hand, deep in thought
> (pondering expression). The window only grazes the edge of the frame — she has not
> properly looked outside yet. The cup stays blank, no logo or brand name.
> Keep her large enough to read clearly on a small (mobile) screen — do not draw her too small.
> Render this Korean text large, in neat handwriting style:
> Top — "자리에 앉으니 안은 조용하다. 근데 곡은 느린 악장인데 저 아래에서 뭔가 계속 웅웅거린다."
> Small, bottom — "조용한 부분인데 왜 하나도 안 편하지?"
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
> 고개를 돌려 창밖을 보는 루아. 유리 한 장 너머로 퍼붓는 비, 우산 쓴 사람들, 젖은 길이 그대로 다 보인다.
> 실내에는 소리가 없다. 표정은 생각 중.
> 이 컷의 핵심: 유리를 경계로 **안쪽(루아 쪽)은 선이 거의 없이 비우고, 바깥쪽은 빗줄기 해칭을 빽빽하게** 채워서
> 같은 화면 안에 고요와 폭우가 나란히 붙어 있게 그려줘. 이 에피소드의 가장 조용한 컷이다.
> 밖의 사람들은 얼굴 없는 실루엣으로만.
> 캐릭터가 화면에서 작아지지 않게, 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로 그려줘.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> "유리 한 장 너머로 비가 그대로 다 보인다. 소리만 없고 나머지는 하나도 안 사라졌다."
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
> Scene: Lua turns her head to look out the window. Through a single pane of glass, the
> pouring rain, people under umbrellas, and the soaked street are all fully visible.
> Inside there is no sound. Thoughtful expression.
> The key to this panel: use the window as a divider — **the inside (Lua's side) is left
> almost empty with barely any linework, while the outside is filled with dense rain
> hatching** — so stillness and downpour sit side by side in one frame. This is the
> quietest panel of the episode. People outside are faceless silhouettes only.
> Keep her large enough to read clearly on a small (mobile) screen — do not draw her too small.
> Render this Korean text large, in neat handwriting style:
> "유리 한 장 너머로 비가 그대로 다 보인다. 소리만 없고 나머지는 하나도 안 사라졌다."
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
> 여전히 창밖을 보는 루아의 옆모습, 옅은 미소(좋아하는 순간 → 미소). 컵을 두 손으로 감싸 쥐고 있다.
> 배경은 유리창과 빗줄기만, 여백을 크게 남긴다. 컵에 로고나 브랜드명을 넣지 마.
> 4장과 같은 유리 경계 구도를 유지하되, 이번엔 화면을 조금 더 비운다.
> 캐릭터가 화면에서 작아지지 않게, 작은 화면(모바일)에서도 형태가 뚜렷이 보이는 크기로 그려줘.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘:
> 상단 — "아, 조용해져도 밖은 안 사라지니까 그렇구나. 비발디는 그 조용함을 이렇게 써놨다."
> 하단에 작게 — "잘 썼다는 말이 이제야 무슨 뜻인지 알겠다."
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
> Scene: Lua's side profile, still watching out the window, a faint smile (a moment of
> quiet enjoyment → smile), both hands wrapped around the cup. Background is only the
> window and rain, with generous negative space. The cup stays blank, no logo or brand name.
> Keep the same window-as-divider composition as the previous panel, but empty the frame
> a little further.
> Keep her large enough to read clearly on a small (mobile) screen — do not draw her too small.
> Render this Korean text large, in neat handwriting style:
> Top — "아, 조용해져도 밖은 안 사라지니까 그렇구나. 비발디는 그 조용함을 이렇게 써놨다."
> Small, bottom — "잘 썼다는 말이 이제야 무슨 뜻인지 알겠다."
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
> 멀리서 본 창가 자리. 이어폰을 뺀 루아의 작은 뒷모습이 창밖을 보고 있다. 원경.
> 여백이 화면의 60% 이상. 유리에 맺힌 물방울 몇 개만 소품으로.
> 캐릭터는 작게 배치하되, 작은 화면에서도 뒷모습의 형태는 뚜렷이 보이는 크기를 유지해줘.
> 카페 간판·컵 어디에도 브랜드 이름이나 로고를 넣지 마.
> 이미지 안에 다음 한글 텍스트를 손글씨 느낌으로 크게, 정확히 넣어줘 (상단 여백에):
> "이어폰을 뺐다. 창밖이 계속 그 곡이었다."
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
> Scene: a wide shot of the window seat from a distance. Lua's small figure from behind,
> earphones now removed, still facing the window. Negative space covers 60%+ of the frame.
> Only a few droplets on the glass as props. No brand name or logo on the signage or cup.
> Keep her small in the frame, but her silhouette from behind should still read clearly
> even on a small screen.
> Render this Korean text large, in neat handwriting style, in the top margin:
> "이어폰을 뺐다. 창밖이 계속 그 곡이었다."
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
- [x] 로고·브랜드명 노출 금지 지시가 있는가 (카페 간판·컵 포함, 매 컷)
