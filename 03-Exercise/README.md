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
## کاراکترهای بَدچاپ (Escape Characters)
برخی کاراکترها هستند که چاپ کردن آن‌ها به سادگی انجام نمی‌شود. مثلاً فرض کنید بخواهیم فقط یک دبل کوتیشن را چاپ کنیم اما اگر بنویسیم `print(""")` نه تنها کاراکتر موردنظر چاپ نمی‌شود بلکه برنامه خطا داده و متوقف می‌شود. برای غلبه بر این مشکل می‌توانیم قبل از چنین کاراکترهایی از بک‌اسلش (`\`) استفاده کنیم. مثلاً برای چاپ یک دبل کوتیشن می‌توانیم به این صورت عمل کنیم:
```python
print("\"")
``` 
از دیگر کاراکترهای بدچاپ پراستفاده می‌توان به `'`، `\`، `\n` و `\t` اشاره کرد.

## چاپ کردن و خط بعد نرفتن
دستور `print` به طور پیش‌فرض پس از چاپ یک رشته به خط بعد می‌رود. اگر بخواهیم چنین اتفاقی نیفتد، می‌توانیم به شکل زیر از پارامتر `end` درون دستور `print` استفاده کنیم:
```python
print('Salam', end = '')
```
## عملیات روی رشته‌ها
در زیر گزیده‌ای از مهم‌ترین عملیات‌هایی که می‌توانیم روی رشته‌ها انجام دهیم به همراه مثال ذکر شده است.

### ۱) گزینش یک حرف یا زیررشته از رشته
```python
s = "Mohagheghi"
print(s[3]) # output: a
print(s[3:7]) # output: aghe
print(s[3:]) # output: agheghi
print(s[:5]) # output: Mohag
print(s[-1]) # output: i
print(s[::-1]) # output: ihgehgahoM (reveresed)
print(s[::2]) # output: Mhgeh
```

### ۲) شمارش و جستجو
```python
print(s.count('gh')) #output: 2
print(s.find('a')) #output: 3 (index of first)
```

### ۳) طول رشته
```python
print(len(s)) # output: 10
```
### ۴) حذف زوائد پیش و پس

گاهی ممکن است بخواهیم تا فاصله‌های زائد در ابتدا و انتهای یک رشته را حذف کنیم. برای این کار می‌توانیم از دستور `strip` برای یک رشته استفاده کنیم.

```python
a = "  Ali  "
b = "Ali"
c = a.strip()
if a==b:
	print("True")
else:
	print("False")
if a==c:
	print("True")
else:
	print("False")	
```
در مثال بالا، ابتدا `False` چاپ می‌شود و سپس `True`؛ زیرا ابتدا رشته‌ی `"   Ali   "` با رشته‌ی `"Ali"` مقایسه می‌شود که پاسخ منفی است و سپس با رشته‌ی strip شده مقایسه می‌شود که این بار درست است.

### ۵) جایگزین کردن
برای جایگزین کردن یک حرف یا زیررشته در یک رشته با یک حرف یا زیررشته‌ی دیگر می‌توانید از دستور `replace` استفاده کنید.

```python
s = "abcdabcd"
print(s.replace('a','z'))
print(s.replace('ab', 'nice'))
```
حاصل قطعه کد بالا به ترتیب `zbcdzbcd` و `nicecdnicecd` خواهد شد.


