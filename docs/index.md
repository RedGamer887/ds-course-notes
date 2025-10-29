## Модуль 1

### 1. Установка пакета Date A Scientist

Для установки используйте следующую команду в терминале:

```python
pip install --quiet date-a-scientist
```

### 2. Что такое Kernel (Ядро) в контексте Jupyter Notebook?

**Kernel** (ядро) — это интерпретатор Python, который используется для выполнения кода в ноутбуке Jupyter. Именно он отвечает за обработку и выполнение всех ячеек с кодом.

### 3. Что такое Markdown?

**Markdown** — это язык разметки, который позволяет просто форматировать текст.  
С его помощью можно создавать заголовки, списки, ссылки, изображения, таблицы, вставки кода и многое другое.

---

## Модуль 2

### 1. Что такое медиана?

**Медиана** — это значение, ниже которого находится 50% всех данных.  
Медиана также известна как второй квартиль (КВАРТИЛЬ 2) или 50-й перцентиль (ПЕРЦЕНТИЛЬ 50).  
Первый квартиль (КВАРТИЛЬ 1) — это 25-й перцентиль, а третий квартиль (КВАРТИЛЬ 3) — 75-й перцентиль.

### 2. Что такое среднее арифметическое?

**Среднее арифметическое** — это сумма всех значений, делённая на их количество.

**Пример расчёта среднего арифметического для чисел 1, 4, 6, 13:**

```python
(1 + 4 + 6 + 13) / 4 = 6
```

### 3. Что такое EDA?

**EDA** (Exploratory Data Analysis) — это разведывательный анализ данных, который используется для исследования, визуализации и предварительного понимания структуры и особенностей данных.

---

## Модуль 3

### 1. Что такое Conda?

**Conda** — это система управления пакетами и средами.  
Conda позволяет устанавливать и управлять пакетами, а также создавать изолированные среды для работы с разными версиями библиотек и языков программирования.

### 2. Как удалить среду Conda?

Выполните команду:
```python
conda env remove --name "имя_среды"
```

### 3. Как установить пакет из PyPI с помощью Conda?

1. Активируйте нужную среду:
    ```python
    conda activate "имя_среды"
    ```
2. Установите пакет через pip:
    ```python
    pip install "название_пакета"
    ```
    Например:
    ```python
    pip install date-a-scientist
    ```

### 4. Как установить, например, Jupyter Lab в среде Conda?

1. Активируйте среду:
    ```python
    conda activate "имя_среды"
    ```
2. Установите Jupyter Lab:
    ```python
    pip install jupyterlab
    ```

### 5. Как деактивировать среду Conda?

Выполните команду:
```python
conda deactivate
```

### 6. Как удалить пакет из среды Conda?

1. Активируйте среду:
    ```python
    conda activate "имя_среды"
    ```
2. Удалите пакет:
    ```python
    conda remove "название_пакета"
    ```
    Например:
    ```python
    conda remove pandas
    ```

### 7. Как создать новую среду Conda?

Выполните команду:
```python
conda create --name "имя_новой_среды"
```

### 8. Как проверить версию установленного пакета?

1. Активируйте среду:
    ```python
    conda activate "имя_среды"
    ```
2. Проверьте версию пакета:
    ```python
    conda list "название_пакета"
    ```
    Например:
    ```python
    conda list pandas
    ```

### 9. Как вывести список всех установленных пакетов в среде?

1. Активируйте среду:
    ```python
    conda activate "имя_среды"
    ```
2. Выведите список пакетов:
    ```python
    conda list
    ```

### 10. Как посмотреть доступные среды Conda на компьютере?

Выполните команду:
```python
conda env list
```

### 11. Как создать новую среду с определённой версией Python?

Выполните команду:
```python
conda create --name "имя_среды" python=="версия"
```
Например:
```python
conda create --name od_zera_do_ai python==3.11
```

### 12. Для чего используется модуль datetime?

Модуль `datetime` предоставляет функции для работы с датой и временем. Например:

```python
import datetime
now = datetime.datetime.now()
print(now)  # Выводит текущую дату и время
```

### 13. Какие функции предоставляет модуль math?

Модуль `math` включает множество математических функций: вычисление корней, тригонометрические функции, логарифмы и др. Например:

```python
import math
print(math.sqrt(16))           # Вычисляет квадратный корень из 16
print(math.sin(math.pi / 2))   # Вычисляет синус 90 градусов
```

### 14. Есть ли в Python встроенные модули?

Да, в Python есть множество встроенных модулей, которые предоставляют функционал для работы с файлами, операционной системой, временем и др.

### 15. Для чего используется модуль random?

Модуль `random` предоставляет функции для генерации случайных чисел и выполнения случайных операций, например, выбора случайных элементов из списка. Например:

```python
import random
print(random.randint(1, 10))  # Генерирует случайное целое число от 1 до 10
print(random.choice(['apple', 'banana', 'cherry']))  # Случайно выбирает элемент из списка
```

### 16. Для чего используется модуль os в Python?

Модуль `os` позволяет взаимодействовать с операционной системой: менять каталоги, создавать файлы, получать информацию о файлах и др. Например:

```python
import os
print(os.getcwd())  # Показывает текущий рабочий каталог (getcwd = Get Current Working Directory)
```

---

## Модуль 4

### 1. Как добавить новый столбец с вычисляемым значением в DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df['age_in_months'] = df['age'] * 12
```

### 2. Как вывести первые строки DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    # ... 1000 строк
    {"name": "Bob", "age": 30},
])

df.head() # выведет первые 5 строк
```

### 3. Как изменить названия всех столбцов в DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df.columns = ['имя', 'возраст']
```

### 4. Как вывести последние строки DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    # ... 1000 строк
    {"name": "Bob", "age": 30},
])

df.tail() # выведет последние 5 строк
```

### 5. Как узнать индекс DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
], index=['a', 'b'])

df.index
# Index(['a', 'b'], dtype='object')
```

### 6. Как добавить новый столбец с постоянным значением в DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df['is_human'] = True
```

### 7. Что такое DataFrame в pandas?

**DataFrame** — это двумерная структура данных, похожая на таблицу в базе данных или лист в Excel, содержащая строки и столбцы.

### 8. Что такое индекс (index) в pandas DataFrame?

**Индекс** — это метки для строк и столбцов в DataFrame. Индекс может быть числом, датой, строкой или другим объектом.

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
], index=['a', 'b'])

df
#    name  age
# a Alice   25
# b   Bob   30
```

### 9. Как обратиться к строке по индексу в DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
], index=['a', 'b'])

df.loc['b'] # вернёт строку с индексом 'b'
```

### 10. Для чего нужен индекс в DataFrame?

Индекс в DataFrame служит для идентификации строк и столбцов.  
Индекс может быть числом, датой, строкой или другим объектом.  
Индекс неизменяемый, его нельзя изменить после создания DataFrame.  
Если индекс не указан, pandas создаёт его автоматически от 0 до n-1, где n — количество строк.

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
], index=['a', 'b'])

# можно обратиться к строке по индексу
df.loc['a']
```

### 11. Как вывести информацию о DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30}
])

df.info() # выведет основную информацию о DataFrame
```

### 12. Как вывести список столбцов DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df.columns # выведет что-то вроде ['name', 'age']
```

### 13. Что такое Series в pandas?

**Series** — это одномерный массив данных, который может хранить любые типы данных с метками (индексами) для каждого элемента.

### 14. Как изменить порядок столбцов в DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df = df[['age', 'name']]
```

### 15. Как вывести случайные строки DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    # ... 1000 строк
    {"name": "Bob", "age": 30},
])

df.sample(5) # выведет 5 случайных строк
```

### 16. Как вывести последние 20 строк DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    # ... 1000 строк
    {"name": "Bob", "age": 30},
])

df.tail(20) # выведет последние 20 строк
```

### 17. Как называть переменные, хранящие объекты DataFrame?

Переменную с объектом DataFrame называют df или добавляют к имени суффикс _df.  
Это неофициальная конвенция, которая помогает сразу понять, что переменная — это DataFrame.

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

# или если имя df уже занято:
names_df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])
```

### 18. Как отсортировать DataFrame по столбцу?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df = df.sort_values('age') # сортировка по возрастанию
df = df.sort_values('age', ascending=False) # сортировка по убыванию
```

### 19. Как изменить названия отдельных столбцов в DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df = df.copy()
df = df.rename(columns={'name': 'имя'})
```

### 20. Как вывести базовые статистики DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df.describe()
# выведет основные статистики для числовых столбцов:
# count, mean, std, min, 25%, 50%, 75%, max
```

### 21. Как создать DataFrame из списка словарей?

```python
import pandas as pd

data = [
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35},
]
df = pd.DataFrame(data)
```

### 22. Как применить функцию ко всем столбцам DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"salary": 3200, "age": 25},
    {"salary": 4500, "age": 30},
])

def add_one(x):
    return x + 1

df.apply(add_one)
```

### 23. Что такое пакет Pandas?

1. **Pandas** — это пакет для анализа данных, предоставляющий структуры данных и инструменты для работы с ними.
2. Pandas специализируется на табличных данных.
3. Pandas крайне необходим для работы с данными в Python!

### 24. Как вывести уникальные значения столбца DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df['age'].unique() # вернёт массив уникальных значений, например [25, 30]
```

### 25. Как создать DataFrame из словаря списков?

```python
import pandas as pd

data = {
    "name": ["Alice", "Bob", "Charlie"],
    "age": [25, 30, 35],
}
df = pd.DataFrame(data)
```

### 26. Как вывести первые 20 строк DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    # ... 1000 строк
    {"name": "Bob", "age": 30},
])

df.head(20) # выведет первые 20 строк
```

### 27. Как сделать так, чтобы pandas показывал все столбцы?

По умолчанию pandas показывает только часть столбцов.  
Чтобы видеть все столбцы, выполните следующее:

```python
import pandas as pd

pd.options.display.max_columns = None
```

Лучше добавить этот код в начале ноутбука, чтобы всегда видеть все столбцы.

### 28. Как удалить столбец из DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df = df.drop('age', axis=1)
```

### 29. Как импортировать библиотеку pandas?

```python
import pandas as pd
```

### 30. Как вывести количество уникальных значений в столбце DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 25},
    {"name": "Charlie", "age": 24},
])

df.nunique()
# вернёт количество уникальных значений в каждом столбце:
# name    3
# age     2
```

### 31. Как вывести количество уникальных значений в столбце DataFrame и их частоту?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 25},
    {"name": "Charlie", "age": 24},
])

df['age'].value_counts()
# вернёт:
# 25    2
# 24    1
# Name: age, dtype: int64
```

---

### 32. Как найти дубликаты по выбранным столбцам в DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "city": "Warsaw"},
    {"name": "Alice", "age": 25, "city": "Opole"},
    {"name": "Bob", "age": 30, "city": "Krakow"},
])

df.duplicated(subset=['name', 'age']) # вернёт True там, где строка является дубликатом
```

### 33. Как отфильтровать DataFrame по значению столбца, которого нет в списке?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35},
])

df = df[~df['name'].isin(['Alice', 'Charlie'])]
# `~` означает отрицание, то есть вернёт строки, которых нет в списке
```

### 34. Как фильтровать DataFrame по дате?

```python
import pandas as pd

df = pd.DataFrame([
    {"date": "2021-01-01"},
    {"date": "2021-02-01"},
])
df['date'] = pd.to_datetime(df['date'])

df = df[df['date'] > '2021-01-15']
df
# вернёт
#         date
# 1 2021-02-01
```

### 35. Как удалить строки с пропущенными значениями в выбранных столбцах DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": None},
    {"name": None, "age": 45},
])

df = df.dropna(subset=['age'])
# удалит строки с пропущенными значениями в столбце 'age'
```

### 36. Как удалить дубликаты из DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35},
])

df = df.drop_duplicates() # удалит строки-дубликаты
```

### 37. Как отфильтровать DataFrame по значениям столбца из списка?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35},
])

df = df[df['name'].isin(['Alice', 'Charlie'])]
# вернёт строки, которые есть в списке
```

### 38. Как удалить строки с пропущенными значениями из DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": None}
])

df = df.dropna() # удалит строки с пропущенными значениями
```

### 39. Как вывести дубликаты в DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df[df.duplicated()] # вернёт строки-дубликаты
```

### 40. Как удалить дубликаты по выбранным столбцам DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "city": "Warsaw"},
    {"name": "Alice", "age": 25, "city": "Opole"},
    {"name": "Bob", "age": 30, "city": "Krakow"},
])

df = df.drop_duplicates(subset=['name', 'age'])
# удалит строки, которые являются дубликатами по столбцам 'name' и 'age'
```

### 41. Как найти дубликаты в DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

df.duplicated() # вернёт True там, где строка — дубликат
```

### 42. Как заполнить пропущенные значения в DataFrame средним значением?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": None},
])

df['age'] = df['age'].fillna(df['age'].mean()) # заполнит пропуски в столбце 'age' средним значением
```

### 43. Как удалить дубликаты по выбранным столбцам DataFrame и оставить последний?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "city": "Warsaw"},
    {"name": "Alice", "age": 25, "city": "Opole"},
    {"name": "Bob", "age": 30, "city": "Krakow"},
])

df = df.drop_duplicates(subset=['name', 'age'], keep='last')
# удалит дубликаты по столбцам 'name' и 'age', оставив последний (например, строку с city='Opole')
```

### 44. Как заполнить пропущенные значения в выбранных столбцах DataFrame константами?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "city": None},
    {"name": "Bob", "age": None, "city": "Warsaw"},
])

df = df.fillna({'age': 30, 'city': 'Opole'}) # заполнит пропуски в 'age' и 'city' значениями 30 и 'Opole'
```

### 45. Как фильтровать DataFrame по значению столбца?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35},
])

df = df[df['age'] > 30]
```

### 46. Как заполнить пропущенные значения в DataFrame постоянным значением?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": None},
])

df['age'] = df['age'].fillna(30) # заполнит пропуски в 'age' значением 30
```

### 47. Как фильтровать DataFrame по значению столбца с несколькими условиями?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35},
])

# Используем `&` для "и"
df = df[(df['age'] >= 30) & (df['age'] <= 35)]

# Используем `|` для "или"
df = df[(df['age'] <= 25) | (df['age'] >= 35)]
```

### 48. Как найти пропущенные значения в DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35},
])

df.isnull() # вернёт True там, где значение отсутствует (является пропущенным)
```

### 49. Как вычислить корреляцию между столбцами DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 24, "height": 160},
    {"name": "Bob", "age": 30, "height": 155},
    {"name": "Charlie", "age": 20, "height": 165},
    {"name": "Andrzej", "age": 21, "height": 192},
    {"name": "Adam", "age": 23, "height": 190},
])

df[["age", "height"]].corr()
```

### 50. Как построить круговую диаграмму (pie chart) из DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 24, "height": 160},
    {"name": "Bob", "age": 30, "height": 155},
    {"name": "Charlie", "age": 20, "height": 165},
    {"name": "Andrzej", "age": 21, "height": 192},
    {"name": "Adam", "age": 23, "height": 190},
])

df.plot(kind='pie', y='age', labels=df['name'], legend=False)
```

### 51. Как построить столбчатую диаграмму (bar chart) из DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 24, "height": 160},
    {"name": "Bob", "age": 30, "height": 155},
    {"name": "Charlie", "age": 20, "height": 165},
    {"name": "Andrzej", "age": 21, "height": 192},
    {"name": "Adam", "age": 23, "height": 190},
])

df.plot(kind='bar', x='name', y=['age', 'height'])
```

### 52. Как "сохранить" DataFrame в виде списка словарей?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])

data = df.to_dict(orient='records')
# вернёт список словарей
# [
#     {'name': 'Alice', 'age': 25},
#     {'name': 'Bob', 'age': 30},
# ]
```

### 53. Как считать CSV-файл с точкой с запятой как разделителем в pandas?

```python
import pandas as pd

df = pd.read_csv("file.csv", sep=";")
```

### 54. Как считать CSV-файл в pandas?

```python
import pandas as pd

df = pd.read_csv("file.csv")
```

### 55. Как сохранить DataFrame в CSV-файл в pandas?

```python
import pandas as pd

df.to_csv("file.csv", index=False)
```

### 56. Как построить boxplot (ящик с усами) из DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 24, "height": 160},
    {"name": "Bob", "age": 30, "height": 155},
    {"name": "Charlie", "age": 20, "height": 165},
    {"name": "Andrzej", "age": 21, "height": 192},
    {"name": "Adam", "age": 23, "height": 190},
])

df.plot(kind='box')
```

### 57. Как считать определённый лист из Excel-файла в pandas?

```python
import pandas as pd

df = pd.read_excel("file.xlsx", sheet_name="Sheet1")
```

### 58. Как построить точечную диаграмму (scatter plot) из DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 24, "height": 160},
    {"name": "Bob", "age": 30, "height": 155},
    {"name": "Charlie", "age": 20, "height": 165},
    {"name": "Andrzej", "age": 21, "height": 192},
    {"name": "Adam", "age": 23, "height": 190},
])

df.plot(kind='scatter', x='height', y='age')
```

### 59. Как построить гистограмму по выбранному столбцу DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 24, "height": 160},
    {"name": "Bob", "age": 30, "height": 155},
    {"name": "Charlie", "age": 20, "height": 165},
    {"name": "Andrzej", "age": 21, "height": 192},
    {"name": "Adam", "age": 23, "height": 190},
])

df['age'].hist(bins=3)
```

### 60. Как считать Excel-файл в pandas?

```python
import pandas as pd

df = pd.read_excel("file.xlsx")
```

### 61. Как сохранить DataFrame в определённый лист Excel-файла в pandas?

```python
import pandas as pd

df.to_excel("file.xlsx", sheet_name="Sheet1", index=False)
```

### 62. Как сохранить DataFrame в Excel-файл в pandas?

```python
import pandas as pd

df.to_excel("file.xlsx", index=False)
```

### 63. Как построить график для числовых столбцов DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "height": 5.6},
    {"name": "Bob", "age": 30, "height": 6.0},
    {"name": "Charlie", "age": 20, "height": 5.8},
])

df.plot()
```

### 64. Как построить гистограмму для всех числовых столбцов DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 24, "height": 160},
    {"name": "Bob", "age": 30, "height": 155},
    {"name": "Charlie", "age": 20, "height": 165},
    {"name": "Andrzej", "age": 21, "height": 192},
    {"name": "Adam", "age": 23, "height": 190},
])

df.hist(bins=2)
```

### 65. Как извлечь месяц из столбца с датой?

```python
import pandas as pd

df = pd.DataFrame([
    {"date": "2021-01-01"},
    {"date": "2021-02-01"},
])
df['date'] = pd.to_datetime(df['date'])

df['month'] = df['date'].dt.month
df
# вернёт
#         date  month
# 0 2021-01-01      1
# 1 2021-02-01      2
```

### 66. Как объединить два DataFrame по общему столбцу, присоединяя данные с обеих сторон (outer join)?

```python
import pandas as pd

df1 = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35},
])
df2 = pd.DataFrame([
    {"name": "Alice", "city": "Warsaw"},
    {"name": "Bob", "city": "Krakow"},
    {"name": "Dorothy", "city": "Opole"},
])

df = pd.merge(df1, df2, on='name', how='outer')
df

# вернёт DataFrame с колонками name, age, city
#      name     age    city
# 0   Alice   25.0  Warsaw
# 1     Bob   30.0  Krakow
# 2 Charlie   35.0     NaN
# 3 Dorothy    NaN   Opole
```

### 67. Как извлечь год из столбца с датой?

```python
import pandas as pd

df = pd.DataFrame([
    {"date": "2021-01-01"},
    {"date": "2021-02-01"},
])
df['date'] = pd.to_datetime(df['date'])

df['year'] = df['date'].dt.year
df
# вернёт
#         date  year
# 0 2021-01-01  2021
# 1 2021-02-01  2021
```

### 68. Как объединить два DataFrame по общему столбцу (inner join)?

```python
import pandas as pd

