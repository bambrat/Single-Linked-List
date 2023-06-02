## Single linked list<br>
Контейнер — односвязный список.
___
# Описание программы<br>
Работа над учебным проектом помогла мне лучше понять устройство контейнеров C++, а также научиться эффективно использовать их.

# Используемый стек:
  `forward_list` `Шаблонные классы` 
  
# Системые требования:
  1. C++17(STL)

## Использование: Загрузить файлы проекта в среду разработки для сборки. Вариант использования и тесты показаны в main.cpp.<br>

## Связный односвязный список, также известный как линейный список, является одной из основных структур данных, используемых в программировании. Понимание его работы является важным шагом в изучении более сложных структур данных. В стандартной библиотеке односвязный список представлен шаблоном класса `forward_list`.
<br>

### Реализованы конструктор и методы:
 Конструктор по умолчанию создаёт пустой список;<br>
 `GetSize` возвращает количество элементов в списке;<br>
 `IsEmpty` возвращает **true**, если список пустой, и **false** в противном случае.<br>
 `PushFront` вставляет элемента в начало односвязного списка.<br>
 `PushFront` гарантирует безопасность исключений: если в процессе работы метода будет выброшено исключение, состояние списка будет таким же, как до вызова метода.<br>
 `Clear` очищает список и не выбрасывает исключений. <br>
 При разрушении списка удаляются все его элементы.<br>
 `PopFront` удаляет первый элемента непустого списка за время **O(1)**. Не выбрасывает исключений.<br>
 `InsertAfter` вставляет в список новое значение следом за элементом, на который ссылается переданный в InsertAfter итератор. Гарантия безопасности исключений. Сложность **O(1)**<br>
 `EraseAfter` удаляет из списка элемент, следующий за элементом, на который ссылается переданный в `InsertAfter` итератор. Не выбрасывает исключений. **O(1)**<br>
 `before_begin` и `cbefore_begin` возвращают итераторы, ссылающиеся на фиктивную позицию перед первым элементом списка. Используется как параметр для методов `InsertAfter` и `EraseAfter`, когда нужно вставить или удалить элемент в начале списка. Разыменовывать этот итератор нельзя.<br>

### Реализован перебор элементов контейнера SingleLinkedList.
Класс `BasicIterator`, на основе которого объявлены константный и неконстантный итераторы списка.<br>
В классе списка есть константная и неконстантная версия методов `begin` и `end`, они возвращают итераторы на первый элемент контейнера и позицию, следующую за последним элементом. Созданы также методы `cbegin` и `cend`.<br>

 Операции сравнения ==, !=, <, >, <=, >=;<br>
 Обмен содержимого двух списков с использованием метода swap и шаблонной функции swap;<br>
