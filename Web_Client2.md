# [ 웹 프로그래밍 기술 - 클라이언트 ] 2

URL 주소 잘못 입력했을 때 => 웹서버가 기동되었다는 뜻이고, (nginx 기동중) 404 Not Found 라는 오류가 뜸.

ex) http://localhost:8000/edu/images/clover.png 인데 확장자만 잘못 입력해도 404 오류가 뜸

---

**HTTP**(HyperText Transfer Protocol)는 W3 상에서 정보를 주고받을 수 있는 프로토콜이다. 주로 HTML 문서를 주고받는 데에 쓰인다. 주로 TCP를 사용하고 HTTP/3 부터는 UDP를 사용하며, 80번 포트를 사용한다.

HTTP는 클라이언트와 서버 사이에 이루어지는 요청/응답(request/response) 프로토콜이다. 예를 들면, 클라이언트인 웹 브라우저가 HTTP를 통하여 서버로부터 웹페이지(HTML)나 그림 정보를 요청하면, 서버는 이 요청에 응답하여 필요한 정보를 해당 사용자에게 전달하게 된다. 이 정보가 모니터와 같은 출력 장치를 통해 사용자에게 나타나는 것이다.

HTTP를 통해 전달되는 자료는 http:로 시작하는 URL(인터넷 주소)로 조회할 수 있다.



클라이언트가 서버에 접속하여 어떠한 요청을 하면, 서버는 세 자리 수로 된 응답 코드와 함께 응답한다. HTTP의 응답 코드는 다음과 같다.  <a href = "https://ko.wikipedia.org/wiki/HTTP/">HTTP</a>에서  확인

---

http://localhost:8000/edu/images/xmas/g14.png  html 뿐만 아니라 사진 파일도 렌더링을 해준다.

---

파이썬에 들어가서 프로젝트 열기해서 C:\jsj\nginx-1.18.0\html\edu 하면 조회 가능함.

exam2 생성하기

"<hr>" 태그는 수평선 그려주는 태그!

```shell
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>HTML 태그 학습</title>
</head>
<body>
<h1>HTML의 단락 태그</h1>
<hr>
파이썬 프로그래밍
HTML 작성 방법
CSS 작성 방법
자바스크립트 프로그래밍<jQeury도 조금 학습해요>
장고 프로그래밍(DB 연동, AJAX)
</body>
</html>
```

http://localhost:8000/edu/htmlexam/exam2.html

<jQeury도 조금 학습해요> 조회 안됨.

무조건 태그로 인식하려는 특성을 보임. 이해할 수 없는 태그는 무시하는 경향. 없는 거로 간주하여 화면에 랜더링을 안해준다.

<> 대신에 일반 괄호롤 바꿔주어야한다.

----

<> 꼭 쓰고 싶다면 

```sh
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>HTML 태그 학습</title>
</head>
<body>
<h1>HTML의 단락 태그</h1>
<hr>
파이썬 프로그래밍
HTML 작성 방법
CSS 작성 방법
자바스크립트 프로그래밍&lt;jQeury도 조금 학습해요&gt;
장고 프로그래밍(DB 연동, AJAX)
</body>
</html>&lt;
```

특수문자 엔터티 :  

| **특수코드 값** | **실제 표현**       | **뜻 / 용도**                                                |
| --------------- | ------------------- | ------------------------------------------------------------ |
| **<**           | **< (부등호 꺽쇠)** | 오른쪽으로 열린 부등호. 수식에서 A < B 와 같은 형태로 사용. HTML 코드에서 모든 태그의 시작 기호. |
| **>**           | **> (부등호 꺽쇠)** | 왼쪽으로 열린 부등호. 수식에서 A > B 와 같은 형태로 사용. HTML 코드에서 모든 태그의 끝 기호. |



**br 태그**는 종료태그가 따로 없고 (사이에 컨텐드 없음) **개행처리**해주는 태그

```sh
<hr>
파이썬 프로그래밍<br>
HTML 작성 방법<br>
CSS 작성 방법<br>
자바스크립트 프로그래밍&lt;jQeury도 조금 학습해요&gt;<br>
장고 프로그래밍(DB 연동, AJAX)
```

**p 태그**는 단락을 나누고자 할 때 문단 처리 해주는 태그(종료태그로 묶어주면됨.)