df1 = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])
df2 = pd.DataFrame([
    {"name": "Alice", "city": "Warsaw"},
    {"name": "Bob", "city": "Krakow"},
])

df = pd.merge(df1, df2, on='name')
# то же самое, что:
# df = pd.merge(df1, df2, on='name', how='inner')

df
# вернёт DataFrame с колонками name, age, city
#    name  age    city
# 0 Alice   25  Warsaw
# 1   Bob   30  Krakow
```

### 69. Как объединить два DataFrame по общему столбцу, присоединяя данные только из левого DataFrame (left join)?

```python
import pandas as pd

df1 = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35},
])
df2 = pd.DataFrame([
    {"name": "Alice", "city": "Warsaw"},
    {"name": "Bob", "city": "Krakow"},
    {"name": "Dorothy", "city": "Opole"},
])

df = pd.merge(df1, df2, on='name', how='left')
df

# вернёт DataFrame с колонками name, age, city
#      name   age    city
# 0   Alice   25  Warsaw
# 1     Bob   30  Krakow
# 2 Charlie   35     NaN
```

### 70. Как объединить два DataFrame с одинаковой структурой (без объединения по ключу)?

```python
import pandas as pd

df1 = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
])
df2 = pd.DataFrame([
    {"name": "Charlie", "age": 35},
    {"name": "David", "age": 40},
])

df = pd.concat([df1, df2])
df
# вернёт DataFrame с 4 строками
```

### 71. Как вычислить количество дней между датой и сегодняшним днём?

```python
import pandas as pd

df = pd.DataFrame([
    {"date": "2021-01-01"},
    {"date": "2021-02-01"},
])
df['date'] = pd.to_datetime(df['date'])

df['days_since'] = (pd.to_datetime('today') - df['date']).dt.days
df
# вернёт (days_since может отличаться в зависимости от даты запуска кода)
#         date  days_since
# 0 2021-01-01        1297
# 1 2021-02-01        1266
```

### 72. Как преобразовать столбец строк в формат даты?

```python
import pandas as pd

df = pd.DataFrame([
    {"date": "2021-01-01"},
    {"date": "2021-02-01"},
])

df['date'] = pd.to_datetime(df['date'])
```

### 73. Как объединить два DataFrame по общему столбцу, присоединяя данные только из правого DataFrame (right join)?

```python
import pandas as pd

df1 = pd.DataFrame([
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35},
])
df2 = pd.DataFrame([
    {"name": "Alice", "city": "Warsaw"},
    {"name": "Bob", "city": "Krakow"},
    {"name": "Dorothy", "city": "Opole"},
])

df = pd.merge(df1, df2, on='name', how='right')
df

# вернёт DataFrame с колонками name, age, city
#      name   age   city
# 0   Alice  25.0  Warsaw
# 1     Bob  30.0  Krakow
# 2 Dorothy   NaN   Opole
```

### 74. Как фильтровать DataFrame по дате?

```python
import pandas as pd

df = pd.DataFrame([
    {"date": "2021-01-01"},
    {"date": "2021-02-01"},
])
df['date'] = pd.to_datetime(df['date'])

df = df[df['date'] > '2021-01-15']
df
# вернёт
#         date
# 1 2021-02-01
```

### 75. Как вычислить длину строки в столбце DataFrame?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice"},
    {"name": "Bob"},
])

df['name_length'] = df['name'].str.len()
df
# вернёт
#     name  name_length
# 0  Alice            5
# 1    Bob            3
```

### 76. Как преобразовать все буквы в столбце в заглавные (прописные)?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice"},
    {"name": "Bob"},
])

df['name'] = df['name'].str.upper()
df
# вернёт
#     name
# 0  ALICE
# 1    BOB
```

### 77. Как сделать первую букву в столбце большой?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "alice"},
    {"name": "bob"},
])

df['name'] = df['name'].str.title()
df
# вернёт
#     name
# 0  Alice
# 1    Bob
```

### 78. Как заменить выбранные символы в столбце?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice"},
    {"name": "Bob"},
])

df['name'] = df['name'].str.replace('A', 'Z')
df
# вернёт
#     name
# 0  Zlice
# 1    Bob
```

### 79. Как объединить значения столбцов типа string?

```python
import pandas as pd

df = pd.DataFrame([
    {"first_name": "Alice", "last_name": "Smith"},
    {"first_name": "Bob", "last_name": "Brown"},
])

df['full_name'] = df['first_name'] + ' ' + df['last_name']
df
# вернёт
#   first_name last_name    full_name
# 0      Alice     Smith  Alice Smith
# 1        Bob     Brown    Bob Brown
```

### 80. Как преобразовать все буквы в столбце в строчные?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice"},
    {"name": "Bob"},
])

df['name'] = df['name'].str.lower()
df
# вернёт
#     name
# 0  alice
# 1    bob
```

### 81. Как удалить лишние пробелы из столбца?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": " Alice "},
    {"name": " Bob "},
])

df['name'] = df['name'].str.strip()
df
# вернёт
#     name
# 0  Alice
# 1    Bob
```

### 82. Как добавить столбцы, разделяя значения другого столбца?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice Smith"},
    {"name": "Bob Brown"},
])

df['first_name'] = df['name'].str.split(' ').str[0]
df
# вернёт
#           name first_name
# 0  Alice Smith      Alice
# 1    Bob Brown        Bob
```

### 83. Как проверить, содержит ли столбец определённую подстроку?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice"},
    {"name": "Bob"},
])

df['name'].str.contains('A') # вернёт True там, где столбец содержит 'A'
```

### 84. Как разделить столбец на два новых столбца?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice Smith"},
    {"name": "Bob Brown"},
])

df[['first_name', 'last_name']] = df['name'].str.split(' ', expand=True)
df
# вернёт
#          name first_name last_name
# 0 Alice Smith      Alice     Smith
# 1  Bob Brown        Bob     Brown
```

### 85. Как сгруппировать DataFrame по столбцу и выполнить несколько агрегаций?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "city": "Warsaw"},
    {"name": "Bob", "age": 30, "city": "Krakow"},
    {"name": "Charlie", "age": 20, "city": "Warsaw"},
    {"name": "Ed", "age": 21, "city": "Warsaw"},
])

df.groupby('city')[['age']].agg(['mean', 'median'])
#         age
#        mean median
# city
# Krakow 30.0   30.0
# Warsaw 22.0   21.0
```

### 86. Как сгруппировать DataFrame по году из столбца с датой?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "date": "2021-01-01"},
    {"name": "Bob", "date": "2021-02-01"},
    {"name": "Charlie", "date": "2022-01-01"},
])

df['date'] = pd.to_datetime(df['date'])
df.groupby(df['date'].dt.year).count()
```

### 87. Как сгруппировать DataFrame по столбцу и посчитать количество элементов?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "city": "Warsaw"},
    {"name": "Bob", "age": 30, "city": "Krakow"},
    {"name": "Charlie", "age": 35, "city": "Warsaw"},
])

df.groupby('city').count()
#        name  age
# city
# Krakow    1    1
# Warsaw    2    2
```

### 88. Что возвращает метод groupby в сочетании с агрегацией (mean, count и др.)?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "city": "Warsaw"},
    {"name": "Bob", "age": 30, "city": "Krakow"},
    {"name": "Charlie", "age": 35, "city": "Warsaw"},
])

df.groupby('city')[['age']].mean() # вернёт DataFrame с индексом city
```

### 89. Как сгруппировать DataFrame по столбцу и вычислить среднее?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "city": "Warsaw"},
    {"name": "Bob", "age": 30, "city": "Krakow"},
    {"name": "Charlie", "age": 35, "city": "Warsaw"},
])

df.groupby('city')[['age']].mean()
#         age
# city
# Krakow  30.0
# Warsaw  30.0
```

### 90. Как сгруппировать DataFrame по столбцу и вычислить медиану?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "city": "Warsaw"},
    {"name": "Bob", "age": 30, "city": "Krakow"},
    {"name": "Charlie", "age": 35, "city": "Warsaw"},
])

df.groupby('city')[['age']].median()
#         age
# city
# Krakow  30.0
# Warsaw  25.0
```

### 91. Как сгруппировать DataFrame по столбцу и выполнить несколько агрегаций для разных столбцов?

```python
import pandas as pd

df = pd.DataFrame([
    {"name": "Alice", "age": 25, "city": "Warsaw", "height": 160},
    {"name": "Bob", "age": 30, "city": "Krakow", "height": 170},
    {"name": "Charlie", "age": 35, "city": "Warsaw", "height": 150},
    {"name": "Dorothy", "age": 33, "city": "Warsaw", "height": 150},
])

df.groupby('city').agg({'age': ['mean', 'median'], 'height': ['mean', 'median']})
#         age            height
#        mean median       mean median
# city
# Krakow 30.0   30.0 170.000000  170.0
# Warsaw 31.0   33.0 153.333333  150.0
```

---

## Модуль 5

### 1. Как создать объект Path?

```python
from pathlib import Path

path = Path('data.txt')
```

### 2. Что такое XML?

**XML** (eXtensible Markup Language) — это язык разметки, предназначенный для представления данных в текстовом виде.

Пример:
```xml
<person>
    <name>John</name>
    <age>30</age>
    <city>New York</city>
</person>
```

### 3. Как игнорировать заголовок при чтении CSV-файла в DataFrame Pandas?

```python
import pandas as pd

df = pd.read_csv('data.csv', header=None, names=['name', 'age', 'city'])
```

### 4. Как проверить, указывает ли путь на файл?

```python
from pathlib import Path

path = Path('data.txt')
print(path.is_file())
```

### 5. Что такое pathlib?

**pathlib** — это модуль Python, предоставляющий класс Path для работы с путями файловой системы.

### 6. Как получить имя файла без расширения из объекта Path?

```python
from pathlib import Path

path = Path('data.txt')
print(path.stem)
```

### 7. Как загрузить JSON-файл в DataFrame Pandas?

```python
import pandas as pd

df = pd.read_json('data.json')
```

### 8. Как загрузить содержимое JSON-файла в переменную Python?

```python
import json

with open('data.json', 'r') as f:
    data = json.loads(f.read())
```

### 9. Как перебрать все CSV-файлы в каталоге?

```python
from pathlib import Path

path = Path('data')
for file_path in path.glob('*.csv'):
    print(file_path)
```

### 10. Как загрузить CSV-файл в DataFrame Pandas и сконвертировать столбцы с датами?

```python
import pandas as pd

df = pd.read_csv('data.csv', parse_dates=['date'])
```

### 11. Как получить расширение файла из объекта Path?

```python
from pathlib import Path

path = Path('data.txt')
print(path.suffix)
```

### 12. Как загрузить JSON-файл в DataFrame Pandas и сконвертировать столбцы с датами?

```python
import pandas as pd

df = pd.read_json('data.json', convert_dates=['date'])
```

### 13. Как объединить пути?

```python
from pathlib import Path

path = Path('data') / 'file.txt'
```

### 14. Что такое JSON?

**JSON** (JavaScript Object Notation) — это формат обмена данными, который легко читается как человеком, так и машиной.

Пример:
```json
{
    "name": "John",
    "age": 30,
    "city": "New York"
}
```

### 15. Как проверить, существует ли путь?

```python
from pathlib import Path

path = Path('data.txt')
print(path.exists())
```

### 16. Что такое CSV?

**CSV** (Comma Separated Values) — это формат хранения табличных данных в текстовом виде.

Пример:
```
name,age,city
John,30,New York
Alice,25,Los Angeles
```

### 17. Как получить имя файла из объекта Path?

```python
from pathlib import Path

path = Path('data.txt')
print(path.name)
```

### 18. Как представить значение с запятой в CSV-файле?

Значение, содержащее запятую, должно быть заключено в кавычки.

Пример:
```
name,age,city
"John, Jr.",30,New York
Alice,25,Los Angeles
```

### 19. Как загрузить XML-файл в DataFrame Pandas и сконвертировать столбцы с датами?

```python
import pandas as pd

df = pd.read_xml('data.xml', parse_dates=['date'])
```

### 20. Как загрузить XML-файл в DataFrame Pandas?

```python
import pandas as pd

df = pd.read_xml('data.xml')
```

### 21. Как проверить, указывает ли путь на каталог?

```python
from pathlib import Path

path = Path('data')
print(path.is_dir())
```

### 22. Как перебрать файлы в каталоге?

```python
from pathlib import Path

path = Path('data')
for file_path in path.iterdir():
    print(file_path)
```

### 23. Как записать данные в JSON-файл?

```python
import json

data = {
    "name": "John",
    "age": 30,
    "city": "New York"
}

with open('data.json', 'w') as f:
    f.write(json.dumps(data))
```

### 24. Как построить ответ OpenAI с использованием Pydantic?

```python
from pydantic import BaseModel

class Invoice(BaseModel):
    number: str
    date: str
    total: float
```

### 25. Как использовать OpenAI для извлечения данных с изображения?

```python
import openai
import base64

with open('invoice.png', 'rb') as f:
    image_data = base64.b64encode(f.read()).decode('utf-8')

response = openai_client.chat.completions.create(
    model="gpt-4o",
    temperature=0,
    messages=[
        {
            "role": "user",
            "content": [
                {
                    "type": "text",
                    "text": '''
                        Извлеки всю информацию, содержащуюся на счёте-фактуре.
                        Представь данные в формате JSON.
                    ''',
                },
                {
                    "type": "image_url",
                    "image_url": {
                        "url": f"data:image/png;base64,{image_data}",
                        "detail": "high"
                    },
                },
            ],
        },
    ],
)
```

### 26. Как подготовить изображение для обработки в OpenAI?

Изображение нужно преобразовать в формат, поддерживаемый OpenAI, например, в Base64.

Пример:
```python
import base64

with open('image.png', 'rb') as f:
    image_base64 = base64.b64encode(f.read()).decode('utf-8')
# теперь `image_base64` можно передать в OpenAI
```

### 27. Как использовать библиотеку instructor для работы с OpenAI?

```python
import instructor
from pydantic import BaseModel
from openai import OpenAI

openai_key = "your-opeanai-key"

class Invoice(BaseModel):
    number: str
    date: str
    total: float

instructor_openai_client = instructor.from_openai(OpenAI(api_key=openai_key))

with open('invoice.png', 'rb') as f:
    image_data = base64.b64encode(f.read()).decode('utf-8')

invoice_info = instructor_openai_client.chat.completions.create(
    model="gpt-4o",
    response_model=Invoice,
    messages=[
        {
            "role": "user",
            "content": [
                {
                    "type": "text",
                    "text": "Извлеки детали счёта-фактуры",
                },
                {
                    "type": "image_url",
                    "image_url": {
                        "url": f"data:image/png;base64,{image_data}",
                        "detail": "high"
                    },
                },
            ],
        },
    ],
)
```

### 28. Можно ли использовать OpenAI для распознавания данных с изображений?

Да! Некоторые модели OpenAI могут извлекать данные с изображений.  
Примеры таких мультимодальных моделей: GPT-4o и GPT-4o-mini.

### 29. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт записи из таблицы users, где age больше 30 и меньше 50:

```sql
SELECT * FROM users WHERE age > 30 AND age < 50;
```

### 30. Составь SQL-запрос, который обновит запись в таблице users, где id равен 1, изменив age на 35:

```sql
UPDATE users SET age = 35 WHERE id = 1;
```

### 31. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт записи из таблицы users, где age больше 30, отсортированные по убыванию age:

```sql
SELECT * FROM users WHERE age > 30 ORDER BY age DESC;
```

### 32. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт 10 записей из таблицы users, где age больше 30, начиная с 10-й записи:

```sql
SELECT * FROM users WHERE age > 30 LIMIT 10 OFFSET 10;
```

### 33. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт записи, где age равно NULL:

```sql
SELECT * FROM users WHERE age IS NULL;
```

### 34. Что такое SQLite?

**SQLite** — это база данных, хранящаяся в одном файле.

### 35. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт первые 10 записей, где age больше 30:

```sql
SELECT * FROM users WHERE age > 30 LIMIT 10;
```

### 36. Пусть есть две таблицы users и orders с колонками id, name и age, а также user_id, product и price  
Составь SQL-запрос, который вернёт все записи из orders и подходящие записи из users, где user_id равен id:

```sql
SELECT
    *
FROM users
RIGHT JOIN orders
ON users.id = orders.user_id;
```

### 37. Пусть есть две таблицы users и orders с колонками id, name и age, а также user_id, product и price  
Составь SQL-запрос, который вернёт все записи из users и подходящие записи из orders, где user_id равен id:

```sql
SELECT
    *
FROM users
LEFT JOIN orders
ON users.id = orders.user_id;
```

### 38. Что такое SQL?

**SQL** (Structured Query Language) — это язык запросов для управления реляционными базами данных.

### 39. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт колонку name из users с алиасом full_name:

```sql
SELECT name AS full_name FROM users;
```

### 40. Пусть есть две таблицы users и orders с колонками id, name и age, а также user_id, product и price  
Составь SQL-запрос, который вернёт записи из users и orders, где user_id равен id:

```sql
SELECT
    *
FROM users
JOIN orders
ON users.id = orders.user_id;
```

### 41. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт записи, где age не NULL:

```sql
SELECT * FROM users WHERE age IS NOT NULL;
```

### 42. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт все записи из users:

```sql
SELECT * FROM users;
```

### 43. Что такое база данных?

**База данных** — это совокупность данных, организованных для эффективного управления и доступа.

### 44. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт только name и age:

```sql
SELECT name, age FROM users;
```

### 45. Составь SQL-запрос, который удалит запись из users, где id равен 1:

```sql
DELETE FROM users WHERE id = 1;
```

### 46. Составь SQL-запрос, который удалит таблицу users:

```sql
DROP TABLE users;
```

### 47. Как сохранить данные из DataFrame Pandas в базу SQLite?

```python
import sqlite3
import pandas as pd

df = pd.DataFrame({
    'id': [1, 2, 3],
    'name': ['John', 'Alice', 'Bob'],
    'age': [30, 25, 35],
})

with sqlite3.connect('learning_select.db') as conn:
    df.to_sql('employees', conn, if_exists='replace', index=False)
```

### 48. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт записи, где age больше 30:

```sql
SELECT * FROM users WHERE age > 30;
```

### 49. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт количество записей для каждого значения age:

```sql
SELECT age, COUNT(*) FROM users GROUP BY age;
```

### 50. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт минимальный, максимальный и средний возраст:

```sql
SELECT MIN(age), MAX(age), AVG(age) FROM users;
```

### 51. Составь SQL-запрос, который вставит запись в users с id=1, name=John, age=30:

```sql
INSERT INTO users (id, name, age) VALUES (1, 'John', 30);
```

### 52. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт количество записей для каждого значения age, где их больше 1:

```sql
SELECT
    age,
    COUNT(*) AS count
FROM users
GROUP BY age
HAVING count > 1;
```

### 53. Пусть есть таблица users с колонками id, name и zawod  
Составь SQL-запрос, который вернёт минимальный, максимальный и средний возраст для каждой профессии:

```sql
SELECT zawod, MIN(age), MAX(age), AVG(age) FROM users GROUP BY zawod;
```

### 54. Пусть есть две таблицы users и orders с колонками id, name и age, а также user_id, product и price  
Составь SQL-запрос, который вернёт все записи из users и orders, где user_id равен id (FULL JOIN):

```sql
SELECT
    *
FROM users
FULL JOIN orders
ON users.id = orders.user_id;
```

### 55. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт записи, где name содержит 'John':

```sql
SELECT * FROM users WHERE name LIKE '%John%';
```

### 56. Как загрузить данные из SQLite в DataFrame Pandas?

```python
import sqlite3
import pandas as pd

with sqlite3.connect('learning_select.db') as conn:
    df = pd.read_sql('SELECT * FROM employees', conn)

df
```

