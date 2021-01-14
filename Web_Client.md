# [ 웹 프로그래밍 기술 - 클라이언트 ]

웹 사이트를 구축하려면 웹 페이지를 먼저 개발해야한다.

#### ---> **HTML(Hyper Text Markup Language)**

텍스트, 이미지, 동영상 등을 어떻게 표현할지를 정하는 언어로서 마크업 방식으로 구현한다.



<h1> 울라프 </h1> 

제일 크게 출력됨. **더블사이즈태크: 시작과종료지정**

<h3>울라프</h3>



<a href = "http://www.w3schools.com/">울라프</a>

하이퍼 링크 텍스트

<img src="olaf1.png">   

**싱글사이즈태크:시작만지정, 종료태크 없음**

울라프이미지 출력 (울라프 이미지가 같은 폴더내에 있다 가정하에)



<table border="1"><tr><td>올라프</td></tr></table>

**border 속성은 표의 굵기를 지정하는 속성**

**tr태크 : 행 원하는 만큼 반복 지정, td 태크 : 열 원하는 만큼 반복 지정**

<참고>

<th> 내용</th> : table head 의 약자로, 표의 제목을 쓰는 역할 (기본값 : 굵은 글씨체, 중앙정렬)

<tr>내용</tr> : table row  의 약자로, 가로줄을 만드는 역할 (기본값 : 보통 글씨체, 왼쪽정렬)

<td>내용</td> : table data 의 약자로, 셀을 만드는 역할 (기본값 : 보통 글씨체, 왼쪽정렬)

<table border="1">
    <tr>
        <th>번호</th>
        <th>이름</th>
    </tr>
    <tr>
        <td>1</td>
        <td>강호동</td>
    </tr>
    <tr>
        <td>2</td>
        <td>이수근</td>
    </tr>
</table>



<a href = "https://www.w3schools.com/tags/default.asp/">html 태크들</a>







#### ---> **CSS**(Cascading Style Sheets)

HTML 태그에 의해서 웹 페이지가 출력(랜더링)될 때 스타일을 조정할 수 있는 기술

<h1 style = "color : orange">올라프</h1>

원래 칼라는 검은색이지만, 오렌지 색으로 출력한다.



<h1 style = "color : orange; background-color:green">올라프</h1>





<style>
    h1{
        color:orange;
        background-color:green
    }
</style>

이 웹페이지에 있는 h1을 찾아서 칼라는 오렌지색, 배경색은 그린으로 한다.



#### ----> JavaScript

웹 페이지를 만들 때 프로그램적으로 처리해야하는 기능이 있을 때 사용하는 주로 웹 개발에서 사용되는 프로그래밍 언어

브라우저에서 수행 가능한 프로그래밍 언어

(대부분의 브라우저에서는 자바스크립트 인터프리터(엔진)를 내장하고 있다.)  

=> 동적인(상황에 따라서 자동으로 달라지는) 웹 페이지 개발 필수 기술





-----> **URL**(Uniform Resource Locator)

웹 자원의 위치를 알려주는 단일화된 형식의 문자열

웹 사이트(웹 페이지의) 주소 문자열

프로토콜명://서버도메인명(IP주소) : 포트번호/패스/.../파일명?Query문자열

http(https)://www.naver.com/   -> 네이버 웹사이트의 index.html(기본파일, 웰컴파일)

패스나 파일명을 생략하기도함.

1월 11일 실습1에서 주소 복붙함.

https://www.w3schools.com/colors/colors_picker.asp

https://www.google.com/search?q=%EC%9D%BC%EA%B8%B0+%
EC%98%88%EB%B3%B4&oq=%EC%9D%BC%EA%B8%B0+%EC%
98%88%EB%B3%B4&aqs=chrome..69i57j0l7.10632j1j7&sourceid=
chrome&ie=UTF-8

URL작성할때 포트번호가 80인경우에는 생략한다.

**localhost**는 자신의 컴퓨터를 의미한다. 

IPv4에서의 IP 주소는 127.0.0.1이다.

http://localhost:8000/ 

http://127.0.0.1:8000/



파이참에서 다음과 같이 작성함.

```sh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>진수정</title>
</head>
<body>
<h1>진수정의 첫 웹 페이지입니다요...</h1>
</body>
</html>
```

http://localhost:8000/edu/first.html

docbase, document root --> nginx설치된 폴더/html



### < 실습1 > 

프로젝트 폴더에 htmlexam 폴더 만들고 exam1.html 생성

"**<hr>**": 수평선 그려주는 태그 ( 구분 표시용 )

```sh
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>HTML 학습</title>
</head>
<body>
<h1>주요 HTML 태그 학습</h1>
<hr>
<h2>제목-2</h2>
<h3>제목-3</h3>
<h4>제목-4</h4>
<h5>제목-5</h5>
<h6>제목-6</h6>
<hr>
<a href="http://www.w3schools.com/">W3C Schools</a>
<a href="http://www.w3.org/">W3C</a>
<a href="http://www.phython.org/">PYTHON</a>
</body>
</html>
```

http://localhost:8000/edu/htmlexam/exam1.html

클릭해서 확인해 본다.



h1~6 : 숫자가 커질수록 숫자가 작아짐.

<**a href** = "URL주소">하이퍼링크 텍스트**</a>** :  클릭하면 해당 URL 주소로 페이지 이동이 된다.



images 폴더를 다운받아서 C:\jsj\nginx-1.18.0\html\edu에 저장해 놓는다.



