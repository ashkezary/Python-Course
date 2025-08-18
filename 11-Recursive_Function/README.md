# جلسه یازدهم (تابع بازگشتی)

در برنامه‌نویسی می‌توانیم درون یک تابع، تابع دیگری را فراخوانی کنیم. برای مثال در قطعه کد زیر، تابع اصلی ما، تابع `type_of_mail` است که درون آن سه تابع دیگر فراخوانی شده است:

```python
def is_gmail(s):
    if '@gmail' in s:
        return True
    return False

def is_yahoo(kamran):
    if '@yahoo' in kamran:
        return True
    return False

def is_Edu(s):
    if '.edu' in s:
        return True
    return False

def type_of_mail(x):
    if is_gmail(x):
        return 'Gmail'
    elif is_yahoo(x):
        return 'Yahoo'
    elif is_Edu(x):
        return 'Educational'
    else:
        return 'Outlier'
```
اگر یک تابع خودش را فراخوانی کند، اصطلاحاً آن را تابع بازگشتی می‌نامیم. در توابع بازگشتی توجه به این نکته ضروری است که باید یک شرط توقف بگذاریم وگرنه فرایند بازگشت هیچگاه تمام نخواهد شد. در مثال زیر شرط `if x==1` این نقش را بازی می‌کند.
```python
def say_hello(x):
    if x==1:
        print('Salam')
        return 'Tamam'
    else:
        print('Salam')
        say_hello(x-1)

print(say_hello(5))
```
### مثال: جمله‌ی n-ام فیبوناچی به طور بازگشتی
```python
def fibo(n):
    if n<=0:
        return -1
    elif n==1:
        return 1
    elif n==2:
        return 1
    return fibo(n-1)+fibo(n-2)

for i in range(1,11):
    print(fibo(i))
```  
خوب است زمان اجرای برنامه بالا را با برنامه‌ای که جلسه قبل نوشتیم، مقایسه کنید.
