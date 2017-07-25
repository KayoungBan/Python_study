## 1.  Make Trinary Group (OOP)

### 1) Make Trinary Class
* object에 'a', 'b', 'c' 중 하나를 넣지 않으면, error 프린트하고 'a'를 넣어줌.
* ex) A = Trinary('k') → A : Trinary('a')
``` python
class Trinary(object):
    def __init__(self, elt):
        if(elt not in ['a','b','c']):
            self.e = 'a'
            print('Trinary must be in [a,b,c]')
            print("Set default 'a'")
        else:
            self.e = elt
```



### 2) Define Methods
* Add & multiple : 그냥 하나씩 정의

``` python
    def __add__(self, other):
        if self.e=='a':
            if other.e=='a':
                return Trinary('c')
            elif other.e=='b':
                return Trinary('c')
            else:
                return Trinary('b')
        elif self.e=='b':
            if other.e=='a':
                return Trinary('c')
            elif other.e=='b':
                return Trinary('a')
            else:
                return Trinary('a')
        else:
            if other.e=='a':
                return Trinary('b')
            elif other.e=='b':
                return Trinary('a')
            else:
                return Trinary('b')
    def __mul__(self,other):
        if self.e=='a':
            if other.e=='a':
                return Trinary('a')
            elif other.e=='b':
                return Trinary('a')
            else:
                return Trinary('a')
        elif self.e=='b':
            if other.e=='a':
                return Trinary('a')
            elif other.e=='b':
                return Trinary('b')
            else:
                return Trinary('c')
        else:
            if other.e=='a':
                return Trinary('a')
            elif other.e=='b':
                return Trinary('c')
            else:
                return Trinary('b')
```

* Power :
```python
    def __pow__(self, num):
        if num==1:
            return self
        else:
            return self*self**(num-1)
```
* String : self.e(string)과 '[Trinary]'(string)은 +를 이용하면 출력할 때 붙어서 나온다.

    ex) A가 Trinary('a')였다면, print(A) → a[Trinary]
```python
    def __str__(self):
        return self.e + '[Trinary]'
```

<br>

## 2. Orbit of the Earth (Numerical Integration)


