# Unemployment-Analysis
Analyze unemployment rate (% unemployed) with Python: clean data, visualize trends, quantify Covid-19 impact, spot seasonal patterns, and present actionable insights to inform economic and social policy.
# Unemployment Analysis with Python


Analyze unemployment rate data representing the percentage of unemployed people. Clean and explore the data, visualize trends, assess the impact of Covid‑19, identify seasonal patterns, and present insights that can inform policy.


## Quick start (Local)


1) Create a virtual environment and install packages


```bash
python -m venv venv
source venv/bin/activate # macOS/Linux
venv\Scripts\activate # Windows
pip install -r requirements.txt
##Results
Saving Unemployment in India.csv to Unemployment in India (1).csv
Saving Unemployment_Rate_upto_11_2020.csv to Unemployment_Rate_upto_11_2020.csv
Dataset shape: (768, 7)
First 5 rows:
           Region         Date  Frequency   Estimated Unemployment Rate (%)  \
0  Andhra Pradesh   31-05-2019    Monthly                              3.65   
1  Andhra Pradesh   30-06-2019    Monthly                              3.05   
2  Andhra Pradesh   31-07-2019    Monthly                              3.75   
3  Andhra Pradesh   31-08-2019    Monthly                              3.32   
4  Andhra Pradesh   30-09-2019    Monthly                              5.17   

    Estimated Employed   Estimated Labour Participation Rate (%)   Area  
0           11999139.0                                     43.24  Rural  
1           11755881.0                                     42.05  Rural  
2           12086707.0                                     43.50  Rural  
3           12285693.0                                     43.97  Rural  
4           12256762.0                                     44.68  Rural  

Columns after renaming: ['region', 'date', 'frequency', 'estimated_unemployment_rate_(%)', 'estimated_employed', 'estimated_labour_participation_rate_(%)', 'area']

Missing values:
 region                                     1
date                                       1
frequency                                  1
unemployment_rate                          1
estimated_employed                         1
estimated_labour_participation_rate_(%)    1
area                                       1
dtype: int64
/tmp/ipython-input-4062568230.py:30: UserWarning: Parsing dates in  %d-%m-%Y format when dayfirst=False (the default) was specified. Pass `dayfirst=True` or specify a format to silence this warning.
  df["date"] = pd.to_datetime(df["date"], errors="coerce")

<img width="700" height="470" alt="image" src="https://github.com/user-attachments/assets/eb14763c-26d3-4e72-b2f9-e808b7ec8675" />

<img width="997" height="584" alt="image" src="https://github.com/user-attachments/assets/7cc53328-3323-4c51-8e70-9fb0ce8139c2" />

<img width="996" height="547" alt="image" src="https://github.com/user-attachments/assets/d7ffe134-1322-49a2-ad54-a37999a0ab31" />

Average unemployment rate before Covid (till Feb 2020): 9.51%
Average unemployment rate during first Covid wave (Mar-Sep 2020): 17.77%
/tmp/ipython-input-4062568230.py:82: FutureWarning: 

The `ci` parameter is deprecated. Use `errorbar=None` for the same effect.

  sns.barplot(x="unemployment_rate", y="region",
/tmp/ipython-input-4062568230.py:82: FutureWarning: 

Passing `palette` without assigning `hue` is deprecated and will be removed in v0.14.0. Assign the `y` variable to `hue` and set `legend=False` for the same effect.

  sns.barplot(x="unemployment_rate", y="region",

<img width="949" height="547" alt="image" src="https://github.com/user-attachments/assets/5b970de3-cbf1-453c-8ad6-18803c1717e6" />

/tmp/ipython-input-4062568230.py:95: FutureWarning: 

Passing `palette` without assigning `hue` is deprecated and will be removed in v0.14.0. Assign the `x` variable to `hue` and set `legend=False` for the same effect.

  sns.boxplot(x="month", y="unemployment_rate", data=df, palette="coolwarm")

/tmp/ipython-input-4062568230.py:95: FutureWarning: 

Passing `palette` without assigning `hue` is deprecated and will be removed in v0.14.0. Assign the `x` variable to `hue` and set `legend=False` for the same effect.

  sns.boxplot(x="month", y="unemployment_rate", data=df, palette="coolwarm")

<img width="841" height="547" alt="image" src="https://github.com/user-attachments/assets/6f744148-4caa-4f0b-b7d7-f68811a314d9" />


Key Insights:
1. Covid-19 had a significant impact, with unemployment peaking during Mar-Sep 2020.
2. Some regions consistently show higher unemployment than others.
3. Seasonal fluctuations are visible across months.
4. Average unemployment rates increased notably in 2020 compared to pre-Covid periods.
5. Policymakers should focus on vulnerable regions and prepare employment safety nets for shocks like pandemics.
