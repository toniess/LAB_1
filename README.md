# LAB_1
Этот репозиторий создан для лабораторной работы №1 по ВвИТ.

## Отчет по Лабораторной работе

### 0. Постановка цели
Целью данной работы ставлю познакомиться с основой работы с терминалом, с системой контроля версий git и удаленным репозиторием GitHub. Также вспомнить синтаксис языка Python, написав несложную программу. 

### 1. Установка Python

Я установил python3 следующей командой:
`brew install python3`

### 2. Установка Git

Я установил Git следующей командой:
`brew install git`

### 3. Установка PyCharm
PyCharm уже был установлен, но я бы мог сделать это так:
`brew install pycharm`

### 4. Настройка директории проекта
В папке /Documents/ создал директорию `MyApp`
`mkdir MyApp && cd MyApp/`

Создал и активировал виртуально акружение python
`python3 -m venv venv`
`source ./venv/bin/activate`

<img width="947" alt="Снимок экрана 2022-09-27 в 21 45 26" src="https://user-images.githubusercontent.com/64589798/192610378-ecd141e5-d5e8-48d9-a05e-9ba21902c489.png">

### 5. Работа с файлами
Создал файл `main.py`
`touch main.py`

Открыл файл и вставил код из методички (Неудобно использовать тяжелый PyCharm)
`micro main.py`

<img width="949" alt="Снимок экрана 2022-09-27 в 21 52 48" src="https://user-images.githubusercontent.com/64589798/192611633-00d89889-a800-4daf-bf13-02059ea9e2ef.png">

Сохранил код (ctrl-s), вышел (ctrl-q) и запустил код:
`python3 main.py`
и он работает, получаем вывод:

<img width="947" alt="Снимок экрана 2022-09-27 в 21 51 15" src="https://user-images.githubusercontent.com/64589798/192611383-173254fd-6812-47a3-ae8d-25708e7c1bfa.png">


### 6. Отправка изменений на удаленный реп.
Проинициализировал новый репозиторий:
`git init`

Добавил в индекс **только** файл `main.py`:
`git add main.py`

Сделал локальный коммит:
`git commit -m "Find max square of triangles"`

<img width="940" alt="Снимок экрана 2022-09-27 в 21 57 00" src="https://user-images.githubusercontent.com/64589798/192612375-11300b59-265c-4a29-8cbe-e1a95c59baba.png">

Далее создал публичный репозитория на ГитХабе и подключился к нему
`-   git remote add origin <этот репозиторий>`

По совету Гитхаба прописал еще одну команду:
`git branch -M main`

И сделал пуш в удаленный реп.
`git push -u origin main`

Гит попросил авторизоваться на Хабе, вместо пароля ввёл сгенерированный в настройках профиля токен, и пуш улетел.

### 7. Домашнее задание.
Создал еще один файл для новой программы:
`micro equation.py`

Написал программку: 
```
#equation.py

#Обработка исключения при вводе
while True:
    try:
        a, b, c = map(float, input(
        "Введите коэффициенты a b c уравнения ax^2 + bx + c = 0 через пробел\n"
            ).split())
        break;
    except:
        print("Некорректный ввод")

D = b*b - 4*a*c
if a == 0:
    if b == 0:
        print (f"Это что за анаконда?)")
    else:
        print (f"Уравнение имеет 1 действительный корень: x = {-c / b}")
elif b == 0:
    x1 = (-c/a)**(1/2)
    x2 = -x1
    print (f"Уравнение имеет 2 действительных корня: x1 = {x1} \t x2 = {x2}")
elif D < 0:
    print (f"Уравнение не имеет действительных корней :(")
elif D == 0:
    print (f"Уравнение имеет 2 совпадающих действительных корня: x1 = x2 = {-b / 2 / a}")
else:
    sqrtD = D ** (1/2)
    x1 = (-b + sqrtD)/(2*a)
    x2 = (-b - sqrtD)/(2*a)
    print (f"Уравнение имеет 2 действительных корня: x1 = {x1} \t x2 = {x2}")
```

Далее, сохранил и вышел. Добавил файл в индекс гита, закоммитил и запушил.

```
git add equation.py
git commit -m "Find the roots of a quadratic equation"
git push -u origin main
``` 

Проверяем 'git log'

<img width="947" alt="Снимок экрана 2022-09-28 в 00 23 34" src="https://user-images.githubusercontent.com/64589798/192640034-e70d3062-8437-47c7-8e5d-094ed8144a96.png">


Вот и все, потом написал этот readme файл и также залил на гит). 

 
### 8. Вывод

В данной лабораторной работе я познакомился с системой контроля версий и удаленный репозиторием. написал программу и залил её на GitHub, работая через терминал. 
