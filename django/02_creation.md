# 생성된 프로젝트를 파이참으로 옮기기

1. 파이참에서 **File>Open**을 선택한 후, **C:\yyj\DJANGOexam\studyproject** 를 open한다.

![image-20210723141957520](md-images/image-20210723141957520.png)

open이 잘 되면 다음과 같이 인식되는 것을 볼 수 있다.

![image-20210723140222343](md-images/image-20210723140222343.png)



2. **File>Settings** 를 선택하고 **studyproject의 프로젝트 인터프리터를 가상환경으로 선택**한다.

![image-20210723142102784](md-images/image-20210723142102784.png)

다음과 같은 서브윈도우가 출력되면 **Project: studyproject**의 **Python Interpreter**를 선택한다.

![image-20210723140553954](md-images/image-20210723140553954.png)

![image-20210723140619987](md-images/image-20210723140619987.png)

![image-20210723140651769](md-images/image-20210723140651769.png)

![image-20210723140721346](md-images/image-20210723140721346.png)

![image-20210723140758279](md-images/image-20210723140758279.png)

![image-20210723140925685](md-images/image-20210723140925685.png)



3. 환경 구성이 완료될 때까지 기다린 후, 파이참 하단 왼쪽에 있는 **Terminal**을 선택하여 cmd와 비슷한 창을 출력한다.

![image-20210723141029883](md-images/image-20210723141029883.png)

![image-20210723141120957](md-images/image-20210723141120957.png)



4. 학습용 소스들을 작성할 **firstapp**이라는 장고 앱을 하나 생성한다.

![image-20210723141159322](md-images/image-20210723141159322.png)



5. firstapp이라는 장고 앱을 생성하면 다음과 같은 디렉토리 구조가 생성된다.

![image-20210723141253817](md-images/image-20210723141253817.png)



6. 그 중 특정 파일들의 내용을 수정한다.

* studyproject>views.py

![image-20210723141602649](md-images/image-20210723141602649.png)



* studyproject>settings.py

![image-20210723141429080](md-images/image-20210723141429080.png)



* studyproject>urls.py

![image-20210723141536761](md-images/image-20210723141536761.png)



7. 세 개의 파일의 수정이 된 것을 확인한 후, 서버를 기동시킨다.

![image-20210723141738672](md-images/image-20210723141738672.png)



8. 브라우저에서 다음 URL로 요청해 본다.

![image-20210723141815898](md-images/image-20210723141815898.png)

