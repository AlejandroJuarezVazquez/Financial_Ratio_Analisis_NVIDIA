# Nvidia_Financial_Analysis
In this project, I show Financial Ratios and their formulas from the last 4 fiscal years from NVIDIA using Financial Statements, one of the biggest and most important companies in the world nowadays. 

I also included an analysis of the cash flow focused on 2023 and 2024. This is because, with the first analysis, the insights found motivated this due to the high improve from year to year.

I used a lot of tools for this analysis, such as Python and Pandas for downloading the financial states by using the Yahoo Finance API. Then, I used Excel for the study with all the financial ratios.

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

# Cash Flow Analysis

For the Cash Flow Analysis, I repeated the process of extracting the information:

```python
import yfinance as yf
import pandas as pd

ticker = "NVDA"  # Nvidia
empresa = yf.Ticker(ticker)

cash_flow = empresa.balance_sheet
cash_flow.to_csv('Nvidia_cash_flow.csv', index = True, sep=',', encoding='utf-8', header=True)
```

With the past analysis, we could see NVIDIA had an excellent last year. The reported 2024 was presumably better than 2023. The analysis will be focused on these 2 years, to see the management of the money in this last 2 years' scenario.

The cash flow is divided into three main categories: Operating Activities, Investing Activities, and Financing Activities. We will also identify any notable trends or behaviors that stand out, offering insights into the company’s financial strategy and liquidity position.

1. Operating Activities
Operating activities reflect cash generated or used by Nvidia's core business functions, such as revenue from sales, payments to suppliers and employees, and tax payments.

Cash and Cash Equivalents (2024 vs. 2023):

2024: $7.28 billion
2023: $3.39 billion
Analysis: Nvidia experienced significant growth in cash and cash equivalents, which indicates a strong operating cash flow. The increase of approximately $3.89 billion suggests that Nvidia's operations have generated substantial cash, contributing to higher liquidity in 2024.
Accounts Receivable (2024 vs. 2023):

2024: $9.99 billion
2023: $3.83 billion
Analysis: The surge in accounts receivable by $6.16 billion signals that Nvidia may have experienced strong sales growth, especially in the latter part of the fiscal year. However, it also indicates a higher reliance on credit terms, which could suggest increased risk in terms of customer payment delays.
Accounts Payable (2024 vs. 2023):

2024: $2.70 billion
2023: $1.19 billion
Analysis: A notable increase in accounts payable of $1.51 billion suggests that Nvidia is effectively managing its supplier payments and is possibly extending its payment terms with vendors. This could indicate a strategic use of supplier credit to optimize working capital.
Tax Payable (2024 vs. 2023):

2024: $296 million
2023: $467 million
Analysis: The decrease in tax payable by $171 million reflects a reduction in short-term tax liabilities, possibly as a result of favorable tax adjustments or tax payments made during the period.
2. Investing Activities
Investing activities provide insights into the company's capital expenditures, investments in other businesses, and asset acquisitions or divestitures.

Net PPE (Property, Plant, and Equipment) (2024 vs. 2023):

2024: $5.26 billion
2023: $4.84 billion
Analysis: Nvidia’s investment in tangible assets has grown by $420 million. This could indicate the expansion of facilities, infrastructure, or research and development (R&D) activities that are crucial for future growth. The relatively steady increase reflects a commitment to maintaining competitive capacity and technological leadership.
Intangible Assets (2024 vs. 2023):

2024: $5.54 billion
2023: $6.05 billion
Analysis: Nvidia has seen a slight decrease in intangible assets by $510 million, suggesting a possible reduction in new acquisitions or impairments to goodwill or intellectual property.
Short-Term Investments (2024 vs. 2023):

2024: $18.70 billion
2023: $9.91 billion
Analysis: A sharp increase of $8.79 billion in short-term investments reflects a shift in liquidity management, where Nvidia appears to be holding more investments in marketable securities or other financial instruments, likely to maximize returns on idle cash. This may suggest a more cautious approach, positioning for growth opportunities or strategic acquisitions.
3. Financing Activities
Financing activities reveal how the company funds its operations through debt, equity, or other financial instruments.

Net Debt (2024 vs. 2023):

2024: $2.43 billion
2023: $7.56 billion
Analysis: Nvidia significantly reduced its net debt by $5.13 billion, indicating a strong de-leveraging trend. This decrease suggests that the company may have used its operational cash flows to pay down debt, potentially strengthening its balance sheet and reducing interest expenses in the future.
Total Debt (2024 vs. 2023):

2024: $11.06 billion
2023: $12.03 billion
Analysis: The decrease in total debt by $970 million reinforces the trend of debt reduction. Nvidia’s capacity to lower its debt load can be viewed as a sign of financial stability and may allow it to access favorable financing terms in the future if needed.
Shareholder Equity (2024 vs. 2023):

2024: $42.98 billion
2023: $22.10 billion
Analysis: Nvidia experienced an impressive growth in shareholder equity, more than doubling its value from the previous year. This is a direct result of strong earnings and retained profits, contributing to an enhanced capital base. The increase in equity also signals investor confidence in Nvidia’s long-term prospects.
Retained Earnings (2024 vs. 2023):

2024: $29.82 billion
2023: $10.17 billion
Analysis: The surge in retained earnings by $19.65 billion demonstrates Nvidia's robust profitability, with a large portion of earnings retained for reinvestment or debt reduction. This reflects a strong capacity to generate profits and reinvest them strategically in business growth or shareholder returns.

4. Notable Trends and Insights
Strong Liquidity and Growth: Nvidia's cash and cash equivalents, along with short-term investments, show a marked increase, signaling strong liquidity and the company's ability to fund future growth without relying heavily on external financing.

Debt Reduction Strategy: The significant reduction in net debt is a key point, as it shows Nvidia’s focus on strengthening its balance sheet and reducing leverage. This could enhance investor confidence and lower future financial risk.

Investment in R&D and Infrastructure: The consistent increase in tangible assets (PPE) indicates a strategic focus on expanding the company’s infrastructure to support future innovations, possibly in AI, GPUs, and other high-growth markets.

Increased Working Capital: The jump in working capital suggests Nvidia is effectively managing its short-term assets and liabilities, positioning itself for smoother operations and the ability to fund its ongoing and future projects.




