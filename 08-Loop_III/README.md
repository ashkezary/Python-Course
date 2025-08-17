# جلسه هشتم (حلقه)

### مثال یک: پیمایش روی رشته
 برنامه‌ای که رشته‌ای را از کاربر می‌گیرد و در صورتی که در آن بعد از حرف q حرف u نیامده باشد، wrong چاپ می‌کند و در غیر این صورت correct.
```python
s = input()
i = 0
n = len(s)
flag = True
while i<n:
    if s[i]=='q':
        if i==n-1:
            flag = False
        elif s[i+1]!='u':
            flag = False
    i += 1
if flag:
    print('correct')
else:
    print('wrong')
```
### مثال دو: پیمایش روی لیست

- برنامه‌ای بنویسید که عدد طبیعی n را گرفته و سپس n عدد از کاربر گرفته و کمینه آن‌ها را چاپ کند.
```python
n = int(input())
mini = float(input())
i = 0
while i<n-1:
    x = float(input())
    if x<mini:
        mini = x
    i += 1
print(mini)
```
### مثال سه: اول بودن یا نبود
برنامه‌ای بنویسید که عدد طبیعی n را گرفته و اول بودن یا نبودن آن را مشخص کند.

```python
n = int(input())
i = 2
is_prime = False
while i<n:
    if n%i==0:
        is_prime = True
    i += 1
if is_prime:
    print(f"{n} is prime.")
else:
    print(f"{n} is not prime.")
```
### مثال چهار: شمارنده‌های یک عدد
برنامه‌ای بنویسید که عدد طبیعی n را گرفته و شمارنده‌های آن را چاپ کند.
```python
n = int(input())
i = 1
dividers = []
while i<=n:
    if n%i==0:
        dividers.append(i)
    i += 1
print(dividers)
```
☑️ استفاده از break برای پایان دادن به حلقه

- برنامه‌ای بنویسید که عدد طبیعی n را گرفته و تمام اعداد اول کوچکتر از آن را چاپ کند.

# معرفی for


 ### مثال: پیمایش روی لیست به کمک for و محاسبه حاصل جمع
```python
my_list = [1,2,3,4,5,6]

sumoflist = 0
for x in my_list:
 sumoflist = sumoflist + x
print(sumoflist)
```