```
<hr>
<p>파이썬 프로그래밍<br>
HTML 작성 방법<br>
CSS 작성 방법</p>
<p>
자바스크립트 프로그래밍&lt;jQeury도 조금 학습해요&gt;<br>
장고 프로그래밍(DB 연동, AJAX)
</p>
```

http://localhost:8000/edu/htmlexam/exam2.html

<참고- exam2 전체 내용>

```sh
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>HTML 태그 학습</title>
</head>
<body>
<h1>HTML의 단락 태그</h1>
<hr>
파이썬 프로그래밍
HTML 작성 방법
CSS 작성 방법
자바스크립트 프로그래밍&lt;jQeury도 조금 학습해요&gt;
장고 프로그래밍(DB 연동, AJAX)
<hr>
파이썬 프로그래밍<br>
HTML 작성 방법<br>
CSS 작성 방법<br>
자바스크립트 프로그래밍&lt;jQeury도 조금 학습해요&gt;<br>
장고 프로그래밍(DB 연동, AJAX)
<hr>
<p>파이썬 프로그래밍<br>
HTML 작성 방법<br>
CSS 작성 방법</p>
<p>
자바스크립트 프로그래밍&lt;jQeury도 조금 학습해요&gt;<br>
장고 프로그래밍(DB 연동, AJAX)
</p>
</body>
</html>
```

---

exam3

```sh
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>HTML 태그 학습</title>
</head>
<body>
<h1>HTML의 입력폼 태그</h1>
<hr>
<h2>계정과 패스워드를 입력하세요</h2>
<form method="get" action="http://localhost:8000/edu/serverprogram">
    계정 <input type="text" name="account" required>
    패스워드 <input type="password" name="pwd" required>
    <input type="submit" value="로그인">
    <input type="reset" value="재작성">
</form>   
</body>
</html>
```

- type를 password로 했기 때문에 입력창에 입력시 ***로 보임

- type를 submit로 했기 때문에 버튼 기능 생성 ---> value 안줄 경우엔 자동으로 버튼생성

- 이름 변경원하면 value="원하는 이름" 설정하면 된다.

- type를 reset 으로하면 초기상태로 되돌려주는 버튼 생성

- submit 하면 get 방식으로 action 방법으로 요청하게됨.

- required 는 반드시 입력해야한다는 뜻

  ```shell
  <hr>
  <h2>좋아하는 음식과 칼라를 선택하세요</h2>
  <form method="get" action="http://localhost:8000/edu/serverprogram">
      좋아하는 음식 : <br>
      <input type="checkbox" name="food" value="불고기">불고기<br>
      <input type="checkbox" name="food" value="치킨">치킨<br>
      <input type="checkbox" name="food" value="피자">피자<br>
      <input type="checkbox" name="food" value="감자탕">감자탕<br><br>
      좋아하는 칼라 : <br>
      <input type="radio" name="fcolor" value="노란색">노란색<br>
      <input type="radio" name="fcolor" value="녹색">녹색<br>
      <input type="radio" name="fcolor" value="주황색">주황색<br>
      <input type="submit" value="전송">
      <input type="reset" value="재작성">
  </form>
  ```

선택형 입력 컨퍼런티 

**type=checkbox** 는 여러 항목중에서 원하는 만큼 선택 가능함.

**type=radio**는 여러 항목 중에서 하나만 선택 가능함.

value="피자">**피자** 에서  **피자**는 content이며 사용자에게 보여주는 값이고 , value="피자" 는 선택했을때 서버에게 전달해주는 value 속성임.

<img src="C:\Users\jinsujeong\Desktop\빅\1월15일\1.png">  

전송하면 **?food=치킨&food=피자&food=감자탕&fcolor=녹색** 뜬다. 

키=value  쿼리 문자열이 뜸. 



실제로 네이버 입력창에 파이썬 검색하면 ?where=nexearch&sm=top_hty&fbm=1&ie=utf8&query=파이썬 붙음.

쿼리 문자열로 원하는 게 뭔지 같이 전달해준다.

---

```sh
<hr>
<h2>년도 조사</h2>
<form method="get" action="http://localhost:8000/edu/serverprogram">
    태어난 년도를 입력하시오 :<br>
    <input type="number" name="age" min = "2000" max="2005"><br>
    <input type="submit" value="전송">
    <input type="reset" value="재작성">
</form>
```

**type=number** 는 숫자만 입력가능

범위 설정 시, 범위 내에서만 입력가능함. 



