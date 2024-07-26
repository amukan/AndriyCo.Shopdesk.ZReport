# Опис структури касового підсумкового звіту (Z звіту)


Підсумковий (дений, Z) звіт створюється касою в кінці зміни та включає в себе підсумкові значення за всіма торговими точками, що обслуговуються на цій касі та колекцію таких звітів по кожній з точок (окремо по фіскальній та нефіскальній касі).

Приклад імені файлу підсумкового звіту:

Z_REPORT_D753_F11_P19_U1_2024-07-26_16-00-15.tcurep, де:

* Z_REPORT – Z звіт
* D753 - Документ номер 753,
* F11  - ID франчайзі 11
* P19  - ID торгової точки 19
* U1   - ID касира (користувача облікової системи) 1
* Дата та час збереження файлу контейнера (2024-07-26_16-00-15)

## <a id="table1">Таблиця 1. Загальний підсумковий звіт
|Ім'я елементу|[req](## "Обов'язкове поле: '+' - так, '-' - ні")|Тип даних|Опис|
|:---|:---:|:---|:---|
|AmountOfCashWithdrawals         | + |Double |Сума зняття готівки з карток на касі|
|AmountOfReturnsBonus            | + |Double |Сума повернення бонусів|
|AmountOfReturnsCard             | + |Double |Сума повернень на картки|
|AmountOfReturnsCardOnline       | + |Double |Сума повернень на картки по чекам, сплаченим онлайн|
|AmountOfReturnsCash             | + |Double |Сума повернень готівкою|
|AmountOfReturnsCertificate      | + |Double |Сума повернень з оплат сертфікатами|
|AmountOfReturnsCredit           | + |Double |Сума повернень з оплат у кредит (чеками)|
|AmountOfSales                   | + |Double |Сума продажів до застосування бонусних знижок (продаж = сума всіх оплат), а саме: AmountOfSales = AmountOfSalesCash + AmountOfSalesCard + AmountOfSalesCredit + AmountOfSalesCertificate + AmountOfSalesBonus|
|AmountOfSalesBonus              | + |Double |Сума оплат бонусами|
|AmountOfSalesCard               | + |Double |Сума оплат картками|
|AmountOfSalesCardOnline         | + |Double |Сума оплат картками по чекам, сплаченим онлайн|
|AmountOfSalesCash               | + |Double |Сума оплат готівкою|
|AmountOfSalesCertificate        | + |Double |Сума оплат сертифікатами|
|AmountOfSalesCredit             | + |Double |Сума оплат у кредит (чеками)|
|AmountOfServicePayIn            | + |Double |Сума службових внесків|
|AmountOfServicePayOut           | + |Double |Сума службових виносів|
|ArrayOfDetails                  | + |Array  |Колекція [Z звітів по кожній торговій точці (касі)](#table2)|
|CreatedByUser                   | + |Int32  |ID користувача (касира), який створив Z звіт|
|CreatedByUserFullName           | + |String |Повне ім'я користувача (касира), який створив Z звіт|
|CreatedByUserName               | + |String |Логін користувача (касира), який створив Z звіт|
|DateOfIssue                     | + |Date   |Дата випуску Z звіту|
|DateOfReport                    | + |Date   |Дата створення Z звіту|
|DateOfStart                     | + |Date   |Дата першого документа зміни (дата відкриття зміни)|
|FranchiseeId                    | + |Int32  |ID франчайзі|
|IssuedByUser                    | + |Int32  |ID користувача (касира), який випустив Z звіт|
|IssuedByUserFullName            | + |String |Повне ім'я користувача (касира), який випустив Z звіт|
|IssuedByUserName                | + |String |Логін користувача (касира), який випустив Z звіт|
|NumberOfReceiptsCashWithdrawals | + |Int32  |Підсумкова кількість чеків зі зняттям готівки з картки на касі|
|NumberOfReceiptsReturn          | + |Int32  |Підсумкова кількість чеків повернень по всіх точках|
|NumberOfReceiptsSales           | + |Int32  |Підсумкова кількість чеків продажів по всіх точках|
|NumberOfReceiptsServicePayIn    | + |Int32  |Підсумкова кількість чеків службових внесків за всіма точками|
|NumberOfReceiptsServicePayOut   | + |Int32  |Підсумкова кількість чеків службових вилучень по всіх точках|
|ReportGuid                      | + |GUID   |GUID звіту|
|ReportNumber                    | + |Int32  |ID підсумкового звіту|

## <a id="table2">Таблиця 2. Елемент колекції звітів по торговій точці
|Ім'я елементу|[req](## "Обов'язкове поле: '+' - так, '-' - ні")|Тип даних|Опис|
|:---|:---:|:---|:---|
|AmountOfCashWithdrawals         | + |Double |Сума зняття готівки з карток на касі|
|AmountOfReturnsBonus            | + |Double |Сума повернення бонусів|
|AmountOfReturnsCard             | + |Double |Сума повернень на картки|
|AmountOfReturnsCardOnline       | + |Double |Сума повернень на картки по чекам, сплаченим онлайн|
|AmountOfReturnsCash             | + |Double |Сума повернень готівкою|
|AmountOfReturnsCertificate      | + |Double |Сума повернень з оплат сертфікатами|
|AmountOfReturnsCredit           | + |Double |Сума повернень з оплат у кредит (чеками)|
|AmountOfSales                   | + |Double |Сума продажів до застосування бонусних знижок (продаж = сума всіх оплат), а саме: AmountOfSales = AmountOfSalesCash + AmountOfSalesCard + AmountOfSalesCredit + AmountOfSalesCertificate + AmountOfSalesBonus|
|AmountOfSalesBonus              | + |Double |Сума оплат бонусами|
|AmountOfSalesCard               | + |Double |Сума оплат картками|
|AmountOfSalesCardOnline         | + |Double |Сума оплат картками по чекам, сплаченим онлайн|
|AmountOfSalesCash               | + |Double |Сума оплат готівкою|
|AmountOfSalesCertificate        | + |Double |Сума оплат сертифікатами|
|AmountOfSalesCredit             | + |Double |Сума оплат у кредит (чеками)|
|AmountOfServicePayIn            | + |Double |Сума службових внесків|
|AmountOfServicePayOut           | + |Double |Сума службових виносів|
|ChequeFiles                     | + |String |Перелік чеків, які увійшли у поточний звіт, а саме імен файлів чеків та їх гвідів через кому у наступному форматі: ім'я чека №1:{GUID чека №1}, ім'я чека №2:{GUID чека №2}, ..., ім'я чека №N:{GUID чека №N}|
|DepartmentId                    | + |Int32  |ID торгової точки|
|FiscalRegisterFiscalNumber      | + |String |Фіскальний номер реєстратора із налаштувань ShopDesk. Для ПРРО Checkbox дані беруться безпосередньо із конфігурації ПРРО|
|FiscalRegisterId                | + |String |Внутрішній ID фіскального реєстратора, що відповідає його моделі|
|FiscalRegisterName              | + |String |Коротка назва із фіскального реєстратора налаштувань ShopDesk|
|FiscalRegisterSerialNumber      | + |String |Серійний номер реєстратора із налаштувань ShopDesk. Для ПРРО Checkbox дані беруться безпосередньо із конфігурації ПРРО|
|Id                              | + |Int32  |ID звіту|
|IsFiscal                        | + |Byte   |0 – нефіскальна каса, 1 – фіскальна каса|
|NumberOfReceiptsCashWithdrawals | + |Int32  |Підсумкова кількість чеків зі зняттям готівки з картки на касі|
|NumberOfReceiptsReturn          | + |Int32  |Підсумкова кількість чеків повернень|
|NumberOfReceiptsSales           | + |Int32  |Підсумкова кількість чеків продажів|
|NumberOfReceiptsServicePayIn    | + |Int32  |Підсумкова кількість чеків службових внесків|
|NumberOfReceiptsServicePayOut   | + |Int32  |Підсумкова кількість чеків службових вилучень|


# Зразок підсумкового денного звіту

1. Службове внесення 1093.20 грн (1 документ)
2. Продажі на суму 24913.40 грн (145 документів)
3. Службове вилучення 26006.60 грн (1 документ)

```xml
<?xml version="1.0" encoding="windows-1251"?>
<ArrayOfReports xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" software="Shopdesk 5.24.704 ©ANDRIY.CO" wpGuid="{DC8AA91F-9BDA-4DEE-936B-0D5F684EA1CA}" wpName="Shopdesk ЧЧ Маркет Галатерея" originalFileName="Z_REPORT_D753_F0_P19_U1_2024-07-26_16-00-15.tcurep" hash="3542b0c963281cac14b2f620b7918397">
  <Report>
    <AmountOfCashWithdrawals>0.00</AmountOfCashWithdrawals>
    <AmountOfReturnsBonus>0.00</AmountOfReturnsBonus>
    <AmountOfReturnsCard>0.00</AmountOfReturnsCard>
    <AmountOfReturnsCardOnline>0.00</AmountOfReturnsCardOnline>
    <AmountOfReturnsCash>0.00</AmountOfReturnsCash>
    <AmountOfReturnsCertificate>0.00</AmountOfReturnsCertificate>
    <AmountOfReturnsCredit>0.00</AmountOfReturnsCredit>
    <AmountOfSales>24913.40</AmountOfSales>
    <AmountOfSalesBonus>0.00</AmountOfSalesBonus>
    <AmountOfSalesCard>0.00</AmountOfSalesCard>
    <AmountOfSalesCardOnline>0.00</AmountOfSalesCardOnline>
    <AmountOfSalesCash>24913.40</AmountOfSalesCash>
    <AmountOfSalesCertificate>0.00</AmountOfSalesCertificate>
    <AmountOfSalesCredit>0.00</AmountOfSalesCredit>
    <AmountOfServicePayIn>1093.20</AmountOfServicePayIn>
    <AmountOfServicePayOut>26006.60</AmountOfServicePayOut>
    <ArrayOfDetails>
      <Detail>
        <AmountOfCashWithdrawals>0.00</AmountOfCashWithdrawals>
        <AmountOfReturnsBonus>0.00</AmountOfReturnsBonus>
        <AmountOfReturnsCard>0.00</AmountOfReturnsCard>
        <AmountOfReturnsCardOnline>0.00</AmountOfReturnsCardOnline>
        <AmountOfReturnsCash>0.00</AmountOfReturnsCash>
        <AmountOfReturnsCertificate>0.00</AmountOfReturnsCertificate>
        <AmountOfReturnsCredit>0.00</AmountOfReturnsCredit>
        <AmountOfSales>24913.4</AmountOfSales>
        <AmountOfSalesBonus>0.00</AmountOfSalesBonus>
        <AmountOfSalesCard>0.00</AmountOfSalesCard>
        <AmountOfSalesCardOnline>0.00</AmountOfSalesCardOnline>
        <AmountOfSalesCash>24913.4</AmountOfSalesCash>
        <AmountOfSalesCertificate>0.00</AmountOfSalesCertificate>
        <AmountOfSalesCredit>0.00</AmountOfSalesCredit>
        <AmountOfServicePayIn>1093.20</AmountOfServicePayIn>
        <AmountOfServicePayOut>26006.60</AmountOfServicePayOut>
        <ChequeFiles>(!!!Перелік скорочено. Тут мало б бути 147 пар імен та GUID!!!) 
        	DOC_D355360_F0_P19_U1_2024-07-23_07-13-12.tcudoc:{194941A4-03A1-42F0-820D-93F79FDAEA87}, 
        	DOC_D355361_F0_P19_U1_2024-07-23_07-14-01.tcudoc:{F3B2BF1D-FE39-45A6-95A2-64C3B5466720}, 
        	DOC_D355362_F0_P19_U1_2024-07-23_07-26-20.tcudoc:{71F8B24B-DD7B-430E-9092-5B4A40DCAA35}, 
        	DOC_D355363_F0_P19_U1_2024-07-23_07-27-21.tcudoc:{514E5319-1C1D-4F7B-947D-EB2D71CF86B9}, 
        	DOC_D355504_F0_P19_U1_2024-07-23_12-46-10.tcudoc:{05201458-A0BD-43BC-9DCF-BB61C92D5089}, 
        	DOC_PAYTRANSFER_D355359_F0_P19_U1_2024-07-23_07-12-09.tcudoc:{82C9CEC6-9169-4423-805F-8758517DB4C3}, 
        	DOC_PAYTRANSFER_D355505_F0_P19_U1_2024-07-26_15-59-32.tcudoc:{E6198DC9-B51A-4965-8F26-A404160B6A82}</ChequeFiles>
        <DepartmentId>19</DepartmentId>
        <FiscalRegisterFiscalNumber></FiscalRegisterFiscalNumber>
        <FiscalRegisterId>0</FiscalRegisterId>
        <FiscalRegisterName></FiscalRegisterName>
        <FiscalRegisterSerialNumber></FiscalRegisterSerialNumber>
        <Id>759</Id>
        <IsFiscal>0</IsFiscal>
        <NumberOfReceiptsCashWithdrawals>0</NumberOfReceiptsCashWithdrawals>
        <NumberOfReceiptsReturn>0</NumberOfReceiptsReturn>
        <NumberOfReceiptsSales>145</NumberOfReceiptsSales>
        <NumberOfReceiptsServicePayIn>1</NumberOfReceiptsServicePayIn>
        <NumberOfReceiptsServicePayOut>1</NumberOfReceiptsServicePayOut>
      </Detail>
    </ArrayOfDetails>
    <CreatedByUser>1</CreatedByUser>
    <CreatedByUserFullName>Касир</CreatedByUserFullName>
    <CreatedByUserName>Касир</CreatedByUserName>
    <DateOfIssue>2024-07-26 16:00:15</DateOfIssue>
    <DateOfReport>2024-07-26 16:00:13</DateOfReport>
    <DateOfStart>2024-07-23 07:12:09</DateOfStart>
    <FranchiseeId>0</FranchiseeId>
    <IssuedByUser>1</IssuedByUser>
    <IssuedByUserFullName>Касир</IssuedByUserFullName>
    <IssuedByUserName>Касир</IssuedByUserName>
    <NumberOfReceiptsCashWithdrawals>0</NumberOfReceiptsCashWithdrawals>
    <NumberOfReceiptsReturn>0</NumberOfReceiptsReturn>
    <NumberOfReceiptsSales>145</NumberOfReceiptsSales>
    <NumberOfReceiptsServicePayIn>1</NumberOfReceiptsServicePayIn>
    <NumberOfReceiptsServicePayOut>1</NumberOfReceiptsServicePayOut>
    <ReportGuid>{694E12D4-CE52-4645-BFF6-EAC92B923CFF}</ReportGuid>
    <ReportNumber>753</ReportNumber>
  </Report>
</ArrayOfReports>
```
