# جلسه سوم

## حل تمرین



**پرسش یکم.** نام و سن کاربر را گرفته و معرفی‌نامه او را به شکل زیر چاپ کنید:

"I am name and I am age years old."


 نمونه ورودی: 
```
hamid
23
```
نمونه خروجی:
```
I am hamid and I am 23 years old.
```
**پاسخ.**
```python
name = input()
age = input()
#One way
print('I am ',name," and I am ",age," years old.")
#Another way
print(f"I am {name} and I am {age} years old.")
```
**پرسش دوم.** دو مدل پیراهن داریم و می‌خواهیم به ترتیب قیمت و تعداد هر کدام را از کاربر گرفته و قیمت کل را محاسبه کنیم.
 
قالب ورودی:
```
cost of shirt A
number of shirt A
cost of shirt B
number of shirt B
```
خروجی:
```
The total cost is n.
```
**پاسخ.**
```python
cost_a = float(input("Enter the cost of A: "))
num_a = int(input("Enter the number of A: "))
cost_b = float(input("Enter the cost of B: "))
num_b = int(input("Enter the number of B: "))

tot_cost = cost_a*num_a + cost_b*num_b
print("The total cost is",tot_cost)
```
## چئد چیز دیگر در مورد رشته‌ها
- پایان دستور print
- چاپ کردن n\
```python
s = "Mohammad"
print(s.count('amma'))
print(s[0])
print(s[2:5])
print(s[2:])
print(s[:5])
print(s[-1])
print(s.find('amma'))
print(s.replace('a',''))

print("salam", end="")
s = "Mohagheghi"
print(s.count('gh'))
print(len(s))
print(s[3])
print(s[3:7])
print(s[3:])
print(s[:5])
print(s[-1])
print(s[::-1])
print(s[::2])
```
