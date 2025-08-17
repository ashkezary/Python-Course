# جلسه سیزدهم

# ساختمان داده

1⃣ چند نکته تکمیلی در مورد دیکشنری

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
