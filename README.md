# 🧌 Locators
* // - поиск по всему документу
* / - ищем только следующий элемент родителя
* /.. - поднимаемся выше
### 1. Поиск с предикатом (при таком указании, ищется точно по слову container)
```python
//div[@class='container']
//div[@class='container']/ul/li[1] #Поиск по container -> первый элемент ul 
//a[@class='guide-tags__badge-link custom-btn-amp-events' and @title='Automated UI Testing'] #Поиск по нескольким атрибутам
//a[contains(@href, 'example.com')] #Поиск по частичному совпадению (можно указать два contains)
```
### 2. Не должен содержать элемент 
  ```python
//a[contains(@href, 'example.com') and not(contains(@text(), 'kitty')]
  ```
### 3. Поиск по id
  ```python
//div[@id='good']
  ```
### 4. Ищем следующий элемент 
```python
//div[contains(@class, 'guide-template__tags')]/div
  ```
### 5.  Найти все элементы с классом example
```python
//*[@class='example']
  ```
### 6. Поиск по осям
```python
//select/ancestor::div #Находит все элементы <div>, которые являются предками (ancestors) элемента <select>.
//select/ancestor-or-self::div #Находит все элементы <div>, которые являются предками или самим элементом <select> (если <select> находится внутри <div>)
//div[@class='sort']/select #Находит элемент <select>, который является прямым потомком элемента <div> с классом sort
//div[@class='sort']/child::select #Аналогично предыдущему, но с использованием оси child. Находит элемент <select>, который является прямым потомком элемента <div> с классом sort
//div[@class='sort']/descendant::* #Находит все элементы, которые являются потомками (descendants) элемента <div> с классом sort
//div[@class='sort']/descendant-or-self::* #Находит все элементы, которые являются потомками или самим элементом <div> с классом sort.
//div[@class='sort']/following::* #Находит все элементы, которые идут после элемента `<div>` с классом sort в документе
//div[@class='sort']/following-sibling::* #Находит все элементы, которые идут после элемента <div> с классом sort в документе
//div[@class='sort']/.. #Находит родительский элемент элемента <div> с классом sort.
//div[@class='sort']/preceding::* #Находит все элементы, которые идут перед элементом <div> с классом sort в документе
//div[@class='sort']/preceding-sibling::* #Находит все элементы, которые являются соседями (siblings) элемента <div> с классом sort и идут перед ним
//div[@class='sort']/. #Находит сам элемент <div> с классом sort. Точка (`.`) обозначает текущий контекст.
  ```
### 7. Поиск по mat
```python
//input[@type='text' and @name='username']
//input[@type='text' or @type='password']
//input[@age>5]
//input[@age<5 and @age>2]
  ```
### 8. Поиск вложенным элементам
```python
//div[@class='container']//li
  ```
### 9. Поиск по позициям
```python
//ul/li[1]
//ul/li[last()]
//ul/li[last()-1]
  ```
### 10. Поиск по тексту
```python
//button[text()='Submit']
//a[contains(text(), 'Login')]
  ```
## Полезные ссылки:
* https://habr.com/ru/articles/817555/
* https://hackr.io/blog/xpath-cheat-sheet
