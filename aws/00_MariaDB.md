# HeidiSQL을 사용한 MariaDB사용

> SQL
>
> * RDBMS 시스템의 테이블에 저장되어 있는 데이터에 대한 CRUD를 처리하는 언어
> * RDBMS 시스템의 데이터 처리 시 사용되는 표준언어

* AWS 에 준비되어 있는 MariaDB 에 접속하고 작업하기 위해서 HidiSQL을 기동하고 신규 버튼을 클릭한다.

![image-20211014191631000](md-images/image-20211014191631000.png)



* Unnamed 라는 이름을 myaws 로 변경한다.

![image-20211014191650712](md-images/image-20211014191650712.png)

![image-20211014191700946](md-images/image-20211014191700946.png)



* 호스트명 : multi-big-mariadb.cux0ffgbppdt.ap-northeast-1.rds.amazonaws.com
  * 계정 : lab01~lab16  암호(공통) : ***

![image-20211014191908568](md-images/image-20211014191908568.png)

![image-20211014191912186](md-images/image-20211014191912186.png)

![image-20211014191938472](md-images/image-20211014191938472.png)



* 수업에 사용할 데이터베이스를 생성한다.

![image-20211014192000113](md-images/image-20211014192000113.png)

![image-20211014192008971](md-images/image-20211014192008971.png)

* 데이터베이스명은 원하는 것으로 해도 되지만 강사가 제공한 소스는 unicodb 로 되어 있다.
* 생성하려는 데이터베이스의 문자셋 정보를 반드시 변경한다.

![image-20211014192048871](md-images/image-20211014192048871.png)

![image-20211014192106384](md-images/image-20211014192106384.png)



* 학습용 데이터베이스 테이블을 생성한다.  (테이블명 : emp)

![image-20211014192128088](md-images/image-20211014192128088.png)

![image-20211014192204366](md-images/image-20211014192204366.png)

![image-20211014192210334](md-images/image-20211014192210334.png)

![image-20211014192214380](md-images/image-20211014192214380.png)



* emp.csv 파일을 읽어서 생성한 emp 테이블에 데이터로 저장한다.

![image-20211014192304041](md-images/image-20211014192304041.png)

![image-20211014192343642](md-images/image-20211014192343642.png)



* 경고창이 출력되지만 무시하고 확인 버튼을 클릭한 후에 문서파일가져오기 창은 x 버튼을 클릭하여 종료한다.

![image-20211014192409353](md-images/image-20211014192409353.png)



* HidiSQL의 메인 윈도우에서 unicodb15의 emp 테이블 옆에 데이터라는 탭을 클릭한다. 다음과 같이 emp.csv 파일의 내용이 emp 라는 테일의 데이터로 삽입된 것을 볼 수 있다. 

![image-20211014192521422](md-images/image-20211014192521422.png)



* 생성된 emp 테이블을 가지고 테이블의 데이터를 추출하는 쿼리를 실행하기 위해서는 데이터라는 탭 옆의 쿼리라는 탭을 클릭한다.

![image-20211014192602441](md-images/image-20211014192602441.png)



* 다음과 같이 SELECT * from emp; 라는 SQL 명령을 입력한 후, 입력된 SQL 명령을 블록킹한 후에 마우스 오른쪽 버튼을 클릭하면 팝업메뉴가 출력되면 여기에서 선택 실행이라는 메뉴를 클릭하여 실행한다.

![image-20211014192610599](md-images/image-20211014192610599.png)

![image-20211014192632697](md-images/image-20211014192632697.png)



* 또 다른 SQL 명령을 실행해 본다. 

  > SELECT empno, ename FROM emp WHERE empno = 7839;

![image-20211014192659347](md-images/image-20211014192659347.png)



> SELECT * FROM emp WHERE sal > 2000;

![image-20211014192739146](md-images/image-20211014192739146.png)



* SQL 명령의 마지막에 세미콜론(;)을 입력하는 것은 선택이다. 가급적 입력해 주는 것이 좋다. 
* 여러 개의 SQL 명령을 한번에 실행할 때 필요하다. 
* 작성된 SQL 명령들을 파일로 저장하기 위해서는 다음과 같이 파일 메뉴에서 저장이라는 메뉴를 선택한다.

![image-20211014192847052](md-images/image-20211014192847052.png)



* 그러면 다음과 같이 다른 이름으로 저장이라는 윈도우 창이 출력된다. 
* 어느 폴더에 저장해도 관계는 없지만 가급적 소스 디렉토리에 SQLexam 이라는 폴더를 만들고 이 폴더안에 exam1 이라는 이름으로 저장한다.

![image-20211014192909722](md-images/image-20211014192909722.png)

![image-20211014192915281](md-images/image-20211014192915281.png)



* 다음과 같이 종료한다.

![image-20211014193100726](md-images/image-20211014193100726.png)

