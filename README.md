# Опис основних таблиць

## База Oblkred
"Пісочниця" для ДпУР.

### dic.Branchs
Відділення.

| Назва поля | Тип даних | Опис |
|:----|:----|:----|
| ID | int | ID відділення. |
| Name | varchar(100) | |
|  |  | |
|  |  | |
|  |  | |
|  |  | |
|  |  | |

### <a herf="dic.Products.md">dic.Products</a>
Продукти.

### mis.Credits
Кредитні угоди.

| Назва поля | Тип даних | Опис |
|:----|:----|:----|
| Treatyid | int | ID угоди. Для старих угод відповідає коду угоди зі Скруджа. Для нових угод з Б2 код формується за правилом DEALID + 4 000 000, де DEALID - це код угоди з Б2. |
| MainMoniker | varchar(20) | Основний рахунок угоди. |
| BeginDate | datetime | Дата угоди. |
| EndDate | datetime | Очікувана дата закриття угоди. |
| CloseDate | datetime | Фактична дата закриття угоди. |
| ProductId | int | ID продукту з довідника <a href="#PRODUCTS">dic.Products</a>. |
| BranchId | int | ID відділення з довідника <a href="#BRANCHS">dic.Branchs</a>. |
| ClientId | int | ID клієнта з HD.dbo.Clients. |
| CurrencyId | int | ID валюти. |
| CredAmount | float | Початкова сума кредиту. |
| CredAmountUAH| float | Початкова сума кредиту у грн. (по курсу на дату кредиту). |
| ClientCode | varchar(10) | ClientCode з <a href="#PRODUCTS">dic.Products</a>. Одна з основних характеристик продукту, по якій здійснюється базовий поділ на типи продуктів: готівка, карта, МСБ та ін. |
| FirstPayment | float | Сума першого платежу. |
| FirstPaymentDate | datetime | Планова дата першого платежу. |
| SecondPayment | float | Сума другого платежу. |
| SecondPaymentDate | datetime | Планова дата другого платежу. |
| ThirdPayment | float | Сума третього платежу. |
| ThirdPaymentDate | float | Планова дата третього платежу. |
| FirstPaymentMinDate | datetime | Дата, з якої сума здійснених платежів є не меншою, ніж 10 грн. |
| FirstPayment90Date | datetime | Дата, з якої сума здійснених платежів перекриває 90% першого платежу. |
| FirstPaymentAllDate | dateime | Дата, з якої сума здійснених платежів перекриває 100% першого платежу. |
| SecondPaymentMinDate | datetime | Дата, з якої сума здійснених платежів є не меншою, ніж 10 грн. |
| SecondPayment90Date | datetime | Дата, з якої сума здійснених платежів перекриває 90% першого+другого платежу.|
| SecondPaymentAllDate | datetime | Дата, з якої сума здійснених платежів перекриває 100% першого+другого платежу. |
| ThirdPaymentMinDate | datetime | Дата, з якої сума здійснених платежів є не меншою, ніж 10 грн. |
| ThirdPayment90Date | datetime | Дата, з якої сума здійснених платежів перекриває 90% першого+другого+третього платежу. |
| ThirdPaymentAllDate | datetime | Дата, з якої сума здійснених платежів перекриває 100% першого+другого+третього платежу. |
||||
||||

---
