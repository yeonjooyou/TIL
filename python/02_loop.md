# Loop

> 반복적으로 처리하는 명령
>
> ex) 1+2+3+4+5+6+7+8+9+10+ ...

```python
for i in range(0,3,1) :
	print(i, ": 안녕하세요? for 문을 공부 중입니다.^^")
```



 ## for 문

```python
for student in [1, 2, 3, 4, 5] :
    print(student, "번 학생의 성적을 처리한다.")
```

```python
# range 명령
range(11)     # --> 0,1,2,3,4,5,6,7,8,9,10
range(1,11)   # --> 1,2,3,4,5,6,7,8,9,10
range(1,11,2) # --> 1,3,5,7,9
range(5,21,5) # --> 5,10,15,20

sum = 0
for num in range(1, 101) :
    sum += num
print("sum =", sum)
```

```python
# break
score = [92, 86, 68, 120, 56]
for s in score :
    if(s < 0 or s > 100) :
        break
    print(s)
print("성적 처리 끝")

# continue
score = [92, 86, 68, -1, 56]
for s in score :
    if(s == -1) :
        continue
    print(s)
print("성적 처리 끝")
```

```python
# 이중 루프
for dan in range(2, 10) :
    print(dan, "단")
    for hang in range(2, 10) :
        print(dan, "*", hang, "=", dan * hang)
    print()
```



## while 문

```python
num = 1
sum = 0
while num <= 100 :
    sum += num
    num += 1
print("sum =", sum)
```

```python
# 이중 루프
dan = 2
while dan <= 9 :
    hang = 2
    print(dan, "단")
    while hang <= 9 :
        print(dan, "*", hang, "=", dan * hang)
        hang += 1
    dan += 1
    print()
```

