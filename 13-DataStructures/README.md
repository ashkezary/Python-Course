# جلسه سیزدهم (ساختمان داده)

در زبان‌های برنامه‌نویسی برای نگهداشتن تعدادی داده، می‌توانیم از ساختمان‌داده‌های مختلفی استفاده کنیم. در این درس تا اینجای کار با داده‌ساختار لیست آشنا شدیم که با آن می‌توانستیم به سادگی داده‌ها را به ترتیب نگه داریم و به هر خانه با اندیس مشخصی دسترسی داشته باشیم. در این جلسه سه ساختمان‌داده دیگر نیز معرفی خواهد شد.

## ۱) مجموعه (set)
اگر بخواهیم داده‌هایی را به صورت غیرتکراری نگه داریم، می‌توانیم از داده‌ساختار `set` استفاده کنیم. در قطعه کد زیر عملیات‌های اولیه‌ای که روی یک مجموعه می‌توانیم انجام دهیم، معرفی شده است.
```python
s1 = {}     # Create an empty set
s2 = set()  # Create an empty set
directors = {'Fellini', 'Bergman', 'Kieslowski'}    # Create a set of strings
print(directors)    # Print set members
directors.add('Fellini')    # Add a member to the set
print(directors)
directors.pop()             # Delete a member of set
print(directors)
dir2 = directors.union({'Mehjuyee','Hatami', 'Beyzaee'})    # Union of two sets
print(dir2)
print(directors.intersection({'Tarkowski', 'Wajda', 'Bergman'}))    # Intersection of two sets
print(set(l3))
print(list(directors))    # Convert a set to list
print(list(set(l3)))
```

## ۲) واژه‌نامه (dictionary)
```python
aircrafts = {'F4':'Phantom',
             'F5': 'Tiger',
             'F14': 'Tomcat'}
print(aircrafts)
print(aircrafts['F4'])
print(aircrafts.keys())
aircrafts['F16'] = 'Falcon'
print(aircrafts)
print(aircrafts.values())
print(aircrafts.get('F14'))
aircrafts.items()
for x,y in aircrafts.items():
    print(x,y)
```
### نکاتی در مورد دیکشنری

- تفاوت get و [] برای دسترسی به مقدار یک کلید
- تغییر مقدار به کمک [] و update
- نحوه ادغام دو دیکشنری به کمک update

```python
d = dict()
info = {'title': 'Strada',
        'Year': 1962,
        'Cast': ['A. Quine', 'J. Massina']}
print(info['title'])
print(info.get('title', 'Gashtam Nabood'))
info['Country'] = 'Italy'
info.update({'Director': 'F. Fellini'})
print(info)
```
