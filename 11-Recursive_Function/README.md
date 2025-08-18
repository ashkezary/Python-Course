# جلسه یازدهم (تابع بازگشتی)

1⃣ فراخوانی یک تابع درون تابعی دیگر
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
2⃣ تابع بازگشتی: فراخوانی یک تابع توسط خودش
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
⏺ جمله n ام دنباله فیبوناچی با استفاده از تابع بازگشتی
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
