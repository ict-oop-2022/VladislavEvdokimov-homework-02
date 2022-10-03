# Троеборье (Вторая домашка)

Данная домашка состоит из двух частей -- одна из них
обязательна для всех, а вторая является дополнительным заданием на бонусные баллы (10 доп. баллов)

Если вы хотите выбрать выбрать простую
версию домашки (по-умолчанию выбрана сложная версия). Для
этого надо отредактировать файл `CMakeLists.txt` 
согласно комментарию в первой его строке.

## Число (Обязательна)

Суть первой части реализовать класс, который прикидывается
числом.

Нужно реализовать кучу всяких штук:
1) Конструкторы (пустой, копирования, от числа)
2) Оператор присвоения
3) Каст (`bool`, числу, `std::string`)
4) Бинарные арифметические и битовые операторы
5) Унарные операторы   
6) Операторы инкремента и декремента
7) Операторы сравнения
8) Операторы вывода в поток и ввода из потока

Для реализации домашки вам надо редактировать файлы 
`number/number.h` и `number/number.cpp` 
(Напомню, что в хедер мы помещаем декларации, а цпп-шник -- реализации)

(В целом там достаточно мощные тесты. Если тесты проходят, то скорее всего
вы сделали все правильно)

(Ну и еще раз хочу отметить что числа в плюсах не бесконечные)

## Бор (Опционально)

Описание структруры данных и псевдо-реализация основных методов:

https://habr.com/ru/post/111874/

В файле `trie/trie.h` лежит декларация 
этого класса, там же указано, что каждый метод должен делать. 
В соотвествующем цпп-шнике вам надо реализовать
методы из этой декларации.

Там есть еще файлы с подстрокой `naive` -- это реализация
необходимая для тестов. Она реализует тот же интерфейс, но
совсем по-другому -- _наивно_. Подсматривать там особо нечего.

**ОБРАТИТЕ ВНИМАНИЕ, ЧТО СТРОКИ МОГУТ ПОВТОРЯТЬСЯ В КОНТЕЙНЕРЕ,
ИНЫМИ СЛОВАМИ, ЕСЛИ ДВАЖДЫ ДОБАВИТЬ КАКУЮ-ТО СТРОКУ, ТО ВО ВСЕХ
МЕТОДАХ ДОЛЖНЫ УЧИТЫВАТЬСЯ ВСЕ КОПИИ СТРОК**

В рамках этой части домашки вы можете править файлы `trie/trie.h` и
`trie/trie.cpp`

## Тестирование

Чтобы собрать и запустить тесты надо выполнить: 

`python3 scripts/run-tests.py`

Некоторые тесты достаточно нагруженные и часть задания уложить каждый тест 
в определенный таймаут -- плосекунды на тест.

Чтобы запустить тесты с проверкой скорости надо выполнить:

`python3 scripts/run-tests.py -c Release`

Соотвественно, если вы выбрали простую версию домашки, то код для бора
(сам код и тесты) собираться и запускаться не будут -- ни у вас, ни в github-е

Если у вас падает какой-то конкретный тест и вы хотите запускать только его,
то вы можете открыть файл в **CLion** `number/number-test.cpp` или 
`trie/trie-test.cpp` (смотря для какой части домашки вы хотите
запустить тест). Найти этот тест в коде и нажать на зеленый треугольничек 
слева от декларации теста. Единственный минус такого запуска в том, что
не будут проверены таймауты.