### 57. Составь SQL-запрос, который создаст таблицу users с колонками id, name и age:

```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    name TEXT,
    age INT
);
```

### 58. Пусть есть таблица users с колонками id, name и age  
Составь SQL-запрос, который вернёт записи, где name равен одному из: John, Alice или Bob:

```sql
SELECT * FROM users WHERE name IN ('John', 'Alice', 'Bob');
```

### 59. Что такое ORC?

**ORC** (Optimized Row Columnar) — это формат хранения данных, оптимизированный для хранения табличных данных.

ORC — это колоночный формат, то есть данные сохраняются по столбцам, а не по строкам.

### 60. Как сохранить данные в файл ORC?

```python
import pandas as pd

df = pd.DataFrame({
    'id': [1, 2, 3],
    'name': ['John', 'Alice', 'Bob'],
    'age': [30, 25, 35],
})

df.to_orc('users.orc', engine='pyarrow')
```

---

## Модуль 6

### 1. Как сгенерировать фейковый текст?

```python
from faker import Faker

fake = Faker()
print(fake.text())
# Если нужен текст примерно определённой длины:
print(fake.text(300))
```

### 2. Как сгенерировать фейковые имя и фамилию?

```python
from faker import Faker

fake = Faker()
print(fake.name())
# или отдельно:
print(fake.first_name(), fake.last_name())
```

### 3. Как установить Faker?

```bash
pip install Faker
```

### 4. Как сгенерировать фейковый DataFrame?

```python
from faker import Faker
import pandas as pd

fake = Faker()

data = {
    'name': [fake.name() for _ in range(5)],
    'address': [fake.address() for _ in range(5)],
    'email': [fake.email() for _ in range(5)]
}

df = pd.DataFrame(data)
df
```

### 5. Как начать пользоваться библиотекой Faker?

```python
from faker import Faker

fake = Faker()
print(fake.name())
```

### 6. Как сгенерировать фейковый e-mail?

```python
from faker import Faker

fake = Faker()
print(fake.email())
```

### 7. Как сгенерировать список фейковых данных?

```python
from faker import Faker

fake = Faker()
data = []
for _ in range(5):
    data.append(fake.name())

print(data)
```

### 8. Как сгенерировать фейковый адрес?

```python
from faker import Faker

fake = Faker()
print(fake.address())
```

### 9. Как сгенерировать фейковые данные на польском языке?

```python
from faker import Faker

fake = Faker('pl-PL')
print(fake.name())
print(fake.address())
```

### 10. Что такое Faker?

Библиотека **Faker** — это инструмент на Python для генерации фейковых данных.  
Особенно полезна для тестирования приложений или создания примеров данных.

### 11. Как сгенерировать случайные целые числа в NumPy?

```python
import numpy as np

a = np.random.randint(0, 10, 5)
print(a)
# [4 7 6 6 9]
```

### 12. Как выполнять арифметические операции над массивами в NumPy?

```python
import numpy as np

a = np.array([1, 2, 3, 4])
b = np.array([5, 7, 7, 10])

print(a + b)
# [ 6  9 10 14]

print(a - b)
# [-4 -5 -4 -6]

print(a * b)
# [ 5 14 21 40]

print(a / b)
# [0.2        0.28571429 0.42857143 0.4       ]
```

### 13. Как установить NumPy?

```bash
pip install numpy
```

### 14. Как сгенерировать случайные данные в NumPy?

```python
import numpy as np

a = np.random.random(5)
print(a)
# [0.5488135  0.71518937 0.60276338 0.54488318 0.4236548]
```

### 15. Как создать массив в NumPy?

```python
import numpy as np

a = np.array([1, 2, 3, 4])
print(a)
```

### 16. Как сгенерировать данные из нормального распределения в NumPy?

```python
import numpy as np

a = np.random.normal(0, 1, 5)
print(a)
# [-0.52817175 -1.07296862  0.86540763 -2.3015387   1.74481176]
```

### 17. Как выполнять арифметические операции между числом и массивом в NumPy?

```python
import numpy as np

a = np.array([1, 2, 3, 4])

print(a + 2)
# [3 4 5 6]

print(a - 2)
# [-1  0  1  2]

print(a * 2)
# [2 4 6 8]

print(a / 2)
# [0.5 1.  1.5 2. ]
```

### 18. Что такое NumPy?

**NumPy** — это библиотека Python для численных вычислений.  
Она является одной из важнейших библиотек для работы с числовыми данными.

### 19. Как начать пользоваться Matplotlib?

```python
import matplotlib.pyplot as plt

plt.plot([1, 4, 3, 9])
plt.show()
# визуализирует линейный график
```

### 20. Как изменить подпись оси Y в Matplotlib?

```python
import matplotlib.pyplot as plt

plt.plot([1, 4, 3, 9])
plt.ylabel('Значение')
plt.show()
# визуализирует линейный график с подписью оси Y: Значение
```

### 21. Как нарисовать красные точки в Matplotlib?

```python
import matplotlib.pyplot as plt

plt.plot([1, 2, 3, 4], 'ro') # ro = Red Ovals
plt.show()
# визуализирует линейный график, где вместо линии — красные точки
```

### 22. Как построить точечный график с размером и цветом в Matplotlib?

```python
import matplotlib.pyplot as plt
import random

data = {
    "x": [],
    "y": [],
    "color": [],
    "size": []
}

for i in range(0, 100):
    data["x"].append(random.random())
    data["y"].append(random.randint(0, 50))
    data["color"].append(random.random())
    data["size"].append(random.random() * 100)

plt.scatter('x', 'y', c='color', s='size', data=data)
plt.show()
# визуализирует точечный график с индивидуальным размером и цветом точек
```

### 23. Как установить Matplotlib?

```bash
pip install matplotlib
```

### 24. Какие формы можно нарисовать в Matplotlib?

В Matplotlib можно рисовать различные формы, например:

- треугольники: '^'
- квадраты: 's'
- звёздочки: '*'
- крестики: '+'
- точки: '.'

Пример:
```python
import matplotlib.pyplot as plt

plt.plot([1, 2, 3, 4], 's')   # квадраты
plt.plot([2, 3, 4, 2], 'r*')  # красные звёздочки
plt.plot([3, 4, 5, 1], 'g^')  # зелёные треугольники
plt.plot([4, 5, 6, 3], 'b+')  # синие крестики
plt.show()
# визуализирует несколько линейных графиков с разными маркерами
```

### 25. Что такое Matplotlib?

**Matplotlib** — это библиотека Python для построения графиков.  
Это одна из самых популярных библиотек для визуализации данных.

### 26. Как контролировать диапазон по осям X и Y в Matplotlib?

```python
import matplotlib.pyplot as plt

plt.plot([1, 2, 3, 4], [1, 4, 9, 16])
plt.axis([0, 6, 0, 20]) # X: 0-6; Y: 0-20
plt.show()
# визуализирует линейный график с заданными диапазонами по осям
```

### 27. Как построить гистограмму с текстом в Matplotlib?

```python
import matplotlib.pyplot as plt
import numpy as np

mu, sigma = 100, 15  # mu — среднее, sigma — стандартное отклонение
x = mu + sigma * np.random.randn(10000)

# Гистограмма данных
n, bins, patches = plt.hist(x, 50, density=True, facecolor='g', alpha=0.75)

plt.xlabel('IQ')
plt.ylabel('Вероятность')
plt.title('Гистограмма IQ')
plt.text(60, .025, r'$\mu=100,\ \sigma=15$')
plt.axis([40, 160, 0, 0.03])
plt.grid(True)
plt.show()
# визуализирует гистограмму с текстом
```

### 28. Как изменить подпись оси X в Matplotlib?

```python
import matplotlib.pyplot as plt

plt.plot([1, 2, 3, 4])
plt.xlabel('Индекс')
plt.show()
# визуализирует линейный график с подписью оси X: Индекс
```

### 29. Как создать несколько графиков в Matplotlib?

```python
import matplotlib.pyplot as plt

fig, axs = plt.subplots(2)
axs[0].plot([1, 2, 6, 4])
axs[1].plot([4, 6, 4, 1])
plt.show()
# визуализирует несколько линейных графиков с собственными настройками
```

### 30. Как построить столбчатую диаграмму в Matplotlib?

```python
import matplotlib.pyplot as plt

labels = ['A', 'B', 'C', 'D']
values = [10, 30, 60, 50]

plt.bar(labels, values)
plt.show()
# визуализирует столбчатую диаграмму с заданными значениями
```

### 31. Как установить Seaborn?

```bash
pip install seaborn
```

### 32. Как изучать взаимосвязь между переменными/столбцами с помощью seaborn и линейных графиков (с доверительными интервалами)?

```python
import seaborn as sns

fmri_df = sns.load_dataset("fmri")

sns.relplot(
    data=fmri_df,
    kind="line",
    x="timepoint",
    y="signal",
    col="region",
    hue="event",
    style="event"
)
```

### 33. Как строить линии регрессии с помощью seaborn?

```python
import seaborn as sns

tips_df = sns.load_dataset("tips")

sns.lmplot(
    data=tips_df,
    x="total_bill",
    y="tip",
    col="time",
    hue="smoker"
)
```

### 34. Как исследовать распределения числовых переменных с помощью seaborn?

```python
import seaborn as sns

tips_df = sns.load_dataset("tips")

sns.displot(
    data=tips_df,
    x="total_bill",
    col="time",
    kde=True
)
```

### 35. Как исследовать распределения категориальных переменных с помощью seaborn и столбчатых диаграмм?

```python
import seaborn as sns

tips_df = sns.load_dataset("tips")

sns.catplot(
    data=tips_df,
    kind="bar",
    x="day",
    y="total_bill",
    hue="smoker"
)
```

### 36. Как исследовать распределения категориальных переменных с помощью seaborn?

```python
import seaborn as sns

tips_df = sns.load_dataset("tips")

sns.catplot(
    data=tips_df,
    kind="violin",
    x="day",
    y="total_bill",
    hue="smoker",
    split=True
)
```

### 37. Как изучать взаимосвязь между переменными/столбцами с помощью seaborn и точечных графиков?

```python
import seaborn as sns

tips_df = sns.load_dataset("tips")

sns.relplot(
    data=tips_df,
    x="total_bill",
    y="tip",
    col="time",
    hue="smoker",
    style="smoker",
    size="size"
)
```

### 38. Что такое Seaborn?

**Seaborn** — это библиотека Python для визуализации данных.  
Она основана на Matplotlib и предлагает более удобное API для построения графиков.

### 39. Как исследовать взаимосвязи между переменными с помощью seaborn?

```python
import seaborn as sns

penguins_df = sns.load_dataset("penguins")

sns.pairplot(
    data=penguins_df,
    hue="species"
)
```

### 40. Как построить boxplot (ящик с усами) в plotly?

```python
import plotly.express as px
import seaborn as sns

tips_df = sns.load_dataset("tips")
fig = px.box(tips_df, x="day", y="tip")
fig.update_layout(
    title="Распределение чаевых в зависимости от дня недели",
    xaxis_title="День недели",
    yaxis_title="Чаевые"
)
fig.show()
```

### 41. Как построить bubble chart (пузырьковую диаграмму) в plotly?

```python
import plotly.express as px
import seaborn as sns

tips_df = sns.load_dataset("tips")
fig = px.scatter(
    tips_df,
    x="total_bill",
    y="tip",
    color="smoker",
    size="size"
)
fig.update_layout(
    title="Зависимость чаевых от суммы счёта",
    xaxis_title="Сумма счёта",
    yaxis_title="Чаевые"
)
fig.show()
```

### 42. Как построить столбчатую диаграмму в plotly?

```python
import plotly.express as px
import seaborn as sns

tips_df = sns.load_dataset("tips")
tips_df["tip_percentage"] = tips_df["tip"] / tips_df["total_bill"] * 100
mean_tips_df = tips_df.groupby("day", as_index=False)["tip_percentage"].mean()

fig = px.bar(mean_tips_df, x="day", y="tip_percentage")
fig.update_layout(
    title="Средний процент чаевых по дням недели",
    xaxis_title="День недели",
    yaxis_title="Средний процент чаевых",
)
fig.show()
```

### 43. Как построить тепловую карту (heatmap) в plotly?

```python
import plotly.express as px
import seaborn as sns

tips_df = sns.load_dataset("tips")
fig = px.imshow(
    tips_df.corr(numeric_only=True),
    color_continuous_scale="Inferno_r",
)
fig.show()
```

### 44. Что такое Plotly?

**Plotly** — это библиотека Python для интерактивной визуализации данных.  
Позволяет создавать интерактивные графики, карты, диаграммы и многое другое.

### 45. Как строить гистограммы с помощью plotly?

```python
import plotly.express as px
import seaborn as sns

tips_df = sns.load_dataset("tips")
fig = px.histogram(
    tips_df,
    x="total_bill",
    title="Распределение суммы счетов",
    nbins=nbins,
    width=600,
    height=400,
)
fig.show()
```

### 46. Как установить Plotly?

```bash
pip install plotly
```

### 47. Как построить точечный график (scatter plot) в plotly?

```python
import plotly.express as px
import seaborn as sns

tips_df = sns.load_dataset("tips")
fig = px.scatter(tips_df, x="total_bill", y="tip")
fig.update_layout(
    title="Зависимость чаевых от суммы счёта",
    xaxis_title="Сумма счёта",
    yaxis_title="Чаевые",
)
fig.show()
```

### 48. Как сгенерировать отчёт по анализу данных с помощью ydata-profiling?

```python
import pandas as pd
from ydata_profiling import ProfileReport

hm_2024_df = pd.read_csv(
    'halfmarathon_wroclaw_2024__final.csv',
    sep=';'
)
hm_2024_report = ProfileReport(
    hm_2024_df,
    title="Анализ данных полумарафона Вроцлав 2024"
)
hm_2024_report
```

### 49. Что такое ydata-profiling?

**ydata-profiling** — это библиотека Python для автоматического анализа данных.  
Позволяет генерировать отчёты с описанием данных, включая статистики, гистограммы, корреляционные матрицы и многое другое.

### 50. Как сравнить два набора данных с помощью ydata-profiling?

```python
import pandas as pd
from ydata_profiling import ProfileReport

hm_2024_df = pd.read_csv(
    'halfmarathon_wroclaw_2024__final.csv',
    sep=';'
)
hm_2023_df = pd.read_csv(
    'halfmarathon_wroclaw_2023__final.csv',
    sep=';'
)
hm_2024_report = ProfileReport(
    hm_2024_df,
    title="Анализ данных полумарафона Вроцлав 2024"
)
hm_2024_report.to_file("hm_2024_report.html")

hm_2023_report = ProfileReport(
    hm_2023_df,
    title="Анализ данных полумарафона Вроцлав 2023"
)
hm_2023_report.to_file("hm_2023_report.html")

comparison_report = hm_2023_report.compare(hm_2024_report)
comparison_report.to_file("comparison_report.html")
```

### 51. Как установить ydata-profiling?

```bash
pip install ydata-profiling
```

### 52. Как задать заголовок приложения в Streamlit?

```python
import streamlit as st

st.title("Заголовок приложения")
```

### 53. Как добавить боковую панель в приложении Streamlit?

```python
import streamlit as st

with st.sidebar:
    st.write('Боковая панель')
```

### 54. Как изменить макет страницы в Streamlit?

```python
import streamlit as st
# (в самом верху файла)
st.set_page_config(layout='wide')
```

### 55. Как добавить кнопку для загрузки файла в Streamlit?

```python
import streamlit as st

uploaded_file = st.file_uploader('Выберите файл')
```

### 56. Что такое Streamlit?

**Streamlit** — это библиотека Python, которая позволяет легко создавать веб-приложения для анализа данных и машинного обучения.

### 57. Как вывести код в приложении Streamlit?

```python
import streamlit as st

code = '''
a = 4
b = 5
c = a + b
'''

st.code(code, language='python')
```

### 58. Как отобразить изображение в приложении Streamlit?

```python
import streamlit as st

st.image('путь_к_изображению')
```

### 59. Как отобразить столбчатую диаграмму в Streamlit?

```python
import streamlit as st
import pandas as pd
import numpy as np

df = pd.DataFrame({
    'A': np.random.randint(0, 100, 5),
    'B': np.random.randint(0, 100, 5)
})

st.bar_chart(df)
```

### 60. Как отключить кнопку в приложении Streamlit?

```python
import streamlit as st

st.button('Нажми меня', disabled=True)
```

### 61. Как добавить текстовое поле в приложении Streamlit?

```python
import streamlit as st

text = st.text_input('Введите текст')
st.write('Введено:', text)
```

### 62. Как добавить аудио в приложение Streamlit?

```python
import streamlit as st

st.audio('путь_к_аудиофайлу')
```

### 63. Как добавить поле для даты в приложении Streamlit?

```python
import streamlit as st

date = st.date_input('Выберите дату')
st.write('Введено:', date)
```

### 64. Как добавить видео в приложение Streamlit?

```python
import streamlit as st

st.video('путь_к_видео/URL')
```

### 65. Как добавить кнопку в приложении Streamlit?

```python
import streamlit as st

if st.button('Нажми меня'):
    st.write('Кнопка нажата!')
```

### 66. Как вывести Markdown в приложении Streamlit?

```python
import streamlit as st

st.markdown('''
## Добро пожаловать в приложение Streamlit!

Это **Markdown**
''')
```

### 67. Как отобразить DataFrame в приложении Streamlit?

```python
import streamlit as st
import pandas as pd

df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6]
})

st.dataframe(df, hide_index=True)
```

### 68. Как сообщать о статусе приложения в Streamlit?

```python
import streamlit as st

st.error('Это ошибка')        # Красная панель
st.warning('Это предупреждение') # Жёлтая панель
st.info('Это информация')     # Синяя панель
st.success('Успешно!')        # Зелёная панель
```

### 69. Как добавить поле для времени в приложении Streamlit?

```python
import streamlit as st

time = st.time_input('Укажите время')
st.write('Введено:', time)
```

### 70. Как добавить слайдер в приложении Streamlit?

```python
import streamlit as st

value = st.slider('Выберите значение', 0, 100, 50)
st.write('Выбрано:', value)
```

### 71. Как добавить текст-подсказку к компоненту в Streamlit?

```python
import streamlit as st

st.text_input('Введите текст', help='Подсказка, объясняющая, что вводить')
```

### 72. Как отобразить график Matplotlib в Streamlit?

```python
import streamlit as st
import matplotlib.pyplot as plt
import numpy as np

x = np.random.randn(100)
y = np.random.randn(100)

fig, ax = plt.subplots()
ax.scatter(x, y)

st.pyplot(fig)
```

### 73. Как добавить кнопку для скачивания файла в приложении Streamlit?

```python
import streamlit as st

st.download_button(
    'Скачать файл',
    data='''
name,age
Alice,25
Bob,30
    ''',
    file_name="data.csv",
    mime="text/csv",
)
```

### 74. Как использовать радиокнопки в Streamlit?

```python
import streamlit as st

option = st.radio('Выберите вариант', ['A', 'B', 'C'])
st.write('Выбрано:', option)
```

### 75. Как добавить множественный выбор в приложении Streamlit?

```python
import streamlit as st

options = st.multiselect('Выберите варианты', ['A', 'B', 'C'])
st.write('Выбрано:', options)
```

### 76. Что такое st.session_state?

**st.session_state** — это объект для хранения данных между запусками приложения.  
Позволяет делать данные доступными в разных частях приложения.

### 77. Как использовать колонки в Streamlit?

```python
import streamlit as st

[col1, col2] = st.columns(2)

with col1:
    st.write('Первая колонка')

with col2:
    st.write('Вторая колонка')
```

### 78. Как добавить числовое поле в приложении Streamlit?

```python
import streamlit as st

number = st.number_input('Введите число')
st.write('Введено:', number)
```

### 79. Как установить Streamlit?

С помощью pip:
```bash
pip install streamlit
```

