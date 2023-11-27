# s21_decimal
Пишу для себя и для своей команды памятку по работе s21_decimal

[s21_decimal @lucankri 12.02.2023](https://youtu.be/kJU4JOLa8l0)
Смотрел недавно ролик на ютубе по этой теме, в целом довольно много интересных вещей говорит лектор, однако ошибки:
**тут надо бы вставить список ошибок**
Структура Decimal:
![[Pasted image 20231127034421.png]]

По этой структуре предлагается написать программу:
```c
typedef struct {
    int bits[4];
} s21_decimal;
```
Посмотрев и поработав с этим проектом я считаю что чуть удобнее будет использовать  `unsigned int`, потому что в нем не резервируется первый бит для знака числа
```c
typedef struct {
    unsigned int bits[4];
} s21_decimal;
```

Структура:
## Преобразования
##### Из `int`
```c
int s21_from_int_to_decimal(int src, s21_decimal *dst)
```
##### Из `float`
```c
int s21_from_float_to_decimal(float src, s21_decimal *dst)
```
##### В `int`
```c
int s21_from_decimal_to_int(s21_decimal src, int *dst)
```
##### В `float`
```c
int s21_from_decimal_to_float(s21_decimal src, float *dst)
```
