# 두 번째 장고 앱 생성

1. 파이참 하단 왼쪽에 있는 Teminal을 선택하여 터미널 창을 출력한 후,

   학습용 소스들을 작서할 **secondapp**이라는 장고 앱을 하나 생성한다.

![image-20210723151304343](md-images/image-20210723151304343.png)



2. secondapp에 **templates**라는 새로운 폴더를 생성한다. 

![image-20210723151556938](md-images/image-20210723151556938.png)

![image-20210723151610196](md-images/image-20210723151610196.png)



## exam1.html

3. templates 폴더에 **exam1.html**이라는 새로운 파일을 생성한다.

![image-20210723152210137](md-images/image-20210723152210137.png)

![image-20210723152214541](md-images/image-20210723152214541.png)

​	3-1. 생성한 파일에 다음과 같은 내용을 작성한다.

![image-20210723152450474](md-images/image-20210723152450474.png)



4. secondapp에 **urls.py**라는 Python File을 하나 생성한다.

![image-20210723153258184](md-images/image-20210723153258184.png)

​	4-1. 생성한 파일에 다음과 같은 내용을 작성한다.

![image-20210723153421292](md-images/image-20210723153421292.png)



5. **views.py**라는 파일에 다음과 같은 내용을 작성한다.

![image-20210723153511657](md-images/image-20210723153511657.png)



6. **studyproject**라는 폴더의 **settings.py**라는 파일에서

   **33행**에 다음과 같은 내용을 작성한다.

![image-20210723153624261](md-images/image-20210723153624261.png)



7. 이어서 같은 폴더의 **urls.py**라는 파일에 다음과 같은 내용을 추가한다.

![image-20210723153710104](md-images/image-20210723153710104.png)



8. 지금까지 작성한 코드에 대해, 서버를 기동시킨다.

![image-20210723153914232](md-images/image-20210723153914232.png)



9. 브라우저에서 다음 URL로 요청해 본다.

![image-20210723153928251](md-images/image-20210723153928251.png)

> 이때, *templates>urls.py*가 main이며, 전역적으로 사용된다.





## exam2.html

1. **exam2.html**파일을 생성한다.

![image-20210723154913126](md-images/image-20210723154913126.png)

![image-20210723154919153](md-images/image-20210723154919153.png)



2. 다음과 같은 내용을 exam2.html에 작성한다.

![image-20210723154953796](md-images/image-20210723154953796.png)



3. **views.py**파일에 다음과 같은 내용을 추가한다.

![image-20210723154841924](md-images/image-20210723154841924.png)



4. **urls.py**파일에 다음과 같은 내용을 추가한다.

![image-20210723155020123](md-images/image-20210723155020123.png)



5. 브라우저에서 다음 URL로 요청해 본다.

![image-20210723155144969](md-images/image-20210723155144969.png)

​	5-1. **?name=연주** 를 덧붙여서 브라우저에 요청해 본다.

> 'name'이라는 변수에 '연주'라는 값을 전달하여 브라우저에 전달한다.

![image-20210723155341557](md-images/image-20210723155341557.png)