С помощью conda:
```bash
conda activate od_zera_do_ai
conda install -y streamlit
```

### 80. Как добавить выпадающий список в приложении Streamlit?

```python
import streamlit as st

option = st.selectbox('Выберите вариант', ['A', 'B', 'C'])
st.write('Выбрано:', option)
```

### 81. Как добавить метрику в приложение Streamlit?

```python
import streamlit as st

st.metric('Стоимость звонка (PLN)', 123.45)
```

### 82. Как добавить текстовое поле с паролем в Streamlit?

```python
import streamlit as st

password = st.text_input('Введите пароль', type='password')
st.write('Введено:', password)
```

### 83. Какие чат-компоненты доступны в Streamlit?

Streamlit предлагает несколько чат-компонентов:

1. **st.chat_input** — поле для ввода текста.
2. **st.chat_message** — сообщение в чате.

### 84. Как создать форму в приложении Streamlit?

Используйте st.form и st.form_submit_button:
```python
import streamlit as st

with st.form(key='my_form'):
    text_input = st.text_input('Введите имя')
    submit_button = st.form_submit_button('Отправить')
    if submit_button:
        st.write('Введено:', text_input)
```

### 85. Как запустить приложение Streamlit?

Используйте команду:
```bash
streamlit run app.py
```
где app.py — это файл с кодом приложения.

### 86. Как добавить чекбокс в приложении Streamlit?

```python
import streamlit as st

if st.checkbox('Отметь меня'):
    st.write('Отмечено!')
```

### 87. Когда использовать st.rerun?

**st.rerun** позволяет вручную перезапустить приложение Streamlit.  
Используйте, если нужно, чтобы приложение перезапустилось после определённого условия (например, изменился st.session_state, но изменения не видны сразу).

### 88. Как добавить многострочное текстовое поле в приложении Streamlit?

```python
import streamlit as st

text = st.text_area('Введите текст')
st.write('Введено:', text)
```

### 89. Как добавить заголовок в приложение Streamlit?

```python
import streamlit as st

st.header('Ваш заголовок')
```

### 90. Как использовать st.session_state?

```python
import streamlit as st

if 'counter' not in st.session_state:
    st.session_state["counter"] = 0

st.write(f"Counter: {st.session_state['counter']}")
if st.button("Increment"):
    st.session_state["counter"] += 1
```

---

## Модуль 7

### 1. Как узнать длительность аудиофайла?

Чтобы узнать длительность аудиофайла, используйте атрибут `duration_seconds`:

```python
from pydub import AudioSegment

# Загружаем аудиофайл
audio = AudioSegment.from_mp3("plik.mp3")

# Проверяем длительность файла
duration = audio.duration_seconds
print(duration)
```

### 2. Как переконвертировать аудиофайл в другой формат?

Чтобы переконвертировать аудиофайл в другой формат, используйте функцию `export`:

```python
from pydub import AudioSegment

# Загружаем аудиофайл
audio = AudioSegment.from_mp3("plik.mp3")

# Конвертируем в формат WAV
audio.export("plik.wav", format="wav")
```

### 3. Как повторить аудио 4 раза?

Чтобы повторить аудио 4 раза, используйте оператор `*`:

```python
from pydub import AudioSegment

# Загружаем аудиофайл
audio = AudioSegment.from_mp3("plik.mp3")

# Повторяем аудио 4 раза
audio_repeated = audio * 4
audio_repeated.export("repeated.mp3", format="mp3")
```

### 4. Как наложить одно аудио на другое?

Чтобы наложить одно аудио на другое, используйте функцию `overlay`:

```python
from pydub import AudioSegment

# Загружаем два аудиофайла
audio1 = AudioSegment.from_mp3("audio1.mp3")
audio2 = AudioSegment.from_mp3("audio2.mp3")

# Накладываем audio2 на audio1
audio_overlayed = audio1.overlay(audio2)
audio_overlayed.export("overlayed.mp3", format="mp3")
```

### 5. Как использовать embeddings?

Чтобы использовать embeddings, отправьте текст в API OpenAI:

```python
from dotenv import dotenv_values
from openai import OpenAI

env = dotenv_values(".env")

openai_client = OpenAI(api_key=env["OPENAI_API_KEY"])

response = openai_client.embeddings.create(
    input=[
        "Dawno temu w trawie",
        "Gdzieś na końcu świata",
        "W krainie czarów",
    ],
    model="text-embedding-3-large"
)
```

### 6. Как увеличить громкость аудиофайла?

Чтобы увеличить громкость аудиофайла, используйте оператор `+=`:

```python
from pydub import AudioSegment

# Загружаем аудиофайл
audio = AudioSegment.from_mp3("plik.mp3")

# Увеличиваем громкость на 10 dB
audio += 10
audio.export("increased_volume.mp3", format="mp3")
```

### 7. Как воспроизвести первые 5 секунд аудиофайла?

Чтобы воспроизвести первые 5 секунд аудиофайла, используйте срез:

```python
from pydub import AudioSegment

# Загружаем аудиофайл
audio = AudioSegment.from_mp3("plik.mp3")

# Первые 5 секунд аудио
audio_first_5_seconds = audio[:5000]
audio_first_5_seconds.export("first_5_seconds.mp3", format="mp3")
```

### 8. Как загрузить аудиофайл?

Чтобы загрузить аудиофайл, используйте функцию `AudioSegment.from_file`:

```python
from pydub import AudioSegment

# Загружаем аудиофайл
audio = AudioSegment.from_mp3("plik.mp3")
```

### 9. Как использовать модель Whisper-1?

Чтобы использовать модель Whisper-1, отправьте аудиофайл с речью в API OpenAI:

```python
from dotenv import dotenv_values
from openai import OpenAI

env = dotenv_values(".env")

openai_client = OpenAI(api_key=env["OPENAI_API_KEY"])

with open("audio.mp3", "rb") as f:
    transcript = openai_client.audio.transcriptions.create(
        file=f,
        model="whisper-1",
        response_format="verbose_json",
    )
```

### 10. Что такое md5?

**md5** — это криптографический алгоритм, который генерирует хэш (сумму) для входных данных.  
md5 полезен для проверки, были ли изменены данные.

### 11. Как объединить два аудиофайла?

Чтобы объединить два аудиофайла, используйте оператор `+`:

```python
from pydub import AudioSegment

# Загружаем два аудиофайла
audio1 = AudioSegment.from_mp3("audio1.mp3")
audio2 = AudioSegment.from_mp3("audio2.mp3")

# Объединяем два файла
audio_combined = audio1 + audio2
audio_combined.export("combined.mp3", format="mp3")
```

### 12. Как использовать md5?

Модуль `hashlib` содержит функцию md5 для вычисления хэша:

```python
import hashlib

# Создаём объект md5
md5_value = hashlib.md5(b"hello")

# Генерируем хэш
hash_value = md5_value.hexdigest()
print(hash_value)
# Output: 5d41402abc4b2a76b9719d911017c592
```

### 13. Что такое Whisper-1?

**Whisper-1** — это модель распознавания речи, созданная OpenAI.  
Модель обучена на большом наборе данных и обеспечивает точное распознавание речи на разных языках и акцентах.

### 14. Что такое embeddings?

**Embeddings** — это представления слов в виде числовых векторов.  
Embeddings позволяют отображать слова в многомерном пространстве, упрощая анализ текста.  
Embeddings для похожих по смыслу фраз будут иметь близкие значения и находиться рядом в пространстве.

### 15. Когда стоит использовать io.BytesIO?

- Когда вы работаете с библиотеками, которым нужен файловый объект, но не хотите записывать данные на диск
- Когда нужно передать бинарные данные в функцию, ожидающую объект файла

### 16. Как использовать io.BytesIO?

Модуль `io` содержит класс BytesIO для работы с бинарными данными в памяти:

```python
import io

# Создаём объект BytesIO
bio = io.BytesIO()

# Записываем бинарные данные
bio.write(b"Hello World!")

# Ставим указатель на начало
bio.seek(0)

# Читаем данные из объекта
print(bio.read())
```

### 17. Какая команда позволяет узнать, какие удалённые репозитории подключены к локальному репозиторию?

```
git remote -v
```

### 18. Какие команды нужно использовать, чтобы зафиксировать изменения?

```
git commit -m "сообщение_коммита"
```

### 19. Как инициализировать репозиторий Git?

```
git init
```

### 20. Что такое основная (main) ветка в Git?

Основная ветка (main branch) в Git — это ветка, которая создаётся по умолчанию при инициализации репозитория. Именно в ней обычно находится самая актуальная версия проекта.

### 21. Что такое репозиторий в контексте Git?

Репозиторий в Git — это место, где хранятся файлы проекта и история изменений. Проще говоря, это папка под наблюдением git, в которой находится исходный код проекта.

### 22. Какая команда связывает локальный репозиторий с удалённым?

```
git remote add origin адрес_репозитория
```

### 23. Какие команды нужно использовать, чтобы отправить зафиксированные изменения в удалённый репозиторий?

Для этого используется команда `git push`. При первом пуше нужно указать имя ветки, например:  
```
git push -u origin main
```
где `origin` — название удалённого репозитория, а `main` — имя ветки.

### 24. За что отвечает команда: git remote add origin адрес_репозитория?

Команда `git remote add origin адрес_репозитория` связывает локальный репозиторий с удалённым. `адрес_репозитория` нужно заменить на адрес вашего удалённого репозитория.

### 25. Какую команду выполнили, чтобы получить информацию?

```
git status
```

### 26. Как проверить состояние репозитория Git?

```
git status
```

### 27. За что отвечает параметр -m в команде: git commit -m '...'?

В команде `git commit -m '...'` параметр `-m` позволяет добавить сообщение коммита. В этом сообщении нужно описать внесённые изменения.

### 28. Что значит, что git — распределённая система контроля версий?

Git — распределённая система контроля версий, то есть каждый пользователь имеет полную копию репозитория на своём компьютере. Даже если сервер с репозиторием выйдет из строя, пользователи смогут продолжать работать над проектом.

### 29. Что такое GitHub?

**GitHub** — это веб-платформа для размещения исходного кода и совместной работы над ним.

### 30. Как выглядит рабочий процесс с Git? Какие шаги нужно выполнить, чтобы добавить изменения в удалённый репозиторий?

1. Сначала добавьте файл(ы) в индекс (стадия подготовки):  
   `git add путь/к_файлу.py`  
   или `git add .`, чтобы добавить все изменения.
2. Затем зафиксируйте изменения:  
   `git commit -m "сообщение_коммита"`
3. После этого отправьте зафиксированные изменения на удалённый репозиторий:  
   `git push`

### 31. Что делает команда: git status?

Команда `git status` показывает текущее состояние репозитория: изменения, добавленные, но не зафиксированные, а также неотслеживаемые файлы.

### 32. Что делает команда: git init?

Команда `git init` создаёт новый репозиторий в каталоге проекта. С этого момента git будет отслеживать изменения в файлах.

### 33. Что такое Git?

**Git** — это система контроля версий. Это инструмент для отслеживания изменений в исходном коде и совместной работы над ним.

### 34. Что делает команда: git add?

Команда `git add` добавляет изменения в индекс, готовя их к фиксации.  
Можно использовать для отдельного файла: `git add файл.py`,  
или для всего каталога: `git add .`.  
Добавляет как новые файлы, так и изменённые (уже отслеживаемые).

### 35. Как добавить изменения в индекс Git (перевести файлы в состояние "готово к фиксации")?

```
git add путь/к_файлу.py
```
или
```
git add .
```

### 36. За что отвечает команда git push?

Команда `git push` отправляет зафиксированные изменения из локального репозитория в удалённый.

### 37. Что такое .gitignore?

Файл `.gitignore` содержит правила, указывающие git, какие файлы и каталоги нужно игнорировать.  
Это позволяет исключить из отслеживания, например, секретные данные или временные файлы.

### 38. Как игнорировать файлы в Git?

Создайте файл `.gitignore` в корневой папке проекта.  
Добавьте в него имена файлов/каталогов, которые должны быть проигнорированы.  
Примеры:
- чтобы игнорировать файл `secrets.txt`, добавьте строку `secrets.txt`
- чтобы игнорировать все файлы `.log`, добавьте строку `*.log`
- чтобы игнорировать папку `data`, добавьте `data/`

### 39. Что такое удалённый репозиторий (remote) в Git?

Удалённый репозиторий (remote) в Git — это репозиторий, расположенный на сервере.  
Позволяет совместно использовать исходный код.

### 40. За что отвечает команда git commit?

Команда `git commit` фиксирует изменения, добавленные в индекс.

### 41. Какую команду или команды выполнили (до git status), чтобы получить информацию?

Пример:
```
git add database.py
git add users.py
git add notebooks/analysis.ipynb
```

### 42. Как развернуть приложение, созданное на Streamlit?

Чтобы развернуть приложение на Streamlit, используйте платформу Streamlit Community Cloud.  
Нужно создать аккаунт на этой платформе и опубликовать приложение.

### 43. Что такое системные зависимости?

Системные зависимости — это библиотеки, необходимые для запуска приложения на сервере, которые НЕ устанавливаются через pip.

Примеры системных зависимостей: ffmpeg (необходим для работы с python-библиотекой pydub).

Преимущество conda над pip: conda устанавливает также системные зависимости.

### 44. Что такое Streamlit Community Cloud?

**Streamlit Community Cloud** — это платформа, позволяющая бесплатно публиковать приложения, созданные на Streamlit.

### 45. Что такое файл requirements.txt?

**requirements.txt** — это файл, где указываются зависимости приложения.  
В нём содержится список библиотек, необходимых для запуска приложения.  
Библиотеки можно установить через команду:  
```
pip install -r requirements.txt
```

### 46. Что такое развёртывание (deployment)?

**Внедрение** (deployment) — это процесс публикации приложения, то есть размещения его в рабочем (продуктивном) окружении.  
Это означает запуск приложения на сервере, чтобы оно стало доступно для пользователей.

### 47. Какой файл позволяет указать системные зависимости в Streamlit Community Cloud?

В Streamlit Community Cloud системные зависимости можно определить в файле **packages.txt**.

### 48. Как сохранить модель в PyCaret?

Чтобы сохранить модель, используйте функцию `save_model`:

```python
import pandas as pd
from pycaret.clustering import setup, create_model, save_model

df = pd.read_csv('data.csv', sep=';')
setup(df)
model = create_model('kmeans')

# Сохраняем модель
save_model(model, 'my_model.pkl')
```

### 49. Что такое PyCaret?

**PyCaret** — это библиотека для автоматизации машинного обучения.  
Позволяет быстро создавать модели машинного обучения без необходимости писать много кода.

### 50. Как загрузить модель в PyCaret?

Чтобы загрузить модель, используйте функцию `load_model`:

```python
from pycaret.clustering import load_model

model = load_model('my_model.pkl')
```

### 51. Как сделать предсказание в PyCaret?

Чтобы сделать предсказание, используйте функцию `predict_model`:

```python
import pandas as pd
from pycaret.clustering import load_model, predict_model

model = load_model('my_model.pkl')
predict_df = pd.read_csv('predict_data.csv', sep=';')

# Делаем предсказание
predictions = predict_model(model, data=predict_df)
```

### 52. Как создать модель кластеризации в PyCaret?

Сначала установите библиотеку PyCaret и загрузите данные:

```python
import pandas as pd
from pycaret.clustering import setup, create_model

df = pd.read_csv('data.csv', sep=';')

# Инициализируем окружение
setup(df)

# Создаём модель кластеризации
model = create_model('kmeans')
```

### 53. Как визуализировать кластеры в PyCaret?

Чтобы визуализировать кластеры, используйте функцию `plot_model`:

```python
import pandas as pd
from pycaret.clustering import setup, create_model, plot_model

df = pd.read_csv('data.csv', sep=';')
setup(df)
model = create_model('kmeans')

# Визуализируем кластеры
plot_model(model, plot='cluster')
```

### 54. Как присвоить кластеры данным в PyCaret?

Чтобы присвоить кластеры данным, используйте функцию `assign_model`:

```python
import pandas as pd
from pycaret.clustering import setup, create_model, assign_model

df = pd.read_csv('data.csv', sep=';')
setup(df)
model = create_model('kmeans')

# Присваиваем кластеры данным
df_clusters = assign_model(model)
```

---

## Модуль 8

### 1. Как найти лучшую модель регрессии в PyCaret?

Чтобы создать модель регрессии, используйте функцию `compare_models`:

```python
import pandas as pd
from pycaret.regression import setup, compare_models

df = pd.read_csv('data.csv', sep=';')

# Инициализируем окружение
setup(df, target='price')

# Сравниваем модели
best = compare_models()
```

### 2. Какой регрессионный модель лучше? Модель A с MSE = 10.1 или модель B с MSE = 25.6?

Модель A лучше, потому что меньший MSE означает меньшую среднеквадратичную ошибку.

### 3. Какая классификационная модель лучше? Модель A с F1 = 0.7 или модель B с F1 = 0.9?

Модель B лучше, потому что больший F1-score означает лучший баланс между Precision и Recall.

### 4. Какой регрессионный модель лучше? Модель A с MSE = 20.5 или модель B с MSE = 15.3?

Модель B лучше, потому что меньший MSE означает меньшую среднеквадратичную ошибку.

### 5. Какая классификационная модель лучше? Модель A с AUC = 0.92 или модель B с AUC = 0.88?

Модель A лучше, потому что больший AUC означает лучшее различение между классами.

### 6. Как сделать предсказание в PyCaret для классификационной модели?

Чтобы сделать предсказание, используйте функцию `predict_model`:

```python
import pandas as pd
from pycaret.classification import load_model, predict_model

model = load_model('classification_pipeline')
predict_df = pd.read_csv('predict_data.csv', sep=';')

# Делаем предсказание
predictions = predict_model(model, data=predict_df)
```

### 7. Какой регрессионный модель лучше? Модель A с R² = 0.92 или модель B с R² = 0.89?

Модель A лучше, потому что больший R² означает лучшее соответствие модели данным.

### 8. Какой регрессионный модель лучше? Модель A с MAPE = 5% или модель B с MAPE = 8%?

Модель A лучше, потому что меньший MAPE означает меньшую среднюю абсолютную процентную ошибку.

### 9. Как визуализировать важность признаков в регрессионной модели PyCaret?

Для визуализации важности признаков используйте функцию `plot_model`:

```python
import pandas as pd
from pycaret.regression import setup, compare_models, plot_model

df = pd.read_csv('data.csv', sep=';')
setup(df, target='price')
best = compare_models()

# Визуализируем важность признаков
plot_model(best, plot="feature")
```

### 10. Какая классификационная модель лучше? Модель A с Accuracy = 0.85 или модель B с Accuracy = 0.89?

Модель B лучше, потому что большая Accuracy означает более высокую точность классификации.

### 11. Какой регрессионный модель лучше? Модель A с RMSE = 4.5 или модель B с RMSE = 3.2?

Модель B лучше, потому что меньший RMSE означает меньший квадратный корень из среднеквадратичной ошибки.

### 12. Как визуализировать классификационную модель в PyCaret?

Для визуализации модели используйте функцию `plot_model`:

```python
import pandas as pd
from pycaret.classification import setup, compare_models, plot_model

df = pd.read_csv('data.csv', sep=';')
setup(df, target='sentiment')
best = compare_models()

# Визуализируем модель
plot_model(best, plot="confusion_matrix")
```

### 13. Какая классификационная модель лучше? Модель A с F1 = 0.82 или модель B с F1 = 0.76?

Модель A лучше, потому что больший F1-score означает лучший баланс между Precision и Recall.

### 14. Как сделать предсказание в PyCaret для регрессионной модели?

Чтобы сделать предсказание, используйте функцию `predict_model`:

```python
import pandas as pd
from pycaret.regression import load_model, predict_model

model = load_model('regression_pipeline')
predict_df = pd.read_csv('predict_data.csv', sep=';')

# Делаем предсказание
predictions = predict_model(model, data=predict_df)
```

