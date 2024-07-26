# AndriyCo.Shopdesk.ZReport
Опис касового Z звіту

## <a id="table1">Таблиця 1. Звіт
|Ім'я елементу|[req](## "Обов'язкове поле: '+' - так, '-' - ні")|Тип даних|Опис|
|:---|:---:|:---|:---|
|AmountOfReturnsBonus            | + |Double |Сума повернення бонусів|
|AmountOfReturnsCard             | + |Double |Сума повернень на карти|
|AmountOfReturnsCash             | + |Double |Сума повернень готівкою|
|AmountOfReturnsCertificate      | + |Double |Сума повернень з оплат сертфікатами|
|AmountOfReturnsCredit           | + |Double |Сума повернень з оплат у кредит (чеками)|
|AmountOfSales                   | + |Double |Сума продажів до застосування бонусних знижок (продаж = сума всіх оплат), а саме: AmountOfSales = AmountOfSalesCash + AmountOfSalesCard + AmountOfSalesCredit + AmountOfSalesCertificate + AmountOfSalesBonus|
|AmountOfSalesBonus              | + |Double |Сума оплат бонусами|
|AmountOfSalesCard               | + |Double |Сума оплат картками|
|AmountOfSalesCash               | + |Double |Сума оплат готівкою|
|AmountOfSalesCertificate        | + |Double |Сума оплат сертифікатами|
|AmountOfSalesCredit             | + |Double |Сума оплат у кредит (чеками)|
|AmountOfServicePayIn            | + |Double |Сума службових внесків|
|AmountOfServicePayOut           | + |Double |Сума службових виносів|
|ArrayOfDetails                  | + |Array  |Колекція Z звітів по кожній торговій точці (касі) – див. далі|
|CreatedByUser                   | + |Long   |ID користувача (касира), який створив Z звіт|
|CreatedByUserFullName           | + |String |Повне ім'я користувача (касира), який створив Z звіт|
|CreatedByUserName               | + |String |Логін користувача (касира), який створив Z звіт|
|DateOfIssue                     | + |Date   |Дата випуску Z звіту|
|DateOfReport                    | + |Date   |Дата створення Z звіту|
|DateOfStart                     | + |Date   |Дата першого документа зміни (дата відкриття зміни)|
|FranchiseeId                    | + |Long   |ID франчайзі|
|IssuedByUser                    | + |Long   |ID користувача (касира), який випустив Z звіт|
|IssuedByUserFullName            | + |String |Повне ім'я користувача (касира), який випустив Z звіт|
|IssuedByUserName                | + |String |Логін користувача (касира), який випустив Z звіт|
|NumberOfReceiptsReturn          | + |Long   |Підсумкове число чеків повернень по всіх точках|
|NumberOfReceiptsSales           | + |Long   |Підсумкова кількість чеків продажів по всіх точках|
|NumberOfReceiptsServicePayIn    | + |Long   |Підсумкове число чеків службових внесків за всіма точками|
|NumberOfReceiptsServicePayOut   | + |Long   |Підсумкове число чеків службових виносів по всіх точках|
|ReportGuid                      | + |GUID   |GUID звіту|
|ReportNumber                    | + |Long   |ID підсумкового Z звіту|
![image](https://github.com/user-attachments/assets/e0e3308b-b3fd-4702-a41e-4e3f2bd0d23a)
