# C-lab-5

## Лабораторная работа №5 (Функции)

### Задача №1

```
    Написать программу, которая принимает от пользователя строку и
выводит ее на экран, перемешав слова в случайном порядке.
```

**Пояснение**

Для входной строки создается массив указателей на char, в который заносятся
адреса первых символов каждого слова. Затем организуется новая строка, при использовании этого
массива из указателей. Массив из указателей должен объявляться внутри функции **randomWords**.

Порядок слов может быть любым, но главное, чтобы слова не повторялись и строка отличалась от исходной.

**Состав**

Программа должна состоять из функций:

```
    - char * randomWords(char * in, char *out) - функция, изменяющая порядок слов из in и записывающую их в out
    - main() - организация ввода строки
```

Создаются три файла: task1.h,task1.cpp,main1.cpp.

### Задача №2

```
   Написать программу ”Калейдоскоп”, выводящую на экран изобра-
   жение, составленное из симметрично расположенных звездочек ’*’.
   Изображение формируется в двумерном символьном массиве, в од-
   ной его части и симметрично копируется в остальные его части.
```

**Пояснение**

Решение задачи протекает в виде следующей последовательности шагов:

1. Очистка массива (заполнение пробелами)
1. Формирование случайным образом верхнего левого квадранта (из символов)
1. Копирование символов в другие квадранты массива
1. Очистка экрана
1. Вывод массива на экран (построчно)
1. Временная задержка
1. Переход к шагу 1.

**Состав**

Программа должна состоять из функций:

```
   void clearMatrix(char (* arr)[M]) - заполнение двумерного массива (матрицы) пробелами
   void fillMatrix(char (* arr)[M]) - заполнение верхнего левого квадранта матрицы звездочками
   void setMatrix(char (* arr)[M]) - копирование элементов в другие области матрицы
   void printMatrix(char (* arr)[M]) - печать матрицы
   int main()
```

Создаются три файла: task2.h,task2.cpp,main2.cpp.

### Задача №3

```
   Написать программу, переставляющую случайным образом симво-
   лы каждого слова каждой строки текстового файла, кроме первого
   и последнего, то есть начало и конец слова меняться не должны.
```

**Пояснение**

Программа открывает существующий тектстовый файл и читает его построчно. Для каждой строки выполняется разбивка на слова и независимая обработка каждого слова

**Состав**

Программа должна состоять из функций:

```
   - char *mixChars(char *in, char *out) -  перемешивание символов в одном слове
   - char *mixLine(char *instr, char * outstr) - перемешивание для целой строки
   - int main()
```

Создаются три файла: task3.h,task3.cpp,main3.cpp.

### Задача №4

```
    Написать программу, которая читает построчно текстовый файл и
    переставляет случайно слова в каждой строке
```

**Пояснение**

Программа открывает существующий тектстовый файл и читает его построчно. 
Для каждой строки вызывается функция, разработанная в рамках задачи 1.


**Состав**

Программа должна состоять из функций:

```
   - char * randomWords(char * in, char *out) - функция, изменяющая порядок слов из in и записывающую их в out
   - int main()
```

Создается файл: main4.cpp. Используется также task1.h и task1.cpp
