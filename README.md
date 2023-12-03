# Туда-сюда, там-сям. Что-то здесь, что-то там. Что-то с одними, что-то с другими. Кручусь-верчусь. То вверх, то вниз. Тудым-сюдым
## Физическая модель базы данных, которая разработана с учетом третьей нормальной формы на платформе MySql workbench
![БД_фото](https://github.com/Starkidze/MySQL_educational_projects2/blob/main/222.png)

## Создание базы данных и таблиц
<pre class="mysql" style="font-family:monospace;font-size:10px;"><a href="http://search.oracle.com/search/search?group=MySQL&amp;q=CREATE"><span style="color: #990099; font-weight: bold;">CREATE</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=TABLE"><span style="color: #990099; font-weight: bold;">TABLE</span></a> author <span style="color: #FF00FF;">&#40;</span>
    author_id <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INT"><span style="color: #999900; font-weight: bold;">INT</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=PRIMARY%20KEY"><span style="color: #990099; font-weight: bold;">PRIMARY KEY</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=AUTO_INCREMENT"><span style="color: #FF9900; font-weight: bold;">AUTO_INCREMENT</span></a><span style="color: #000033;">,</span>
    name_author <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=VARCHAR"><span style="color: #999900; font-weight: bold;">VARCHAR</span></a><span style="color: #FF00FF;">&#40;</span><span style="color: #008080;">50</span><span style="color: #FF00FF;">&#41;</span>
<span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">;</span>
&nbsp;
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INSERT"><span style="color: #990099; font-weight: bold;">INSERT</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INTO"><span style="color: #990099; font-weight: bold;">INTO</span></a> author <span style="color: #FF00FF;">&#40;</span>name_author<span style="color: #FF00FF;">&#41;</span>
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=VALUES"><span style="color: #990099; font-weight: bold;">VALUES</span></a> <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Булгаков М.А.'</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
       <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Достоевский Ф.М.'</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
       <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Есенин С.А.'</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
       <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Пастернак Б.Л.'</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
       <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Лермонтов М.Ю.'</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">;</span>
&nbsp;
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=CREATE"><span style="color: #990099; font-weight: bold;">CREATE</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=TABLE"><span style="color: #990099; font-weight: bold;">TABLE</span></a> genre <span style="color: #FF00FF;">&#40;</span>
    genre_id <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INT"><span style="color: #999900; font-weight: bold;">INT</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=PRIMARY%20KEY"><span style="color: #990099; font-weight: bold;">PRIMARY KEY</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=AUTO_INCREMENT"><span style="color: #FF9900; font-weight: bold;">AUTO_INCREMENT</span></a><span style="color: #000033;">,</span>
    name_genre <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=VARCHAR"><span style="color: #999900; font-weight: bold;">VARCHAR</span></a><span style="color: #FF00FF;">&#40;</span><span style="color: #008080;">30</span><span style="color: #FF00FF;">&#41;</span>
<span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">;</span>
&nbsp;
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INSERT"><span style="color: #990099; font-weight: bold;">INSERT</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INTO"><span style="color: #990099; font-weight: bold;">INTO</span></a> genre<span style="color: #FF00FF;">&#40;</span>name_genre<span style="color: #FF00FF;">&#41;</span>
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=VALUES"><span style="color: #990099; font-weight: bold;">VALUES</span></a> <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Роман'</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
       <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Поэзия'</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
       <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Приключения'</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">;</span>
&nbsp;
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=CREATE"><span style="color: #990099; font-weight: bold;">CREATE</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=TABLE"><span style="color: #990099; font-weight: bold;">TABLE</span></a> book <span style="color: #FF00FF;">&#40;</span>
    book_id <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INT"><span style="color: #999900; font-weight: bold;">INT</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=PRIMARY%20KEY"><span style="color: #990099; font-weight: bold;">PRIMARY KEY</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=AUTO_INCREMENT"><span style="color: #FF9900; font-weight: bold;">AUTO_INCREMENT</span></a><span style="color: #000033;">,</span>
    title <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=VARCHAR"><span style="color: #999900; font-weight: bold;">VARCHAR</span></a><span style="color: #FF00FF;">&#40;</span><span style="color: #008080;">50</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
    author_id <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INT"><span style="color: #999900; font-weight: bold;">INT</span></a> <a href="http://dev.mysql.com/doc/refman/%35%2E%31/en/non-typed-operators.html"><span style="color: #CC0099; font-weight: bold;">NOT</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=NULL"><span style="color: #9900FF; font-weight: bold;">NULL</span></a><span style="color: #000033;">,</span>
    genre_id <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INT"><span style="color: #999900; font-weight: bold;">INT</span></a><span style="color: #000033;">,</span>
    price <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=DECIMAL"><span style="color: #999900; font-weight: bold;">DECIMAL</span></a><span style="color: #FF00FF;">&#40;</span><span style="color: #008080;">8</span><span style="color: #000033;">,</span> <span style="color: #008080;">2</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
    amount <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INT"><span style="color: #999900; font-weight: bold;">INT</span></a><span style="color: #000033;">,</span>
    <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=FOREIGN%20KEY"><span style="color: #990099; font-weight: bold;">FOREIGN KEY</span></a> <span style="color: #FF00FF;">&#40;</span>author_id<span style="color: #FF00FF;">&#41;</span>
        <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=REFERENCES"><span style="color: #990099; font-weight: bold;">REFERENCES</span></a> author <span style="color: #FF00FF;">&#40;</span>author_id<span style="color: #FF00FF;">&#41;</span>
        <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=ON"><span style="color: #990099; font-weight: bold;">ON</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=DELETE"><span style="color: #990099; font-weight: bold;">DELETE</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=CASCADE"><span style="color: #990099; font-weight: bold;">CASCADE</span></a><span style="color: #000033;">,</span>
    <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=FOREIGN%20KEY"><span style="color: #990099; font-weight: bold;">FOREIGN KEY</span></a> <span style="color: #FF00FF;">&#40;</span>genre_id<span style="color: #FF00FF;">&#41;</span>
        <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=REFERENCES"><span style="color: #990099; font-weight: bold;">REFERENCES</span></a> genre <span style="color: #FF00FF;">&#40;</span>genre_id<span style="color: #FF00FF;">&#41;</span>
        <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=ON"><span style="color: #990099; font-weight: bold;">ON</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=DELETE"><span style="color: #990099; font-weight: bold;">DELETE</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=SET"><span style="color: #990099; font-weight: bold;">SET</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=NULL"><span style="color: #9900FF; font-weight: bold;">NULL</span></a>
<span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">;</span>
&nbsp;
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INSERT"><span style="color: #990099; font-weight: bold;">INSERT</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INTO"><span style="color: #990099; font-weight: bold;">INTO</span></a> book <span style="color: #FF00FF;">&#40;</span>title<span style="color: #000033;">,</span> author_id<span style="color: #000033;">,</span> genre_id<span style="color: #000033;">,</span> price<span style="color: #000033;">,</span> amount<span style="color: #FF00FF;">&#41;</span>
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=VALUES"><span style="color: #990099; font-weight: bold;">VALUES</span></a>  <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Мастер и Маргарита'</span><span style="color: #000033;">,</span> <span style="color: #008080;">1</span><span style="color: #000033;">,</span> <span style="color: #008080;">1</span><span style="color: #000033;">,</span> <span style="color: #008080;">670.99</span><span style="color: #000033;">,</span> <span style="color: #008080;">3</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
        <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Белая гвардия '</span><span style="color: #000033;">,</span> <span style="color: #008080;">1</span><span style="color: #000033;">,</span> <span style="color: #008080;">1</span><span style="color: #000033;">,</span> <span style="color: #008080;">540.50</span><span style="color: #000033;">,</span> <span style="color: #008080;">5</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
        <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Идиот'</span><span style="color: #000033;">,</span> <span style="color: #008080;">2</span><span style="color: #000033;">,</span> <span style="color: #008080;">1</span><span style="color: #000033;">,</span> <span style="color: #008080;">460.00</span><span style="color: #000033;">,</span> <span style="color: #008080;">10</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
        <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Братья Карамазовы'</span><span style="color: #000033;">,</span> <span style="color: #008080;">2</span><span style="color: #000033;">,</span> <span style="color: #008080;">1</span><span style="color: #000033;">,</span> <span style="color: #008080;">799.01</span><span style="color: #000033;">,</span> <span style="color: #008080;">2</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
        <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Игрок'</span><span style="color: #000033;">,</span> <span style="color: #008080;">2</span><span style="color: #000033;">,</span> <span style="color: #008080;">1</span><span style="color: #000033;">,</span> <span style="color: #008080;">480.50</span><span style="color: #000033;">,</span> <span style="color: #008080;">10</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
        <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Стихотворения и поэмы'</span><span style="color: #000033;">,</span> <span style="color: #008080;">3</span><span style="color: #000033;">,</span> <span style="color: #008080;">2</span><span style="color: #000033;">,</span> <span style="color: #008080;">650.00</span><span style="color: #000033;">,</span> <span style="color: #008080;">15</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
        <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Черный человек'</span><span style="color: #000033;">,</span> <span style="color: #008080;">3</span><span style="color: #000033;">,</span> <span style="color: #008080;">2</span><span style="color: #000033;">,</span> <span style="color: #008080;">570.20</span><span style="color: #000033;">,</span> <span style="color: #008080;">6</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
        <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Лирика'</span><span style="color: #000033;">,</span> <span style="color: #008080;">4</span><span style="color: #000033;">,</span> <span style="color: #008080;">2</span><span style="color: #000033;">,</span> <span style="color: #008080;">518.99</span><span style="color: #000033;">,</span> <span style="color: #008080;">2</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">;</span>
&nbsp;
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=CREATE"><span style="color: #990099; font-weight: bold;">CREATE</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=TABLE"><span style="color: #990099; font-weight: bold;">TABLE</span></a> city <span style="color: #FF00FF;">&#40;</span>
    city_id <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INT"><span style="color: #999900; font-weight: bold;">INT</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=PRIMARY%20KEY"><span style="color: #990099; font-weight: bold;">PRIMARY KEY</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=AUTO_INCREMENT"><span style="color: #FF9900; font-weight: bold;">AUTO_INCREMENT</span></a><span style="color: #000033;">,</span>
    name_city <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=VARCHAR"><span style="color: #999900; font-weight: bold;">VARCHAR</span></a><span style="color: #FF00FF;">&#40;</span><span style="color: #008080;">30</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
    days_delivery <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INT"><span style="color: #999900; font-weight: bold;">INT</span></a>
<span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">;</span>
&nbsp;
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INSERT"><span style="color: #990099; font-weight: bold;">INSERT</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INTO"><span style="color: #990099; font-weight: bold;">INTO</span></a> city<span style="color: #FF00FF;">&#40;</span>name_city<span style="color: #000033;">,</span> days_delivery<span style="color: #FF00FF;">&#41;</span>
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=VALUES"><span style="color: #990099; font-weight: bold;">VALUES</span></a> <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Москва'</span><span style="color: #000033;">,</span> <span style="color: #008080;">5</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
       <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Санкт-Петербург'</span><span style="color: #000033;">,</span> <span style="color: #008080;">3</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
       <span style="color: #FF00FF;">&#40;</span><span style="color: #008000;">'Владивосток'</span><span style="color: #000033;">,</span> <span style="color: #008080;">12</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">;</span>
&nbsp;
<a href="http://search.oracle.com/search/search?group=MySQL&amp;q=CREATE"><span style="color: #990099; font-weight: bold;">CREATE</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=TABLE"><span style="color: #990099; font-weight: bold;">TABLE</span></a> client <span style="color: #FF00FF;">&#40;</span>
    client_id <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INT"><span style="color: #999900; font-weight: bold;">INT</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=PRIMARY%20KEY"><span style="color: #990099; font-weight: bold;">PRIMARY KEY</span></a> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=AUTO_INCREMENT"><span style="color: #FF9900; font-weight: bold;">AUTO_INCREMENT</span></a><span style="color: #000033;">,</span>
    name_client <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=VARCHAR"><span style="color: #999900; font-weight: bold;">VARCHAR</span></a><span style="color: #FF00FF;">&#40;</span><span style="color: #008080;">50</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
    city_id <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=INT"><span style="color: #999900; font-weight: bold;">INT</span></a><span style="color: #000033;">,</span>
    email <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=VARCHAR"><span style="color: #999900; font-weight: bold;">VARCHAR</span></a><span style="color: #FF00FF;">&#40;</span><span style="color: #008080;">30</span><span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">,</span>
    <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=FOREIGN%20KEY"><span style="color: #990099; font-weight: bold;">FOREIGN KEY</span></a> <span style="color: #FF00FF;">&#40;</span>city_id<span style="color: #FF00FF;">&#41;</span> <a href="http://search.oracle.com/search/search?group=MySQL&amp;q=REFERENCES"><span style="color: #990099; font-weight: bold;">REFERENCES</span></a> city <span style="color: #FF00FF;">&#40;</span>city_id<span style="color: #FF00FF;">&#41;</span>
<span style="color: #FF00FF;">&#41;</span><span style="color: #000033;">;</span></pre>
