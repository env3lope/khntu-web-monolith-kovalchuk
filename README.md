## Предметна область опис предметної області "Інтернет-магазин"

Предметною областю є інформаційна система інтернет-магазину, призначена для зберігання та обробки інформації про користувачів, товари, категорії товарів і замовлення. Користувач може створювати замовлення, кожне з яких містить один або декілька товарів. Один товар може входити до багатьох різних замовлень. Для представлення зв'язку між замовленнями та товарами використовується проміжна сутність `ORDER_ITEM`, яка додатково зберігає кількість товару та його ціну на момент придбання. Кожен товар належить до певної категорії. Одна категорія може містити багато товарів.

### ER-діаграма
[![](https://mermaid.ink/img/pako:eNqNU21r2zAQ_iviPqfBdlu_fQtJNsooCWn6YcNQhKQ6YrbkySdomuS_V47tJIvLOoFBeu65u-fufDtgmgtIQZiZpLmhZaaIO89P8xXZ729u9I4sVjP3SElVUCbq1j6drOffF6ufPWe5Wsyep2vHYlohlarjtb4Nad8FenlYzx8HvN7_MmXPlIoVlgv-IlWmLuTt2ntzpEIiOVn-OEM1GqlyIkoqiwGqaCkGoNFFBx76PK38fydqIFsL88DJtwuYUxQoS0GYEe7KJ3i2vRaaIkGNtJiU2iocaKmRoq2v1PRN-loPcxlzbbZXmrrgKLEQ12oqI9l1-acp_1erz039u3_tHL8WrQ0fdLHBK6O5ZfiJ5Y-lyhWz_bSWCS6tYRta96JgBLmRHNJXWtRiBKUw7udwbzhqywA3wlUAqbtyan5nkKnGqaLql9YlpGisczPa5ptTEFs1g-5250QRypUybSYL6Z13f4wB6Q7eIA1ib5z4_t1tlMRxEPuBs24hjbzxrQPDJPD8MHTfYQTvx6zeOL6P_MiL_SgIAy9MkhEILlGbx3Z1jxt8-AD2Qhug?type=png)](https://mermaid.ai/live/edit#pako:eNqNU21r2zAQ_iviPqfBdlu_fQtJNsooCWn6YcNQhKQ6YrbkySdomuS_V47tJIvLOoFBeu65u-fufDtgmgtIQZiZpLmhZaaIO89P8xXZ729u9I4sVjP3SElVUCbq1j6drOffF6ufPWe5Wsyep2vHYlohlarjtb4Nad8FenlYzx8HvN7_MmXPlIoVlgv-IlWmLuTt2ntzpEIiOVn-OEM1GqlyIkoqiwGqaCkGoNFFBx76PK38fydqIFsL88DJtwuYUxQoS0GYEe7KJ3i2vRaaIkGNtJiU2iocaKmRoq2v1PRN-loPcxlzbbZXmrrgKLEQ12oqI9l1-acp_1erz039u3_tHL8WrQ0fdLHBK6O5ZfiJ5Y-lyhWz_bSWCS6tYRta96JgBLmRHNJXWtRiBKUw7udwbzhqywA3wlUAqbtyan5nkKnGqaLql9YlpGisczPa5ptTEFs1g-5250QRypUybSYL6Z13f4wB6Q7eIA1ib5z4_t1tlMRxEPuBs24hjbzxrQPDJPD8MHTfYQTvx6zeOL6P_MiL_SgIAy9MkhEILlGbx3Z1jxt8-AD2Qhug)

## Зв'язки між сутностями

- `USER` - `ORDER` 1:N. Один користувач може створити багато замовлень, а кожне замовлення належить одному користувачу.
- `CATEGORY` - `PRODUCT` 1:N. Одна категорія може містити багато товарів, а кожен товар належить одній категорії.
- `ORDER` - `PRODUCT` N:M. Одне замовлення може містити багато товарів, а один товар може входити до багатьох замовлень. Зв'язок реалізується через проміжну сутність `ORDER_ITEM`.
- `ORDER` - `ORDER_ITEM` 1:N. Одне замовлення може містити багато записів `ORDER_ITEM`.
- `PRODUCT` - `ORDER_ITEM` 1:N. Один товар може бути присутнім у багатьох записах `ORDER_ITEM`.
