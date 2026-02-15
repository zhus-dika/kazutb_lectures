Основа курса: **YSDA `nlp_course` (branch: `2025`)** https://github.com/yandexdataschool/nlp_course — структура по неделям `week01`–`week11`.

---

## План лекций (по неделям) + краткое содержание

1. **Week 01 — Word Embeddings**  
   **О чём лекция:** как превратить слова в векторы и почему “смысл” можно учить по контекстам.  
   **Кратко:** распределительная гипотеза, count-based матрицы (co-occurrence/PMI), Word2Vec (Skip-gram/CBOW, negative sampling), GloVe, оценка (intrinsic/extrinsic), анализ семантического пространства.

2. **Week 02 — Language Modeling**  
   **О чём лекция:** языковая модель как фундамент генерации и современных LLM.  
   **Кратко:** left-to-right LM, n-gram LM и сглаживание, neural LM, оценка (perplexity), генерация и temperature, практические трюки вроде weight tying.

3. **Week 03 — Seq2seq & Attention**  
   **О чём лекция:** как строится машинный перевод и почему attention стал “переломным моментом”.  
   **Кратко:** encoder–decoder, инференс (beam search), attention, переход к transformer/self-attention, subword segmentation (BPE), базовые идеи анализа attention.

4. **Week 04 — Transfer Learning**  
   **О чём лекция:** предобучение и адаптация (BERT/GPT) под прикладные задачи.  
   **Кратко:** words-in-context, ELMo/CoVe как ступень, GPT/BERT, fine-tuning, вводные по HF Transformers, стабильность и оценка.

5. **Week 05 — Large Language Models (LLM)**  
   **О чём лекция:** что такое LLM и как с ними практично работать.  
   **Кратко:** landscape open-source моделей, работа через `transformers`, ограничения лицензий/доступов, эффекты/аномалии (glitch tokens), обсуждение масштабирования.

6. **Week 06 — Prompting & In-Context Learning**  
   **О чём лекция:** prompting как способ управления моделью без изменения весов.  
   **Кратко:** техники prompting, шаблоны и типовые ошибки, оценка промптов, границы in-context learning.

7. **Week 07 — Fine-tuning / PEFT + RLHF**  
   **О чём лекция:** как дообучать LLM эффективно и что такое alignment/RLHF на уровне пайплайна.  
   **Кратко:** PEFT (LoRA/адаптеры), пайплайны fine-tuning, обзор RLHF, опционально: task-driven chatbots.

8. **Week 08 — LLM Efficiency**  
   **О чём лекция:** как ускорять и удешевлять инференс LLM.  
   **Кратко:** узкие места latency/throughput/память, квантование/ускорение, системные оптимизации (по материалам недели).

9. **Week 09 — Retrieval / RAG**  
   **О чём лекция:** retrieval как основа RAG-приложений.  
   **Кратко:** пайплайн RAG (индексация → поиск → контекст → генерация), практическая сборка retrieval+generation.

10. **Week 10 — AI Agents**  
   **О чём лекция:** LLM-агенты и инструментальные действия.  
   **Кратко:** agentic loop, tools, паттерны построения агентов, материалы семинара недели, домашка в отдельной папке.

11. **Week 11 — Interpretability**  
   **О чём лекция:** интерпретируемость LLM и анализ внутренних механизмов.  
   **Кратко:** подходы к интерпретации/анализу, практики в ноутбуках (семинар + ДЗ), ориентиры по современным направлениям.

---

## СРОП / задания

> Формат: делаем задания из указанных ноутбуков/папок. Дедлайны и правила сдачи — объявляются отдельно.

| Неделя | Папка | Что сдаём (ноутбуки/части) | Баллы |
|---:|---|---|---:|
| 1 | `week01_embeddings` | `seminar.ipynb` + `homework.ipynb` (**enrolled: submit both для полного балла**) | — |
| 2 | `week02_lm` | `seminar.ipynb` + `homework_*.ipynb` | — |
| 3 | `week03_attention` | общий `new_practice_and_homework.ipynb` (семинар + ДЗ) | — |
| 4 | `week04_transfer` | `seminar.ipynb` + `homework.ipynb` (**enrolled: submit both**) | — |
| 5 | `week05_llm` | `seminar.ipynb` (practice session) | — |
| 6 | `week06_prompting` | `homework.ipynb` (**enrolled: можно сдавать только homework**) + `seminar.ipynb` (практика) | — |
| 7 | `week07_finetuning` | 2 задания: `seminar.ipynb` + `homework.ipynb` (есть optional hardcore RL FT) | **5 + 5** |
| 8 | `week08_efficiency` | `hw_8.ipynb` | — |
| 9 | `week09_retrieval` | `practice.ipynb` | — |
| 10 | `week10_agents` | `seminar/ysda_agents_sem.ipynb` + (для YSDA students) `homework/` | — |
| 11 | `week11_interpretability` | `seminar_interpretability.ipynb` + `homework_interpretability.ipynb` | — |

---

## Сдача

- Сдаём **.ipynb** (и/или ссылку на репозиторий/Colab — как настроишь).
- Ноутбуки должны запускаться **Restart & Run All**.
- Если в неделе указано **“submit both”** — сдаём **оба** ноутбука этой недели.

