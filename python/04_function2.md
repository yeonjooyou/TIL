# 함수의 이용

1. 

```python
def Func1(name, *names):
    print(name)  # 가인수 : 홍길동
    print(names)  # 가변 인수 : ('이순신', '유관순')


Func1("홍길동", "이순신", "유관순")

#Character(문자) : 'a' , '1'
#String(문자열) : 'bcd'
#리스트(List) : [1,2,3,4, 'a', 'bcd', True, 3.14]
#튜플 : (1,2,3,4, 'a', 'bcd', True, 3.14)
#셋(set) : { 1,2,3,4, 'a', 'bcd', True, 3.14}
#딕트(Dict) : {key1:value1,key2:value2,....}
#dict_var = {'홍길동': 35, addre:'서울시', height:175, weight:65}
#print('dict_var =', dict_var)
#dict('홍길동', 35, addre='서울시', height=175, weight=65)

#lst = [1,2,3,4, [1,2,3,4], (1,2,3,4)'a', 'bcd', True, 3.14]
#print('lst = ', lst)
```



```python
def intsum(*ints) :
    sum = 0
    print('intsum = ', ints)
    for num in ints : # 1, 2, 3
        sum += num
    return sum

print(intsum(1, 2, 3))
print(intsum(5, 7, 9, 11, 13))
print(intsum(8, 9, 6, 2, 9, 7, 5, 8))
```

> intsum =  (1, 2, 3)
> 6
> intsum =  (5, 7, 9, 11, 13)
> 45
> intsum =  (8, 9, 6, 2, 9, 7, 5, 8)
> 54
>
> Process finished with exit code 0



2. 축약함수(lambda function)

> 한 줄 함수
>
> 형식) 변수 = (lambda 인수 : 리턴값).upper().split()
>
> ex) lambda x, y : x + y

```python
print('add = ', (lambda x, y : x + y)(10, 20))
```

>add =  30
>
>Process finished with exit code 0



```python
height = input("키를 입력하세요 :")
if height.isdecimal():
    print("키 =", height)
else:
    print("숫자만 입력하세요.")
```



3. 사전형 가변인수(dict_change_variable function)

```python
def emp_func(name, *age, **other) :
    print(name)
    print()
    print(age)
    print()
    print(other) # {'addre': '서울시', 'height': 175, 'weight': 65}
    
emp_func('홍길동', 35, 45, addre='서울시', height=175, weight=65)
```

> 홍길동
>
> (35, 45)
>
> {'addre': '서울시', 'height': 175, 'weight': 65}
>
> Process finished with exit code 0



4. 재귀함수(reculsive function)

```python
def Counter(n) :
    if n == 0 :
        return 0 # exit 조건
    else :
        print('n = ', n)
        Counter(n-1)
    print(n, end = ' ')
    
#pring('n = 0 : ', Counter(0))
Counter(5)
```

>n =  5
>n =  4
>n =  3
>n =  2
>n =  1
>1 2 3 4 5 
>Process finished with exit code 0

