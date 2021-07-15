# 파일

## 1. 파일 입출력

### 1.1 파일 쓰기

* 파일

  * 정보를 저장하는 기본 단위
  * 문서, 이미지, 멀티미디어 자료 등을 모두 보관

* 파일 입출력

  * 오픈

    * open(파일경로, 모드)

  * 모드

    * 파일로 무엇을 할 것인지 지정

    ![image-20210715130637530](md-images/image-20210715130637530.png)

* `open` 함수

  * 파일 입출력 준비 및 파일 객체 반환
  * 출력할 데이터 인수로 전달하여 `write` 메서드 호출
  * 파일 사용 후 `close` 메서드로 닫기

  ```python
  f = open("live.txt", "wt", encoding="UTF-8")
  print(f, type(f))
  f.write("""삶이 그대를 속일지라도
  슬퍼하거나 노하지 말라!
  우울한 날들을 견디면
  믿으라, 기쁨의 날이 오리니""")
  f.close()
  ```

  

### 1.2 파일 읽기

* 적절한 함수를 골라 파일 데이터 읽기
* `read` 함수

```python
try:
    f = open("live.txt", "rt", encoding="UTF-8")
    print(f, type(f))
    text = f.read()
    print(text)
except FileNotFoundError:
    print("파일이 없습니다.")
finally:
    f.close()
```

* `readline` 함수

  * 한 줄씩 읽기
  * 파일 마지막에 빈 문자열 반환

  ```python
  f = open("live.txt", "rt", encoding="UTF-8")
  text = ""
  line = 1
  while True:
      row = f.readline() # 한 행씩 읽기
      if not row: break
      text += str(line) + " : " + row
      line += 1
  f.close()
  print(text)
  ```

  

### 1.3 입출력 위치

* 순차 접근
  * 파일을 순서대로 읽음
* 임의 접근
  * 입출력 위치를 바꿔가며 원하는 부분을 자유롭게 읽음
* `tell` 함수
  * 입출력 위치 조사
* `seek` 함수
  *  위치 변경



### 1.4 내용 추가

* `a` 모드

  * 기존 내용 그대로 유지하고 뒤에 덧붙임

* `w` 모드

  * 파일이 이미 있는 경우 덮어쓰고 새로 만듦

  ```python
  # =============== append  ===============
  f = open("live.txt", "at", encoding="UTF-8")
  f.write("\n\n[추가]푸쉬킨 형님의 말씀이었습니다.")
  f.close()
  ```

  ```python
  # =============== withas  ===============
  with open("live.txt", "rt", encoding="UTF-8") as f:
     text = f.read()
  print(text)
  
  help(f.seek)
  ```




![image-20210715172102870](md-images/image-20210715172102870.png)





## 2. 파일 관리

### 2.1 파일 관리 함수

![image-20210715131332077](md-images/image-20210715131332077.png)

```python
# =============== filecopy  ===============
import shutil
import os

if os.path.exists("live2.txt") :
   print("파일이 존재합니다.")
else :
   print("파일이 존재하지 않습니다.")

print("[ 파일 복사 ]")
shutil.copy("live.txt", "live2.txt")
if os.path.exists("live2.txt") :
   print("파일이 존재합니다.")
else :
   print("파일이 존재하지 않습니다.")
```



### 2.2 디렉토리 관리 함수

![image-20210715131419660](md-images/image-20210715131419660.png)

```python
# =============== listdir  ===============
import os

files = os.listdir("c:\\Temp")
print(type(files))
for f in files:
    print(f)
```



### 2.3 파일 관리 유틸리티

> ex) 파일명 일괄 수정
>
> ```python
> import os
> 
> path = "C:\\Temp"
> files = os.listdir(path)
> for f in files:
>     if (f.find("_") and f.endswith(".jpg")):
>         name = f[0:-4]
>         ext = f[-4:]
>         part = name.split("_")
>         newname = part[1].strip() + "-" + part[0].strip()+"-new" + ext
>         print(newname)
>         os.rename(path + "\\" + f, path + "\\" + newname)
> ```

* `listdir` 함수
  * 모든 파일 목록 조사한 후 각 파일 순회
  * 해당되는 파일 재조립
* `split` 함수
  * `-` 기준으로 파일명을 두 조각으로 나눔
  * 순서를 바꾸어 합치기 위함
* `strip` 함수
  * 불필요한 공백 제거

