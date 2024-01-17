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


Датасет содержит все транзакции, произошедшие за период с 01/12/2010 по 09/12/2011, для базирующейся в Великобритании компании, занимающейся розничной онлайн-торговлей. Многие клиенты являются оптовиками.