### 15. Какой регрессионный модель лучше? Модель A с MAE = 5.3 или модель B с MAE = 3.1?

Модель B лучше, потому что меньший MAE означает меньшую среднюю абсолютную ошибку.

### 16. Какого типа модель используешь для: Прогнозирование отказов машин в промышленности?

Модель из семейства **data-to-category** (классификатор), например, собственноручно обученная модель.

### 17. Какого типа модель используешь для: Автоматическая расшифровка интервью для журналистов?

Модель из семейства **speech-to-text** (распознавание речи), например, **whisper-1**.

### 18. Какого типа модель используешь для: Сегментация рынка в недвижимости?

Модель из семейства **data-to-cluster** (кластеризация), например, собственноручно обученная кластерная модель.

### 19. Какого типа модель используешь для: Поиск групп генов в генетических исследованиях?

Модель из семейства **data-to-cluster** (кластеризация), например, собственноручно обученная кластерная модель.

### 20. Какого типа модель используешь для: Классификация заявок на гранты?

Модель из семейства **data-to-category** (классификатор), например, собственноручно обученная модель.

### 21. Какого типа модель используешь для: Оценка сложности образовательного контента?

Модель из семейства **text-to-category** (отнесение текста к категории), например, **gpt-4o** или **gpt-4o-mini**.

### 22. Какого типа модель используешь для: Классификация типа преступлений на основе криминальных данных?

Модель из семейства **data-to-category** (классификатор), например, собственноручно обученная модель.

### 23. Какого типа модель используешь для: Автоматическая генерация блоговых статей?

Модель из семейства **text-to-text** (генерация текста), например, **gpt-4o** или **gpt-4o-mini**.

### 24. Какого типа модель используешь для: Поиск групп в демографических данных городов?

Модель из семейства **data-to-cluster** (кластеризация), например, собственноручно обученная модель.

### 25. Какого типа модель используешь для: Генерация эмбеддингов для описаний изображений и видео?

Модель из семейства **text-to-embeddings** (векторизация текста), например, **text-embedding-3-small** или **text-embedding-3-large**.

### 26. Какого типа модель используешь для: Сегментация пользователей по содержанию сообщений?

Модель из семейства **text-to-category** (отнесение текста к категории), например, **gpt-4o** или **gpt-4o-mini**.

### 27. Какого типа модель используешь для: Автоматическое сокращение текста до ключевых пунктов?

Модель из семейства **text-to-text** (генерация текста), например, **gpt-4o** или **gpt-4o-mini**.

### 28. Какого типа модель используешь для: Семантический поиск по заметкам?

Модель из семейства **text-to-embeddings** (векторизация текста), например, **text-embedding-3-small** или **text-embedding-3-large**.

### 29. Какого типа модель используешь для: Поиск групп пациентов в медицинском анализе?

Модель из семейства **data-to-cluster** (кластеризация), например, собственноручно обученная модель.

### 30. Какого типа модель используешь для: Озвучка для обучающих видео и онлайн-курсов?

Модель из семейства **text-to-speech** (озвучка текста), например, **tts-1**.

### 31. Какого типа модель используешь для: Распознавание дорожных знаков для автономных систем?

Модель из семейства **image-to-json** (анализ изображения в структуру JSON), например, **gpt-4o** или **gpt-4o-mini**.

### 32. Какого типа модель используешь для: Прогнозирование зарплат на рынке труда?

Модель из семейства **data-to-cluster** (регрессия, прогнозирование), например, собственноручно обученная модель.

### 33. Какого типа модель используешь для: Автоматическое структурирование отзывов на продукты?

Модель из семейства **text-to-json** (структурирование текста в JSON), например, **gpt-4o** или **gpt-4o-mini**.

### 34. Какого типа модель используешь для: Генерация обложек музыкальных альбомов?

Модель из семейства **text-to-image** (генерация изображения по описанию), например, **dall-e-2** или **dall-e-3**.

### 35. Какого типа модель используешь для: Преобразование спецификаций продуктов в JSON?

Модель из семейства **text-to-json** (структурирование текста в JSON), например, **gpt-4o** или **gpt-4o-mini**.

### 36. Какого типа модель используешь для: Генерация описаний к фотографиям в приложениях знакомств?

Модель из семейства **image-to-text** (описание изображения), например, **gpt-4o** или **gpt-4o-mini**.

### 37. Какого типа модель используешь для: Автоматическое создание базы научной литературы?

Модель из семейства **text-to-json** (структурирование текста в JSON), например, **gpt-4o** или **gpt-4o-mini**.

### 38. Какого типа модель используешь для: Аудиокниги для детей?

Модель из семейства **text-to-speech** (озвучка текста), например, **tts-1**.

### 39. Какого типа модель используешь для: Генерация субтитров для фильмов и видео?

Модель из семейства **speech-to-text** (распознавание речи), например, **whisper-1**.

---

## Модуль 9

### 1. Какая функция используется для валидации DataFrame в Pandera?

Для валидации DataFrame в Pandera используется метод `validate`. Он проверяет, соответствуют ли данные в DataFrame правилам валидации, определённым в схеме.

```python
import pandera as pa

schema = pa.DataFrameSchema({
    "age": pa.Column(pa.Int)
})

df = pd.DataFrame({
    "age": [25, 30, 35]
})

schema.validate(df)
```

### 2. Что происходит, если данные не соответствуют правилам валидации в Pandera?

Если данные не соответствуют правилам валидации, метод `validate` выбрасывает исключение `SchemaError`. Исключение содержит информацию о причинах ошибки (например, отсутствующие значения, несоответствие типов и др.).

### 3. Что такое Pandera?

**Pandera** — это библиотека Python для валидации данных простым и декларативным способом. Позволяет определить правила валидации, которые автоматически проверяются при обработке данных.

### 4. Как получить DataFrame с ошибками валидации в Pandera?

Для получения DataFrame с ошибками валидации используйте метод `validate` с параметром `lazy=True`. В этом случае Pandera вернёт все ошибки одним списком.

```python
import pandera as pa

schema = pa.DataFrameSchema({
    "age": pa.Column(pa.Int)
})

df = pd.DataFrame({
    "age": ["25", "30", "35"]
})

try:
    schema.validate(df, lazy=True)
except pa.errors.SchemaErrors as err:
    errors_df = err.failure_cases
    print(errors_df)
```

### 5. Какова роль параметра lazy в методе validate в Pandera?

Параметр `lazy` определяет поведение валидации:
- `lazy=False` (по умолчанию): валидация останавливается на первой ошибке и выбрасывает исключение.
- `lazy=True`: валидация проверяет все данные и возвращает сразу все ошибки.

### 6. Каковы преимущества валидации данных?

Валидация данных даёт целый ряд преимуществ:
- Повышение точности моделей: исключает некорректные или неполные данные.
- Гарантия согласованности: данные соответствуют нужным форматам и правилам.
- Защита от ошибок: раннее обнаружение ошибок (например, пропусков, аномалий, неправильных типов).
- Повышение доверия к результатам: валидированные данные более надёжны.
- Экономия времени и ресурсов: исправление ошибок на ранних этапах снижает затраты, связанные с их устранением позже.

### 7. Как убедиться, что столбец содержит целые числа в Pandera?

Определите схему со столбцом типа `pa.Int`:

```python
import pandera as pa

schema = pa.DataFrameSchema({
    "age": pa.Column(pa.Int)  # Проверка на целочисленный столбец
})
```

### 8. Как убедиться, что столбец является целым числом и приводится из другого типа в Pandera?

Используйте параметр `coerce=True` для автоматического приведения типов:

```python
import pandera as pa

schema = pa.DataFrameSchema(
    columns={
        "person_id": pa.Column(pa.Int),
        "height_in_cm": pa.Column(pa.Int, pa.Check.greater_than(0), coerce=True),  # <-- coerce=True
        "age_category": pa.Column(pa.Str)
    }
)

people_df = pd.DataFrame({
    "person_id": [1, 2, 3, 4, 5, 6],
    "height_in_cm": ["182", "185", "160", "155", "190", "190"],
    "age_category": ["20-30", "10-20", "10-20", "20-30", "10-20", "10-20"]
})

try:
    validated_df = schema.validate(people_df)
except pa.errors.SchemaErrors as e:
    display(e.failure_cases)
    raise
```

### 9. Как убедиться, что столбец содержит только значения из определённого множества в Pandera?

Используйте `check=pa.Check.isin([...])`:

```python
import pandera as pa

schema = pa.DataFrameSchema({
    "currency": pa.Column(pa.Str, check=pa.Check.isin(["USD", "EUR", "GBP"]))
})
```

### 10. Как убедиться, что значения столбца имеют заданную длину в Pandera?

Используйте `pa.Check.str_length`:

```python
import pandera as pa

schema = pa.DataFrameSchema({
    "username": pa.Column(pa.Str, check=pa.Check.str_length(8))
})
```

### 11. Каковы риски отсутствия валидации данных?

Отсутствие валидации может привести к:
- Тихим ошибкам, которые ухудшают качество данных и моделей
- Сбоям в работе системы (crash)
- Распространению ошибок по всей цепочке обработки и анализа данных

### 12. Как убедиться, что столбец соответствует определённому формату в Pandera?

Используйте `pa.Check.str_matches` с регулярным выражением:

```python
import pandera as pa

schema = pa.DataFrameSchema({
    "email": pa.Column(pa.Str, check=pa.Check.str_matches(r"^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$"))
})
```

### 13. Как разрешить значения null в столбце Pandera?

Используйте параметр `nullable=True`:

```python
import pandera as pa

schema = pa.DataFrameSchema({
    "age": pa.Column(pa.Int, nullable=True)
})
```

### 14. В чём разница между этими двумя способами валидации данных в Pandera?

```python
schema.validate(df)
```
и
```python
schema.validate(df, lazy=True)
```

- `schema.validate(df)`: проверка останавливается на первой ошибке (вызывает SchemaError).
- `schema.validate(df, lazy=True)`: проверка продолжается до конца и возвращает все ошибки сразу (вызывает SchemaErrors).

### 15. Что такое целостность данных?

Целостность данных — это свойство данных, гарантирующее их согласованность и точность.  
Данные соответствуют нужным форматам, правилам и не содержат противоречий и ошибок.

### 16. Какие существуют способы валидации данных?

- Валидация типа (например, число, строка, дата)
- Валидация диапазона значений (например, возраст в диапазоне 18-65)
- Валидация формата (например, email)

В целом, это процесс проверки данных на соответствие заданным условиям.

### 17. Как убедиться, что столбец содержит значения из заданного диапазона в Pandera?

Используйте `pa.Check.range(min, max)`:

```python
import pandera as pa

schema = pa.DataFrameSchema({
    "age": pa.Column(pa.Int, pa.Check.range(18, 65))
})
```

### 18. Как убедиться, что значения столбца состоят из двух частей, разделённых определённым символом, в Pandera?

Используйте `pa.Check.str_matches` с нужным регулярным выражением:

```python
import pandera as pa

schema = pa.DataFrameSchema({
    "name": pa.Column(pa.Str, check=pa.Check.str_matches(r"^\w+\s\w+$"))
})
```

### 19. Что такое схема (schema) в Pandera?

Схема — это набор правил валидации, описывающих ожидаемый формат и структуру данных (типы, диапазоны, обязательные поля и т.д.).

### 20. Что возвращает метод валидации в Pandera?

Метод валидации возвращает новый объект DataFrame с данными, прошедшими проверку:

```python
import pandera as pa

schema = pa.DataFrameSchema(
    columns={
        "person_id": pa.Column(pa.Int),
        "height_in_cm": pa.Column(pa.Int, pa.Check.greater_than(0)),
        "age_category": pa.Column(pa.Str)
    }
)

people_df = pd.DataFrame({
    "person_id": [1, 2, 3, 4, 5, 6],
    "height_in_cm": ["182", "185", "160", "155", "190", "190"],
    "age_category": ["20-30", "10-20", "10-20", "20-30", "10-20", "10-20"]
})

try:
    validated_df = schema.validate(people_df)
except pa.errors.SchemaErrors as e:
    display(e.failure_cases)
    raise
```

### 21. Что такое анонимизация данных?

Анонимизация данных — это процесс удаления или изменения идентифицирующей информации для защиты приватности лиц, к которым относятся данные. Цель анонимизации — сделать так, чтобы данные нельзя было связать с конкретным человеком, что минимизирует риск нарушения приватности.

### 22. Зачем мы хотим анонимизировать данные?

Анонимизация позволяет использовать данные шире, сохраняя приватность людей. Это даёт возможность обмениваться данными с другими организациями или публиковать их без риска нарушения приватности. Это также снижает вероятность того, что модель случайно вернёт личные данные, на которых обучалась. Если данные будут украдены, анонимизация уменьшает риск их использования в преступных целях.

### 23. Какие существуют методы анонимизации данных?

- **Маскирование данных** — частичное скрытие идентифицирующей информации (например, замена цифр в номере карты на звёздочки).
- **Псевдонимизация** — замена идентифицирующей информации уникальными идентификаторами.
- **Рандомизация данных** — замена значений случайными, что делает идентификацию невозможной.
- **Генерализация данных** — замена точных значений более общими (например, возраст на возрастной диапазон).
- **Удаление данных** — полное удаление идентифицирующих данных из набора.
- **Шум (пертурбация)** — добавление случайного шума к значениям (например, добавление случайного значения к возрасту или балансу).
- **Генерация синтетических данных** — создание новых данных, похожих на исходные, но не связанных с реальными людьми.

### 24. Почему анонимизация данных важна?

- **Соответствие закону** — многие законы (например, GDPR) требуют защиты персональных данных.
- **Защита приватности** — гарантирует, что данные не могут быть использованы для идентификации.
- **Доверие пользователей** — организации, которые заботятся о приватности, вызывают больше доверия.
- **Безопасность** — снижает риск злоупотребления украденными данными.

### 25. Когда применяется маскирование в анонимизации?

Маскирование применяется, когда нужно сохранить структуру данных, но скрыть часть информации. Примеры:
- Скрытие номеров карт в финансовых документах
- Скрытие номеров PESEL в медицинских документах
- Скрытие e-mail в базах данных

### 26. Когда применяется рандомизация в анонимизации?

Рандомизация используется, чтобы затруднить идентификацию, но сохранить структуру данных. Обычно применяется к колонкам, не важным для анализа, но потенциально идентифицирующим:
- Замена имён и фамилий случайными
- Замена email на случайные адреса
- Замена телефонов на случайные номера

### 27. Когда применяется псевдонимизация в анонимизации?

Псевдонимизация используется, когда нужно однозначно идентифицировать записи, но при этом защитить приватность. Примеры:
- Замена имени и фамилии уникальным идентификатором
- Замена номера PESEL идентификатором в медицине
- Замена номера клиента уникальным идентификатором

Ключ для идентификации хранится отдельно, что при необходимости позволяет восстановить исходные данные.

### 28. Какие есть сложности и вызовы у анонимизации данных?

- Сохранение полезности данных: чем сильнее анонимизация, тем меньше ценность данных
- Потеря качества: агрегация может ухудшить точность
- Риск повторной идентификации: даже после анонимизации, при объединении с другими источниками возможна повторная идентификация
- Изменчивые стандарты и законы: отсутствие единых стандартов и меняющиеся требования
- Техническая сложность: разнородность, сложная структура, большие объёмы данных

### 29. Как сгенерировать синтетические данные?

Для простых случаев можно использовать библиотеку Faker и написать скрипт на Python. Для более сложных данных — использовать модели искусственного интеллекта. Есть компании, которые специализируются на генерации синтетических данных и иногда публикуют их.

### 30. Каковы преимущества анонимизации через генерацию синтетических данных?

Генерация синтетических данных позволяет сохранить структуру и характеристики исходных данных, обеспечивая при этом приватность. Такие данные похожи на оригинальные, но не позволяют идентифицировать людей. Однако важно следить за качеством синтетических данных и корректно их обновлять.

### 31. Когда применяется удаление данных в анонимизации?

Удаление применяется, когда идентифицирующие данные не нужны для анализа. Примеры:
- Удаление PESEL из документов, если не требуется идентификация
- Удаление email из баз, если они не нужны для связи
- Удаление телефонов, если не требуется контакт с клиентами

### 32. Когда применяется генерализация в анонимизации?

Генерализация применяется, когда нужно сохранить общую информацию, скрыв детали. Примеры:
- Замена точного возраста на диапазоны
- Замена дохода на диапазоны
- Замена адреса на общую локацию

Для числовых данных можно использовать интервалы, чтобы затруднить идентификацию, но сохранить полезность.

### 33. Лучшие практики анонимизации данных

- Определить цели анонимизации — зачем и для кого она проводится
- Использовать разные методы с учётом типа данных и задач
- Следить за полезностью данных — чтобы они оставались пригодными для анализа после анонимизации
- Мониторить и оценивать эффективность — проверять, действительно ли анонимизация защищает приватность

### 34. Какие бывают типы облачных сервисов?

К облачным сервисам относятся, в частности:

- **Infrastructure as a Service (IaaS)** — предоставление ИТ-инфраструктуры (серверы, сети, хранилище). Пример: DigitalOcean Droplets.
- **Platform as a Service (PaaS)** — предоставление платформы для разработки, тестирования и развертывания приложений. Пример: DigitalOcean App Platform.
- **Software as a Service (SaaS)** — предоставление программного обеспечения как сервиса, доступного через браузер. Пример: Anaconda Cloud.

### 35. Что такое S3 в контексте облачного хранения данных?

**S3** (Simple Storage Service) — это облачный сервис хранения данных от Amazon Web Services (AWS). Он стал стандартом в индустрии хранения, а протокол S3 используют и другие облачные сервисы (например, DigitalOcean Spaces, Google Cloud Storage).

### 36. Что такое bucket в облачном хранении данных?

**Bucket** в облачном хранилище — это контейнер, в котором хранятся файлы и папки. Можно думать о нем как о главной папке для хранения всех данных, непосредственно или во вложенных папках.

### 37. Как выглядит адрес файла в DigitalOcean Spaces?

Структура адреса файла:

```
s3://<bucket-name>/<file-path-1>/<file-path-2>/<file-name>
```

- `<bucket-name>` — имя bucket'а DigitalOcean Spaces
- `<file-path-1>`, `<file-path-2>` — путь к файлу внутри bucket'а (опционально)
- `<file-name>` — имя файла

В начале присутствует протокол `s3://`, что означает использование протокола S3 (Simple Storage Service).

### 38. Какое основное преимущество DigitalOcean в сравнении с другими облачными провайдерами?

Главное преимущество DigitalOcean — простота и интуитивность платформы.  
DigitalOcean предлагает удобный интерфейс, прозрачные цены и быстрое развертывание сервисов.  
Для начинающих пользователей DigitalOcean часто более доступен и дружелюбен, чем AWS, Google Cloud или Azure, хотя у них шире функционал.

### 39. Как использовать Boto3 для работы с DigitalOcean Spaces?

Для работы с DigitalOcean Spaces настройте клиента Boto3 с нужными данными доступа:

```python
import boto3

# Настройка клиента Boto3 для DigitalOcean Spaces
s3 = boto3.client('s3',
    endpoint_url='https://nyc3.digitaloceanspaces.com',
    aws_access_key_id='ACCESS_KEY',
    aws_secret_access_key='SECRET_KEY'
)

# Вывод всех объектов в бакете
response = s3.list_objects_v2(Bucket='my-bucket')
for obj in response.get('Contents', []):
    print(obj['Key'])
```

### 40. Как настроить переменные доступа к API OpenAI в DigitalOcean App Platform?

Для этого рекомендуется использовать переменные окружения.

### 41. Как загрузить файл из DigitalOcean Spaces в Pandas DataFrame?

Используйте функцию `read_csv` с соответствующим URL (и установленными pandas + s3fs):

```python
import pandas as pd

url = 's3://my-bucket/data.csv'
df = pd.read_csv(url)
```

