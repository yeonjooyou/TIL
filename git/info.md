## GitHub Q&A

### 질문1

> github와 같이 사용되는 협업 툴

* 소스코드 관리를 위한 Github
* 커뮤니케이션을 위한 slack
* 사내 위키 / 문서화 등을 위한 Notion, Confluence
* 프로젝트 관리(kanban 구조)를 위한 Trello, Jira



### 질문2

> 블로그에 올린 내용들을 깃허브에 옮기는 방법

* 안타깝게도 네이버 블로그에 올린 부분들은 어렵다.
* 마크다운 기반의 기술 블로그를 하려면 아래와 같은 정적 사이트 생성기를 사용해야한다.
  * Jekyll
  * Gatsby
  * Hexo
* 그리고 대부분 Github pages를 활용하는 편이다.



### 질문3

> 오류발생

```bash
$ git push -u origin main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/.../first.git'
```

* 현재 Git bash 2.32에서 인증 창이 안뜨는 버그가 존재한다.

```bash
$ git config --global credential.provider generic
```

을 입력 후 진행하거나 2.31 버전으로 다운그레이드 시키는 방법이 있다.



## 공유문서

#### [더보기]

* 강사님 github
  * [김00 강사님](https://github.com/edutak)

* 알고리즘 문제풀이

  * [알고리즘 문제풀이](https://github.com/edutak/algorithm)

* 카카오 택시가 바꿔놓은 대중교통 지도 (카카오 택시 데이터(2018))

  * [카카오 빅데이터의 발견 / 카카오 교통 020 백서 프리뷰(3편)](https://brunch.co.kr/@kakao-it/38)

* NAVER O2_백엔드 개발자 되기

  * [백엔드 개발자를 꿈꾸는 학생개발자에게](https://d2.naver.com/news/3435170)
  * 레벨0: 이미 쓰고 있는 개발도구의 사용법을 알려주거나 가이드 문서를 줘도 잘 못 씀
  * 레벨1: 알려주거나 같은 팀에서 만든 가이드 문서에 있는 만큼만 쓸 수 있음
  * 레벨2
    - 개발도구의 공식 레퍼런스를 보고 사용법을 스스로 익힐 수 있음
    - 자신이 경험한 사용법을 문서화해서 팀 내에 전파할 수 있음
  * 레벨3
    - 여러 개발도구를 비교 분석해서 상황에 적합한 도구를 선택할 수 있음
    - 공식 레퍼런스 문서에서 부족한 부분을 수정해서 기여할 수 있음
  * 레벨4
    - 개발도구의 문제를 소스 코드를 수정해서 Fork/패치해서 사용할 수 있음

  신입사원이라도 레벨2 정도는 함께 일할 개발자에게 기대를 하게 됩니다.

* Git 안내서

  * [Git 간편 안내서](http://rogerdudler.github.io/git-guide/index.ko.html)
  * [GitHub 홈페이지 안내서](https://guides.github.com/activities/hello-world/)
  * [Git 책](https://git-scm.com/book/ko/v2)
  * [누구나 쉽게 이해할 수 있는 Git 입문](https://backlog.com/git-tutorial/kr/stepup/stepup1_1.html)

