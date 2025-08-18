# جلسه دهم (تابع)

به طور ساده منظور از تابع قطعه مشخصی از کد است که کار خاصی را انجام می‌دهد و می‌توانیم در جاهای مختلف و به دفعات آن را فراخوانی کنیم. در پایتون تابع می‌تواند ورودی یا خروجی هم نداشته باشد. منظور از خروجی در اینجا چیزی است که تابع، با استفاده از دستور `return` برمی‌گرداند. به مثال‌های زیر توجه کنید:

### مثال ۱: تابع بدون ورودی، بدون خروجی
```python
def print_star():
    print('******')
```
### مثال ۲: تابع با ورودی، بدون خروجی
```python
def print_star(n):
    print(n*'*')
```
### مثال ۳: تفاوت return و print
```python
def add(x,y):
    print(x+y)

def add2(x,y):
    return x+y

y = add(2,3)
x = add2(2,3)
print(y)
print(x)
```
### مثال ۴: تابع با ورودی و با خروجی
```python    
def is_even(n):
    if n%2==0:
        return True
    else:
        return False

print(is_even(2))
```
توجه کنید در برنامه بالا، اگر در خط آخر از `print` استفاده نمی‌کردیم، چیزی چاپ نمی‌شد.

**نکته.** در توابع آماده‌ای هم که در پایتون وجود دارد، بعضی توابع `return` دارند و برخی ندارند. برای مثال، برای مرتب کردن یک لیست، تابع `sort` چیزی برنمی‌گرداند (البته خود لیست را مرتب می‌کند) ولی تابع `sorted` یک لیست مرتب برمی‌گرداند.
```python
nums = [2,5,1,-3]
nums.sort()
print(sorted(nums))
```
### مثال ۵: جمع دو ماتریس مربعی

```python
# Matrix Addition
def mtrx_add(m1, m2):
    ans = []
    if len(m1)!=len(m2):
        return "Error"
    else:
        length = len(m1)
        for i in range(length):
            row = []
            for j in range(length):
                c = m1[i][j] + m2[i][j]
                row.append(c)
            ans.append(row)
        return ans
n = int(input())
matrix1 = []
for _ in range(n):
    s = input().split()
    nums = []
    for x in s:
        nums.append(int(x))
    matrix1.append(nums)
matrix2 = []
for _ in range(n):
    s = input().split()
    nums = []
    for x in s:
        nums.append(int(x))
    matrix2.append(nums)

print(mtrx_add(matrix1, matrix2))
```
**نکته.** این امکان وجود دارد که در برنامه‌نویسی اصلاً از تابع استفاده نکنیم. اما برای خواناتر بودن برنامه و امکان استفاده مجدد از آن، بهتر است که در برنامه خود، از تابع استفاده کنیم. اگر بخواهیم از توابع و متغیرهای یک ماژول (فایل پایتون) دیگر در برنامه خود استفاده کنیم، می‌توانیم از دستور `import` استفاده کنیم:

```python
import five01

five01.say_hello()
```
در قطعه کد بالا، از فایل `five01.py` تابع `say_hello` را فراخوانی کرده‌ایم.

**نکته.** برای ورودی‌های یک تابع می‌توانید به شکل زیر مقدار پیش‌فرض تعیین کنید:

```python
def say_hello(n=1):
	print(n*'salam')
say_hello()
```
بسیاری از توابع آماده خود پایتون، مقادیر پیش‌فرض دارند. برای مثال، تابع `split` که در جلسات پیش دیدیم، به صورت پیش‌فرض، جداکننده را `' '` در نظر می‌گیرد.

### مثال ۶: نوشتن تابع split

```python
# split: string, sep ---> list of strings
# Separator is just one character.
def mysplit(s, sep=' '):
    n = len(s)
    word = ""
    words = []
    m = len(sep)
    i = 0
    while i<n:
        if s[i:i+m]==sep:
            words.append(word)
            word = ""
            i += m-1
        else:
            word += s[i]
        i += 1
    words.append(word)        
    return words

s = "It**is**an**amazing**event."
print(mysplit(s, '**'))
```

### مثال ۷: تابع تبدیل دلار به ریال
```python
def dollar_to_rial(x):
 return x*900000

x = int(input())
print(dollar_to_rial(x))
```
### مثال ۸: تابع کف (floor)
**روش یک:**
```python
def floor(x):
 y = int(x)
 if x<0:
  if int(x)==x:
   return x
  else:
   return y-1
 else:
  return y

print(floor(5.2))
print(floor(-5.2))
print(floor(5))
print(floor(-5))
```
**روش دو.** تابع کف
```python
def floor(x):
 return x//1
``` 
### مثال ۹: نوشتن تابع سوتی‌شمار
```python
def sooti_shomar(s):
 counter = 0
 for i in range(len(s)):
  if s[i:i+5]=="sooti":
   counter = counter + 1
 return counter

x = sooti_shomar("sootisootisooti")
print(x)
```
### مثال ۱۰: تابع ضرب‌کننده دو ماتریس مربعی
```python
def matrix_mult(A, B):
 n = len(A)
 C = []
 for i in range(n):
  row = A[i]
  ans = []
  for j in range(n):
   col = []
   total = 0
   for p in range(n):
    col.append(B[p][j])
   for k in range(n):
    total += row[k]*col[k]
   ans.append(total)
  C.append(ans)
 return C

m1 = [[1, 0], [1,1]]
m2 = [[2, 3], [4, 5]]
print(matrix_mult(m1,m2))
```
