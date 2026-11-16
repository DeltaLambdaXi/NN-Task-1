# Практическое задание 1

Решение через MobileNetV3-Small с ImageNet, дообучение на `train_small`.

На `test` (4500): accuracy **0.9767**.
`test_tiny`: **0.9778**.

Метки в коде:

- `#LBL1` — 15% train на валидацию
- `#LBL3` — чекпоинт каждой эпохи, лучшая модель отдельно
- `#LBL4` — `load_epoch(4)`, на test_tiny сравнил с лучшими весами
- `#LBL5` — loss и accuracy печатаются каждую эпоху
- `#LBL6` — график loss/accuracy
- `#LBL7` — accuracy на test после каждой эпохи
- `#LBL8` — матрица ошибок, sensitivity и specificity
- `#LBL10` — картинка и json в `results/`
- `#LBL11` — flip, поворот, ColorJitter. На сетке классов оттенок разный, верх у патча не задан
- `#LBL12` — resume поднимает Adam из чекпоинта и продолжает со следующей эпохи (проверка на tiny, `checkpoints/resume_demo`)
- `#LBL13` — сначала голова, потом вся сеть, cosine по эпохам

**Ссылка на Colab**: https://drive.google.com/file/d/12B83BphD8eR1dlqugFj2Iqr5cm_qeIPL/view?usp=sharing
