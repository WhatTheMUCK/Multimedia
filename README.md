# Студент группы М8О-407-21 Меркулов Фёдор Алексеевич

В файле ```Мультимедиа.ipynb``` лежат выполненные лабораторные работы 1-5 по курсу "Методы, средства и технологии мультимедиа"

# Подведение итогов

В следующей таблице в ячейках, относящихся к классифкации я буду отображать **accuracy**; в ячейках, относящихся к регрессии я буду отображать **MAE** и в скобках (**MAPE**)

*Метрика качества на тестовом наборе данных*
<table>
    <tr>
        <th rowspan="1">Алгоритм</th>
        <th>Задача</th>
        <th>Бейзлайн</th>
        <th>Улучшенный бейзлайн</th>
        <th>Самостоятельная имплементация алгоритма</th>
    </tr>
    <tr>
        <td rowspan="2">KNN</td>
        <td>классификация</td>
        <td>0.6291</td>
        <td>0.7556</td>
        <td>0.7222</td>
    </tr>
    <tr>
        <td>регрессия</td>
        <td>158.5869 <br> (38.1310%)</td>
        <td>110.8991 <br> (25.2993%)</td>
        <td>109.3256 <br> (25.2951%)</td>
    </tr>
    <tr>
        <td rowspan="2">Линейные модели</td>
        <td>классификация</td>
        <td>0.5219</td>
        <td>0.525</td>
        <td>0.5306</td>
    </tr>
    <tr>
        <td>регрессия</td>
        <td>210.3182 <br> (51.8933%)</td>
        <td>202.4122 <br> (53.6364%)</td>
        <td>203.6512 <br> (54.3687%)</td>
    </tr>
    <tr>
        <td rowspan="2">Решающее дерево</td>
        <td>классификация</td>
        <td>0.7005</td>
        <td>0.75</td>
        <td><strong>0.75</strong></td>
    </tr>
    <tr>
        <td>регрессия</td>
        <td>136.6670 <br> (30.7884%)</td>
        <td>108.6093 <br> (24.4918%)</td>
        <td>104.9442 <br> (22.7875%)</td>
    </tr>
    <tr>
        <td rowspan="2">Случайный лес</td>
        <td>классификация</td>
        <td>0.7060</td>
        <td><strong>0.7833</strong></td>
        <td><strong>0.75</strong></td>
    </tr>
    <tr>
        <td>регрессия</td>
        <td><strong>122.9956 <br> (26.8666%)</strong></td>
        <td><strong>101.5597 <br> (23.2280%)</strong></td>
        <td>104.1647 <br> (24.0724%)</td>
    </tr>
    <tr>
        <td rowspan="2">Градиентный бустинг</td>
        <td>классификация</td>
        <td><strong>0.7225</strong></td>
        <td>0.73611</td>
        <td>0.6806</td>
    </tr>
    <tr>
        <td>регрессия</td>
        <td>124.4211 <br> (29.5335%)</td>
        <td>112.2774 <br> (28.0399%)</td>
        <td><strong>97.7754 <br> (20.0485%)</strong></td>
    </tr>
</table>


<br><br>
Укажу по 2 лучшие модели для каждого отдельного кейса:
<br>

**Классификация**

*Бейзлайн*:  
$1) Градиентный\ бустинг; 2) Случайный\ лес$  

*Улучшенный бейзлайн*:  
$1) Случайный\ лес; 2) Решающее\ дерево$

*Самостоятельная имплементация алгоритма*:  
$1) Градиентный\ бустинг; 2) Случайный\ лес$  

<br>

**Регрессия**

*Бейзлайн*:  
$1) Случайный\ лес; 2) Градиентный\ бустинг$ 

*Улучшенный бейзлайн*:  
$1) Случайный\ лес; 2) Решающее\ дерево$  

*Самостоятельная имплементация алгоритма*:  
$1) Градиентный\ бустинг; 2) Случайный\ лес$  

Хуже всего на моих данных показали себя линейные модели, моё предположение, что это связано с тем, что данные, вероятно, характеризуются нелинейными зависимостями, шумом и/или сложными взаимодействиями между переменными, что катастрофически сказывается на точности линейных моделей.

Лучше всего себя показал случайный лес, что по моему мнению, было связано с переобучением отдельных деревьев, что положительно сказалось на итоговом результате. Случайный лес сумел извлечь больше информации из моих данных благодаря своей способности обрабатывать сложные взаимоотношения и устойчивости к переобучению, что и привело к его превосходным результатам.

<br>

В заключение хотелось бы сказать, что это было увлекательно - проводить исследования с различными моделями и пытаться понять, что значат те или иные показания метрик.