Не забудьте:
- Установить библиотеки `pandas` и `s3fs`
- Настроить переменные окружения `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, и (для DigitalOcean Spaces) `AWS_ENDPOINT_URL_S3`.

### 42. Какова польза правильного партиционирования данных в облачном хранилище?

Партиционирование данных повышает эффективность управления, поиска и обработки данных.  
Стоит ориентироваться на особенности данных (например, по дате или региону):

Пример по датам:
- my-bucket/rok=2022/miesiac=01/dzien=01/data.csv
- my-bucket/rok=2022/miesiac=01/dzien=02/data.csv

Пример по регионам:
- my-bucket/country=PL/company=YYY/20210101.csv
- my-bucket/country=DE/company=YYY/20210101.csv

### 43. Как настроить DigitalOcean App для запуска приложения Streamlit?

- Создать файл `app.py` с кодом Streamlit
- Создать `requirements.txt` с необходимыми библиотеками
- В DigitalOcean App Platform выбрать "Create App" и указать исходный код с GitHub
- Указать репозиторий с приложением Streamlit
- Проверить, что Resource Type — Web Service, Python
- Run Command: `streamlit run app.py`
- Port: 8501

### 44. Что такое файл requirements.txt?

Это текстовый файл со списком зависимостей Python-приложения.

### 45. Что такое облако (cloud computing)?

- Это модель предоставления ИТ-услуг через интернет.
- Облачные сервисы позволяют пользоваться ресурсами (серверы, БД, сети, ПО, хранилище) без собственной инфраструктуры.
- Провайдер управляет инфраструктурой, обеспечивая масштабируемость, гибкость и безопасность.

### 46. Что такое Boto3?

**Boto3** — официальный Python SDK для работы с Amazon Web Services (AWS), стандартно используется для работы с cloud storage.

### 47. Что такое облачное хранение данных (cloud storage)?

Это сервис хранения данных на удалённых серверах с доступом через интернет.  
Примеры: Amazon S3, Google Cloud Storage, Azure Blob, DigitalOcean Spaces.  
Это виртуальный диск для хранения, обмена и управления данными.

### 48. Что такое развертывание в облаке (cloud deployment)?

Cloud deployment — процесс размещения приложений, сервисов или моделей в облаке, что обеспечивает доступ по интернету, масштабируемость, гибкость и снижение затрат на инфраструктуру.

### 49. Какой сервис использовать для развертывания приложения в DigitalOcean?

**DigitalOcean App Platform** — это платформа для развертывания, масштабирования и управления приложениями в облаке.

### 50. Какие преимущества у DigitalOcean App Platform по сравнению со Streamlit Community Cloud?

Больше контроля над средой, конфигурацией и ресурсами, хостинг БД, облачного хранилища, виртуальных машин и других сервисов — всё в одном месте.

### 51. Какова роль endpoint_url при доступе к DigitalOcean Spaces?

`endpoint_url` указывает на адрес сервера для подключения.  
Для DigitalOcean Spaces указывается свой endpoint, например:

```
https://fra1.digitaloceanspaces.com
```

В Boto3:
```python
import boto3

s3 = boto3.client(
    "s3",
    aws_access_key_id="ВАШ_ACCESS_KEY",
    aws_secret_access_key="ВАШ_SECRET_KEY",
    endpoint_url="https://fra1.digitaloceanspaces.com",
)
```

### 52. Какие есть дополнительные техники работы с пропущенными данными?

- **Импутация данных** — замена пропусков средним, медианой или наиболее частым значением.
- **Заполнение на основе других колонок** — в отдельных случаях можно восстановить пропуски, используя данные из других столбцов.
- **Удаление строк или столбцов с пропущенными значениями** — если в строке или столбце слишком много пропусков, и их нельзя корректно восстановить, их можно удалить.
- **Использование ML-моделей для предсказания пропусков** — можно обучать модели, чтобы заполнять пропущенные значения по другим признакам.

### 53. Как удалить целые столбцы с пропущенными данными в Pandas?

Используйте `dropna(axis=1)`:

```python
import pandas as pd

df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [None, None, None]
})

df = df.dropna(axis=1)
```

### 54. Как удалить строки с пропущенными данными сверх заданного порога в Pandas?

Используйте `dropna(thresh=...)`:

```python
import pandas as pd

df = pd.DataFrame({
    'A': [1, 2, None, 4],
    'B': [3, 4, None, 6],
    'C': [5, None, None, None]
})

df = df.dropna(thresh=2)
# thresh=2 — в строке должно быть минимум 2 непустых значения, иначе строка удаляется
```

### 55. Какое преимущество у forward filling для пропущенных данных?

Forward filling позволяет сохранять непрерывность данных во времени: пропуски заменяются предыдущим известным значением. Особенно полезно для временных рядов.

### 56. Какую технику можно применить к категориальным данным с пропусками?

Для категориальных данных часто используют импутацию наиболее частым значением (mode).

### 57. Какую технику можно применить к логическим (boolean) данным с пропусками?

Для логических данных также часто используют импутацию наиболее частым значением (mode).

### 58. Что такое forward filling в Pandas?

Forward filling — это заполнение пропусков предыдущим значением:

```python
import pandas as pd

df = pd.DataFrame({
    'date': ['2022-01-01', '2022-01-02', '2022-01-03'],
    'price': [100, None, 120]
})

df['price'] = df['price'].fillna(method='ffill')
```

Результат:
```
date        price
2022-01-01  100.0
2022-01-02  100.0
2022-01-03  120.0
```

### 59. Что такое интерполяция в Pandas?

Интерполяция — это заполнение пропусков оценочным значением на основе имеющихся данных:

```python
import pandas as pd

df = pd.DataFrame({
    'date': ['2022-01-01', '2022-01-02', '2022-01-03'],
    'price': [100, None, 120]
})

df['price'] = df['price'].interpolate()
```

Результат:
```
date        price
2022-01-01  100.0
2022-01-02  110.0
2022-01-03  120.0
```

Есть разные методы интерполяции: linear, quadratic, cubic и др. По умолчанию — linear.

### 60. Какую технику можно применить к числовым данным с пропусками?

Для числовых данных часто используют импутацию средним (mean) или медианой (median). Можно также применять интерполяцию, forward filling или backward filling — выбор зависит от характера данных.

### 61. Что такое backward filling в Pandas?

Backward filling — это заполнение пропусков следующим известным значением:

```python
import pandas as pd

df = pd.DataFrame({
    'date': ['2022-01-01', '2022-01-02', '2022-01-03'],
    'price': [100, None, 120]
})

df['price'] = df['price'].fillna(method='bfill')
```

Результат:
```
date        price
2022-01-01  100.0
2022-01-02  120.0
2022-01-03  120.0
```

### 62. В чём разница между линейной и квадратичной интерполяцией?

- **Линейная интерполяция:** значения между известными точками изменяются равномерно (по прямой).
- **Квадратичная интерполяция:** значения изменяются по параболе, что позволяет учитывать нелинейные изменения, но требует больше вычислений.

### 63. Почему важно сортировать данные перед интерполяцией?

Интерполяция в Pandas работает по порядку данных. Для корректных результатов перед интерполяцией данные должны быть отсортированы по нужной колонке (например, по времени). Несортированные данные могут привести к некорректной интерполяции.

### 64. Какую технику можно использовать для временных рядов с пропусками?

Для временных рядов часто используют интерполяцию (оценку значения по тренду), а также forward или backward filling (заполнение предыдущим/следующим значением).

### 65. Как применить PCA в PyCaret?

Чтобы применить PCA в PyCaret, используйте аргумент `pca` в функции `setup`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)

# Применение PCA с 2 компонентами
exp = setup(data=wine_df, target='type', pca=True, pca_components=2)

# Можно сравнить исходные данные и преобразованные
exp.dataset
exp.dataset_transformed
```

### 66. Что такое One Hot Encoding и как его применить в PyCaret?

One Hot Encoding — это техника кодирования категориальных переменных, при которой каждая уникальная категория превращается в отдельную бинарную переменную (1 — присутствует, 0 — отсутствует).

В PyCaret One Hot Encoding можно включить через аргумент `categorical_features` в функции `setup`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

employee_df = get_data('employee', verbose=False)

exp = setup(
    data=employee_df,
    target='left',
    categorical_features=['department'],
)

exp.dataset
exp.dataset_transformed
```

### 67. Как указать PyCaret, что переменная — текстовая?

Передайте имя текстовой переменной через аргумент `text_features` в функции `setup`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data
from faker import Faker

employee_df = get_data('employee', verbose=False)
fake = Faker()
employee_df['name'] = [fake.name() for _ in range(len(employee_df))]

exp = setup(
    data=employee_df,
    target='left',
    text_features=['name'],
)

exp.dataset
exp.dataset_transformed
```

### 68. Как указать PyCaret, что переменная — категориальная?

Передайте имя переменной через аргумент `categorical_features`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

employee_df = get_data('employee', verbose=False)

exp = setup(
    data=employee_df,
    target='left',
    categorical_features=['department'],
)

exp.dataset
exp.dataset_transformed
```

### 69. Как указать PyCaret, что переменная — числовая?

Передайте имя переменной через аргумент `numeric_features`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

employee_df = get_data('employee', verbose=False)

exp = setup(
    data=employee_df,
    target='left',
    numeric_features=['last_evaluation'],
)

exp.dataset
exp.dataset_transformed
```

### 70. Как управлять количеством фолдов при кросс-валидации в PyCaret?

Используйте аргумент `fold` в соответствующих функциях:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)
exp = setup(data=wine_df, target='type')

best_model = exp.compare_models(fold=5)
rf_model = exp.create_model('rf', fold=5)
tuned_model = exp.tune_model(rf_model, fold=5)
```

### 71. Как провести настройку гиперпараметров в PyCaret?

Используйте функцию `tune_model`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)
exp = setup(data=wine_df, target='type')

rf_model = exp.create_model('rf')
tuned_rf_model = exp.tune_model(rf_model, optimize='F1')
```

### 72. Как вернуть оригинальную модель, если после тюнинга результат хуже в PyCaret?

Используйте аргумент `choose_better=True` в функции `tune_model`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)
exp = setup(data=wine_df, target='type')

rf_model = exp.create_model('rf')
tuned_rf_model = exp.tune_model(rf_model, optimize='F1', choose_better=True)
```

### 73. Как сравнить между собой модели после тюнинга в PyCaret?

Можно использовать функцию `compare_models`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)
exp = setup(data=wine_df, target='type')

best_models = exp.compare_models(sort='F1', n_select=3)
tuned_best_models = [exp.tune_model(m, optimize='F1') for m in best_models]
best_model = exp.compare_models(best_models + tuned_best_models, sort='F1')
```

### 74. Что такое PCA и для чего оно нужно?

**PCA (Principal Component Analysis)** — это метод уменьшения размерности данных. Он преобразует исходные переменные в новые, называемые компонентами, которые сохраняют максимум информации.  
PCA позволяет уменьшить число переменных, сохраняя как можно больше информации из исходных данных.

### 75. Зачем кодировать категориальные переменные?

Модели машинного обучения требуют числовых данных.  
Категориальные переменные нужно преобразовывать в числа (например, One-Hot Encoding), чтобы не терять информацию и позволить моделям обучаться на этих данных.

### 76. Как указать PyCaret, что переменная — это дата?

Используйте аргумент `date_features`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data
import pandas as pd
from faker import Faker

employee_df = get_data('employee', verbose=False)
fake = Faker()
employee_df['join_date'] = pd.to_datetime([fake.date_between(start_date='-10y', end_date='today') for _ in range(len(employee_df))])

exp = setup(
    data=employee_df,
    target='left',
    date_features=['join_date'],
)

exp.dataset
exp.dataset_transformed
```

### 77. Как решить проблему дисбаланса классов в PyCaret?

Используйте аргумент `fix_imbalance` в `setup`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)
exp = setup(data=wine_df, target='type', fix_imbalance=True)

exp.dataset["type"].value_counts(normalize=True)
exp.dataset_transformed["type"].value_counts(normalize=True)
```

### 78. Как протестировать модель на holdout dataset в PyCaret?

Используйте функцию `predict_model`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)
exp = setup(data=wine_df, target='type')

best_model = exp.compare_models()

predictions = exp.predict_model(best_model)
```

### 79. Как игнорировать определённые признаки в PyCaret?

Передайте их список в аргумент `ignore_features`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)
exp = setup(data=wine_df, target='type', ignore_features=['alcohol', 'residual sugar'])

exp.dataset
exp.dataset_transformed
```

### 80. Как масштабировать данные в PyCaret?

Используйте аргументы `normalize` и `normalize_method`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)

exp = setup(
    data=wine_df,
    target='type',
    normalize=True,
    normalize_method='zscore',
)

exp.dataset
exp.dataset_transformed
```

### 81. Как сделать данные более "нормальными" в PyCaret?

Используйте аргумент `transformation`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)
exp = setup(
    data=wine_df,
    target='type',
    transformation=True,
    transformation_method='yeo-johnson',
)

exp.dataset
exp.dataset_transformed
```

### 82. Что такое настройка гиперпараметров в машинном обучении?

Это процесс оптимизации параметров модели, которые не обучаются во время тренировки, а задаются заранее. Подбор оптимальных значений увеличивает эффективность модели.

### 83. Почему важно удалить выбросы перед обучением модели?

Выбросы могут ухудшать качество модели, делать результаты ошибочными, приводить к переобучению или недообучению.  
Удаление выбросов делает модель более стабильной и точной.

### 84. Как автоматически выбрать признаки в PyCaret?

Передайте аргумент `feature_selection=True` и укажите долю признаков в `n_features_to_select`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)
wine_df.columns = [col.replace(" ", "_") for col in wine_df.columns]

exp = setup(data=wine_df, target='type', feature_selection=True, n_features_to_select=0.6)

exp.dataset
exp.dataset_transformed
```

### 85. Что такое эксперимент в MlFlow?

Эксперимент в MlFlow — это набор запусков (run-ов), связанных с определённой задачей машинного обучения.

У каждого эксперимента есть уникальный идентификатор, имя и описание, что позволяет отслеживать и сравнивать результаты моделей.

### 86. Что такое модель в MlFlow?

Модель в MlFlow — это сериализованная модель машинного обучения, сохранённая в формате MlFlow.

Модель содержит информацию о метриках, параметрах и артефактах.

Её можно загружать и использовать в других приложениях, средах или сервисах.

Также модель можно зарегистрировать в MlFlow Model Registry для управления версиями и обмена с другими пользователями.

### 87. Как использовать MlFlow в PyCaret?

Чтобы использовать MlFlow в PyCaret, укажите аргумент `log_experiment` в функции `setup`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data
import mlflow

wine_df = get_data('wine', verbose=False)

mlflow.set_tracking_uri("http://localhost:5000")

exp = setup(
    data=wine_df,
    target='type',
    log_experiment=True,
    log_plots=True,
    experiment_name='wine_classification',
    experiment_custom_tags={'author': 'Maciej Sobczak', 'data': 'wine'},
)
best_model = exp.compare_models()
```

### 88. Как добавить собственную модель в PyCaret?

Чтобы добавить свою модель в PyCaret, используйте функцию `create_model`:

```python
from pycaret.regression import setup
from pycaret.datasets import get_data
from gplearn.genetic import SymbolicRegressor

insurance_df = get_data('insurance', verbose=False)
exp = setup(data=insurance_df, target='charges')

sc = SymbolicRegressor()
best_model = exp.compare_models(include=[sc, "gbr", "ada"])
```

### 89. Как и для чего PyCaret использует Scikit-learn?

PyCaret использует Scikit-learn как основную библиотеку для машинного обучения, предоставляющую реализации алгоритмов, метрики и инструменты для обработки данных.

С помощью Scikit-learn в PyCaret выполняется обучение моделей, оценка их качества, настройка гиперпараметров и трансформация данных (кодирование признаков и др.).

### 90. Как добавить метрику в PyCaret?

Для добавления метрики используйте функцию `add_metric`:

```python
import numpy as np
from pycaret.classification import setup
from pycaret.datasets import get_data

def heavily_penalized_false_negatives(y_true, y_pred, **kwargs):
    penalty_weight = 10
    TP = np.sum((y_true == 1) & (y_pred == 1))
    FN = np.sum((y_true == 1) & (y_pred == 0))
    if (TP + FN) == 0:
        return 0
    return TP / (TP + FN * penalty_weight)

employee_df = get_data('employee', verbose=False)
exp = setup(data=employee_df, target='left')
exp.add_metric(
    id='heavily_penalized_false_negatives',
    name='Heavily Penalized False Negatives',
    score_func=heavily_penalized_false_negatives,
    greater_is_better=True,
)
exp.compare_models(sort='heavily_penalized_false_negatives')
```

### 91. Что такое run в MlFlow?

Run в MlFlow — это отдельный запуск задачи машинного обучения, связанный с экспериментом.

Каждый run содержит информацию о метриках, параметрах, артефактах и коде, использованном для запуска.

### 92. Для чего нужны теги в MlFlow?

Теги в MlFlow — это метки, которые можно присваивать run-ам, экспериментам и моделям для категоризации, группировки и фильтрации.

Теги могут содержать информацию об окружении, авторе, источнике данных или других метаданных.

### 93. Как показать доступные модели в PyCaret?

Чтобы отобразить доступные модели в PyCaret, используйте функцию `models()`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

employee_df = get_data('employee', verbose=False)
exp = setup(data=employee_df, target='left')
exp.models()
```

### 94. Что такое метрики в MlFlow?

Метрики в MlFlow — это числовые значения, связанные с run-ом, описывающие качество модели или результаты задачи.

Метрики могут включать точность, precision, recall, F1-score и другие показатели оценки модели.

### 95. Как удалить метрику из PyCaret?

Для удаления метрики используйте функцию `remove_metric`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

employee_df = get_data('employee', verbose=False)
exp = setup(data=employee_df, target='left')
exp.remove_metric('f1')
exp.compare_models()
```

### 96. Как запустить локально сервер MlFlow?

Откройте терминал и выполните команду:

```
mlflow ui
```

### 97. Что такое MlFlow?

MlFlow — это open-source платформа для управления жизненным циклом моделей машинного обучения.

Позволяет отслеживать эксперименты, управлять метриками, параметрами, артефактами и моделями.

Обеспечивает автоматизацию обучения, мониторинг качества и развертывание моделей.

Состоит из компонентов: Tracking, Models Registry, UI и др.

### 98. В чем разница между экспериментом в PyCaret и экспериментом в MlFlow?

Эксперимент в PyCaret — это набор данных, преобразований и моделей, обучаемых и оцениваемых в одной задаче.

Эксперимент в MlFlow — это набор run-ов, связанных с задачей, содержащих информацию о метриках, параметрах, артефактах и моделях.

### 99. Что такое параметры в MlFlow?

Параметры в MlFlow — это значения, связанные с run-ом, описывающие настройки, конфигурацию или гиперпараметры модели.

### 100. Как отобразить метрики в PyCaret?

Используйте функцию `get_metrics()`:

```python
from pycaret.classification import setup
from pycaret.datasets import get_data

employee_df = get_data('employee', verbose=False)
exp = setup(data=employee_df, target='left')
exp.get_metrics()
```

### 101. Что такое scikit-learn?

scikit-learn — это библиотека машинного обучения на Python, предоставляющая инструменты для классификации, регрессии, кластеризации, уменьшения размерности и др.

Одна из самых популярных ML-библиотек с простым и единым API и множеством готовых алгоритмов.

### 102. Что такое артефакт в MlFlow?

Артефакт в MlFlow — это файл или ресурс, связанный с run-ом, который был сгенерирован во время выполнения задачи машинного обучения.

Артефактом может быть результат модели, файл, график или другой ресурс, относящийся к run-у.

### 103. Что такое бэктестинг (backtesting) при мониторинге языковых моделей (LLM)?

