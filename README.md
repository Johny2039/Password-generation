# Password-generation


from random import randint as r
from os import system as s

chars = ('qwertyuiop[]\asdfghjkl;zxcvbnm,./QWERTYUIOP[]ASDFGHJKLZXCVBNM0123456789')

def create():
    n = int(input('Введите количество символов пароля: '))
    password = ''
    for i in range(n):
          password = f'{password}{chars[r(0, len(chars)-1)]}'
    print(password)

prog = True
while prog:
    create()
    k = int(input('Продолжить? (1/0): '))
    if k == 1:
        prog = True
    elif k == 0:
        prog == False
    s('cls')    
