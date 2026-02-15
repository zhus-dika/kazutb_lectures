Yandex handbook https://education.yandex.ru/handbook/ml

# Разработка искусственных нейронных сетей
Основа курса: **YSDA Practical_DL (branch: fall25)** https://github.com/yandexdataschool/Practical_DL — структура по неделям `week01`–`week14`.

---

## План лекций (по неделям) + краткое содержание

1. **Week 01 — Intro / Backprop / Adaptive Optimization**  
   **О чём лекция:** что такое обучение нейросетей “под капотом”.  
   **Кратко:** forward/backward, вычисление градиентов по правилу цепочки, градиентный спуск и его варианты, почему learning rate критичен, что такое адаптивные оптимизаторы и зачем они нужны.

2. **Week 02 — Autodiff / Frameworks / DL Tricks**  
   **О чём лекция:** как современные фреймворки считают градиенты и почему DL — это инженерия абстракций.  
   **Кратко:** autodiff и вычислительные графы (динамические/статические), уровни стеков (CUDA/библиотеки/фреймворк), базовые “трюки” стабильного обучения (инициализация, регуляризация, нормализации, residual connections).

3. **Week 03 — Convolutional Neural Networks (CNN)**  
   **О чём лекция:** почему свёртки работают для изображений.  
   **Кратко:** свёртка как локальный фильтр и разделение параметров, receptive field, pooling/stride, data augmentation, базовые архитектуры ConvNet и практические пайплайны для CV.

4. **Week 04 — Fine-tuning / Transfer Learning**  
   **О чём лекция:** как использовать предобученные модели и дообучать их под свою задачу.  
   **Кратко:** backbone + head, заморозка/разморозка слоёв, discriminative LR, регуляризация при малых данных, доменный сдвиг, практики fine-tuning для классификации/распознавания.

5. **Week 05 — Interpretability / Style Transfer**  
   **О чём лекция:** как “заглядывать” в нейросеть и понимать, на что она опирается.  
   **Кратко:** карты важности (saliency/attribution), визуализация признаков/представлений, ошибки интерпретации, практические методы анализа; + стиль-перенос как пример оптимизации по признаковым представлениям.

6. **Week 06 — NLP (embeddings, text conv)**  
   **О чём лекция:** базовый NLP до трансформеров.  
   **Кратко:** токенизация, эмбеддинги, простые модели для текста (в т.ч. сверточные/MLP-подходы), классификация текстов, метрики и особенности данных (длина, OOV, дисбаланс).

7. **Week 07 — Language Modeling**  
   **О чём лекция:** языковое моделирование как фундамент для современных LLM.  
   **Кратко:** цель LM, next-token prediction, perplexity, обучение и оценка LM, RNN/seq-модели (если присутствуют), attention как шаг к трансформерам, практические нюансы обучения (truncation, batching).

8. **Week 08 — Transformer**  
   **О чём лекция:** архитектура трансформера и self-attention.  
   **Кратко:** Q/K/V, multi-head attention, positional encoding, encoder/decoder, LayerNorm и residual blocks, масштабирование и типовые причины нестабильности/дороговизны.

9. **Week 09 — LLM**  
   **О чём лекция:** что такое большие языковые модели и как их адаптируют.  
   **Кратко:** prompting, instruction tuning, fine-tuning под задачу, PEFT (LoRA/адаптеры — по материалам недели), практические ограничения: контекст, стоимость инференса, безопасность/качество.

10. **Week 10 — Generative Models (VAE/GAN и др.)**  
   **О чём лекция:** генеративное моделирование как обучение распределения данных.  
   **Кратко:** likelihood vs implicit, latent space, VAE (ELBO, реконструкция + KL), основы GAN (идея состязательности), как оценивать генеративные модели и типичные артефакты.

11. **Week 11 — Diffusion Models**  
   **О чём лекция:** диффузионные модели и генерация изображений “через денойзинг”.  
   **Кратко:** forward noising и reverse denoising, роль U-Net/текстовых кондиционеров, sampling-схемы, fine-tuning (DreamBooth/LoRA — по материалам недели), inpainting как условная генерация.

12. **Week 12 — Inference / Efficiency**  
   **О чём лекция:** как сделать модели быстрее и дешевле на инференсе.  
   **Кратко:** где узкие места (память/latency/throughput), батчинг, кэширование, упрощение вычислений, оптимизация исполнения (компиляция/фьюзинг — по материалам недели), практические trade-offs качества и скорости.

13. **Week 13 — Reinforcement Learning (RL)**  
   **О чём лекция:** обучение агента через награду и взаимодействие со средой.  
   **Кратко:** MDP, policy/value, REINFORCE, actor-critic подходы (A2C/PPO — по материалам недели), стабильность обучения, кредит-ассайнмент, практические советы по диагностике.

14. **Week 14 — Audio (ASR/TTS) + бонус: multimodality**  
   **О чём лекция:** DL для аудио и мультимодальные модели.  
   **Кратко:** представления (waveform vs spectrogram), базовые задачи (ASR/TTS — по материалам недели), особенности метрик и данных; опционально — мультимодальные модели (аудио/текст/видео) как расширение “общих” архитектур.

---

## СРОП / задания (по README каждой недели)

> Формат: делаем задания из указанных ноутбуков. Дедлайны и правила сдачи — объявляются отдельно.

| Неделя | Папка | Что сдаём (ноутбуки/части) | Баллы (если указаны в README) |
|---:|---|---|---:|
| 1 | `week01_backprop` | `backprop.ipynb` (N-layer backprop) + `adaptive_sgd.ipynb` (SGD mods) | 5 + 5 |
| 2 | `week02_autodiff` | `homework_pytorch.ipynb` (и практика `seminar_pytorch.ipynb`) | — |
| 3 | `week03_convnets` | `seminar_pytorch.ipynb` + отчёт/майлстоуны по качеству (см. README) | шкала до 20 (+бонус) |
| 4 | `week04_finetuning` | `seminar_pytorch.ipynb` + опц. `advanced_homework.ipynb` (бонус) | — |
| 5 | `week05_interpretability` | `practice.ipynb` | — |
| 6 | `week06_nlp` | `seminar.ipynb` + `homework.ipynb` | — |
| 7 | `week07_lm` | `seminar.ipynb` + `homework.ipynb` | 3 + 7 |
| 8 | `week08_transformer` | `seminar.ipynb` + `homework.ipynb` (сдать оба) | — |
| 9 | `week09_llm` | `practice_prompting.ipynb` + доп. `practice_peft.ipynb` | — |
| 10 | `week10_generative` | `homework-vae.ipynb` | — |
| 11 | `week11_diffusion` | DreamBooth/LoRA + inpainting + короткий отчёт (см. README) | 3 + 2 |
| 12 | `week12_inference` | `practice.ipynb` | — |
| 13 | `week13_rl` | `reinforce_pytorch.ipynb` + опц. `a2c-optional.ipynb` **или** `ppo.ipynb` | 5 + (5 или 10) |
| 14 | `week14_audio` | `practice.ipynb` + опц. `optional_tts.ipynb` (бонус) | — |

---

## Сдача (коротко)
- Сдаём **.ipynb** (и/или ссылку на репо).
- Ноутбуки должны запускаться **Restart & Run All**.
- Если в неделе указано “submit both” — сдаём **оба** ноутбука этой недели.
