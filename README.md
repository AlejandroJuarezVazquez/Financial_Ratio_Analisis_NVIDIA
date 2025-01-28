# Financial_Ratio_Analisis_NVIDIA
In this project, I show Financial Ratios and their formulas from the last 4 fiscal years from Nvidia, one of the biggest and most important companies in the world nowadays. 

I used a lot of tools for this analysis, such as Python and Pandas for downloading the financial states by using the Yahoo Finance API. Then, I used Excel for the analysis with all the financial ratios.

# Extracting Nvidia Financial Statements with Python
To extract the data i used the Yahoo Finance library in python and pandas to exporting the data as csv files.
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

Although Nvidia has been up and downing on this ratio, we can see the slight increase in current assets. This means Nvidia got $4.17 in 2024 of current assets to answer its current liabilities. 

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

This ratio has reported a historical peak in 2024, 132.59 reported from a 16.96 in the last year. This high-interest coverage ratio suggests that NVIDIA has a significant capacity to meet its interest obligations. The company can handle its debt costs, reflecting low credit risk.

**3.Leverage Ratio (Apalancamiento)**

The leverage ratio has not fluctuated much. The slight reduction in 2024 suggests a more balanced approach to equity and debt financing.

## **Rotation**

**1.Asset Turnover Ratio (Rotacion de Activos)**

The asset turnover ratio has increased from 0.65 in 2023 to 0.93 in 2024. NVIDIA maintains consistent efficiency in generating sales from its total assets.

**2.Inventory Turnover Ratio (Rotacion de Inventario)**

This ratio peaked at 3.62 in 2022, indicating very efficient inventory management, but decreased to 28.87 in 2024. The decline may suggest slower inventory movement, possibly due to increased inventory levels or lower sales growth compared to previous years.

**3.Average Inventory Period (Periodo Promedio de Inventario)**

This period has increased from 8.08 days in 2022 to 12.64 days in 2024. The longer inventory holding period in 2024 indicates a slower inventory cycle, potentially tying up capital in stock for extended periods.

**4.Average Collection Period (Periodo Promedio de Cobro)**

The collection period has lengthened from 51.39 days in 2021 to 61.83 days in 2024. A longer collection period suggests a delay in receiving payments from customers, which could impact cash flow management.

**5.Average Payment Period (Periodo Promedio de Pago)**

The payment period has increased significantly from 54.64 days in 2021 to 89.2 days in 2024. NVIDIA is taking longer to pay its suppliers, potentially as a strategy to conserve cash or leverage supplier terms.

**6.Cash Conversion Cycle (Ciclo de Conversion de Efectivo)**

The cash conversion cycle (CCC) has fluctuated, moving from a positive 8.03 days in 2021 to a negative value of -14.72 days in 2024. A negative CCC in 2024 indicates that NVIDIA collects cash from customers before paying suppliers, improving liquidity and working capital efficiency. This is a favorable trend for operational cash flow.

## **Profitability**

**1.Return on Assets (ROA)**

OA has remained relatively stable, ranging between 0.26 in 2024 and 0.28 in 2022 and 2023. NVIDIA efficiently generates net income from its assets, maintaining consistency over the years. This reflects effective asset utilization in producing profits.

**2.Return on Equity (ROE)**

ROE shows some fluctuations, peaking at 1.97 in 2022 and declining to 1.65 in 2024. NVIDIA generates significant returns for shareholders, but the slight decrease from 2022 to 2024 may indicate increased equity or reduced profitability relative to equity.

**3.Gross Profit Margin (Margen de Utilidad Bruta)**

The gross margin has varied, peaking at 3.37 in 2022 and declining to 3.17 in 2024, though still higher than 2.72 in 2023. NVIDIA's ability to manage production costs and pricing remains strong. However, the slight decline from 2022 suggests minor cost pressures or pricing adjustments.

**4.Net Profit Margin (Margen de Utilidad Neta)**

The net margin has been stable, hovering between 0.24 and 0.26 over the years. NVIDIA consistently converts a substantial portion of its sales into net income, demonstrating strong overall profitability and cost management.

# Financial Dashboard in Excel

![image](https://github.com/user-attachments/assets/4ba2b5c5-d874-4429-872d-4c480c4ffb29)

