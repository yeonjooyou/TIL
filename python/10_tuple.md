# 튜플(tuple)

### 불변 자료 집합

* 튜플은 **초기화한 후 편집할 수 없다**는 점에서 리스트와 차이
* 소괄호 사용하여 정의
* print : 튜플 출력 시 소괄호를 함께 출력하여 리스트가 아님을 나타냄
* 정의할 때에는 소괄호 없이 값만 나열해도 무관함
  * 요소가 하나 밖에 없는 경우에는 값 다음 콤마를 찍어 튜플임을 표시

### 튜플로 가능한 일

* `+` / `*` 연산자를 사용하여 연결 및 반복

  * 요소를 변경하거나 삭제할 수는 없음

  ```python
  tu = 1, 2, 3, 4, 5
  print(tu[3])       # 가능
  print(tu[1:4])     # 가능
  print(tu + (6, 7)) # 가능
  print(tu * 2)      # 가능
  tu[1] = 100        # 불가능
  del tu[1]          # 불가능
  ```

* 여러 개의 변수에 값을 한꺼번에 대입

  * 좌변에 변수 목록, 우변에 튜프을 대입

  ```python
  tu = '이순신', '김유신', 강감찬'
  lee, kim, kang = tu
  print(lee)  # 이순신
  print(kim)  # 김유신
  print(kang) # 강감찬
  ```

* 두 개 이상 값을 반환

  * 내부에 요소 포함하는 튜플 사용

  ```python
  import time
  
  def gettime() :
      now = time.localtime()
      return now.tm_hour, now.tm_min
  
  result = gettime()
  print("지금은 %d시 %d분입니다" % (result[0], result[1]))
  # 지금은 5시 26분 입니다
  ```

  * `import` : 모듈 기능 사용 명령
  * `divmod` : 나눗셈의 몫과 나머지를 튜플로 묶어 리턴

