# Piton-dz

# Задача 10: 
# На столе лежат n монеток. Некоторые из них лежат вверх
#  решкой, а некоторые – гербом. Определите минимальное число
#  монеток, которые нужно перевернуть, чтобы все монетки были
#  повернуты вверх одной и той же стороной. Выведите минимальное
#  количество монет, которые нужно перевернуть.

from random import randint

n = int(input("Введите кол-во монет: "))
count = 0
for i in range(n):
    # генерируем монетки 1 - орел,  0 - решка
    v = randint(0,1) 
    # считаем сколько выпало монеток орлом
    if v == 1:
        count += 1
    # выводим в консль выпавшие монетки
    print(v, end = " ")
print()
# если монеток орлом меньше чем половина то переворачиваем монетки с орлом
if count < n/2:
    print(count)
else:
# иначе переворачиваем монетки с решкой
    print (n-count)
  
    # Задача 12: ДЗ 
# Петя и Катя – брат и сестра. Петя – студент, а Катя –
#  школьница. Петя помогает Кате по математике. Он задумывает два
#  натуральных числа X и Y (X,Y≤1000), а Катя должна их отгадать. Для
#  этого Петя делает две подсказки. Он называет сумму этих чисел S и их
#  произведение P. Помогите Кате отгадать задуманные Петей числа.

import math
#  Вводим исходные данные, сумму = s и произведение = p
s = int(input("Введите сумму 2-х чисел: "))
p = int(input("Введите произведение 2-х чисел: "))

# приводим к квадратному уравнению x * x - s * x + p = 0
# находим дискриминант d
d = ((-s) * (-s)) - 4 * p
print(f"Дискриминант равен = {d}")
if d < 0:
    print ("Уравнение не имеет решение")
elif d > 0:
    x = int((s - math.sqrt(d)) / 2)
    y = int((s + math.sqrt(d)) / 2)
    print (f"Первое число = {x}")
    print (f"Второе число = {y}")
else:
    x = int((s)/2)
    print (f"Первое число = {x}")
    print (f"Второе число = {x}")
  
    # Задача 14: ДЗ 
# Требуется вывести все целые степени двойки (т.е. числа вида 2k), не превосходящие числа N.
# 10 -> 1 2 4 8

n = int(input("Введите число N: "))
pow = 1 
while pow <= n: 
    print (pow, end = ' ') 
    pow = pow * 2
