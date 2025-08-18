# جلسه سیزدهم ساختمان داده

## مجموعه (set)
```python
s1 = {}
s2 = set()
directors = {'Fellini', 'Bergman', 'Kieslowski'}
print(directors)
directors.add('Fellini')
print(directors)
directors.pop()
print(directors)
dir2 = directors.union({'Mehjuyee','Hatami', 'Beyzaee'})
print(dir2)
print(directors.intersection({'Tarkowski', 'Wajda', 'Bergman'}))
print(set(l3))
print(list(directors))
print(list(set(l3)))
```
## واژه‌نامه (dictionary)
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
