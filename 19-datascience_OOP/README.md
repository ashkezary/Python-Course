# جلسه نوزدهم (کار با داده)

## معرفی کتابخانه‌ی numpy
برای کار با آرایه‌ها و توابع ریاضی به طور بهینه، می‌توانیم از کتابخانه‌ی `numpy` استفاده کنیم. این کتابخانه داده‌ها را در قالب `np.array` نگه داشته و مدیریت می‌کند. سازگاری با کتابخانه `pandas`، تبدیل، برش و چسباندن داده‌ها و نیز امکان کار با توزیع‌های آماری از دیگر مزایای این کتابخانه هستند. در ادامه برخی از قابلیت‌های دم‌دستی این کتابخانه را ملاحظه می‌کنیم:

### نگهداری داده‌ها در آرایه با ابعاد مختلف
```python
import numpy as np
a = np.array(42)
b = np.array([1, 2, 3, 4, 5])
c = np.array([[1, 2, 3], [4, 5, 6]])
d = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])
print(a.ndim)
print(b.ndim)
print(c.ndim)
print(d.ndim)
```
### تبدیل نوع‌داده‌ها به یکدیگر
برای مثال در قطعه کد زیر عددهای اعشاری به اعداد صحیح تبدیل می‌شوند.
```python
arr = np.array([1.1, 2.1, 3.1])
newarr = arr.astype('i')
print(newarr)
print(arr.dtype)
print(newarr.dtype)
```
خروجی کد بالا، به شکل زیر خواهد بود:
```
[1 2 3]
float64
int32
```
### تغییر ابعاد
در قطعه کد زیر یک آرایه یک بعدی به آرایه دوبعدی `4x3` تبدیل شده و سپس به همان حالت یک بعدی بازگردانده شده است.
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])
print(arr.shape)
newarr = arr.reshape(4, 3)
print(newarr)
print(newarr.shape)
initial_arr = newarr.reshape(-1)
print(initial_arr)
```
خروجی کد بالا، چنین خواهد شد:
```
(12,)
[[ 1  2  3]
 [ 4  5  6]
 [ 7  8  9]
 [10 11 12]]
(4, 3)
[ 1  2  3  4  5  6  7  8  9 10 11 12]
```
برای دیدن کارکردها و قابلیت‌های بیشتر `numpy` می‌توانید سایت [W3School](https://www.w3schools.com/python/numpy/default.asp) را ملاحظه کنید.

## معرفی کتابخانه matplotlib
برای رسم نمودار از روی داده‌ها و دیداری‌سازی آن‌ها، کتابخانه‌ی `matplotlib` یک کتابخانه‌ی مادر است که امکان رسم انواع نمودارهای پایه و انجام تنظیمات روی آن‌ها را مدیریت می‌کند. برای مثال در شکل زیر نمودار ساده‌ای از کتابخانه `pandas` نمایش داده می‌شود:
```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('data.csv')
df.plot(kind = 'scatter', x = 'Duration', y = 'Calories')
plt.show()
```
یک مزیت plt این است که به صورت لایه لایه می‌شود بخش‌هایی را به آن اضافه کرد. در قطعه کد زیر نمونه‌ای از آن ملاحظه می‌کنید:
```python
import matplotlib.pyplot as plt
import numpy as np
xpoints = np.array([0, 3, 6])
ypoints = np.array([0, 100, 250])
#default xpoint
plt.plot(xpoints, ypoints, 'o') # marker|line|color
plt.plot(xpoints, ypoints, ms=10)
plt.xlabel('something')
plt.grid()
plt.show()
```
اگر بخواهیم چند نمودار را در یک قاب تصویر داشته باشیم، می‌توانیم از دستور `subplot` به شکل زیر استفاده کنیم:
```python
# The code is from w3school
import matplotlib.pyplot as plt
import numpy as np

#plot 1:
x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(1, 2, 1)
plt.plot(x,y)

#plot 2:
x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(1, 2, 2)
plt.plot(x,y)

plt.show()
```
برای رسم هر کدام از نمودارهای نقطه‌ای (scatter)، میله‌ای (bar)، دایره‌ای (pie)، هیستوگرام (hist) و ... هم می‌توانیم از توابع خاص خودشان استفاده کنیم. در ادامه نمونه‌ کدی از هر کدام ذکر شده است:

۱- نمودار نقطه‌ای
```python
plt.scatter(x, y, s = list, color = 'red')
#cmap: colormap
#alpha: transparency
```
۲- نمودار میله‌ای
```python
plt.bar(x,y, width=0.1)
```
اگر بخواهیم نمودار میله‌ای به شکل افقی رسم شود، می‌توانیم از `barh` استفاده کنیم.

۳- نمودار دایره‌ای
```python
plt.pie(x, labels=list)
```
۴- هیستوگرام
```python
plt.hist(x)
```

روشن است که هر کدام از این نمودارها قابلیت‌های بیشتری دارند که ما به آن‌ها نمی‌پردازیم. برای مثال، قطعه کد زیر یک نمودار نقطه‌ای زیباتر را نشان می‌دهد:
```python
import matplotlib.pyplot as plt
import numpy as np
x = np.random.randint(100, size=(100))
y = np.random.randint(100, size=(100))
colors = np.random.randint(100, size=(100))
sizes = 10 * np.random.randint(100, size=(100))
plt.scatter(x, y, c=colors, s=sizes, alpha=0.5,
cmap='nipy_spectral')
plt.colorbar()
plt.show()
```