```sh
<hr>
<h2>년도 조사</h2>
<form method="get" action="http://localhost:8000/edu/serverprogram">
    태어난 년도를 입력하시오 :<br>
    <input type="number" name="age" min = "2000" max="2005"><br>
    태어난 년도를 선택하시오 :<br>
    <select name="year">
        <option value="2000">2000</option>
        <option value="2001">2001</option>
        <option value="2002">2002</option>
        <option value="2003">2003</option>
        <option value="2004">2004</option>
        <option value="2005">2005</option>
    </select><br><br>
    <input type="submit" value="전송">
    <input type="reset" value="재작성">
</form>
```

**select** 로 하면 리스트업 되고, 옵션 중에 하나를 선택하게끔 만들어준다.



**textarea** : 한행의 입력상자를 주는 게 아니라 여러 행 입력할 수 있게끔 할때

```shell
남기려는 글을 입력하세요 : <br>
<textarea name="memo" rows="5" cols="50"></textarea><br>
<input type="submit" value="전송">
<input type="reset" value="재작성">
```

5행의 50열의 크기로 박스가 만들어지며 자유롭게 원하는 만큼 씀( 넘어가면 스크롤 생성)



```sh
생일을 선택하세요 : <br>
<input type="datetime-local" name="birth"<br><br>
<input type="submit" value="전송">
<input type="reset" value="재작성">
```

달력모양 클릭해서 선택할 수 있음.

날짜와 시간 모두 필요



```sh
생일을 선택하세요 : <br>
<input type="date" name="birth"<br><br>
<input type="submit" value="전송">
<input type="reset" value="재작성">
```

**type=date** 는 년월일만 선택하면 됨.

http://localhost:8000/edu/htmlexam/exam3.html

그밖의 input 태그는 여기서 https://www.w3schools.com/tags/tag_input.asp 확인하기.

---

## CSS

exam1 을 복사해서 exam1_css 생성하기

**[인라인 방식]**

http://localhost:8000/edu/htmlexam/exam1_css.html

```sh
<h1 style="color:red">주요 HTML 태그 학습</h1>
```

**style="color:red"**  로 해서 색 바꾸기

```shell
<h2 style="color:blue">좋아하는 음식</h2>
```

