# Сегментирование клиентов онлайн-магазина подарков

### **Бизнес-задача:**  
 произвести сегментацию существующих клиентов, проинтерпретировать эти сегменты и определить стратегию взаимодействия с ними.

### **Техническая задача:**  
 построить модель кластеризации клиентов на основе их покупательской способности, частоты заказов и срока давности последней покупки, определить профиль каждого из кластеров.

### **Основные цели проекта:**
1. Произвести предобработку набора данных.
2. Провести разведывательный анализ данных и выявить основные закономерности.
3. Сформировать категории товаров и клиентов. 
4. Построить несколько моделей машинного обучения, решающих задачу кластеризации клиентов, определить количество кластеров и проинтерпретировать их.
5. Спроектировать процесс предсказания категории интересов клиента и протестировать вашу модель на новых клиентах.

### **Проект будет состоять из шести частей:**

1) Базовый анализ и знакомство с данными

Знакомство с исходными данными и их структурой.

2) Предобработка и очистка данных

Подготовим датасет для кластеризации, очистив его от пропусков, дублей, выбросов и другого «мусора».

3) Разведывательный анализ данных (EDA)

Произведём небольшое исследование данных, первые закономерности и гипотезы.

4) RFM-сегментация клиентов. Часть I

Используем популярный в маркетинге метод сегментации клиентов под названием RFM (Recency, Frequency, Monetary). На основе этого метода сформируем из исходного датасета о транзакциях таблицу с RFM-характеристиками клиентов и произведём их первичную сегментацию.

5) RFM-сегментация клиентов. Часть II

Расширим клиентские сегменты и создадим промежуточные категории с помощью нелинейных преобразований размерности. Это позволит произвести более качественную кластеризацию и улучшить стратегии взаимодействия с клиентами.

6) RFM-сегментация клиентов. Часть III

Необходимо построить модель классификации, которая позволит автоматически определять сегмент клиента на основе нескольких транзакций.


'customer_segmentation_project.csv' Датасет содержит все транзакции, произошедшие за период с 01/12/2010 по 09/12/2011, для базирующейся в Великобритании компании, занимающейся розничной онлайн-торговлей. Многие клиенты являются оптовиками.

Транзакции описываются следующими признаками:

* InvoiceNo — номер счёта-фактуры (уникальный номинальный шестизначный номер, присваиваемый каждой транзакции; буква "C" в начале кода указывает на отмену транзакции);
* Stock Code — код товара (уникальное пятизначное целое число, присваиваемое каждому отдельному товару);
* Description — название товара;
* Quantity — количество каждого товара за транзакцию; 
* InvoiceDate — дата и время выставления счёта/проведения транзакции;
* UnitPrice — цена за единицу товара в фунтах стерлингов;
* CustomerID — идентификатор клиента (уникальный пятизначный номер, однозначно присваиваемый каждому клиенту);
* Country — название страны, в которой проживает клиент.

### В проекте также воспользуемся RFM-анализом  
<center> <img src=https://miro.medium.com/max/1400/1*uYQjy9SUjW7iWHc2gGanQQ.png align="right" width="400"/> </center>

Метод заключается в группировке клиентов на основе следующих параметров:
* Recency (Давность) — давность последней покупки клиента;
* Frequency (Частота) — общее количество покупок клиента;
* Monetary Value (Денежная ценность) — сколько денег потратил клиент.


Суть RFM-анализа состоит в том, что мы разделяем всех клиентов на группы в зависимости от того, как давно они сделали последнюю покупку, как часто покупали и насколько большой была сумма их заказов.

Например, вот так может выглядеть интерпретация кластеров для случая RF-сегментации (анализа на основе давности и частоты заказов клиента):

<img src=https://retailrocket.ru/wp-content/uploads/2017/06/rfm-1.png>

Задача — вести клиента в зону лояльных.

Нужно рассчитать RFM-характеристики для каждого из клиентов в датасете, и на их основе с помощью методов кластеризации построить подобные сегменты клиентов.