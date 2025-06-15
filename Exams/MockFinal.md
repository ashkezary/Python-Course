# آزمون پایانی

توجه داشته باشید که پاسخ‌های داده شده، تنها یکی از روش‌ها بوده و ممکن است راه‌های دیگر و حتی ساده‌تری برای سوالات وجود داشته باشد.

**پرسش یکم.** (۱/۵ نمره) برتامه‌ای بنویسید که عددی در مبنای ۱۰ از کاربر بگیرد و آن را به مبنای ۲ ببرد.

نمونه ورودی.
```
13
```
نمونه خروجی.
```
1101
```

**پاسخ.**
```python
def decimal_to_binary(decimal):
    if decimal == 0:
        return "0"
    binary = ""
    while decimal > 0:
        binary = str(decimal % 2) + binary
        decimal //= 2
    return binary

decimal_num = int(input())
binary_num = decimal_to_binary(decimal_num)
print(binary_num)
```

**پرسش دوم.** (۱/۵ نمره) برنامه‌ای بنویسید که ‌یک رشته‌ی نشان‌دهنده حاصل جمع را از کاربر بگیرد، سپس حاصل جمع را به شکل مرتب نوشته و حاصل را محاسبه کرده و بنویسد.

نمونه ورودی.
```
5+3+9+1+7
```
نمونه خروجی.
```
1+3+5+7+9=25
```

**پاسخ.**
```python
s = input()
str_nums = s.split('+')
nums = []
for x in str_nums:
  nums.append(int(x))
total = nums.sum()
nums.sort()
str_nums = []
for x in nums:
  str_nums.append(str(x))
ans = '+'.join(str_nums)
print(ans+'='+str(total))
```
**پرسش سوم.** (۱/۵ نمره) برنامه‌ای بنویسید که تعداد واژه‌های فایل input.txt را شمرده و چاپ کند.

**پاسخ.**
```python
with open('input.txt', 'r') as f:
  x = f.read().split()
print(len(x))
```
**پرسش چهارم.** (۱/۵ نمره) برنامه‌ای بنویسید عدد n را از کاربر بگیرد و سپس در n خط بعد، در هر خط نام یک نفر را دریافت کند. سپس هزار بار از بین این نام‌ها قرعه‌کشی کرده و نام خوش‌شانس‌ترین فرد و تعداد دفعاتی قرعه به آن نام خورده، چاپ کند.

**پاسخ.**
```python
import random
n = int(input())
names = []
for i in range(n):
  s = input()
  names.append(s)
ss = []
for i in range(1000):
  x = random.randint(0,n)
  ss.append(names[x])
uniq = set(ss)
max_count = 0
max_name = ""
for name in uniq:
  num = ss.count(name)
  if num>max_count:
    max_count = 0
    max_name = name
print(f"The luckiest person is {max_name} with {max_count} times selection.")
```
**پرسش پنجم.** برتامه زیر را به گونه‌ای تغییر دهید که برای هیچ ورودی‌ای خطا ندهد و هر موقع که خطایی پیش آمد، این پیام چاپ شود که: «Hame Chi Aroome».
```python
# Get two numbers from the user
num1 = input("Enter the first number: ")
num2 = input("Enter the second number: ")

# Convert inputs to floats (to allow decimal numbers)
num1 = float(num1)
num2 = float(num2)

# Add the numbers
result = num1 + num2

# Print the result
print("The sum of", num1, "and", num2, "is", result)
```

**پاسخ.**
```python
try:
  # Get two numbers from the user
  num1 = input("Enter the first number: ")
  num2 = input("Enter the second number: ")

  # Convert inputs to floats (to allow decimal numbers)
  num1 = float(num1)
  num2 = float(num2)

  # Add the numbers
  result = num1 + num2

  # Print the result
  print("The sum of", num1, "and", num2, "is", result)
except:
  print("Hame Chi Aroome")
```
