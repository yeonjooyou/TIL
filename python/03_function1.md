# 함수기초

> 입력값  -> 함수 -> 출력값
>
> 1. 함수를 정의하는(만드는) 방법
>
> 2. 정의된 함수를 필요에 따라 사용하는 방법
>
>    ex)  API : print(), input(), int(), chr(), len(), range(), random.randint()

## 함수의 종류

> 함수를 호출하면서 전달하는 데이터 값을 `argument` 또는 인수라고 한다.

### 1. 내장함수(Bulit-in Fuction)

> 파이썬 패키지에서 제공하는 함수
>
> * 입력과 출력 : input, print()
> * 타입 변환 : int(), str(), float()
> * 진법 변환 : hex, oct, bin

* *3.6 버전 기준으로 68개의 내장함수를 제공한다.*

`abs()` , `dict()` , `help()` , `min()` , `max()` , `setattr()` , `all()` , `dir()` , `hex()` , `next()` ,

`slice()` ,`any()` , `divmod()` , `id()` , `object()` , `sorted()` , `ascii()` , `enumerate()` , `input()` , `oct()` ,

`staticmethod()` , `bin()` , `eval()` , `int()` , `open()` , `str()` , `bool()` , `exec()` , `isinstance()` , `ord()` , 

`sum()` , `bytearray()` , `filter()` , `issubclass()` , `pow()` , `super()` , `bytes()` , ` float()` , `iter()` , `print()` , 

`tuple()` , `callable()` , `format()` , `len()` , `property()` , `type()` , `chr()` , `frozenset()` , `list()` , `range()` , 

`vars()` , `classmethod()` , `getattr()` , `locals()` , `repr()` , `zip()` , `compile()` , `globals()` , `map()` , `revesed()` ,

`_ _import_ _()` , `complex()` , `hasattr()` , `round()` , `delattr()` , `hash()` , `memoryview()` , `set()` 



#### 함수의 기능을 모를 땐?

> help() 함수를 이용한다.
>
> ex) help(함수명)




  * package 종류
    * pandas - 데이터 추출, 병합, 가공
    * numpy - 행렬
    * matplotlib, seaborn - 그래프



### 2. 사용자 정의 함수

* 함수 생성 및 호출 방법

```python
def add(a, b) :
    c = a + b
    return c

print(add(5, 7))
```

``` python
def calcsum(n) :
    """1 ~ n 까지의 합을 구해 리턴한다."""
    sum = 0
    for i in range(n + 1) :
        sum += i
    return sum
help(calcsum)
```

> calcsum(n)
>     1 ~ n 까지의 합을 구해 리턴한다.
>
>
> Process finished with exit code 0



### 3. 중첩함수(nested function)

```python
# 변수선언 # 전역변수(global Variable)
n = 2

def 함수1 : # 외부함수(outer function)
    # 변수선언 # 지역변수(local variable)
    for x in [1,2,3,4] :
        i = n + 1
        
    def 함수2 : # 내부함수(inner function)
        # 변수선언 # 지역변수(local variable)
```



### 4. 재귀함수(reculsive function)

> 외부함수 = 내부함수

```python
# 예시 - 팩토리얼 계산
def 함수1(a) :
    z = 0
    n = a
    z += n
    print(z)
    
    if n =  :
        exit()
    z = 함수1(a-1)
    
    return z
```



### 5. 특수함수(lambda)

```python
def func(x, y) :
    # z = x + y
    
    return x + y, x - y
plus = lambda x, y : z = x + y(1, 2)
```





## 함수의 사용

* 함수의 필요성을 점검하는 예제

```python
sum = 0
for num in range(5):
    sum += num
print("~ 4 =", sum)

sum = 0
for num in range(11):
    sum += num
print("~ 10 =", sum)

print("----- 함수 사용 -----")

def calcsum(n):
    sum = 0
    for num in range(n + 1):
        sum += num
    return sum

print("~ 4 =", calcsum(4))
print("~ 10 =", calcsum(10))
```



```python
input_data = input("이름을 입력하세요: ")
name_length = len(input_data)

print(len("abc"))   # -> 3
print(len("가나다")) # -> 3
# 단, 프로그래밍 언어에 따라서 영문은 1 한글은 2로 길이 계산을 하는 것도 있음.
```



- '매개변수'는 함수가 호출 될 때 전달되는 아규먼트를 받는 변수
  예) def myFunction1() :
  코드블럭

      def my Function2(p) :

  코드블럭

      def my Function3(deco, num) :

  코드블럭


리턴값 예) None, True, Flase



```python
# 예) 별 문자열을 자주 출력하는 경우
def printStar() :
	return "*"*10

def printCaret() :
	return"^"*20

printStar()
printCaret()


def printDeco(deco_munja, num) :
	return deco_munja*num

printDeco("*", 50)
```

