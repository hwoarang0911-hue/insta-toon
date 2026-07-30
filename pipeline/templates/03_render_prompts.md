# [epNNN] 제목 — 이미지 렌더링 지시서

6장 각각에 대해 나노바나나(Gemini)용과 GPT용 프롬프트를 모두 제공한다.
사용자는 도구를 골라 해당 프롬프트만 복사해 쓰면 된다.

> ## ⚠️ 프롬프트 안의 한글 문구 = 이미지에 그려질 글자
> 따옴표 안 문구는 `02_storyboard.md`의 **「이미지에 들어가는 글자」 표와
> 글자 하나까지 같아야 한다.** 콘티 대사가 바뀌면 이 파일도 즉시 따라간다.
> 프롬프트를 쓰기 전에 그 표를 먼저 열어 대조한다.

## 공통 준비물
- 참조 1: `assets/character_sheet.png` — **모든 컷에 첨부**
- 참조 2: 직전에 생성한 컷 이미지 — **2장부터 첨부** (연속성)
- 스타일 흔들림 시: `assets/samples/sample_4cut_bruckner_mahler.png` 추가 첨부

## 스타일 고정 문구 (매 컷 프롬프트에 포함됨)
- 한국어: "손으로 그린 만년필 펜 스케치, 불규칙한 선, 흑백, 오프화이트 배경, 해칭 음영, 미니멀한 배경, 여백 많음"
- 영어: "hand-drawn fountain pen sketch, irregular wobbly ink lines, black and white, off-white paper background, hatching for shade, minimal background, generous negative space"
- 네거티브(금지): "3D, realistic skin, anime style, glossy webtoon coloring, gradients, complex background" / "3D, 사실적 피부, 애니풍, 웹툰 광택, 그라데이션, 복잡한 배경 금지"

---

## N장 — (역할: 표지/컷1.../여운)   ← 6장 각각 반복

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
- [ ] 6컷 모두 character_sheet.png 첨부 지시 포함
- [ ] 2장부터 직전 컷 첨부 지시 포함
- [ ] 매 컷 스타일 고정 문구 + 금지 문구 포함
- [ ] 화면 텍스트 원문이 따옴표로 정확히 명시됨
