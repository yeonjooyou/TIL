# Anaconda에 가상환경 만들기

> 파이썬 3.8 기반의 가상환경 pydatavenv 를 생성하는 명령을 실행한다.

* conda create --name **pydatavenv** python=3.8

![image-20210927092318570](md-images/image-20210927092318570.png)

* y 를 입력하고 엔터키를 누른다.

![image-20210927092400202](md-images/image-20210927092400202.png)

* 다음 명령을 실행시켜서 pydatavenv 라는 이름으로 가상환경이 잘 만들어졌는지 확인한다.

> conda info --envs

![image-20210927092519062](md-images/image-20210927092519062.png)

* pydatavenv 라는 이름으로 만든 가상환경을 활성화한다.

> conda activate pydatavenv
>
> conda install ipykernel

![image-20210927092723207](md-images/image-20210927092723207.png)

* y 를 입력하고 엔터키를 누른다.

![image-20210927092803704](md-images/image-20210927092803704.png)

![image-20210927092827408](md-images/image-20210927092827408.png)

* python -m ipykernel install --user --name pydatavenv 명령을 실행시켜서
  pydatavenv 라는 가상환경을 jupyter lab 의 커널로 등록한다.

![image-20210927093445481](md-images/image-20210927093445481.png)



* Anaconda Prompt 창을 한 개 더 오픈하고 jupyter lab 를 기동시킨다.

![image-20210927093537156](md-images/image-20210927093537156.png)

* 다음과 같이 Python3 버튼 옆에 새로 추가한 pydatavenv 라는 커널에 대한 버튼이 추가된 것을 확인할 수 있다.

![image-20210927093621665](md-images/image-20210927093621665.png)

* pydatavenv 라는 커널 버튼을 클릭하면 pydatavenv 라는 커널 기반의 노트북 화면이 하나 출력된다. 파일명을 second.ipynb 로 변경하고 소스작성 셀에 10 * 20 을 입력한후 실행 버튼 클릭 시 200이 결과로 출력되는지 확인한다.

![image-20210927093814819](md-images/image-20210927093814819.png)



# pydatavenv 가상환경에 추가패키지 설치하기

* conda install requests

![image-20210927100750348](md-images/image-20210927100750348.png)

* conda install pillow

![image-20210927100753154](md-images/image-20210927100753154.png)

* conda install bs4

![image-20210927100758240](md-images/image-20210927100758240.png)

* conda install selenium

![image-20210927100801176](md-images/image-20210927100801176.png)

* conda install lxml

![image-20210927100805138](md-images/image-20210927100805138.png)

* conda install html5lib

![image-20210927100809551](md-images/image-20210927100809551.png)

* pip install tweepy

![image-20210927100813688](md-images/image-20210927100813688.png)

