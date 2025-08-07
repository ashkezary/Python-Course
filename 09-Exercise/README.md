# جلسه نهم

# تمرین

0⃣ معرفی in و range و for

1⃣ پیمایش روی لیست به کمک for و محاسبه حاصل جمع
```python
my_list = [1,2,3,4,5,6]

sumoflist = 0
for x in my_list:
 sumoflist = sumoflist + x
print(sumoflist)
```
2⃣ تشخیص مربع کامل بودن یک عدد
```python
n = int(input())
flag = False
for x in range(1,n+1):
 if x*x == n:
  flag = True
  break

if flag:
 print(f"{n} is a perfect square!")
else:
 print(f"{n} is not a perfect square:(")
```
3⃣ تشخیص مربع کامل بودن یک عدد بدون استفاده از حلقه
```python
n = int(input())
rootn = n**0.5

if int(rootn)==rootn:
 print("Perfect Square!")
else:
 print("Not Perfect Square!")
```
4⃣ شمارش تعداد اعداد زوج و فرد در یک لیست
```python
s = input().split()
nums = []
for x in s:
 y = int(x)
 nums.append(y)
odds = 0
evens = 0
for i in nums:
 if i%2==0:
  evens += 1
 else:
  odds = odds + 1

print("#Even numbers:", evens)
print("#Odd numbers:", odds)
```
5⃣ عدد n را بگیرید و جدول ضرب n×n را چاپ کنید.
```python
n = int(input())

for i in range(1,n+1):
 print(i, end=" :")
 for j in range(1,n+1):
  print(i*j, end=" ")
 print()
```
1⃣ برنامه‌ای که عدد n را از کاربر بگیرد و جمله nام دنباله فیبوناچی را چاپ کند.
```python
n = int(input())
if n > 0 :
    fibonacci = []
    fibonacci.append(1)
    fibonacci.append(1)
    if n < 3:
        print(fibonacci[n - 1])
    else :
        for i in range(2, n) :
            num = fibonacci[i - 2] + fibonacci[i - 1]
            fibonacci.append(num)
        print(fibonacci[n - 1])
else :
    print(0)
```
2⃣ برنامه‌ای که عددی در مبنای دو از کاربر بگیرد و آن را به مبنای ۱۰ ببرد.
```python
s = input()
d = 0
for i in range(-1,-len(s)-1,-1):
    x = int(s[i])
    d += x*2**(-i-1)
print(d)
```
☑️ در مورد نحوه کار با ماتریس‌ها و استفاده از for تودرتو

3⃣ برنامه‌ای که عدد n را از کاربر بگیرد و سپس دو ماتریس n×n و حاصل جمع دو ماتریس را چاپ کند.
```python
n = int(input())

matrix1 = []
for i in range(n):
    l = list(map(int, input().split()))
    matrix1.append(l)
matrix2 = []
for i in range(n):
    l = list(map(int, input().split()))
    matrix2.append(l)

m = []
for i in range(n):
    row = []
    for j in range(n):
        u = matrix1[i][j] + matrix2[i][j]
        row.append(u)
    m.append(row)

for x in m:
    print(x)
```