칼라명을 한글로 주면 안되고, 영문 혹은 RGB 값(#...)으로 입력해야한다.



##### [h2 태그마다 모두 색깔을 통일해서 동일색상 주고 싶을 때-- 전역적인 방법]

inline 방식(시작태그에 속성으로 입력해주는 것)으로 태그마다 복붙해서 해도 되지만 번거롭다.

전역적인 방법으로 쓰는 것이 좋다.

**head **태그에 입력한다.

```shell
<head>
    <meta charset="UTF-8">
    <title>HTML 학습</title>
    <style>
        h2 {
            color : green;
        }
    </style>
</head>
```

하지만, 인라인 방식이 전역적인 방법보다 우선순위가 높다.

만약 둘다 설정되어 인라인 방식이 우선적으로 반영된다.

http://localhost:8000/edu/htmlexam/exam1_css.html

---

```shell
<h1 style="color:red; background-color:green">주요 HTML 태그 학습</h1>
```

;로 조건 구분

끝에까지 한행 전체가 그린 색으로 채워짐.

```sh
<h1 style="color:red; background-color:green; text-align:center">주요 HTML 태그 학습</h1>
```

text-align:center 조건 추가로 text를 가운데로 정렬함.



```
<head>
    <meta charset="UTF-8">
    <title>HTML 학습</title>
    <style>
        h1 {
            color:red; 
            background-color:green; 
            text-align:center;
            text-shadow:2px 2px 3px white;
        }
        h2 {
            color:green;
            }
    </style>
</head>
```

text-shadow: offset-x offset-y blur-radius color | none | initial | inherit

- offset-x : 그림자의 수평 거리를 정합니다. (필수)
- offset-y : 그림자의 수직 거리를 정합니다. (필수)
- blur-radius : 흐림 정도를 정합니다. (선택 : 값을 정하지 않으면 0)
- color : 색을 정합니다. (선택 : 값을 정하지 않으면 브라우저 기본값)
- none : 글림자 효과를 없앱니다.
- initial : 기본값으로 설정합니다.
- inherit : 부모 요소의 속성값을 상속받습니다.

참고 https://www.codingfactory.net/10650 





모든 태그에 대해서 적용하고자

```sh
<head>
    <meta charset="UTF-8">
    <title>HTML 학습</title>
    <style>
        h1 {
            color:red;
            background-color:green;
            text-align:center;
            text-shadow:2px 2px 3px white;
        }
        h2 {
            color:green;
            }
        a {
            text-decoration : none;
            }
    </style>
</head>
```

a 태그의 언더라인 없애고자 **text-decoration : none;** 추가함.



태그와 태그와의 간격 : margin

margin-right : 30px; 추가함.

```shell
<head>
    <meta charset="UTF-8">
    <title>HTML 학습</title>
    <style>
        h1 {
            color:red;
            background-color:green;
            text-align:center;
            text-shadow:2px 2px 3px white;
        }
        h2 {
            color:green;
            }
        a {
            text-decoration : none;
            margin-right : 30px;
            }
    </style>
</head>
```

반드시 px 붙여 줘야함. 안 붙이면 무시



```sh
<head>
    <meta charset="UTF-8">
    <title>HTML 학습</title>
    <style>
        h1 {
            color:red;
            background-color:green;
            text-align:center;
            text-shadow:2px 2px 3px white;
            font-size : 3em;
        }
        h2 {
            color:green;
            }
        a {
            text-decoration : none;
            margin-right : 30px;
            }
    </style>
</head>
```

- font-size : 3em;

일반 사이즈이 몇 배로 하겠다 00em

- font-size : 10pt;

10포인트 크기로 하겠다.



```shell
<head>
    <meta charset="UTF-8">
    <title>HTML 학습</title>
    <style>
        h1 {
            color:red;
            background-color:green;
            text-align:center;
            text-shadow:2px 2px 3px white;
            font-size : 30px;
        }
        h2 {
            color:green;
            }
        a {
            text-decoration : none;
            margin-right : 30px;
            }
        a:hover {
            font-weight : bold;
                }
        img {
            opacity:0.3;  /* 0.0~1.0 */
            }
        img:hover {
            opacity : 1.0;
        }

    </style>
</head>
```

- a 태그에 hover 써주면 마우스가 올라가면 font가 굵어진다.

- img 태그는 투명도가 0.3으로 설정하고

- img 태그에 hover 써주면 마우스 올라가면 투명도가 1로 되어 선명해진다.

  (투명도는 0.0~1.0까지 가능)



<!-- HTML 주석태그 -->

/*  */

http://localhost:8000/edu/htmlexam/exam1_css.html

---

### [ CSS 의 작성 방법 ] -- 우선 순위순!

- 인라인 방법 - HTML 엘리먼트에 style 이라는 속성으로 정의하는 방법
  <tag style="property: value">
- 전역적 방법 - <style> 이라는 태그에 웹 페이지의 태그들에 대한 스타일을 정의하는 방법

<style type="text/css">
selector {property: value;}
</style>
- 외부 파일 연결 방법 - 독립된 파읷(확장자 .css)을 만들어서 HTML 문서에 연결하는 방법
  <link rel="stylesheet" type="text/css" href="style.css" />

---

###  [ CSS 스타일 선언 형식 ]

선택자(selector) : 스타일을 적용할 대상을 지정

스타일 속성(property) 블록 : 선택자에 의해 선택된 영역에 적용할 색상, 크기 등의 스타일을 명세로 중괄호({ }) 로 둘러싸며 세미콜론(;) 으로 구분하여하나 이상의 스타일 속성 선언을 포함

![image-20210115135109568](C:\Users\jinsujeong\AppData\Roaming\Typora\typora-user-images\image-20210115135109568.png)

---

img[src$=png]





---

# < 실습 >

http://localhost:8000/edu/cssexam/exam1.html   인라인 방식

```sh
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<h1>CSS로 무엇을 할 수 있을까?</h1>
<hr>
<h2 style="color:green">둘리</h2>
<h2>또치</h2>
<h2 style="color:red">도우너</h2>
<h2>희동이</h2>
<h2>마이콜</h2>
<h2 style="color:#0000ff;background-color:yellow">고길동</h2>
</body>
</html>
```

고길동 : 파란색글씨에 배경색은 노란색

 두개의 숫자가 똑같을 경우에는  #00f 로 적어도 됨.

---

크롬에서 도구더보기에서 개발자도구

---

http://localhost:8000/edu/cssexam/exam2.html 전역적인 방법

```sh
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        #t1 {
            color : green;
        }
        #t2 {
            color : red;
        }
        #t3 {
            color : blue;
            background-color : yellow;
        }
    </style>
</head>
<body>
<h1>CSS로 무엇을 할 수 있을까?</h1>
<hr>
<h2 id="t1">둘리</h2>
<h2>또치</h2>
<h2 id="t2">도우너</h2>
<h2>희동이</h2>
<h2>마이콜</h2>
<h2 id="t3">고길동</h2>
</body>
</html>
```

**id 선택자 지정**

id 값을 입력한 태그에 디자인 효과를 주기 위해서는 CSS 기술이 필요합니다. <head> 태그 사이에서 id 값에 선택자를 지정합니다.

id 속성의 선택자는 샵(#)기호를 id 값 앞에 붙여서 호출합니다. 

두 개의 다른 종류의 요소에 속성이 첨부되어 있어도 같은 문서에 동일한 ID를 가진 두 개의 요소가 없어야합니다. 

---

http://localhost:8000/edu/cssexam/exam3.html 

```
h1 {
    background-color : pink;
    width : 400px;
    }
```

원래 한행 전체가 배경색에 씌워지지만 width 속성을 취하면은 원하는 너비만큼 설정된다. (고정치)

만약 40% 로 하면 지금 사용하는 브라우저 크기에 따라서 달라짐(상대치)

---

```
img {
    width : 30 %;
    }
```

이미지도 마찬가지임.

---

http://localhost:8000/edu/cssexam/exam4.html

**블럭 스타일 태크**

div 태그 : 행 단위로 출력, 행 전체가 태그의 공간임.   --- 행 단위로 랜더링됨.

대표적으로 div 태그 , p 태그 , h1 태그 등등

**인라인 스타일 태그**

span 태그 : 개행처리 안됨. content 공간만 자기 공간임.

대표적으로 div 태그 , img 태그 , input 태그, em 태그 등등

```sh
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<h1>블럭 스타일 태그와 인라인 스타일 태그</h1>
<hr>
<div>가나다라마바사아</div>
<div>0123456789</div>
<div>abcdefghij</div>
<hr>
<span>가나다라마바사아</span>
<span>0123456789</span>
<span>abcdefghij</span>
</body>
</html>
```

---

http://localhost:8000/edu/cssexam/exam4_1.html

```sh
<h1><span class="top">블럭</span> 스타일 태그와 <span class="top">인라인</span> 스타일 태그</h1>
```

h1의 content 중에서 **블럭** 단어와 **인라인** 단어만 색깔을 다르게 지정하겠다.

부분부분 태그화해야함. **span 태그**로 묶음.

클래스 선택자 : .top    < 문서 안에서 여러 번 반복할 스타일이면>

top 이라는 class 선택자를 찾아서 색깔을 지정해줌.   이때 id는 안됨.(unique 해야하기 때문,,!)

width, hight 조절 못함.

```shell
<style>
    div {
        background-color : lime;
        margin : 5px;
        width : 300px;
        height : 200px;
        font-size : 1.5em;
        padding : 10px;
    }
```

블럭 스타일 태크

width, hight 조절 가능함 => 너비 300 높이 200으로 조정

padding : 상하좌우 겉의 테두리부터 안의 간격 (값이 커지면 박스 크기가 커짐)

**마진(margin)**은 요소 주변 여백을 뜻합니다. 

**패딩(padding)**은 콘텐츠 영역과 테두리 사이의 여백입니다. 



---

http://localhost:8000/edu/cssexam/exam4_2.html

```sh
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        div {
            background-color : lime;
            margin : 5px;
            width : 300px;
            height : 200px;
            font-size : 1.5em;
            padding : 10px;
        }
        span {
            background-color : orange;
            margin : 5px;
            width : 300px;
            height : 200px;
            font-size : 1.5em;
            padding : 10px;
        }
        .top {
            color : #cc0099;
        }
    </style>
</head>
<body>
<h1><span class="top">블럭</span> 스타일 태그와 <span class="top">인라인</span> 스타일 태그</h1>
<hr>
<div>가나다라마바사아</div>
<div>0123456789</div>
<div>abcdefghij</div>
<hr>
<span>가나다라마바사아</span>
<span>0123456789</span>
<span>abcdefghij</span>
</body>
</html>
```

span 설정 값 추가





---

http://localhost:8000/edu/cssexam/exam4_3.html

반응형 웹 : CSS 를 이용해서 자동으로 조정되도록 함.

복잡한 사이트는 반응형 웹이 아닌 페이지를 각자 만듦. 모바일 따로 PC 따로. 대표적 네이버!

세로로 가운데서 몰아서 표현함.

```sh
h1 {
    text-align : center;
    text-shadow : -2px -2px 5px green, -4px -4px 5px red;
    }
```

**text-align** 설정으로  가운데 정렬 시킴.

**text-shadow** 설정으로 음의 값을 주면 좌측(양은 우측) 위(양은 아래) 5px 만큼의 그림자 두께

```sh
h1:hover {
    transform : rotate(-2deg);
    transition : transform 2s;
}
```

마우스를 올리면 2초동안 움직여라.

음의 값 주면 반시계 방향, 양의 값 주면 시계 방향

숫자가 커지면 더 많이 회전됨.

```sh
div {
    background-color : lime;
    margin : 5px;
    width : 300px;
    height : 200px;
    font-size : 1.5em;
    padding : 50px;
    text-align : center;
    margin-left : auto;
    margin-right : auto;
    border-radius : 30px;
    line-height : 200px;
    border : 1px solid red;
}
```

좌우 margin 을 auto로 주면 태그의 공간을 가운데로 몰려줌.

**border-radius **를 주면 부드럽게 모서리 부분을 표현해줌.  커질 수록 더 둥글게 나옴. 적을 수록 뾰족함.

**border** 는 테두리 선 이다. 생략하면 테두리 선 안그려짐. (solid 는 실선이라는 뜻)

**text-align** 는 텍스트를 좌우 가운데로 몰아줌..

**line-height** 는 텍스트를 상하 가운데로 몰아줌.

---

http://localhost:8000/edu/cssexam/exam6.html

margin-top, margin-right, margin-bottom, margin-left

margin : 10  상 20 하  30 좌 40 우

margin : 10  상 20 하  30 좌우

margin :10 상하 20 좌우

margin : 10 상하좌우

```shell
<head>
<meta charset="UTF-8">
<title>CSS 학습</title>
<style>
   div {
      width : 60%;
      height : 200px;
      margin : 20px auto;
      padding : 10px;
      text-align : center;
   }  
   div:nth-of-type(1) {
      background-color : yellow;
      border : 2px solid red;
      border-radius : 30px;
   }
   div:nth-of-type(2) {
      background-color : lightgreen;
      border : 2px dotted magenta;
      border-radius : 20px 40px 60px 80px;
   } 
   div:nth-of-type(3) {
      background-color : #000000;
      border : 5px dashed #ffffff;
   }
   div:nth-of-type(4) {
      background-color : silver;
      border : 15px inset #ffffff;
   }
   div:nth-of-type(5) {
      background-color : gold;
      border : 15px outset #ffffff;
   }
</style>
</head>
<body>
<h1>둥근 보더 만들기</h1>
<div>텍스트를 출력합니다.</div>
<div>텍스트를 출력합니다.</div>
<div>텍스트를 출력합니다.</div>
<div>텍스트를 출력합니다.</div>
<div>텍스트를 출력합니다.</div>
</body>
```

div 는 공통

div:nth-of-type(1) 는 div 태그 중 첫 번째만, border-radius 모서리 둥글게

div:nth-of-type(2)  는  div 태그 중 두 번째만, border : 2px dotted magenta;  점선 자홍색

div:nth-of-type(3)  는  div 태그 중 세 번째만, border : 5px dashed #ffffff;  테두리를 약간 긴 점선으로 설정함

inset , outset 입체감있는 느낌

---

```
div.jbGrad01 {
   background-image : linear-gradient(to bottom, yellow, green)
}
```

위에서 아래로 노란색 녹색

```
div.jbGrad02 {
   background-image : linear-gradient(to top, yellow, white, green)
}
```

아래서 위로 노란색 흰색 녹색

```
div.jbGrad03 {
   background-image : linear-gradient(to right, yellow, white, green)
}
```

왼쪽에서 오른쪽으로 노란색 흰색 녹색

```
div.jbGrad06 {
   background-image : linear-gradient(to right, red, orange, yellow, green, blue, navy, purple);
   font-size : 3em;
   text-align : center;
   text-shadow : 2px 2px 5px white, -2px -2px 5px white;
}
```

오른쪽 방향으로 무지개 색,  text-align 는 텍스트를 좌우 가운데로 몰아줌..

```
div.jbGrad07{
   background-image : url("/edu/images/pink.gif");       
}
```

반복해서 채우면서 타일 효과를 냄.

---