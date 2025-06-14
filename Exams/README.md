# پایان‌ترم پاییز ۱۴۰۳

**پرسش یکم.** (۱/۵ نمره) بهنام که امروز صبح هم امتحان داشته، از دشواری روزگار بسیار گله دارد. از همین رو، دست به قلم برده و متنی سراسر شکوه و شکایت نوشته است. در متن بهنام، پی‌درپی کلمه‌ی «difficult» آمده است. برای روحیه دادن به بهنام لطفاً برنامه‌ای بنویسید که رشته‌ی s (که متن بهنام است) را بگیرد و تمام کلمات difficult که در آن نوشته شده، به easy تغییر دهد. (استفاده از replace مجاز نیست.)

**پاسخ.**
```python
s = input()
words = s.split()
new_words = []
for x in words:
    if x=="difficult":
        new_words.append("easy")
    else:
        new_words.append(x)
out = ' '.join(new_words)
```

**پرسش دوم.** (۱/۵ نمره) برنامه‌ای بنویسید که عدد n را در ورودی گرفته و سپس در هر کدام از n خط بعدی، یک اندازه نیرو و یک زاویه نسبت به افق بگیرد و بردار برآیند این n نیرو را حساب کند. یعنی اندازه نیرو و زاویه‌ی آن را با فاصله چاپ کند.

**پاسخ.**
```python
import math

n = int(input())
forces = []
angles = []
for i in range(n):
    s = input().split()
    forces.append(float(s[0]))
    angles.append(float(s[1]))
x_force = 0
y_force = 0
for i in range(n):
    angle = math.radians(angles[i])
    x_force += forces[i]*math.cos(angle)
    y_force += forces[i]*math.sin(angle)
total_force = (x_force**2 + y_force**2)**0.5
final_angle = math.degrees(math.atan(y_force/x_force))
print("The total force is :", total_force)
print("The angle is :", final_angle)
```
**پرسش سوم.** (۱/۵ نمره) برنامه‌ای بنویسید که فایل input.txt را رونوشت بگیرد و فایلی با نام inputcopy.txt ایجاد کند.

**پاسخ.**
```python
with open('input.txt', 'r') as f:
  x = f.read()
with open('inputcopy.txt', 'w') as f:
  f.write(x)
```
**پرسش چهارم.** (۱/۵ نمره) متغیری را تعریف کنید و مقدار آن را صفر بگذارید. با گرفتن عدد n از کاربر، n بار سکه بیندازید و اگر شیر آمد از متغیر یک واحد کم کنید و اگر خط آمد، به آن یک واحد اضافه کنید. مقدار نهایی متغیر را چاپ کنید.

**پاسخ.**
```python
import random
x = 0
n = int(input())
for i in range(n):
  z = random.random()
  if z<0.5:
    x = x-1
  else:
    x = x+1
print(x)
```
**پرسش پنجم.** (۲ نمره) متن محرمانه‌ای به دست‌مان رسیده و متوجه شده‌ایم که در این متن، هر حرف با حرف بعدی خودش در الفبا جایگزین شده است (و حرف z با حرف a). برای مثال، Hello World در این متن به این صورت نوشته شده است: Ifmmp Xpsme برنامه‌ای بنویسید که رشته‌ای از این متن محرمانه بگیرد و آن را برای ما رمزگشایی کند.

**پاسخ.**
```python
print(1)
```
