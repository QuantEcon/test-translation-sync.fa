---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
heading-map:
  Programming for Economics: برنامه‌نویسی برای اقتصاد
  Using `numpy` Arrays: استفاده از آرایه‌های `numpy`
  Using `numpy` Arrays::Creating Arrays with `np.arange()` and `np.linspace()`: ایجاد آرایه‌ها با `np.arange()` و `np.linspace()`
  Working with **Pandas DataFrames**: کار با **DataFrames** در **Pandas**
  'Working with **Pandas DataFrames**::Reading Data: `pd.read_csv()` vs `pd.read_excel()`': 'خواندن داده: `pd.read_csv()` در مقابل `pd.read_excel()`'
  '*Matplotlib* Visualization Basics': مبانی تجسم داده با *Matplotlib*
  '*Matplotlib* Visualization Basics::The `plt.plot()` Function': تابع `plt.plot()`
  Using [QuantEcon](https://quantecon.org) Libraries: استفاده از کتابخانه‌های [QuantEcon](https://quantecon.org)
  Using [QuantEcon](https://quantecon.org) Libraries::Installing `quantecon` Package: نصب بسته `quantecon`
  'Special Cases: $\LaTeX$ in Headings': 'موارد خاص: $\LaTeX$ در عنوان‌ها'
  'Special Cases: $\LaTeX$ in Headings::The $\beta$-Coefficient in Regression': ضریب $\beta$ در رگرسیون
  'Special Cases: $\LaTeX$ in Headings::Computing $\mathbb{E}[X]$ (Expected Values)': محاسبه $\mathbb{E}[X]$ (مقادیر مورد انتظار)
  Questions & Answers: پرسش و پاسخ
  '"Edge Cases" and [Special] {Characters}': '"موارد استثنایی" و [ویژه] {کاراکترها}'
  '"Edge Cases" and [Special] {Characters}::Using `matplotlib`''s `plt.subplot()` for Multiple Plots': استفاده از `matplotlib`'s `plt.subplot()` برای چندین نمودار
  Summary: خلاصه
---

# برنامه‌نویسی برای اقتصاد

این درس مفاهیم برنامه‌نویسی و ابزارهای ضروری برای تحلیل اقتصادی مدرن را پوشش می‌دهد.

## استفاده از آرایه‌های `numpy`

کتابخانه `numpy` عملیات آرایه‌ای کارآمد برای محاسبات عددی فراهم می‌کند. آرایه‌ها پایه و اساس محاسبات علمی در Python هستند.

آرایه‌های NumPy از عملیات برداری‌سازی پشتیبانی می‌کنند و از حلقه‌های کند Python اجتناب می‌نمایند:

```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
result = arr ** 2  # Vectorized squaring
```

### ایجاد آرایه‌ها با `np.arange()` و `np.linspace()`

روش‌های مختلف ایجاد آرایه اهداف متفاوتی را دنبال می‌کنند. تابع `np.arange()` آرایه‌هایی با اندازه گام مشخص ایجاد می‌کند:

```python
x = np.arange(0, 10, 0.5)  # From 0 to 10, step 0.5
```

در همین حال، `np.linspace()` آرایه‌هایی با تعداد نقاط مشخص ایجاد می‌کند:

```python
y = np.linspace(0, 1, 100)  # 100 points from 0 to 1
```

## کار با **DataFrames** در **Pandas**

کتابخانه **pandas** قابلیت‌های قدرتمندی برای دستکاری داده فراهم می‌کند. DataFrameها ساختارهای داده دوبعدی با برچسب هستند.

### خواندن داده: `pd.read_csv()` در مقابل `pd.read_excel()`

فرمت‌های مختلف فایل به توابع خواندن متفاوتی نیاز دارند:

- **فایل‌های CSV**: از `pd.read_csv('data.csv')` استفاده کنید
- **فایل‌های Excel**: از `pd.read_excel('data.xlsx')` استفاده کنید
- **فایل‌های JSON**: از `pd.read_json('data.json')` استفاده کنید

## مبانی تجسم داده با *Matplotlib*

*Matplotlib* کتابخانه پایه رسم نمودار برای Python است. این کتابخانه کنترل دقیقی بر ظاهر نمودار فراهم می‌کند.

### تابع `plt.plot()`

نمودارهای خطی ساده با `plt.plot(x, y)` ایجاد می‌شوند:

```python
import matplotlib.pyplot as plt
plt.plot([1, 2, 3], [4, 5, 6])
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Simple Plot')
plt.show()
```

## استفاده از کتابخانه‌های [QuantEcon](https://quantecon.org)

پروژه [QuantEcon](https://quantecon.org) ابزارهای تخصصی برای مدل‌سازی اقتصادی فراهم می‌کند. برای جزئیات بیشتر به [مستندات](https://quanteconpy.readthedocs.io/) مراجعه کنید.

### نصب بسته `quantecon`

نصب از طریق pip:

```bash
pip install quantecon
```

یا با conda:

```bash
conda install -c conda-forge quantecon
```

## موارد خاص: $\LaTeX$ در عنوان‌ها

نمادگذاری ریاضی به صورت درون‌خطی ظاهر می‌شود: $f(x) = x^2 + 2x + 1$.

### ضریب $\beta$ در رگرسیون

ضریب رگرسیون $\beta$ رابطه بین متغیرها را اندازه‌گیری می‌کند:

$$
y = \alpha + \beta x + \epsilon
$$

### محاسبه $\mathbb{E}[X]$ (مقادیر مورد انتظار)

مقادیر مورد انتظار $\mathbb{E}[X]$ نمایانگر نتایج میانگین هستند:

$$
\mathbb{E}[X] = \sum_{i} x_i P(X = x_i)
$$

## پرسش و پاسخ

پرسش‌های متداول درباره Python برای اقتصاد:

- **پ**: کدام سریع‌تر است: `numpy` یا Python ساده؟
- **پ**: `numpy` معمولاً برای عملیات عددی ۱۰ تا ۱۰۰ برابر سریع‌تر است

- **پ**: آیا می‌توانم از `pandas` با مجموعه داده‌های بزرگ استفاده کنم؟
- **پ**: بله، اما برای مجموعه داده‌هایی که بزرگ‌تر از RAM هستند، استفاده از `dask` را در نظر بگیرید

## "موارد استثنایی" و [ویژه] {کاراکترها}

این بخش کاراکترهای ویژه مختلف را در عناوین آزمایش می‌کند.

### استفاده از `matplotlib`'s `plt.subplot()` برای چندین نمودار

تابع subplot چندین نمودار را در یک شکل ایجاد می‌کند:

```python
fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(12, 5))
ax1.plot(x, y1)
ax2.plot(x, y2)
```

## خلاصه

ابزارهای برنامه‌نویسی مانند **numpy**، *pandas* و `matplotlib` برای پژوهش اقتصادی مدرن ضروری هستند. تسلط بر این کتابخانه‌ها امکان تحلیل کارآمد داده‌ها و تجسم نتایج را فراهم می‌سازد.
