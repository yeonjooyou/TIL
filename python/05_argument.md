## 인수의 형식

> 파이썬은 인수의 활용 방법에 따라서 3가지로 나뉜다.
>
> 1. 일반 인수
> 2. 가변 인수
> 3. 키워드 가변 인수

### 가변인수(positional argument)

> 지원하는 언어: Python, R, JavaScript, (SQL) ...

예) print() 함수

```python
print() # argument를 전달하지 않는 경우(개행처리)
print(10)
print('abc')
print(10, 20, '가나다') # 여러 개의 argument를 전달하는 경우
print(...)

print(10, 20, 30, sep='@', end='\n\n') # keyword argument
```

> 변수명 앞에 `*` 을 붙인다.
>
> 단, 인수 목록의 마지막에 와야 한다.

``` python
def intsum(*ints) :
    sum = 0
    for num in ints :
        sum += num
    return sum
```

```python
intsum(s, *ints)     # 가능
intsum(*ints, s)     # 에러
intsum(*ints, *nums) # 에러
```



```python
range(10) # 시작값: 0, 증가치: 1 (0~9)
range(5, 10) # 5~9
range(10, 20, 2) # 10~19, 증가치: 2
```



### 기본값을 갖는 매개변수

> 실인수를 생략하면 기본값을 전달한 것으로 가정한다.

```python
def calcstep(begin, end, step = 1) :
    sum = 0
    for num in range(begin, end+1, step) :
        sum += num
    return sum

print('1 ~ 10 =', calcstep(1, 10, 2))
print('1 ~ 100 =', calcstep(1, 100))  # step = 1
```



### 키워드 인수

> '변수명 = 데이터 값' 형식으로 (인수 이름을 지정하여 대입 형태로) 전달하는 방식
>
> 단, 앞쪽에 키워드 인수가 있으면 뒤쪽에 위치 인수가 올 수 없다.

```python
def clcstep(begin, end, step) :
    sum = 0
    for num in range(begin, end+1, step) :
        sum += num
    return sum
print('3 ~ 5 =', caclstep(3, 5, 1)) # 위치인수(positional argument)
print('3 ~ 5 =', caclstep(step = 1, end = 5, begin = 3)) # 순서를 지키지 않아도 됨
```



### 위치인수

> 데이터 값만 나열하여 전달하는 경우



### 키워드 가변인수

> `**` 기호를 인수 목록에 붙여 키워드 인수를 가변 개수 전달함

```python
def calcstep(**args) :
    begin = args['begin']
    end = args['end']
    step = args['step']
    
    sum = 0
    for num in range(begin end+1, step) :
        sum += num
    return sum
```







## 변수의 범위

> 변수의 범위(scope): 변수가 생성된 후 언제까지 이 변수를 사용할 수 있는지 정한 범위



### 1. 전역코드

> 생성되는 변수: 전역변수 -> 파이썬 스크립트 파일의 수행이 끝날 때까지 변수 사용이 가능

```python
salerate = 0.9

def kim() :
    print("오늘의 할인율 :", salerate)
def lee() :
    price = 1000
    print("가격 :", price * salerate)
    
kim() # salerate = 0.9 를 적용
salerate = 1.1
lee() # salerate = 1.1 를 적용
```



### 2. 함수코드블럭

> 생성되는 변수: 지역변수 -> 함수 내에서만 사용 가능

```python
# 초기화하는 장소에 따라 변수의 범위가 결정된다.
price = 1000 # 전역변수

def sale() :
    price = 500 # 지역변수
    
sale()
print(price) # 실행결과 : 1000
```