```shell
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>HTML 학습</title>
</head>
<body>
<h1>주요 HTML 태그 학습</h1>
<hr>
<h2>제목-2</h2>
<h3>제목-3</h3>
<h4>제목-4</h4>
<h5>제목-5</h5>
<h6>제목-6</h6>
<hr>
<a href="http://www.w3schools.com/">W3C Schools</a>
<a href="http://www.w3.org/">W3C</a>
<a href="http://www.phython.org/">PYTHON</a>
<hr>
<img src="http://localhost:8000/edu/images/olaf.jpg">
<img src="http://localhost:8000/edu/images/duke.png">
<img src="http://localhost:8000/edu/images/r4.gif">
</body>
</html>
```

jpg 해상도가 좋으나 크기가 큼. 

img src 로 이미지 추가(절대URL- path 정보 다줌)

공간이 모자르면 자동으로 내려감.



```shell
<img src="http://localhost:8000/edu/images/olaf.jpg">
<img src="/edu/images/duke.png">
<img src="../images/r4.gif">
```

서버주소와 포트번호 같으면 생략 가능

htmlexam에 위치해있으니깐 .. 상위 폴더로가서 images 폴더로가서 찾아라.

고유크기 그대로 출력되니깐

사이즈를 조정하는 구문을 써줘야함.



```sh
<hr>
<img src="http://localhost:8000/edu/images/olaf.jpg" width="200">
<img src="/edu/images/duke.png" width="200">
<img src="../images/r4.gif" width="200">
<hr>
<img src="http://localhost:8000/edu/images/olaf.jpg" width="200" height="100">
<img src="/edu/images/duke.png" width="100" height="500">
<img src="../images/r4.gif" width="50" height="50">
```

width 만 쓰면 자동으로 높이 까지 조정되어서 원하는 너비만큼 출력

width와 height  같이 쓰면 너비, 높이 모두 원하는 길이만큼 출력



```shell
<hr>
<figure>
<figcaption>올라프</figcaption>
<img src="http://localhost:8000/edu/images/olaf.jpg" width="200" height="100">
</figure>    
<figure>
<img src="/edu/images/duke.png" width="100" height="500">
<figcaption>듀크</figcaption>
</figure>
<img src="../images/r4.gif" width="50" height="50">
<hr>
```

들여쓰기 해도되고 안해도 됨.

figcaption을 먼저 쓰고 img 쓰면 선제목 그림

img 쓰고 figcaption을 쓰면 그림 후제목

각각의 행으로 출력함.

하나의 행을 주면서 같이 출력 원하면 figure 태그를 같이 묶으면 됨

http://localhost:8000/edu/htmlexam/exam1.html

클릭해서 확인해 본다.



```shell
<h2>좋아하는 음식</h2>
<ol>
    <li>햄버거</li>
    <li>빵</li>
    <li>떡볶이</li>
</ol>
<h2>좋아하는 칼라</h2>
<ul>
    <li>그린</li>
    <li>블루</li>
    <li>옐로우</li>
</ul>
```

ol : 순서가 있는 리스트이다.(번호로 표시)

ul : 순서가 없는 리스트이다. (점으로 표시) --> CSS를 통해 모양 변경 가능

http://localhost:8000/edu/htmlexam/exam1.html

클릭해서 확인해 본다.



**table 만들기**

```sh
<hr>
<h3>주요 CSS 선택자(selector)</h3>
<table border="1">
    <tr><th>선택자</th><th>기능</th></tr>
    <tr><td>태그선택자</td><td>태그명을 가지고 스타일을 적용할 태그를 찾는다.</td></tr>
    <tr><td>ID선택자</td><td>태그에 정의된 id 속성의 값을 가지고 스타일을 적용할 태그를 찾는다.</td></tr>
    <tr><td>CLASS선택자</td><td>태그에 정의된 class 속성의 값을 가지고 스타일을 적용할 태그를 찾는다.</td></tr>
</table>
```

**border 속성은 표의 굵기를 지정**  ==> 표 출력하려면 지정해줘야함.

<th> 내용</th> : table head 의 약자로, 표의 제목을 쓰는 역할 (기본값 : 굵은 글씨체, 중앙정렬)

<tr>내용</tr> : table row  의 약자로, 가로줄을 만드는 역할 (기본값 : 보통 글씨체, 왼쪽정렬)

<td>내용</td> : table data 의 약자로, 셀을 만드는 역할 (기본값 : 보통 글씨체, 왼쪽정렬)

http://localhost:8000/edu/htmlexam/exam1.html

클릭해서 확인해 본다.



**비디오 태그**

동영상 파일 복사해서 C:\jsj\nginx-1.18.0\html\edu\htmlexam 에 넣어 둔다.

```shell
<hr>
<video width = "720" height="400" controls>
    <source src="trailer.mp4">
    <source src="trailer.ogg">
</video>
```

- source src에 대표적인 mp4, ogg 의 여러 확장자의 동영상 파일을 올렸는데 

  크롬은 하나만 줘도 된다. (둘다 지원하기 때문)

  브라우저에 따라서 mp4 혹은 ogg만 지원하기도 함.  (둘중 하나로 인식하게 된다.)



- controls 가 없으면 재생할 방법이 없음.

  대신에 autoplay 하면 되는 데 자동재생은 되나, 중단할 방법이 없음(크롬 지원x , edge에서만 가능)

  왠만하면 controls 꼭 써주기(이용자의 편리함)  --  재생버튼, 중단버튼 모두 가능





### < 실습2 >

homework1.html 파일 만들어서 작성하기

http://localhost:8000/edu/htmlexam/homework1.html

