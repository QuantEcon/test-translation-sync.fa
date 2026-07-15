---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
translation:
  title: برنامه‌نویسی برای اقتصاد
  headings:
    Using `numpy` Arrays: استفاده از آرایه‌های `numpy`
    Using `numpy` Arrays::Creating Arrays with `np.arange()` and `np.linspace()`: ایجاد آرایه‌ها با `np.arange()` و `np.linspace()`
    Working with **Pandas DataFrames**: کار با **Pandas DataFrames**
    'Working with **Pandas DataFrames**::Reading Data: `pd.read_csv()` vs `pd.read_excel()`': 'خواندن داده: `pd.read_csv()` در برابر `pd.read_excel()`'
    '*Matplotlib* Visualization Basics': '*Matplotlib* مبانی تجسم‌سازی'
    '*Matplotlib* Visualization Basics::The `plt.plot()` Function': تابع `plt.plot()`
    Using [QuantEcon](https://quantecon.org) Libraries: استفاده از کتابخانه‌های [QuantEcon](https://quantecon.org)
    Using [QuantEcon](https://quantecon.org) Libraries::Installing `quantecon` Package: نصب بسته `quantecon`
    'Special Cases: $\LaTeX$ in Headings': 'موارد خاص: $\LaTeX$ در عنوان‌ها'
    'Special Cases: $\LaTeX$ in Headings::The $\beta$-Coefficient in Regression': ضریب $\beta$ در رگرسیون
    'Special Cases: $\LaTeX$ in Headings::Computing $\mathbb{E}[X]$ (Expected Values)': محاسبه $\mathbb{E}[X]$ (مقادیر مورد انتظار)
    Questions & Answers: پرسش‌ها و پاسخ‌ها
    '"Edge Cases" and [Special] {Characters}': '"موارد خاص" و [ویژه] {نویسه‌ها}'
    '"Edge Cases" and [Special] {Characters}::Using `matplotlib`''s `plt.subplot()` for Multiple Plots': استفاده از `matplotlib`'s `plt.subplot()` برای رسم‌های چندگانه
    Summary: خلاصه
---

# برنامه‌نویسی برای اقتصاد

این درس مفاهیم برنامه‌نویسی و ابزارهایی را پوشش می‌دهد که برای تحلیل اقتصادی مدرن ضروری هستند.

## استفاده از آرایه‌های `numpy`

کتابخانه `numpy` عملیات آرایه‌ای کارآمدی برای محاسبات عددی فراهم می‌کند. آرایه‌ها بنیان محاسبات علمی در پایتون هستند.

آرایه‌های NumPy از عملیات برداری‌شده پشتیبانی می‌کنند و از حلقه‌های کند پایتون اجتناب می‌کنند:

```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
result = arr ** 2  # Vectorized squaring
```

### ایجاد آرایه‌ها با `np.arange()` و `np.linspace()`

روش‌های مختلف ایجاد آرایه، اهداف متفاوتی را دنبال می‌کنند. تابع `np.arange()` آرایه‌هایی با اندازه گام مشخص ایجاد می‌کند:

```python
x = np.arange(0, 10, 0.5)  # From 0 to 10, step 0.5
```

از سوی دیگر، `np.linspace()` آرایه‌هایی با تعداد نقاط مشخص ایجاد می‌کند:

```python
y = np.linspace(0, 1, 100)  # 100 points from 0 to 1
```

## کار با **Pandas DataFrames**

کتابخانه **pandas** قابلیت‌های قدرتمندی برای دستکاری داده فراهم می‌کند. DataFrameها ساختارهای داده برچسب‌دار دوبعدی هستند.

### خواندن داده: `pd.read_csv()` در برابر `pd.read_excel()`

فرمت‌های مختلف فایل به توابع خواندن متفاوتی نیاز دارند:

- **فایل‌های CSV**: از `pd.read_csv('data.csv')` استفاده کنید
- **فایل‌های Excel**: از `pd.read_excel('data.xlsx')` استفاده کنید
- **فایل‌های JSON**: از `pd.read_json('data.json')` استفاده کنید

## *Matplotlib* مبانی تجسم‌سازی

*Matplotlib* کتابخانه پایه‌ای رسم نمودار برای Python است. این کتابخانه کنترل دقیقی بر ظاهر نمودار فراهم می‌کند.

### تابع `plt.plot()`

نمودارهای خطی پایه با `plt.plot(x, y)` ایجاد می‌شوند:

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

نماد ریاضی به‌صورت درون‌خطی ظاهر می‌شود: $f(x) = x^2 + 2x + 1$.

### ضریب $\beta$ در رگرسیون

ضریب رگرسیون $\beta$ رابطه بین متغیرها را اندازه‌گیری می‌کند:

$$
y = \alpha + \beta x + \epsilon
$$

### محاسبه $\mathbb{E}[X]$ (مقادیر مورد انتظار)

مقادیر مورد انتظار $\mathbb{E}[X]$ نمایانگر پیامدهای متوسط هستند:

$$
\mathbb{E}[X] = \sum_{i} x_i P(X = x_i)
$$

## پرسش‌ها و پاسخ‌ها

پرسش‌های رایج درباره پایتون برای اقتصاد:

- **پرسش**: کدام سریع‌تر است: `numpy` یا پایتون خالص؟
- **پاسخ**: `numpy` معمولاً برای عملیات عددی 10 تا 100 برابر سریع‌تر است

- **پرسش**: آیا می‌توانم از `pandas` با مجموعه‌داده‌های بزرگ استفاده کنم؟
- **پاسخ**: بله، اما برای مجموعه‌داده‌های بزرگ‌تر از RAM، استفاده از `dask` را در نظر بگیرید

## "موارد خاص" و [ویژه] {نویسه‌ها}

این بخش نویسه‌های خاص گوناگون را در تیترها آزمایش می‌کند.

### استفاده از `matplotlib`'s `plt.subplot()` برای رسم‌های چندگانه

تابع subplot چندین نمودار را در یک شکل ایجاد می‌کند:

```python
fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(12, 5))
ax1.plot(x, y1)
ax2.plot(x, y2)
```

## خلاصه

ابزارهای برنامه‌نویسی مانند **numpy**، *pandas* و `matplotlib` برای پژوهش‌های اقتصادی مدرن ضروری هستند. بر این کتابخانه‌ها تسلط پیدا کنید تا بتوانید داده‌ها را به‌طور کارآمد تحلیل کرده و نتایج را به تصویر بکشید.
