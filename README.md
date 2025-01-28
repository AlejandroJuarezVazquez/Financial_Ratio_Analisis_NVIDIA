# Nvidia_Financial_Analysis
In this project, I show Financial Ratios and their formulas from the last 4 fiscal years from NVIDIA using Financial Statements, one of the biggest and most important companies in the world nowadays. 

I used a lot of tools for this analysis, such as Python and Pandas for downloading the financial states by using the Yahoo Finance Library. Then, I used Excel for the study with all the financial ratios.

# Financial Statements

NVIDIA's Financial Statements can be found on the Yahoo! Finance site. This is the link:

https://finance.yahoo.com/quote/NVDA/financials/

This is a small lookup to the statements:

![image](https://github.com/user-attachments/assets/0913f79a-efdb-4688-bf87-8336c333f20c)

![image](https://github.com/user-attachments/assets/59651c18-74fe-4cc8-91cf-6f997a7f5190)

The complete statements can be found in this repository.

# Extracting Nvidia Financial Statements with Python
To extract the data I used the Yahoo Finance library in Python and pandas to export the data as CSV files.
```python
import yfinance as yf
import pandas as pd

ticker = "NVDA"  # Nvidia
empresa = yf.Ticker(ticker)

income_statement = empresa.financials

income_statement.to_csv('Nvidia_income_statement.csv', index = True, sep=',', encoding='utf-8', header=True)

balance_sheet = empresa.balance_sheet

balance_sheet.to_csv('Nvidia_balance_sheet.csv', index = True, sep=',', encoding='utf-8', header=True)
```

# Financial Ratios
The results from the analysis are the following:

![image](https://github.com/user-attachments/assets/15c45acf-ce9c-4901-b19f-f5835f780361)


## **Liquidity**

**1.Current Ratio (Razón Circulante)**

Although Nvidia has been up and down on this ratio, we can see a slight increase in current assets. This means Nvidia got $4.17 in 2024 of current assets to answer its current liabilities. 

**2.Quick Ratio (Prueba Ácida)**

This ratio, due to the excluded inventories, we can tell that Nvidia has enough liquidity to answer its current liabilities. Also, Nvidia should be careful with this, a quick ratio higher than 1  may mean a profitability drop.

**3.Cash Ratio (Cash Ratio)**

This ratio shows us the cash from the current assets that Nvidia got to answer its current liabilities. We can see that a big part of all current assets are from cash or equivalents.

**4.Working Capital to Total Assets Ratio (KTSA)**

This ratio has remained constant between 0.40 and 0.36 during this time. This suggests that NVIDIA keeps an equilibrated administration of its work capital depending on the structure of its assets.

## **Solvency**

**1.Debt Ratio (Razón de Endeudamiento)**

The debt ratio has decreased steadily from 0.46 in 2023 to 0.35 in 2024. We can see that NVIDIA is reducing its reliance on debt financing, as only 35% of its assets are funded through liabilities in 2024. This indicates a conservative approach to leveraging and strong financial health.

**2.Interest Coverage Ratio (Razón de Cobertura de Intereses)**

This ratio has reported a historical peak in 2024, 132.59 reported from 16.96 in the last year. This high-interest coverage ratio suggests that NVIDIA has a significant capacity to meet its interest obligations. The company can handle its debt costs, reflecting low credit risk.

**3.Leverage Ratio (Apalancamiento)**

The leverage ratio has not fluctuated much. The slight reduction in 2024 suggests a more balanced approach to equity and debt financing.

## **Rotation**

**1.Asset Turnover Ratio (Rotacion de Activos)**

The asset turnover ratio has increased from 0.65 in 2023 to 0.93 in 2024. NVIDIA maintains consistent efficiency in generating sales from its total assets.

**2.Inventory Turnover Ratio (Rotacion de Inventario)**

This ratio peaked at 3.62 in 2022, on 2024 it closed at 3.15. It shows a small diminution in inventory rotation but not even that changes that inventory rotated more than 3 times in a year.

**3.Average Inventory Period (Periodo Promedio de Inventario)**

This period has decreased from 162 days in 2023 to 116 days in 2024. The smaller inventory holding period in 2024 indicates a faster inventory cycle.

**4.Average Collection Period (Periodo Promedio de Cobro)**

The collection period has lengthened from 52 days in 2023 to 60 days in 2024. A longer collection period suggests a delay in receiving payments from customers, which could impact cash flow management.

**5.Average Payment Period (Periodo Promedio de Pago)**

The payment period has decreased from 62 days in 2023 to 47 days in 2024. NVIDIA is taking less to pay its suppliers, potentially as a strategy to conserve strong relationships with them.

**6.Cash Conversion Cycle (Ciclo de Conversion de Efectivo)**

The cash conversion cycle (CCC) has decreased in 2024 by 129 days, coming from a big increase of 152 days in 2023. This is a result of an Average Collection Period very low compared to the one in 2023.

## **Profitability**

**1.Return on Assets (ROA)**

ROA has remained relatively stable, until 2024 with a ROA reported of 0.45. NVIDIA efficiently generates net income from its assets. This reflects an effective asset utilization in producing profits in the last year.

**2.Return on Equity (ROE)**

ROE shows some fluctuations, but the peak of 2024 with 0.45 stands out. NVIDIA generates significant returns for shareholders.

**3.Gross Profit Margin (Margen de Utilidad Bruta)**

The gross margin has remained relatively stable, with a peak in 2024 of 0.73, coming from a slight decrease in 2023 of 0.57. NVIDIA's ability to manage production costs and pricing is getting stronger.

**4.Net Profit Margin (Margen de Utilidad Neta)**

The net margin is not the exception. With a peak in 2024 of 0.49 and a decrease of 0.16 in 2023, NVIDIA shows off pretty good work on this last year.


# Financial Dashboard in Excel

![image](https://github.com/user-attachments/assets/4ba2b5c5-d874-4429-872d-4c480c4ffb29)





