# جلسه دهم

# تابع

به طور ساده منظور از تابع قطعه مشخصی از کد است که کار خاصی را انجام می‌دهد و می‌توانیم در جاهای مختلف و به دفعات آن را فراخوانی کنیم. در پایتون تابع می‌تواند ورودی یا خروجی هم نداشته باشد. منظور از خروجی در اینجا چیزی است که تابع، با استفاده از دستور `return` برمی‌گرداند.

☑️ معرفی تابع، دیدن انواع توابع و تاکید بر تمایز خروجی تابع و نمایش یک چیز

### تابع بدون ورودی، بدون خروجی
```python
def print_star():
    print('******')
```
### تابع با ورودی، بدون خروجی
```python
def print_star(n):
    print(n*'*')
```
### تابع با ورودی و با خروجی
```python    
def is_even(n):
    if n%2==0:
        return True
    else:
        return False

print(is_even(2))
```
1⃣ مثالی برای مرور جلسه قبل
```python
def say_hello():
 return "Salam"
def alaki(x):
 return x+x
 
for i in range(10):
 print(say_hello())
 a = alaki("salam")
 print(a)
```
2⃣ تابع تبدیل دلار به ریال
```python
def dollar_to_rial(x):
 return x*850000

x = int(input())
print(dollar_to_rial(x))
```
3⃣ مثال از نوشتن تابع کف
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
4⃣ نوشتن تابع کف به روشی دیگر
```python
def floor(x):
 return x//1
``` 
5⃣ نوشتن تابع سوتی‌شمار
(یک قدم اولیه برای رسیدن به تابع سوتی‌بگیر)
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
6⃣ تابع ضرب‌کننده دو ماتریس مربعی
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
