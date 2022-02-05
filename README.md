Регрессия - зависимость среднего значения какой-либо величины от некоторой другой величины или от нескольких величин.

# Постановка задачи линейной регрессии.

Задача регрессии — это задача предсказания одной непрерывной случайной величины на основе значений других случайных величин.

Модель линейной двумерной регрессии имеет вид:
y = a + b*x + ε

Величина переменной y состоит из двух составляющих:
1) неслучайной составляющей y = a + b*x 
2) случайной составляющей (ошибки) ε

На рисунке (Рис. 1) показано,как комбинация этих двух составляющих определяет величину y<sub>i</sub> для случая парной линейной модели регрессии.

<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/model.png" />
  <div>Рис. 1</div>
</div>


# Метод наименьших квадратов.

Метод наименьших квадратов один из методов теории ошибок для оценки неизвестных величин по результатам измерений, содержащих случайные ошибки.
Задача заключается в нахождении коэффициентов линейной зависимости, при которых функция двух переменных а и b (Рис. 2) принимает наименьшее значение.
<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/mkn.jpg"  />
  <div>Рис. 2</div>
</div>

То есть, при данных а и b сумма квадратов отклонений экспериментальных данных от найденной прямой будет наименьшей. В этом вся суть метода наименьших квадратов.
Таким образом, решение примера сводится к нахождению экстремума функции двух переменных.

Решения (Рис. 3):
<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/min-error.png"  />
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/mnk-algebra.jpg"  />
  <div>Рис. 3</div>
</div>

# Ковариация, корреляция.
Ковариация — это мера того, как две случайные величины изменятся при сравнении друг с другом. Характеризует степень линейной зависимости двух случайных величин.  
Если ковариация положительна, то с ростом значений одной случайной величины, значения второй имеют тенденцию возрастать, а если знак отрицательный — то убывать.
Однако только по абсолютному значению ковариации нельзя судить о том, насколько сильно величины взаимосвязаны, так как масштаб ковариации зависит от их дисперсий. Ковариацию можно найти по следующей формуле (Рис. 4):
<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/cov.jpg"  />
  <div>Рис. 4</div>
</div>

Значение ковариации можно нормировать, поделив её на произведение среднеквадратических отклонений (квадратных корней из дисперсий) случайных величин (Рис. 5). Это будет коэфицент кореляции.
Коэффициент корреляции — это показатель взаимного вероятностного влияния двух случайных величин. Коэффициент корреляции R может принимать значения от -1 до +1.
Если абсолютное значение находится ближе к 1, то это свидетельство сильной связи между величинами, а если ближе к 0 — то, это говорит о слабой связи или ее отсутствии.

<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/cor.jpg"  />
  <div>Рис. 5</div>
</div>

# Коэффициент детерминации (критерий R2).
Одной из наиболее эффективных оценок адекватности регрессионной модели, мерой качества уравнения регрессии, (или, как говорят, мерой качества подгонки регрессионной модели к фактическим наблюдаемым значениям исследуемого показателя), характеристикой  прогностической силы анализируемой регрессионной модели является коэффициент детерминации. Находится коэфицент по формуле ниже (Рис. 6).

<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/r2.jpg"  />
  <div>Рис. 6</div>
</div>

RSS - сумма квадратов всех отклонений. (Residual Sum of Squares)
TSS - общая сумма квадратов

Свойства коэффициента детерминации
1) Величина R 2 показывает, какая часть (доля) вариации зависимой переменной
обусловлена вариацией объясняющей переменной.
2) Так как 0 <= ESS <= TSS , то 0 <= R2 <=  1.
3) Чем ближе R2 к единице, тем лучше регрессия аппроксимирует эмпирические данные, тем теснее наблюдения примыкают к линии регрессии.
4) Очевидно, что R2 = 1 тогда и только тогда, когда ESS = TSS . В
этом случае эмпирические точки  xi ; yi лежат на линии регрессии и между переменными x и y существует линейная функциональная зависимость.
5) Если R2 = 0 , то вариация зависимой переменной полностью обусловлена воздействием неучтенных в модели переменных,и линия регрессии параллельна оси абсцисс.

# Анализ остатков.
Для получения информации об адекватности построенной модели линейной регрессии исследуют регрессионные остатки. Если выбранная регрессионная модель хорошо описывает истинную зависимость, то остатки должны быть независимыми нормально распределенными случайными величинами с нулевым средним и в их значениях должен отсутствовать тренд. Анализ регрессионных остатков - это процесс проверки выполнения этих условий.

# Гомоскедастичность
Гомоскедастичностью называют свойство данных, которое заключается в том, что их дисперсия вдоль прямой регрессии является постоянной (Рис. 7). Гомоскедастичность — одно из условий эффективности регрессионной модели.

<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/hom.jpg"  />
  <div>Рис. 7</div>
</div>

# Квартет Энскомба.
Квартет Энскомба — четыре набора числовых данных, у которых простые статистические свойства идентичны, но их графики существенно отличаются (Рис. 8). Каждый набор состоит из 11 пар чисел.

<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/kvartet.jpg"  />
  <div>Рис. 8</div>
</div>

# Регуляризация LASSO, Ridge, Elastic.
Регрессия по методу наименьших квадратов (МНК) часто может стать неустойчивой, то есть сильно зависящей от обучающих данных, что обычно является проявлением тенденции к переобучению. Избежать такого переобучения помогает регуляризация - общий метод, заключающийся в наложении дополнительных ограничений (штраф) на искомые параметры, которые могут предотвратить излишнюю сложность модели.

Ридж-регрессия, также называемая L2-регрессиея, штраф — это сумма квадратов весов. В ридж-регрессии штрафы уменьшают коэффициенты при соответствующих независимых переменных, но никогда не обнуляют их. Это значит, что шумы всегда будут влиять на результат, но в очень маленькой степени. Формула (Рис. 9)

```py
RSS = sum((y_real – y_predicted)**2)
ridge = RSS + lambda * sum(W*W)
```
<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/ridge.jpg"  />
  <div>Рис. 9</div>
</div>


Второй тип регуляризации — лассо или L1-регуляризация. Вместо того, чтобы начислять штрафы за каждый признак в данных, штрафы в ней начисляются лишь за признаки с большим значением коэффициентов. К тому же лассо может обнулять значения коэффициентов, тем самым полностью убирая признак из датасета. Таким образом, с регрессией лассо модель может полностью избавиться от шумов в данных. Формула (Рис. 10)

```py
RSS = sum((y_real – y_predicted)**2)
lasso = RSS + theta * sum(W)
```
<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/lasso.jpg"  />
  <div>Рис. 10</div>
</div>

Третий — Elastic.Приведенная регуляризация использует как L1, так и L2 регуляризации, учитывая эффективность обоих методов. Ее полезной особенностью является то, что она создает условия для группового эффекта при высокой корреляции переменных, а не обнуляет некоторые из них, как в случае с L1-регуляризацией (Рис. 11).

<div align="center">
  <img src="https://raw.githubusercontent.com/Olegoria3538/linear-regression/main/images/elastic.jpg"  />
  <div>Рис. 11</div>
</div>

