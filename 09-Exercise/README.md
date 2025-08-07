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
