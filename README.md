# Novak-Prompt

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![English](https://img.shields.io/badge/Language-English-blue.svg)](#-english)
[![中文](https://img.shields.io/badge/Language-中文-blue.svg)](#-中文)

**把任何課綱、教案或文章，轉成符合 Novak 理論的概念圖與教學方案的提示詞庫。**
**A prompt library that turns any curriculum, lesson plan, or article into a Novak-style concept map and teaching plan.**

---

## 🇹🇼 中文

### 這是什麼？

Novak-Prompt 收錄一套給大型語言模型用的「課綱轉概念圖」提示詞。它依據 Joseph D. Novak 與 Alberto J. Cañas 的概念圖理論、David Ausubel 的有意義學習理論，要求模型：

- 以**命題**（概念 A + 關係詞 + 概念 B）為最小單位，不寫空泛的「有關」「相關」
- 依**階層分化**排列概念，具體實例放在最底層
- 用 ★ 標出**橫向連結**，沒有就明說，不硬湊
- 控制每張圖 12–20 個節點，超過就拆圖
- 自動判斷輸入類型（單課備課／課綱架構／網路文章／舊教案審查），走對應流程
- 產出概念停車場、命題矩陣、Mermaid 概念圖、教學方案與迷思概念防線

### 怎麼用

1. 打開 [`prompts/novak-concept-map.zh-TW.md`](prompts/novak-concept-map.zh-TW.md)（英文版：[`prompts/novak-concept-map.en.md`](prompts/novak-concept-map.en.md)）
2. 整份複製，在最後一行「在此貼上你的輸入內容」換成你的課綱、教案或文章
3. 貼給任何對話模型。要快速版或完整版，在輸入裡註明即可

### 🕶️ 盲測

同一份提示詞、同一份素材，兩個模型匿名對決。先讀完兩份輸出再揭曉模型：

| # | 素材 | 對決 |
|---|---|---|
| 01 | [安大略省三年級科學「堅固穩定的結構」](blind-tests/01-ontario-grade3-structures/) | 🕶️ 揭曉前保密（提示：同門內戰） |

### 📊 完整測試結果

**即將推出。** 橫跨多個學科與學段、多組模型的完整評測，整理完成後會連結到這裡。

---

## 🌍 English

### What is this?

Novak-Prompt is a prompt for large language models that converts teaching material into concept maps. Grounded in Joseph D. Novak and Alberto J. Cañas's concept-mapping theory and David Ausubel's theory of meaningful learning, it makes the model:

- build on **propositions** (Concept A + linking phrase + Concept B), never vague "related to" links
- arrange concepts by **progressive differentiation**, with concrete examples at the bottom
- mark genuine **cross-links** with ★, and say so when there are none instead of forcing them
- keep each map to 12–20 nodes, splitting larger ones into an overview plus sub-maps
- detect the input type (single lesson, curriculum framework, web article, or lesson-plan review) and follow the matching workflow
- produce a concept parking lot, a proposition matrix, a Mermaid concept map, a teaching plan, and misconception safeguards

### How to use

1. Open [`prompts/novak-concept-map.en.md`](prompts/novak-concept-map.en.md) (original Traditional Chinese: [`prompts/novak-concept-map.zh-TW.md`](prompts/novak-concept-map.zh-TW.md))
2. Copy the whole prompt and replace the last line, "Paste your input here", with your curriculum, lesson plan, or article
3. Send it to any chat model. Ask for the quick or full version in your input if you want one

### 🕶️ Blind tests

Same prompt, same material, two anonymous models. Read both outputs before revealing who is who:

| # | Material | Matchup |
|---|---|---|
| 01 | [Ontario Grade 3 Science — Strong and Stable Structures](blind-tests/01-ontario-grade3-structures/) | 🕶️ Hidden until revealed (hint: a family feud) |

### 📊 Full benchmark results

**Coming soon.** The full evaluation across subjects, grade levels, and model pairs will be linked here once it's ready.

---

## 📄 授權 / License

提示詞與本儲存庫原創內容以 [MIT License](LICENSE) 釋出。盲測素材 `material.txt` 摘錄自 *The Ontario Curriculum, Grades 1–8: Science and Technology (2022)*（© King's Printer for Ontario, 2022），僅供非商業教育用途引用，不受 MIT 授權涵蓋。模型輸出原文保留，未經修改。

The prompts and original content are released under the [MIT License](LICENSE). The blind-test material `material.txt` is excerpted from *The Ontario Curriculum, Grades 1–8: Science and Technology (2022)* (© King's Printer for Ontario, 2022) for non-commercial educational use and is not covered by the MIT License. Model outputs are reproduced verbatim.
