**Основные понятия ООП.Классы,объекты.**

За основу возьмём класс "Ружьё", который выполняет функцию "Стрелять". Исходя из утверждения, что объект - это элемент (экземпляр) класса, то в данном случае к объектам данного класса можно отнести ствол, затвор, приклад и т.д..

**Наследование**

Наследование предполагает создание нового класса на основании уже существующего, с полным или частичным перенесением функционала. На примере: берём класс "Ружьё", меняем в нём объект "Гладкий ствол" на объект "Ствол нарезной". В итоге мы получаем новый класс (потомок) "Винтовка" с родительским (базовым) классом "Ружье". При этом фунционал базового класса (функция "Стрелять") полностью сохранился.

**Полиморфизм**

Данное свойство позволяет использовать объекты с одинаковым интерфейсом без знания их внутренней структуры.
То есть, у нас есть "Ружьё" и есть "Винтовка", они могут быть по разному устроены (разные типы стволов, спусковых 
механизмов и т.п.) но они выполняют одну функцию - "Стрелять". 

**Инкапсуляция**

Инкапсуляция - это сокрытие механизмов выполнения функции от пользователя, который взаимодейстует с объектом через интерфейс.
На примере это выглядит так: стрелок берёт в руки "Ружьё" и запускает функцию "Выстрелить", то есть просто стреляет.Суть инкапсуляции заключается в том, что стрелок взаимодействует с ружьём через интерфейс - предохранитель,курок. Он не видит как срабатывают ударные механизмы внутри стволовой коробки, и как пороховые газы выталкиват пулю. Это делается для удобства и безопасности пользователя. Ведь если бы механизмы были открыты для свободного доступа из-вне, то неосторожные действия пользователя и окружающая среда могли бы повредить механизм.

**Принципы SOLID**

1) Принцип единственной ответственности:
Каждый элемент "Ружья" отвечает только за свою функцию: боёк - за удар по капсулю, затвор - за выброс гильзы и пороховых газов. И всё это инкапсулировано - закрыто от пользователя в стволовой коробке.

2)Принцип открытости/закрытости:
Мы можем установить на "Винтовку" такие расширения как оптический прицел, магазин повышенной ёмкости, улучшеный приклад или подствольный гранатомёт, но внутренний механизм "Винтовки" закрыт для модификации.

3)Принцип подстановки Барбары Лисков:
Мы имеем базовый класс "Ружьё", производный класс - "Винтовка", и допустим, "Снайперская винтовка". Все производные классы могут заменять базовый, так как выполняют одну и ту же функцию - "Стрелять". 

4)Принцип разделения интерфейса:
Несколько специализированных интерфейсов лучше, чем один комплексный. На примере с "Винтовкой": у "Винтовки" есть предохранитель, переключатель режима стрельбы и спусковой курок. Они находятся раздельно друг от друга и каждый реализует свою функцию - всё чётко и практично. А теперь представим, что их свели в один громоздкий механизм. Тут то и начинается путаница - хотел выстрелить, а переключил режим стрельбы (случайно), хотел поставить на предохранитель - и случайно выстрелил. То есть один громоздкий интерфейс в данном случае не только неудобно, но и смертельно опасно. Исходя из этого можно утверждать, что несколько специализированных интерфейсов гораздо лучше, чем один комплексный. 

5)Принцип инверсии зависимостей (насколько смог понять):
"Ружье" это оружие, оно должно стрелять. Раз оно стреляет, то его рабочая часть должна быть выполнена из крепкого материала (из металла). Так как ружьё стреляет и у него есть отдача, то его надо удобно держать, для этого надо рукоять и приклад.

