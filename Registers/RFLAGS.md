## Регистер флагов
![test](https://github.com/JIykSurgut/Opcode/blob/main/Figure/RFLAGS%20Register.jpg)

|бит|Мнемоника|Описание                                                                                                 |
|---|---------|---------------------------------------------------------------------------------------------------------|
|21 |ID       |Флаг идентификации, используется для определения наличия определённых возможностей процессора.           |
|20 |VIP      |Флаг ожидающего виртуального прерывания.                                                                 |
|19 |VIF      |Виртуальный флаг прерываний.                                                                             |
|18 |AC       |Флаг проверки выравнивания, используется для проверки выравнивания данных в памяти.                      |
|17 |VM       |Флаг виртуального режима 8086.                                                                           |
|16 |RF       |Флаг возобновления, используется для предотвращения повторного выполнения прерываний.                    |
|15 |-        |                                                                                                         |
|14 |NT       |Флаг вложенной задачи, используется при переключении задач.                                              |
|13 |IOPL     |Уровень привилегий ввода-вывода.                                                                         |
|12 |IOPL     |Уровень привилегий ввода-вывода.                                                                         |
|11 |OF       |Флаг переполнения, устанавливается, если результат операции выходит за пределы допустимого диапазона.    |
|10 |DF       |Флаг направления, управляет направлением обработки строк данных.                                         |
|09 |IF       |Флаг прерываний, управляет возможностью обработки маскируемых прерываний.                                |
|08 |TF       |Флаг ловушки, используется для пошаговой отладки.                                                        |
|07 |SF       |Флаг знака, показывает знак результата (1 для отрицательного).                                           |
|06 |ZF       |Флаг нуля, устанавливается, если результат операции равен нулю.                                          |
|05 |-        |                                                                                                         |
|04 |AF       |Флаг коррекции, используется для арифметических операций BCD.                                            |
|03 |-        |                                                                                                         |
|02 |PF       |Флаг чётности, устанавливается, если количество установленных битов в результате равно чётному числу.    |
|01 |CF       |Флаг переноса, устанавливается, если в результате выполнения операции произошёл перенос из старшего бита.|


## CF
Флаг переноса (Carry Flag, CF) в регистре RFLAGS устанавливается, когда в результате выполнения арифметической операции происходит перенос из старшего разряда. Например, если мы сложим два 8-битных числа и получим результат, который больше, чем может быть представлен в 8 битах, то флаг переноса будет установлен.

Вот пример кода на ассемблере, который демонстрирует установку флага переноса:
```
MOV AL, 0xFF       ; Загрузка максимального значения для 8-битного числа в регистр AL
ADD AL, 1          ; Прибавление 1 к значению регистра AL
; В результате выполнения этой операции флаг переноса CF будет установлен,
; так как сумма 0xFF и 1 превышает максимальное значение для 8-битного числа (0xFF)
```
После выполнения команды ADD AL, 1, значение в регистре AL будет 0x00, и флаг переноса CF будет установлен, так как произошёл перенос в старший разряд. Если у вас есть дополнительные вопросы, пожалуйста, задавайте.

## OF
Флаг переполнения (Overflow Flag, OF) в регистре RFLAGS устанавливается, когда результат выполнения операции выходит за пределы допустимого диапазона значений для данного размера операнда. Это обычно происходит при выполнении арифметических операций со знаковыми числами.

Вот пример кода на ассемблере, который демонстрирует установку флага переполнения:
```
MOV AL, 0x7F       ; Загрузка максимального положительного значения для 8-битного знакового числа в регистр AL
ADD AL, 1          ; Прибавление 1 к значению регистра AL
; В результате выполнения этой операции флаг переполнения OF будет установлен,
; так как сумма 0x7F и 1 превышает максимальное положительное значение для 8-битного знакового числа
```
После выполнения команды ADD AL, 1, значение в регистре AL будет 0x80, которое интерпретируется как -128 в дополнительном коде для знаковых чисел, и флаг переполнения OF будет установлен, указывая на то, что произошло переполнение. Если у вас есть дополнительные вопросы или вам нужна помощь, пожалуйста, сообщите мне.