Бэктестинг — это процесс тестирования языковых моделей на исторических данных для оценки их производительности и качества. Он позволяет сравнить результаты, генерируемые моделями, с реальными данными и выявлять аномалии или деградацию в модели.

### 104. В чём заключается мониторинг языковых моделей (LLM) в приложениях?

Мониторинг LLM в приложениях — это отслеживание их производительности, качества и поведения во времени. Цель мониторинга — убедиться, что языковые модели работают ожидаемо и не деградируют из-за изменений во входных данных или самой модели.

### 105. Что такое задержка (latency) при мониторинге языковых моделей (LLM)?

Задержка (latency) — это время между отправкой запроса к модели и получением ответа. Это важная метрика, влияющая на производительность и качество работы языковых моделей.

### 106. Для чего можно использовать датасеты Langfuse?

Датасеты Langfuse можно использовать для тестирования и валидации языковых моделей (LLM), а также для сравнения результатов разных моделей. Они могут служить эталонным набором для оценки производительности и качества моделей.

### 107. Что такое Langfuse?

**Langfuse** — это платформа для мониторинга языковых моделей (LLM) в приложениях, позволяющая отслеживать и анализировать производительность, качество и поведение моделей. Она также позволяет сравнивать модели, выявлять аномалии и создавать датасеты для тестирования и валидации.

### 108. Что такое токены в языковых моделях (LLM) и почему они важны?

Токены — это базовые единицы текста (слова, части слов, знаки препинания), на которые разбивается текст для обработки LLM. Количество токенов важно для мониторинга, так как от него зависит стоимость запроса к модели.

### 109. Что такое model drift при мониторинге языковых моделей (LLM)?

Model drift — это явление, при котором модель со временем начинает давать худшие результаты из-за изменений во входных данных или самой модели. Model drift приводит к деградации качества и требует мониторинга и своевременной реакции.

### 110. Как настроить доступ к API OpenAI в DigitalOcean App Platform?

Чтобы настроить доступ к API OpenAI в DigitalOcean App Platform, необходимо использовать переменные окружения.

### 111. Что такое развертывание в облаке (cloud deployment)?

Развертывание в облаке (cloud deployment) — это процесс размещения приложений, сервисов или моделей в облачной инфраструктуре. Это позволяет получить доступ к приложениям через интернет, обеспечивает масштабируемость, гибкость и снижает затраты на инфраструктуру.

### 112. Какой сервис использовать для развертывания приложения в DigitalOcean?

Для развертывания приложения в DigitalOcean можно использовать сервис **DigitalOcean App Platform**. Это платформа для развертывания, масштабирования и управления облачными приложениями.

### 113. Как настроить DigitalOcean App для запуска приложения Streamlit?

- Создайте файл `app.py` с кодом приложения Streamlit
- Создайте файл `requirements.txt` со всеми необходимыми библиотеками
- В консоли DigitalOcean App Platform выберите **Create App** и укажите исходный код из GitHub
- Укажите репозиторий с кодом приложения Streamlit
- Убедитесь, что **Resource Type** — это Web Service, Python
- В поле **Run Command** укажите `streamlit run app.py`
- В поле **Port** укажите `8501`

### 114. Каковы преимущества использования DigitalOcean App Platform по сравнению со Streamlit Community Cloud?

Главное преимущество — больший контроль над средой, конфигурацией приложения и ресурсами. DigitalOcean также позволяет размещать базы данных, облачное хранилище, виртуальные машины и другие сервисы, что позволяет управлять всей системой в одном месте.

---

## Модуль 10

### 1. Что такое DDD и каковы его принципы?

**DDD (Domain-Driven Design)** — это метод проектирования программного обеспечения, который позволяет моделировать ключевые бизнес-процессы, важные для приложения.

### 2. Почему так важно собирать доменную экспертизу?

Доменные знания позволяют лучше понять возникающие задачи и потребности пользователей.  
Для Data Scientist'а понимание предметной области помогает глубже анализировать данные.

### 3. Как писать ясные письма, подытоживающие важные результаты?

1. **Тема:** Сформулируйте понятную тему письма, кратко отражающую его суть.
2. **Зачем:** В первом абзаце объясните, зачем пишете письмо.
3. **Кто:** Помните, что письмо читает человек — пишите понятно.
4. **Завершение / Рекомендации:** Подытожьте письмо и, при необходимости, укажите следующий шаг.

### 4. Проведи Event Storming для процесса заказа еды в ресторане

1. Меню доставлено
2. Еда выбрана
3. Официант вызван
4. Официант подошёл
5. Заказ оформлен

### 5. Что такое Event Storming?

**Event Storming** — это техника моделирования бизнес-процессов.  
Позволяет понять ключевые процессы, важные для приложения.

### 6. Проведи Event Storming для системы бронирования отеля

1. Отель выбран
2. Дата выбрана
3. Опция завтрака выбрана
4. Бронирование добавлено в корзину
5. Бронирование оплачено
6. Бронирование подтверждено

### 7. Что такое доменные знания?

Доменные знания — это знания о предметной области, в которой мы работаем.  
Они помогают лучше понять задачи и проблемы в данной сфере.

### 8. Что такое canvas в Obsidian и как его использовать?

**Canvas** — это рабочее пространство в приложении **Obsidian**, позволяющее создавать заметки в стиле mind map (карты мыслей).

### 9. Что такое приложение Obsidian?

**Obsidian** — это приложение для сбора и организации знаний.  
Позволяет создавать связанные между собой заметки.

### 10. Как добавить градиент фона к DataFrame?

Можно добавить градиент фона с помощью `.style.background_gradient`:

```python
import pandas as pd
import seaborn as sns
import numpy as np

np.random.seed(42)
numbers_df = pd.DataFrame(
    np.random.randint(0, 100, size=(10, 4)),
    columns=["A", "B", "C", "D"],
)
cm = sns.light_palette("green", as_cmap=True)
numbers_df.style.background_gradient(cmap=cm, axis=0)
```

### 11. Как объединить разные методы стилизации DataFrame?

Можно объединять разные методы, используя цепочку методов `.style`:

```python
import pandas as pd

weather_df = pd.DataFrame(
    [
        {"city": "Tokyo", "temperature": 25, "humidity": 80},
        {"city": "Beijing", "temperature": None, "humidity": 50},
        {"city": "New York", "temperature": 20, "humidity": None},
        {"city": "Paris", "temperature": None, "humidity": None},
        {"city": "Rio de Janeiro", "temperature": 30, "humidity": 90},
        {"city": "Istanbul", "temperature": 32, "humidity": 60},
    ]
)

(
    weather_df.style
    .highlight_null(color='cadetblue')
    .highlight_max(
        axis=0,
        props='color:white;background-color:darkgreen'
    )
    .highlight_min(
        axis=0,
        props='color:white;background-color:darkred'
    )
)
```

### 12. Как стилизовать значения в определённых квантилях DataFrame?

Используйте `.style.highlight_quantile`:

```python
import pandas as pd

weather_df = pd.DataFrame(
    [
        {"city": "Tokyo", "temperature": 25, "humidity": 80},
        {"city": "Beijing", "temperature": None, "humidity": 50},
        {"city": "New York", "temperature": 20, "humidity": None},
        {"city": "Paris", "temperature": None, "humidity": None},
        {"city": "Rio de Janeiro", "temperature": 30, "humidity": 90},
        {"city": "Istanbul", "temperature": 32, "humidity": 60},
    ]
)

weather_df.style.highlight_quantile(
    q_left=0.25,
    q_right=0.75,
    color="#0000aa",
    subset=["humidity"],
)
```

### 13. Как форматировать значения в DataFrame?

Используйте `.style.format` с функцией форматирования:

```python
import pandas as pd

weather_df = pd.DataFrame(
    [
        {"city": "Tokyo", "temperature": 25, "humidity": 80},
        {"city": "Beijing", "temperature": None, "humidity": 50},
        {"city": "New York", "temperature": 20, "humidity": None},
        {"city": "Paris", "temperature": None, "humidity": None},
        {"city": "Rio de Janeiro", "temperature": 30, "humidity": 90},
        {"city": "Istanbul", "temperature": 32, "humidity": 60},
    ]
)

def humidity_description(v):
    if pd.isnull(v):
        return "Unknown"
    elif v <= 50:
        return "Dry"
    elif v <= 70:
        return "Normal"
    return "Wet"

weather_df.style.format(humidity_description, subset=["humidity"])
```

### 14. Что такое Pandas Styler?

Pandas Styler — это атрибут DataFrame, который позволяет стилизовать данные (цвет, форматирование текста и др.).  
Доступен через атрибут `.style`.

### 15. Как добавить градиент текста к DataFrame?

Используйте `.style.text_gradient`:

```python
import pandas as pd
import seaborn as sns
import numpy as np

np.random.seed(42)
numbers_df = pd.DataFrame(
    np.random.randint(0, 100, size=(10, 4)),
    columns=["A", "B", "C", "D"],
)
cm = sns.light_palette("green", as_cmap=True)
numbers_df.style.text_gradient(cmap=cm, axis=0)
```

### 16. Что такое reproducibility?

Reproducibility — это возможность воспроизвести результаты вашей работы.  
Позволяет проверить корректность результатов.

### 17. Как ограничить диапазон осей X и Y на графике?

```python
import matplotlib.pyplot as plt
import seaborn as sns

tips_df = sns.load_dataset("tips")

plt.figure(figsize=(10, 5))
sns.regplot(data=tips_df, x="total_bill", y="tip")
plt.title('Зависимость между счётом и чаевыми')
plt.xlabel('Счёт')
plt.ylabel('Чаевые')
plt.xlim(3, 40)
plt.ylim(0, 7)
plt.show()
```

### 18. Как добавить форматирование к Excel-файлу?

Используйте метод `.add_format` из XlsxWriter:

```python
import pandas as pd

df = pd.DataFrame(
    {
        "Numbers": [1010, 2020, 3030, 2020, 1515, 3030, 4545],
        "Percentage": [0.1, 0.2, 0.33, 0.25, 0.5, 0.75, 0.45],
    }
)

with pd.ExcelWriter(
    "pandas_column_formats.xlsx",
    engine="xlsxwriter"
) as writer:
    df.to_excel(writer, sheet_name="Sheet1")

    workbook = writer.book
    worksheet = writer.sheets["Sheet1"]

    format1 = workbook.add_format({"num_format": "#,##0.00"})
    format2 = workbook.add_format({"num_format": "0%"})

    worksheet.set_column(1, 1, 18, format1)
    worksheet.set_column(2, 2, None, format2)
```

### 19. Как обеспечить reproducibility при работе с Scikit-learn?

Используйте аргумент `random_state`:

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split
from pycaret.datasets import get_data

wine_df = get_data('wine', verbose=False)

X, y = wine_df.drop(columns=['type']), wine_df['type']
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42,
)

model = RandomForestClassifier(random_state=42)
model.fit(X_train, y_train)

# ОЖИДАЕМ: 0.9946153846153846
model.score(X_test, y_test)
```

### 20. Как добавить DataFrame в Excel-файл?

Используйте метод `.to_excel`:

```python
import pandas as pd

df1 = pd.DataFrame({"Data": [11, 12, 13, 14]})
df2 = pd.DataFrame({"Data": [21, 22, 23, 24]})
df3 = pd.DataFrame({"Data": [31, 32, 33, 34]})
df4 = pd.DataFrame({"Data": [41, 42, 43, 44]})

with pd.ExcelWriter(
    "pandas_positioning_xlsx",
    engine="xlsxwriter"
) as writer:
    df1.to_excel(writer, sheet_name="Sheet1")
    df2.to_excel(writer, sheet_name="Sheet1", startcol=3)
    df3.to_excel(writer, sheet_name="Sheet1", startrow=6)
    df4.to_excel(
        writer,
        sheet_name="Sheet1",
        startrow=7,
        startcol=4,
        header=False,
        index=False
    )
```

### 21. Как добавить столбиковую диаграмму в ячейку DataFrame?

Используйте `.style.bar`:

```python
import pandas as pd
import numpy as np

np.random.seed(42)
numbers_df = pd.DataFrame(
    np.random.randint(0, 100, size=(10, 3)),
    columns=["A", "B", "C"],
)
numbers_df.style.bar(color='#d65f5f', align='left')
```

### 22. Почему reproducibility важна при генерации случайных чисел?

Reproducibility позволяет воспроизвести результаты и проверить корректность экспериментов.

### 23. Как стилизовать значения в определённом диапазоне в DataFrame?

Используйте `.style.highlight_between`:

```python
import pandas as pd

weather_df = pd.DataFrame(
    [
        {"city": "Tokyo", "temperature": 25, "humidity": 80},
        {"city": "Beijing", "temperature": None, "humidity": 50},
        {"city": "New York", "temperature": 20, "humidity": None},
        {"city": "Paris", "temperature": None, "humidity": None},
        {"city": "Rio de Janeiro", "temperature": 30, "humidity": 90},
        {"city": "Istanbul", "temperature": 32, "humidity": 60},
    ]
)

weather_df.style.highlight_between(
    left=50,
    right=80,
    color="#0000aa",
    subset=["humidity"],
)
```

### 24. Как обеспечить reproducibility при использовании Faker?

Используйте аргумент `.seed`:

```python
from faker import Faker

Faker.seed(42)
fake = Faker()

# ОЖИДАЕМ: 'Allison Hill'
fake.name()
```

---

## Модуль 11

### 1. Каковы основные различия между методологиями Waterfall и Scrum?

**Waterfall** — классическая, жёсткая методология, где все требования определяются заранее. Это затрудняет работу над проектами с непредсказуемыми или меняющимися требованиями.

**Scrum** — гибкая методология, допускающая изменения в ходе проекта. Проект делится на короткие итерации (спринты), после каждой из которых демонстрируются результаты и проводится сессия обратной связи. В Scrum есть роли Product Owner и Scrum Master, а взаимодействие с заказчиком плотнее.

### 2. Что такое Ретроспектива (Sprint Retrospective)?

**Ретроспектива** — встреча после завершения спринта, целью которой является подведение итогов, выявление удачных моментов и областей для улучшения. Позволяет команде непрерывно совершенствовать процесс.

### 3. Основные различия между Kanban и Scrum?

**Scrum** — работа строится спринтами (итерациями), есть роли Scrum Master и Product Owner, задачи выбираются заранее, после каждого спринта — демонстрация результата и фидбек.

**Kanban** — ещё более гибкая методика: нет ролей, работа ведётся непрерывно, задачи добавляются в любой момент, единственное ограничение — количество одновременно выполняемых задач (WIP — work in progress).

### 4. Что такое Product Backlog?

**Product Backlog** — список всех задач проекта, отсортированных по приоритету. Каждая задача имеет бизнес-ценность. Product Owner отвечает за его актуальность и соответствие потребностям клиента.

### 5. Кто такой Project Manager в команде?

**Project Manager** отвечает за:

1. Планирование расписания, бюджета и ресурсов проекта
2. Координацию коммуникации между командой и заинтересованными сторонами
3. Мониторинг прогресса и выявление рисков задержек
4. Контроль за выполнением проекта по плану и соответствием ожиданиям клиента

### 6. Что такое Спринт в Scrum?

**Спринт** — это отрезок времени (обычно 1–4 недели), когда команда работает над определённым функционалом. В течение спринта задачи не меняются и не добавляются. В конце — демонстрация результата и сессия обратной связи, после чего планируется следующий спринт.

### 7. Основные обязанности Data Engineer в команде:

1. Создание систем для сбора и обработки данных из разных источников
2. Проектирование эффективных и безопасных баз данных
3. Обеспечение полноты и точности данных при их перемещении между системами
4. Взаимодействие с Data Analyst и Data Scientist для предоставления нужных данных

### 8. Основные обязанности Data Analyst в команде:

1. Анализ данных для ответов на бизнес-вопросы
2. Создание отчётов и визуализаций для поддержки принятия решений
3. Формулировка выводов и предложений по улучшениям
4. Работа с большими объёмами данных для выявления трендов и закономерностей

### 9. Что такое команда разработчиков (development team)?

**Команда разработчиков** — саморганизующаяся группа, отвечающая за создание продукта (программисты, тестировщики, аналитики, дизайнеры, data scientists и др.).

### 10. Кто такой Product Owner в команде?

**Product Owner** отвечает за:

1. Определение состава и порядка реализации функций продукта
2. Разъяснение приоритетов команде
3. Решение, что делать в первую очередь, а что — потом
4. Общение с клиентами и заинтересованными сторонами для понимания потребностей

Это представитель заказчика в команде, глубоко понимающий продукт и его пользователей.

### 11. Кто такой Scrum Master в команде?

**Scrum Master** отвечает за:

1. Организацию и проведение командных встреч (stand-up, планирование спринтов и др.)
2. Помощь команде в решении проблем, мешающих работе
3. Поддержку команды в достижении целей и сроков
4. Обучение Scrum/Agile-практикам

Он следит за эффективностью и мотивацией команды, а также за регулярностью и результативностью церемоний.

### 12. Что такое Sprint Review?

**Sprint Review** — встреча по завершении спринта, на которой команда демонстрирует выполненную работу, а Product Owner и заинтересованные стороны оценивают результаты и дают обратную связь.

### 13. Что такое Backlog Refinement?

**Backlog Refinement** — совместная работа Product Owner и команды по анализу и уточнению задач Product Backlog для подготовки их к будущим спринтам.

### 14. Кто такой Tech Lead в команде?

**Tech Lead** отвечает за:

1. Техническое развитие проекта и выбор технологий
2. Помощь коллегам в решении технических вопросов
3. Принятие ключевых технических решений для целостности и стабильности проекта
4. Взаимодействие с бизнес-сторонами для понимания требований

### 15. Что такое Sprint Planning?

**Sprint Planning** — встреча в начале спринта, где команда выбирает задачи из Product Backlog для выполнения и формулирует цели на спринт.

### 16. Что такое Jira и Trello?

**Jira** и **Trello** — популярные инструменты управления проектами: позволяют создавать задачи, назначать их, отслеживать прогресс и общаться в команде. Задачи обычно организованы на досках.

### 17. Основные обязанности Data Scientist в команде:

1. Анализ данных для ответов на бизнес-вопросы
2. Создание отчётов и визуализаций
3. Формулировка выводов и предложений по улучшениям
4. Работа с большими данными для поиска трендов и закономерностей

Часто **Data Scientist** решает более сложные задачи: машинное обучение, построение предиктивных моделей, а также может выполнять роли **Data Analyst**, **Data Engineer** и **ML Engineer**, отвечать за инфраструктуру (MLOps).

### 18. Что такое методологии управления проектами?

**Методологии управления проектами** — набор принципов, техник и инструментов для эффективного управления проектом. Основные:

- **Waterfall** (Каскадная): проект делится на последовательные фазы, каждая завершается перед началом следующей
- **Scrum**: проект делится на спринты с регулярной поставкой результата
- **Kanban**: работа организована как поток задач на доске, акцент на плавность процесса и устранение потерь

### 19. Что такое story points?

**Story points** — единица измерения сложности задачи в проекте (не времени, а именно сложности). Обычно используются числа Фибоначчи: 1, 2, 3, 5, 8, 13, 21, 34, 55, 89. Если задача больше 13 points, её стоит разбить на подзадачи.

### 20. Что такое Daily Scrum?

**Daily Scrum** — короткая (до 15 минут) ежедневная встреча для синхронизации команды, обсуждения прогресса и выявления препятствий.

### 21. Основные обязанности DevOps в команде:

1. Автоматизация процессов развертывания
2. Управление серверами и системами приложения
3. Мониторинг и устранение проблем с приложением
4. Оптимизация систем для скорости и безопасности

**DevOps** — это связующее звено между программистами и администраторами, отвечающее за стабильную работу приложения.

### 22. Основные обязанности ML Engineer в команде:

1. Внедрение и оптимизация ML-моделей для реального применения
2. Создание инфраструктуры для обучения и тестирования AI-моделей
3. Проверка корректности работы моделей и их настройка по мере необходимости
4. Улучшение моделей для работы с большими объёмами данных и повышения эффективности

### 23. Что такое Sprint Backlog?

**Sprint Backlog** — список задач, выбранных из Product Backlog для выполнения в текущем спринте. Управляется командой.

### 24. Основные обязанности MLOps в команде:

1. Создание процессов для обучения и развертывания AI-моделей
2. Автоматизация повторяющихся ML-задач
3. Контроль качества и адаптация моделей к новым данным
4. Обеспечение воспроизводимости и прозрачности жизненного цикла моделей

**MLOps** совмещает знания в ML и инженерии ПО, обеспечивая эффективное развертывание и сопровождение моделей.

### 25. Как решить конфликт в системе контроля версий Git?

Чтобы решить конфликт в Git, сделай следующее:

1. Открой файл, в котором возник конфликт
2. Найди участок с конфликтом:
```diff
<<<<<<< HEAD
Локальная версия изменений
=======
Удалённая версия изменений
>>>>>>> branch-name
```
3. Определи, какие изменения оставить, и удали маркеры конфликта
4. Сохрани файл
5. Добавь изменения в индекс: `git add имя_файла`
6. Заверши разрешение конфликта: `git rebase --continue`

### 26. Как создать новую ветку (branch) в Git?

Инструкция:

1. Убедись, что находишься на главной ветке:
    - Выполни `git branch` и посмотри, какая ветка отмечена звёздочкой
    - Если ты не на главной ветке, переключись: `git checkout main`

2. Получи последние изменения с удалённого репозитория: `git pull --rebase`
3. Создай новую ветку: `git checkout -b имя-ветки`

### 27. Для чего нужна команда `git pull --rebase`?

`git pull --rebase` подтягивает изменения с удалённого репозитория на твой компьютер, но делает это более "чисто". В отличие от `git pull`, не создаёт дополнительный коммит слияния ("merge commit"), а просто "переносит" твои коммиты в конец истории.

В итоге: история становится более линейной и читаемой.

### 28. Что такое ветка (branch) в Git?

**Ветка** — это ответвление от основной линии разработки. Позволяет параллельно разрабатывать разные функции, не мешая основной ветке. У каждой ветки своя история изменений.

Можно воспринимать ветку как копию проекта для экспериментов и внедрения новых возможностей, которые потом можно объединить (merge) с основной веткой.

### 29. В чём разница между `git merge` и `git rebase`?

Обе команды объединяют изменения из разных веток, но делают это по-разному:

- `git merge` создаёт дополнительный коммит слияния ("merge commit"):

```
A -- B -- C
  \
   D -- E -- F
