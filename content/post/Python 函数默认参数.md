---
title: "Python 函数默认参数"
date: 2020-02-27T14:10:00+01:00
tags: ["Python"]
categories: ["Skills"]
draft: false
comments:       true
showMeta:       true
showActions:    true
thumbnailImagePosition: "left"
thumbnailImage: /img/function.png
---

Python 中定义函数的默认参数需要注意：将**无默认值**的变量放在前边，不然会报错。<!--more-->

```python
def sale_car(price, brand,color='red',second_hand='True'):
  print('price:',price,
        'color:',color,
        'brand:',brand,
        'second_hand:',second_hand,)
  
sale_car(6000,'Polo',color='blue')
>>> price: 6000 color: blue brand: Polo second_hand: True
```

全局变量和局部变量