# Pet-project: Speech-emotion-analysis
# Идея
 Модель, которая анализирует аудиозапись речи и определяет эмоции в категориях, например: официальная речь, грубая, злая, вежливая, нейтральная.
 Данная модель может быть использована в колл-центрах для анализ звонков для улучшения качества обслуживания, выявления недовольных клиентов, непрофессиональных сотруников и предупреждения конфликтов.
 
## План
1. Сбор данных
  готовые датасеты:

    Для русской речи: Golos
     - https://github.com/sberdevices/golos
   
    Для эмоций: RAVDESS, CREMA-D.
      - https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio
      - https://github.com/CheyneyComputerScience/CREMA-D

3. Взять предобученную модель (Wav2Vec 2.0, Whisper (?)) для извлечения признаков из аудио.
4. Классификация эмоций с использованием английского датасета (RAVDESS или CREMA-D). Обучить модель классификации (например, MLP / LSTM / Transformer-based модели)
5. Затем адаптировать на русскую речь с использованием русскоязычных данных (Golos).
   Применить эту модель к русским записям (Golos) и автоматически назначить метки. Оставить только уверенные предсказания (например, softmax > 0.9).


