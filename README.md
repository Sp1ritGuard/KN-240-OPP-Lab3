# Звіт до роботи №3
## Тема: _Основи ООП та перший клас_
### Мета роботи: _Навчитись створювати класи та обєкти та працювати з ними, розглянути основні елементи для побудови класу та навчитись працювати з ними_

---
### Виконання роботи
* Результати виконання завдання:
    1. Створили клас у цьому [файлі](my_class.py) та попрацювали з ним [у Пайтон ноутбуці](3.ipynb)
    2. Ознайомилися з базовими поняттями ООП:
        - Класи — це абстракція, а об'єкти — конкретна реалізація класів.
        - Імена класів завжди починаються з великої літери.
    3. Зрозуміли щоб працювати в пайтон ноутбуці потрібно кожного разу після зміні в класі перезавантажувати імпорти щоб він був оновлений. Ось як ми це робили

        ```python
        import importlib
        import my_class

        importlib.reload(my_class)
        ```
    4. Далі ми розглянули основні терміни щодо класів в Python:
        - функція взначена в середині класу наивається `методом`;
        - один з методів є особливим і називається `конструктором`;
        - існують також альтернативні коструктори, так звані класові методи;
        - в класах зʼявляється змінна `self` - вказівник на обʼєкт;
        - в середині класу є 2 типи змінних - класові змінні та атрибути класу;
        - існують так звані магічні методи, і всі вони мають подвіне підкреслення на початку і в кінці
        - Існують змінні та методи які не починаються з підкреслення `_` або `__` - з такими значеннями робите що   хочете і вони називаються публічними, якщо вже зявляється одинарне підкреслення `_` вони є захищеними і бажано їх не міняти, але ми можемо це робити. З подвійним підкресленням `__` називаються приватними і їх вже змінювати не можна.
    5. Наступне що ми розлядали це атрибути та властивості і дізналися, що атрибути це дані про наш обєкт які можна змінювати та що властивості це дані які можна лише читати. Також ми дізналися що атрибути можна змінювати та переписувати. Так само дізналися що переприсвоювати властивості не бажано
    6. Наступним ми розглядали шо таке Методи, які вони бувають та змінні self. Дізналися що методи можуть бути викликані як з об'єкту так і з класу передавши об'єкт

        - `self` - вказівник на об'єкт, завжди виступає першою змінною у методах класу. При виклику методу клау з об'єкта, self неявно присвоюється самому об'єкту
        - `self` - коли ми маємо виклик з класу то присвоєння є явним і ми маємо передати перший аргумент який є об'єктом
        - існують методи яким не потрібен об'єкт, тобто це дії які не впливають на об'єкт або не працюють з його атрибутами
        - методи без посилання на об'єкт називаються статичними методами, потребують при створенні використання декоратора `staticmethod`

    7. Також ми дізналися що в Python існіють декоратори такі як `@property`, `@classmethod`,`staticmethod`
    ### `staticmethod`
    - Використовується для методів, які не працюють ні з об'єктом, ні з класом.
    - Це звичайна функція, яка поміщена всередину класу для логічного групування.
    - `@staticmethod` дозволяє викликати метод без створення об'єкта.
    - Використовується для функцій, які не залежать від стану класу або об'єкта.

    ### `@classmethod`
    - Використовується для методів, які працюють із самим класом, а не з конкретним об'єктом.
    - Отримує клас як перший аргумент (cls), замість об'єкта (self).
    - Зручно для створення фабричних методів, які створюють нові об'єкти.

    ### `@property`
    - Використовується для створення гетерів (методів, які виглядають як атрибути).
    - Дозволяє отримати доступ до методу як до звичайного атрибута об'єкта.
    - Зручно, коли вам потрібно виконати обчислення або перевірку перед поверненням значення.
    
### Ось коротке порівняння декорторів: 
| Декоратор       | Доступ до `self` (об'єкта) | Доступ до `cls` (класу) | Використовується для...                |
|------------------|----------------------------|-------------------------|----------------------------------------|
| `@property`      | Так                        | Ні                      | Створення властивостей (гетери/сетери) |
| `@classmethod`   | Ні                         | Так                     | Методи, що працюють із класом          |
| `@staticmethod`  | Ні                         | Ні                      | Незалежні функції, логічно прив'язані до класу |


---
### Висновок:

- :question: Що зроблено в роботі: Ознайомилися з поняттями класів і об'єктів, імпортували класи до Python Notebook.
- :question: Чи досягнуто мети роботи: Мету роботи досягнуто
- :question: Які нові знання отримано: Навчилися працювати з класами та розуміти їх оновлення при імпорті.
- :question: Чи вдалось відповісти на всі питання задані в ході роботи: Так, вдалося.
- :question: Чи вдалося виконати всі завдання: Так, завдання виконані.
- :question: Чи виникли складності у виконанні завдання: Складнощів не виникло.
- :question: Чи подобається такий формат здачі роботи (Feedback): Формат зрозумілий і зручний.
- :question: Побажання для покращення (Suggestions): Немає

---