## Дәрістер жоспары (апталар бойынша) + қысқаша мазмұны

1. **Week 01 — Бейнелермен жұмыс: классикалық өңдеу әдістері**
   
   **Дәріс не туралы:** DL-ге дейінгі бейне өңдеудің негіздері және барлық жерде қолданылатын базалық операциялар.
   
   **Қысқаша:** бейне сигнал ретінде (дискреттеу/кванттау), шудар, свёртка және фильтрлер (blur/sharpen/median), градиенттер және шеттерді табу (Sobel/Canny), морфология, интерполяция/resize, OpenCV-де практикалық пайплайн.
   
   **Материалдар:** OpenCV Docs.

2. **Week 02 — Классификация: үздік тәжірибелер**
   
   **Дәріс не туралы:** бейне классификаторларын дұрыс оқыту: деректер → модель → оқыту → метрикалар.
   
   **Қысқаша:** қойылымдар (binary/multiclass/multilabel), transfer learning және fine-tuning, regularization, аугментациялар (MixUp/CutMix және т.б.), метрикалар (accuracy/F1/PR), losses (CE/BCE/focal), оптимизаторлар және LR-schedule, confusion matrix арқылы қателерді талдау.
   
   **Материалдар:** CS231n, Training recipe.

3. **Week 03 — Детекция (бірсатылы)**
   
   **Дәріс не туралы:** объект детекциясы “классификация + локализация” ретінде және real-time үшін one-stage неге басым.
    
   **Қысқаша:** bounding boxes, IoU және NMS, anchor/anchor-free идеясы, YOLO эволюциясы, инференс және confidence/NMS шектері, mAP/PR-қисықтары, типтік қателер FP/FN.
   
   **Материалдар:** YOLO history.

4. **Week 04 — Сегментация**
   
   **Дәріс не туралы:** сегментация пиксельдік классификация ретінде және оқыту/бағалау құралдары.
   
   **Қысқаша:** semantic vs instance, U-Net тәсілі (encoder-decoder идеясы), класс дисбалансы, шығын функциялары (BCE/Dice/IoU және комбинациялары), IoU/Dice метрикалары, маскаларды постөңдеу және сапаны визуалды валидациялау.
   
   **Материалдар:** Loss functions.

5. **Week 05 — ReID + Tracking**
    
   **Дәріс не туралы:** tracking-by-detection және көпкамера/окклюзияда ReID рөлі.
   
   **Қысқаша:** SOT vs MOT, data association, трекерлер (идея деңгейінде: SORT/DeepSORT/ByteTrack/BoT-SORT), ReID — эмбеддингтерді салыстыру, типтік мәселелер (ID-switch, occlusion), трекинг метрикаларына шолу (IDF1/MOTA — шолулық).
   
   **Материалдар:** Awesome tracking.

6. **Week 06 — Генеративті модельдер**
    
   **Дәріс не туралы:** CV-де генеративті модельдер не үшін керек және diffusion-ды “қарапайым тілмен” түсіну.  
   
   **Қысқаша:** VAE/GAN (шолулық), diffusion: noise → denoising → sampling, guidance/steps — басқарушы параметрлер, қолданулар: inpainting, super-resolution, data augmentation және синтетикалық деректер.  
   
   **Материалдар:** Diffusion: overview.

7. **Week 07 — SSL & Foundation Models**
    
   **Дәріс не туралы:** self-supervised репрезентациялар және “foundation” белгілерін қолданбалы міндеттерге тасымалдау.  
   
   **Қысқаша:** contrastive (идеясы), masked image modeling/MAE (идеясы), feature extraction vs fine-tuning, linear probing, домендік бейімдеу, аз таңбалауда SSL қашан шынымен ұтады.

8. **Week 08 — Нейрондық желі модельдерін жеделдету әдістері**
    
   **Дәріс не туралы:** инференсті жеделдету және сапа/жылдамдық/жад компромистері.  
   
   **Қысқаша:** quantization (FP16/INT8 — шолулық), pruning, distillation, пайплайнды оңтайландыру (resize/батчинг), экспорт/рантаймдар (ONNX/TensorRT — шолулық), latency/throughput өлшеу.

---

## СРОП / тапсырмалар

> Формат: **ноутбуктердегі** тапсырмаларды орындаймыз

| Апта | Бөлім/қалтасы (логикалық атауы) | Тапсыратын нәрсе (ноутбук/бөлігі) | Балл |
|---:|---|---|---:|
| 1 | `Classification` | [Бейнелердің бинарлық классификациясы және класс дисбалансы мәселесін шешу](https://colab.research.google.com/drive/1772rBZGw83yGr2D0jbmOtx8AtDqwuUSp#scrollTo=mLrXWnsp5d6q) | — |
| 2 | `Detection` | [Бірсатылы детекция](https://colab.research.google.com/drive/1PCJFD4YEwXmQnSb0YxrmTnR6bIv8ZDuC?usp=sharing) | — |
| 3 | `Segmentation` | [Семантикалық сегментация](https://colab.research.google.com/drive/1Kni36PCFxxNru6DZ2vwFA8Qk85W-XhL1?usp=sharing) | — |
| 4 | `Tracking` | [Трекингтің нейрондық модулін талдау](https://github.com/zhus-dika/kazutb_lectures/blob/main/%D0%9E%D0%B1%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0%20%D0%B8%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D0%B9%20%D0%B2%20%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0%D1%85%20%D0%B8%D1%81%D0%BA%D1%83%D1%81%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%B8%D0%BD%D1%82%D0%B5%D0%BB%D0%BB%D0%B5%D0%BA%D1%82%D0%B0/%D0%A1%D1%82%D1%83%D0%B4%D0%B5%D0%BD%D1%82%D0%B0%D0%BC_%D0%94%D0%97_14_5_%D0%A0%D0%B0%D0%B7%D0%B1%D0%BE%D1%80_%D0%BD%D0%B5%D0%B9%D1%80%D0%BE%D1%81%D0%B5%D1%82%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE_%D0%BC%D0%BE%D0%B4%D1%83%D0%BB%D1%8F_%D1%82%D1%80%D0%B5%D0%BA%D0%B8%D0%BD%D0%B3%D0%B0.ipynb) | — |
| 5 | `Diffusion` | [Диффузиялық модельдер](https://colab.research.google.com/drive/1_PUs3JPFFWNa7c_xDxxdaSDSz90SZ0gZ?usp=sharing) | — |

---

## Тапсыру тәртібі

- **.ipynb** файлын тапсырамыз (және/немесе репозиторий/Colab сілтемесі — қалай баптайсың).
- Ноутбуктер **Restart & Run All** режимінде толық орындалуы керек.
- Есепте/комментарийде: *не істедіңіз → метрикалар → қорытынды* (қысқа, бірақ нақты).
