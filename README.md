# calculator
В задаче испозуются принципы обратной польской нотация или постфиксная нотация.
Производится парсинг арифметических выражений. Доступные операции: '+', '-', '*', '/'

Операнды расположены перед знаками операций
3 4 +		<--> 3 + 4
10 2 4 * - 	<--> 10 - 2 * 4
Выражение считывается слева на право.
- символ - операнд или операция
- операнд - помещается на вершину стека
- операция - выполнить операцию над знаениями в стеке
(Результат выполнения поместить на вершину стека)

Обработка символов производятся пока они не кончатся
После завершения обработки символов результат находится на его вершине

### Замечание про отрицательные числа и деление:
- в задаче под делением понимается математическое целочисленное деление.
- округление всегда происходит вниз.
- если a/b = c, то b*c — это наибольшее число, которое не превосходит a и одновременно делится без остатка на b.
#### Пример: -1 / 3 = -1
- В текущей задаче гарантируется, что деления на отрицательное число нет.
### Формат ввода
Первая стр. - выражение, записанное в обратной польской нотации.

Числа и арифметические операции записаны через пробел.

Доступные операции: '+', '-', '*', '/'

Доступные операнды: числа, по модулю не превосходящие 10'000.

- Гарантируется, что значение промежуточных выражений в тестовых данных по модулю не больше 50'000.
#### Уточнения
- Операнды - всегда целые числа
- Считать, что деления на ноль не будет
- Встречаются только '+', '-', '*', '/' операции
- Гарантируется корректность обратной польской нотации на входе

### Формат вывода 
вывести число - значение выражения.

### Ограничения: 1секунд	64Mb
#### Пример 1:
    Ввод:           Вывод:
    2 1 + 3 *				9
#### Пример 2:
    Ввод:           Вывод:
    7 2 + 4 * 2 +			38
