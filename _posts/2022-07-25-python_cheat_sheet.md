---
layout: page
title: Cheatsheet for Simple Things in Python
permalink: 
---

#### Format numbers with commas in a print statement
```python
num_to_display = 1000000
print(f'displaying the number with commas {num_to_display:,}')

>>> 1,000,000
```
<br/>

#### Format floats as percentage in a print statement
```python
num_to_display = 10/22
print(f'displaying the number with commas {num_to_display:.2%}')

>>> 45.45%
```
<br/>

#### Format floats with fixed number of decimals in a print statement
```python
num_to_display = 10/22
print(f'displaying the number with commas {num_to_display:.2f}')

>>> 0.45
```
<br>
#### [Use regex in Pandas](https://kanoki.org/2019/11/12/how-to-use-regex-in-pandas/ "Kanoki Blog") - no sense in duplicating the excellent material on this blog, just go see the original source material