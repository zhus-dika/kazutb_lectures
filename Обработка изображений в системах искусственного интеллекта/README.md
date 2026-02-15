## План лекций (по неделям) + краткое содержание

1. **Week 01 — Работа с изображениями: классические методы обработки**
   
   **О чём лекция:** фундамент обработки изображений до DL и базовые операции, которые используются везде.
   
   **Кратко:** изображение как сигнал (дискретизация/квантизация), шумы, свёртка и фильтры (blur/sharpen/median), градиенты и выделение границ (Sobel/Canny), морфология, интерполяция/ресайз, практический пайплайн в OpenCV.
   
   **Материалы:** OpenCV Docs.

2. **Week 02 — Классификация: лучшие практики**
   
   **О чём лекция:** как правильно обучать классификаторы изображений: данные → модель → обучение → метрики.
   
   **Кратко:** постановки (binary/multiclass/multilabel), transfer learning и fine-tuning, regularization, аугментации (MixUp/CutMix и др.), метрики (accuracy/F1/PR), losses (CE/BCE/focal), оптимизаторы и LR-schedule, анализ ошибок через confusion matrix.
   
   **Материалы:** CS231n, Training recipe.

3. **Week 03 — Детекция (одностадийная)**
   
   **О чём лекция:** детекция объектов как “классификация + локализация” и почему one-stage доминирует в real-time.
    
   **Кратко:** bounding boxes, IoU и NMS, anchor/anchor-free идея, эволюция YOLO, инференс и пороги confidence/NMS, метрики mAP/PR-кривые, типовые ошибки FP/FN.
   
   **Материалы:** YOLO history.

4. **Week 04 — Сегментация**
   
   **О чём лекция:** сегментация как пиксельная классификация и инструменты для обучения/оценки.
   
   **Кратко:** semantic vs instance, U-Net-подход (идея encoder-decoder), дисбаланс классов, функции потерь (BCE/Dice/IoU и их комбинации), метрики IoU/Dice, постобработка масок и визуальная валидация качества.
   
   **Материалы:** Функции потерь.

5. **Week 05 — ReID + Tracking**
    
   **О чём лекция:** tracking-by-detection и роль ReID при многокамерности/окклюзиях.
   
   **Кратко:** SOT vs MOT, data association, трекеры (на уровне идеи: SORT/DeepSORT/ByteTrack/BoT-SORT), ReID как сравнение эмбеддингов, типовые проблемы (ID-switch, occlusion), обзор метрик трекинга (IDF1/MOTA — обзорно).
   
   **Материалы:** Awesome tracking.

6. **Week 06 — Генеративные модели**
    
   **О чём лекция:** зачем генеративные модели в CV и что такое diffusion “на пальцах”.  
   
   **Кратко:** VAE/GAN (обзорно), diffusion: шум → денойзинг → sampling, guidance/steps как управляющие параметры, применения: inpainting, super-resolution, data augmentation и синтетика.  
   
   **Материалы:** Diffusion: overview.

7. **Week 07 — SSL & Foundation Models**
    
   **О чём лекция:** self-supervised представления и перенос “foundation” признаков на прикладные задачи.  
   
   **Кратко:** contrastive (идея), masked image modeling/MAE (идея), feature extraction vs fine-tuning, linear probing, доменная адаптация, когда SSL реально выигрывает при малой разметке.

8. **Week 08 — Методы ускорения нейросетевых моделей**
    
   **О чём лекция:** ускорение инференса и компромиссы качество/скорость/память.  
   
   **Кратко:** quantization (FP16/INT8 — обзорно), pruning, distillation, оптимизация пайплайна (resize/батчинг), экспорт/рантаймы (ONNX/TensorRT — обзорно), измерение latency/throughput.

---

## СРОП / задания

> Формат: выполняем задания из **ноутбуков**

| Неделя | Раздел/папка (логическое имя) | Что сдаём (ноутбуки/части) | Баллы |
|---:|---|---|---:|
| 1 | `Classification` | [Бинарная классификация изображений и решение проблемы дисбаланса классов](https://colab.research.google.com/drive/1772rBZGw83yGr2D0jbmOtx8AtDqwuUSp#scrollTo=mLrXWnsp5d6q) | — |
| 2 | `Detection` | [Одностадийная детекция](https://colab.research.google.com/drive/1PCJFD4YEwXmQnSb0YxrmTnR6bIv8ZDuC?usp=sharing) | — |
| 3 | `Segmentation` | [Семантическая сегментация](https://colab.research.google.com/drive/1Kni36PCFxxNru6DZ2vwFA8Qk85W-XhL1?usp=sharing) | — |
| 4 | `Tracking` | [Разбор нейросетевого модуля трекинга](https://github.com/zhus-dika/kazutb_lectures/blob/main/%D0%9E%D0%B1%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0%20%D0%B8%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D0%B9%20%D0%B2%20%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0%D1%85%20%D0%B8%D1%81%D0%BA%D1%83%D1%81%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%B8%D0%BD%D1%82%D0%B5%D0%BB%D0%BB%D0%B5%D0%BA%D1%82%D0%B0/%D0%A1%D1%82%D1%83%D0%B4%D0%B5%D0%BD%D1%82%D0%B0%D0%BC_%D0%94%D0%97_14_5_%D0%A0%D0%B0%D0%B7%D0%B1%D0%BE%D1%80_%D0%BD%D0%B5%D0%B9%D1%80%D0%BE%D1%81%D0%B5%D1%82%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE_%D0%BC%D0%BE%D0%B4%D1%83%D0%BB%D1%8F_%D1%82%D1%80%D0%B5%D0%BA%D0%B8%D0%BD%D0%B3%D0%B0.ipynb) | — |
| 5 | `Diffusion` | [Диффузионные модели](https://colab.research.google.com/drive/1_PUs3JPFFWNa7c_xDxxdaSDSz90SZ0gZ?usp=sharing) | — |

---

## Сдача

- Сдаём **.ipynb** (и/или ссылку на репозиторий/Colab — как настроишь).
- Ноутбуки должны запускаться **Restart & Run All**.
- В отчёте/комментариях: *что делали → метрики → выводы* (коротко, но по делу).
