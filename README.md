# project_lian
![image](https://github.com/user-attachments/assets/4956d5ba-0c07-49c0-9564-a4bac527ba2f)

Этот проект посвящён созданию и обучению нейросети для определения аудиодипфейков. Мне было очень интересно работать над этой темой, так как она актуальна в контексте борьбы с дезинформацией и обеспечением безопасности в медиа.

# Общая информация о проекте

Project Lian использует алгоритмы глубокого обучения, основанные на свёрточных нейронных сетях (CNN) и рекуррентных нейронных сетях (RNN), для анализа аудиофайлов и распознавания манипуляций, связанных с дипфейками. Основная цель моего проекта — разработка модели, которая сможет распознавать и классифицировать аудиоданные, подверженные манипуляциям, что может помочь в проверке подлинности информации в медиа.

# Архитектура нейросети

В проекте я реализовала несколько ключевых компонентов, которые подробно опишу ниже.

#### 1. Датасет

Для обучения нейросети я подготовила специализированный датасет, состоящий из аудиофайлов. Датасет включает как оригинальные аудио записи, так и искусственно созданные дипфейки. Я уделила большое внимание качеству и разнообразию данных, поскольку это критично для успешного обучения модели.

#### 2. Предобработка данных

Перед тем как подать аудиофайлы на вход нейросети, я выполнила этап предобработки данных. Этот процесс включает:

- Преобразование формата: Аудиофайлы были преобразованы в один стандартный формат и частоту дискретизации.
- Извлечение признаков: Я использовала методы извлечения признаков, такие как MFCC (Mel-frequency cepstral coefficients) и спектрограммы, чтобы получить числовое представление звуковых сигналов, что позволяет нейросети лучше их анализировать.
- Аугментация: Для увеличения объема обучающих данных я применила методы аугментации, такие как наложение шума и изменение высоты звука.

#### 3. Модель нейросети
<img width="412" alt="{21DD5346-73A8-4AAF-8C01-7FCAC13F2C1A}" src="https://github.com/user-attachments/assets/e8486893-cfeb-484d-92bb-b8a016560568" />


В моем проекте была реализована комбинированная модель, которая использует как свёрточные, так и рекуррентные нейронные сети:

- Свёрточные слои: Эти слои используются для извлечения пространственных признаков из спектрограмм аудиофайлов.
- Рекуррентные слои: После извлечения признаков свёрточными слоями данные обрабатываются рекуррентными слоями (например, LSTM), которые способны учитывать временные зависимости в аудиосигналах. Это позволяет модели лучше уловить изменения во времени и идентифицировать манипуляции.
- Полносвязные слои: На выходе нейросети применяются полносвязные слои для классификации аудиозаписей на оригинал или дипфейк.

# Обучение модели

Я обучала модель с использованием алгоритма обратного распространения ошибки. Для повышения стабильности обучения использовала методы регуляризации, такие как дроп-аут (dropout), что помогает предотвратить переобучение. Процесс обучения включал несколько эпох, каждая из которых охватывала множество итераций над обучающей выборкой.

# Проверка и тестирование

После завершения обучения я проверяла качество модели на отдельном тестовом наборе данных, который не использовался в ходе обучения. Это позволяет оценить точность и надежность модели в распознавании аудио дипфейков. Я заметила, что результаты могут варьироваться в зависимости от сложности задач и качества входных данных.

# Итоги и применение

Project Lian стал важным шагом в разработке технологий для выявления аудиодипфейков. Применение такой модели может быть весьма широким и включать проверку подлинности новостных аудио материалов, выявление манипуляций в судебных доказательствах и даже мониторинг контента в социальных сетях.


![image](https://github.com/user-attachments/assets/bde256b3-a182-43d8-b6e7-3a421afcf959)