```

После merge:
```
A -- B -- C -- G (merge commit)
  \           /
   D -- E -- F
```

- `git rebase` переносит твои коммиты в конец основной ветки:

```
A -- B -- C
  \
   D -- E -- F
```

После rebase:
```
A -- B -- C -- D -- E -- F
                \
                 (твои локальные коммиты)
```

### 30. Для чего команда `git clone`?

`git clone` — чтобы скопировать удалённый репозиторий на свой компьютер вместе со всей историей изменений. Так ты начинаешь работу с существующим проектом.

### 31. Что такое конфликт в Git?

**Конфликт** — это ситуация, когда два разработчика изменили один и тот же участок файла. Git не может автоматически выбрать правильный вариант, и программист должен вручную разрешить конфликт.

Пример:
```diff
Та же строка в обоих репозиториях

<<<<<<< HEAD
Эта строка была изменена локально
=======
Эта строка была изменена удалённо
>>>>>>> branch-name
```

### 32. Для чего команда `git diff`?

`git diff` показывает различия между файлами в репозитории — позволяет увидеть, что изменилось с момента последнего коммита.

### 33. В чём разница между `git pull` и `git pull --rebase`?

- `git pull` — подтягивает изменения с удалённого репозитория и объединяет их с твоими, создавая merge commit.
- `git pull --rebase` — подтягивает изменения и "переносит" твои коммиты в конец истории, делая историю линейной.

### 34. Как объединить последние изменения из main в свою ветку?

1. Убедись, что находишься на главной ветке:
    - Выполни `git branch` и проверь, какая ветка отмечена звёздочкой
    - Если не на main — `git checkout main`

2. Получи свежие изменения: `git pull --rebase`
3. Переключись на свою ветку: `git checkout имя-ветки`
4. Объедини изменения из main с помощью: `git rebase main`

### 35. Что такое Pull Request в Git?

**Pull Request** — это запрос на принятие изменений из одной ветки в другую. Это механизм для code review: позволяет просматривать, обсуждать и комментировать изменения перед их слиянием в основную ветку.

Это важная часть обмена опытом и повышения качества кода.

### 36. Для чего команда `git branch`?

Команда `git branch` используется для управления ветками:

- Показать список веток: `git branch`
- Создать ветку: `git branch имя-ветки`
- Удалить ветку: `git branch -d имя-ветки`

### 37. Что такое Code Review?

**Code Review** — это процесс, когда один или несколько программистов проверяют код другого члена команды перед объединением его изменений с основной веткой. Цель: найти ошибки, улучшить качество кода и убедиться в соответствии стандартам.

### 38. Для чего команда `git checkout`?

`git checkout` используется для переключения между ветками:  
`git checkout имя-ветки`

Можно также одновременно создать и перейти в новую ветку:  
`git checkout -b имя-ветки`

### 39. Для чего команда `git pull`?

`git pull` — чтобы подтянуть последние изменения из удалённого репозитория на свой компьютер.  
Это обновляет локальную копию до самой свежей версии.

Внимание: если есть расхождения между локальной и удалённой веткой, будет создан merge commit, фиксирующий объединение историй.

## Таблица команд и функций

| Модуль | Функция / Команда | Краткое описание | Пример использования |
|----------|--------------------|--------------------|-----------------|
| 1 | `pip install` | Устанавливает пакет Python | `pip install numpy` |
| 1 | `jupyter notebook` | Запускает Jupyter Notebook | `jupyter notebook` |
| 1 | `%pip install` | Установка пакета прямо из Jupyter | `%pip install pandas` |
| 2 | `median()` | Возвращает медиану из списка чисел | `statistics.median([1, 2, 3, 4])` |
| 2 | `mean()` | Среднее арифметическое | `statistics.mean([1, 2, 3, 4])` |
| 2 | `mode()` | Мода (наиболее часто встречающееся значение) | `statistics.mode([1, 1, 2, 3])` |
| 3 | `conda create` | Создаёт новую среду | `conda create -n myenv python=3.11` |
| 3 | `conda activate` | Активирует среду | `conda activate myenv` |
| 3 | `conda deactivate` | Деактивирует активную среду | `conda deactivate` |
| 3 | `conda remove` | Удаляет пакет или среду | `conda remove numpy` |
| 3 | `conda install` | Устанавливает пакет | `conda install pandas` |
| 3 | `conda list` | Показывает установленные пакеты | `conda list` |
| 3 | `conda env list` | Показывает все среды | `conda env list` |
| 3 | `conda create -n myenv python=3.10` | Создаёт среду с нужной версией Python | `conda create -n testenv python=3.10` |
| 3 | `conda info` | Информация о конфигурации Conda | `conda info` |
| 3 | `import datetime` | Импорт модуля для работы с датами | `datetime.datetime.now()` |
| 3 | `import math` | Импорт математических функций | `math.sqrt(16)` |
| 3 | `import random` | Импорт функций случайных чисел | `random.randint(1, 10)` |
| 3 | `import os` | Работа с операционной системой | `os.listdir()` |
| 4 | `import pandas as pd` | Импорт библиотеки pandas | `import pandas as pd` |
| 4 | `pd.read_csv()` | Загружает CSV-файл | `pd.read_csv('data.csv')` |
| 4 | `pd.read_excel()` | Загружает Excel-файл | `pd.read_excel('data.xlsx')` |
| 4 | `df.head()` | Выводит первые строки DataFrame | `df.head(10)` |
| 4 | `df.tail()` | Выводит последние строки | `df.tail(5)` |
| 4 | `df.info()` | Информация о DataFrame | `df.info()` |
| 4 | `df.describe()` | Статистика по числовым столбцам | `df.describe()` |
| 4 | `df.columns` | Возвращает список столбцов | `df.columns` |
| 4 | `df['col']` | Обращение к столбцу | `df['age']` |
| 4 | `df.iloc[]` | Доступ по индексам | `df.iloc[0:5]` |
| 4 | `df.loc[]` | Доступ по меткам | `df.loc[df['age'] > 30]` |
| 4 | `df.sort_values()` | Сортировка по столбцу | `df.sort_values('age')` |
| 4 | `df.rename()` | Переименование столбцов | `df.rename(columns={'old':'new'})` |
| 4 | `df.isnull()` | Проверка на пропуски | `df.isnull().sum()` |
| 4 | `df.fillna()` | Замена пропусков | `df.fillna(0)` |
| 4 | `df.dropna()` | Удаление строк с NaN | `df.dropna()` |
| 4 | `df.drop()` | Удаление столбцов/строк | `df.drop('column', axis=1)` |
| 4 | `df.value_counts()` | Частота значений в столбце | `df['city'].value_counts()` |
| 4 | `df.unique()` | Уникальные значения столбца | `df['country'].unique()` |
| 4 | `df.groupby()` | Группировка и агрегация | `df.groupby('gender').mean()` |
| 4 | `df.plot()` | Построение графиков | `df.plot(kind='bar')` |
| 4 | `df.hist()` | Гистограмма данных | `df.hist()` |
| 4 | `df.to_csv()` | Сохранение в CSV | `df.to_csv('out.csv', index=False)` |
| 4 | `df.to_excel()` | Сохранение в Excel | `df.to_excel('out.xlsx')` |
| 4 | `pd.concat()` | Объединение DataFrame | `pd.concat([df1, df2])` |
| 4 | `pd.merge()` | Объединение по ключу | `pd.merge(df1, df2, on='id')` |
| 5 | `Path()` | Создание объекта пути | `Path('data/file.csv')` |
| 5 | `Path.exists()` | Проверяет наличие файла/папки | `Path('data').exists()` |
| 5 | `Path.is_file()` | Проверяет, является ли путь файлом | `Path('data.csv').is_file()` |
| 5 | `Path.is_dir()` | Проверяет, является ли путь каталогом | `Path('data').is_dir()` |
| 5 | `Path.glob()` | Перебирает файлы по шаблону | `for f in Path('data').glob('*.csv'):` |
| 5 | `json.load()` | Загрузка JSON | `data = json.load(open('data.json'))` |
| 5 | `json.dump()` | Сохранение JSON | `json.dump(data, open('out.json','w'))` |
| 5 | `pd.read_json()` | Загрузка JSON в DataFrame | `pd.read_json('data.json')` |
| 5 | `pd.read_xml()` | Загрузка XML-файла | `pd.read_xml('data.xml')` |
| 5 | `pd.read_sql()` | Загрузка данных из SQL | `pd.read_sql('SELECT * FROM users', conn)` |
| 5 | `sqlite3.connect()` | Подключение к базе SQLite | `conn = sqlite3.connect('db.sqlite')` |
| 5 | `cursor.execute()` | Выполнение SQL-запроса | `cursor.execute('SELECT * FROM users')` |
| 5 | `conn.commit()` | Сохранение изменений в базе | `conn.commit()` |
| 5 | `SELECT` | Извлекает данные из таблицы | `SELECT * FROM users;` |
| 5 | `WHERE` | Фильтрация записей по условию | `SELECT * FROM users WHERE age > 30;` |
| 5 | `ORDER BY` | Сортировка результатов | `SELECT * FROM users ORDER BY name DESC;` |
| 5 | `LIMIT` | Ограничивает количество строк | `SELECT * FROM users LIMIT 10;` |
| 5 | `OFFSET` | Пропускает первые N строк | `SELECT * FROM users LIMIT 10 OFFSET 5;` |
| 5 | `UPDATE` | Обновляет данные в таблице | `UPDATE users SET age = 35 WHERE id = 1;` |
| 5 | `DELETE` | Удаляет записи | `DELETE FROM users WHERE age < 18;` |
| 5 | `INSERT INTO` | Добавляет новые записи | `INSERT INTO users (name, age) VALUES ('Ivan', 25);` |
| 5 | `JOIN` | Объединяет таблицы | `SELECT * FROM users JOIN orders ON users.id = orders.user_id;` |
| 5 | `LEFT JOIN` | Все строки из левой таблицы + совпадения | `SELECT * FROM users LEFT JOIN orders ON users.id = orders.user_id;` |
| 5 | `RIGHT JOIN` | Все строки из правой таблицы + совпадения | `SELECT * FROM users RIGHT JOIN orders ON users.id = orders.user_id;` |
| 5 | `GROUP BY` | Группировка данных | `SELECT city, COUNT(*) FROM users GROUP BY city;` |
| 5 | `HAVING` | Фильтрация сгруппированных данных | `SELECT city, COUNT(*) FROM users GROUP BY city HAVING COUNT(*) > 5;` |
| 5 | `CREATE TABLE` | Создаёт новую таблицу | `CREATE TABLE users (id INTEGER, name TEXT);` |
| 5 | `DROP TABLE` | Удаляет таблицу | `DROP TABLE users;` |
| 5 | `ALTER TABLE` | Изменяет структуру таблицы | `ALTER TABLE users ADD COLUMN email TEXT;` |
| 6 | `Faker()` | Создание генератора фейковых данных | `fake = Faker()` |
| 6 | `fake.name()` | Фейковое имя | `fake.name()` |
| 6 | `fake.email()` | Фейковый e-mail | `fake.email()` |
| 6 | `fake.address()` | Фейковый адрес | `fake.address()` |
| 6 | `fake.text()` | Генерация случайного текста | `fake.text()` |
| 6 | `fake.date_of_birth()` | Фейковая дата рождения | `fake.date_of_birth()` |
| 6 | `fake.company()` | Фейковая компания | `fake.company()` |
| 6 | `fake.profile()` | Случайный профиль | `fake.profile()` |
| 6 | `fake.simple_profile()` | Упрощённый профиль | `fake.simple_profile()` |
| 6 | `Faker('pl_PL')` | Локализация данных | `fake = Faker('pl_PL')` |
| 7 | `plt.plot()` | Линейный график | `plt.plot(x, y)` |
| 7 | `plt.subplot()` | Несколько графиков в одном окне | `plt.subplot(1, 2, 1)` |
| 7 | `plt.xlim()` | Задать диапазон оси X | `plt.xlim(0, 100)` |
| 7 | `plt.ylim()` | Задать диапазон оси Y | `plt.ylim(0, 50)` |
| 7 | `plt.axhline()` | Горизонтальная линия | `plt.axhline(y=10, color='r')` |
| 7 | `plt.axvline()` | Вертикальная линия | `plt.axvline(x=5, color='g')` |
| 7 | `plt.bar()` | Столбчатая диаграмма | `plt.bar(names, values)` |
| 7 | `plt.scatter()` | Диаграмма рассеяния | `plt.scatter(x, y)` |
| 7 | `plt.hist()` | Гистограмма | `plt.hist(data, bins=10)` |
| 7 | `plt.title()` | Заголовок графика | `plt.title('Результаты')` |
| 7 | `plt.xlabel()` | Подпись оси X | `plt.xlabel('Время')` |
| 7 | `plt.ylabel()` | Подпись оси Y | `plt.ylabel('Скорость')` |
| 7 | `plt.legend()` | Легенда графика | `plt.legend(['A', 'B'])` |
| 7 | `plt.grid()` | Включает сетку | `plt.grid(True)` |
| 7 | `plt.savefig()` | Сохраняет график | `plt.savefig('plot.png')` |
| 8 | `sns.heatmap()` | Тепловая карта | `sns.heatmap(df.corr(), annot=True)` |
| 8 | `sns.boxplot()` | Boxplot (ящик с усами) | `sns.boxplot(x='sex', y='age', data=df)` |
| 8 | `sns.violinplot()` | Violin plot | `sns.violinplot(x='sex', y='age', data=df)` |
| 8 | `sns.pairplot()` | Парные графики | `sns.pairplot(df)` |
| 8 | `sns.countplot()` | Подсчёт категорий | `sns.countplot(x='city', data=df)` |
| 8 | `sns.distplot()` | Распределение данных | `sns.distplot(df['salary'])` |
| 8 | `sns.barplot()` | Средние значения по категориям | `sns.barplot(x='city', y='income', data=df)` |
| 8 | `sns.clustermap()` | Кластерная тепловая карта | `sns.clustermap(df.corr())` |
| 8 | `sns.jointplot()` | Двумерное распределение | `sns.jointplot(x='x', y='y', data=df)` |
| 8 | `sns.lineplot()` | Линейный график | `sns.lineplot(x='year', y='value', data=df)` |
| 8 | `sns.set_style()` | Настройка стиля | `sns.set_style('whitegrid')` |
| 9 | `np.array()` | Создание массива NumPy | `arr = np.array([1, 2, 3])` |
| 9 | `np.arange()` | Диапазон чисел | `np.arange(0, 10, 2)` |
| 9 | `np.zeros()` | Массив из нулей | `np.zeros((3, 3))` |
| 9 | `np.ones()` | Массив из единиц | `np.ones((2, 2))` |
| 9 | `np.random.rand()` | Случайные числа от 0 до 1 | `np.random.rand(3, 3)` |
| 9 | `np.mean()` | Среднее значение | `np.mean(arr)` |
| 9 | `np.median()` | Медиана | `np.median(arr)` |
| 9 | `np.std()` | Стандартное отклонение | `np.std(arr)` |
| 9 | `np.dot()` | Скалярное произведение | `np.dot(a, b)` |
| 9 | `np.concatenate()` | Объединение массивов | `np.concatenate([a, b])` |
| 9 | `np.reshape()` | Изменяет форму массива | `arr.reshape(2, 3)` |
| 9 | `np.linspace()` | Равномерная последовательность | `np.linspace(0, 1, 5)` |
| 9 | `np.max()` | Максимум | `np.max(arr)` |
| 9 | `np.min()` | Минимум | `np.min(arr)` |
| 10 | `sklearn.model_selection.train_test_split()` | Разделение данных на train/test | `X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)` |
| 10 | `sklearn.linear_model.LinearRegression()` | Линейная регрессия | `model = LinearRegression(); model.fit(X, y)` |
| 10 | `sklearn.metrics.mean_squared_error()` | Ошибка MSE | `mean_squared_error(y_test, y_pred)` |
| 10 | `sklearn.metrics.r2_score()` | Коэффициент детерминации | `r2_score(y_test, y_pred)` |
| 10 | `sklearn.preprocessing.StandardScaler()` | Масштабирование признаков | `scaler = StandardScaler(); X = scaler.fit_transform(X)` |
| 10 | `model.predict()` | Предсказание модели | `y_pred = model.predict(X_test)` |
| 10 | `sklearn.tree.DecisionTreeClassifier()` | Классификатор дерева решений | `model = DecisionTreeClassifier()` |
| 11 | `openai.ChatCompletion.create()` | Генерация текста с помощью OpenAI | `openai.ChatCompletion.create(model='gpt-4', messages=[...])` |
| 11 | `openai.Image.create()` | Генерация изображения | `openai.Image.create(prompt='кот в очках')` |
| 11 | `openai.Audio.transcribe()` | Распознавание речи | `openai.Audio.transcribe('whisper-1', file)` |
| 11 | `openai.Embedding.create()` | Создание эмбеддингов | `openai.Embedding.create(input='text')` |
| 11 | `openai.File.create()` | Загрузка файла в OpenAI API | `openai.File.create(file=open('data.json'))` |
| 11 | `openai.Moderation.create()` | Проверка текста на правила | `openai.Moderation.create(input='text')` |
| 11 | `openai.FineTuningJob.create()` | Создание задачи дообучения | `openai.FineTuningJob.create(training_file='file-id')` |