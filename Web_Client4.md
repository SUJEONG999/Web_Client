edu 가 프로젝트의 최상위 폴더 라서 앞 주소는 생략!



http://localhost:8000/edu/cssexam/exam5.html

```shell
<meta charset="UTF-8">
<title>CSS 학습</title>
</head>
<body>
<h1>테이블 출력하기</h1>
<hr>
<table border="20">
   <tr><th>이름</th><th>고향</th><th>나이</th></tr>  
   <tr><td>둘리</td><td>쌍문동쌍문동쌍문동쌍문동쌍문동</td><td>10</td></tr>  
   <tr><td>도우너</td><td>깐따비아</td><td>9</td></tr>  
   <tr><td>또치</td><td>아프리카</td><td>10</td></tr>  
</table>
</body>
</html>
```





http://localhost:8000/edu/cssexam/exam5_1.html

```shell
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>CSS 학습</title>
<style>
   table, th, td {
      border : 1px solid black;
      border-collapse : collapse;
   }
   th {
      background-color : lime;
   }
</style>
</head>
<body>
<h1>테이블 출력하기</h1>
<hr>
<table>
   <tr><th>이름</th><th>고향</th><th>나이</th></tr>  
   <tr><td>둘리</td><td>쌍문동쌍문동쌍문동쌍문동쌍문동</td><td>10</td></tr>  
   <tr><td>도우너</td><td>깐따비아</td><td>9</td></tr>  
   <tr><td>또치</td><td>아프리카</td><td>10</td></tr>  
</table>
</body>
</html>
```

'border-collapse : collapse;' 각자의 선을 분리시켜서 그리는게 아니라 붙여서 선이 하나만 그어지게끔함.

border : 1px dotted red;



http://localhost:8000/edu/cssexam/exam5_2.html

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>CSS 학습</title>
<style>
   td {
      border-bottom : 1px dotted black;
   }
   th {
      background-color : lime;
   }
   tr:hover {
      background-color : pink;
   }
   th:nth-of-type(1) {
      width : 100px;
   }
   th:nth-of-type(2) {
      width : 400px;
   }
</style>
</head>
<body>
<h1>테이블 출력하기</h1>
<hr>
<table>
   <tr><th>이름</th><th>고향</th><th>나이</th></tr>  
   <tr><td>둘리</td><td>쌍문동쌍문동쌍문동쌍문동쌍문동</td><td>10</td></tr>  
   <tr><td>도우너</td><td>깐따비아</td><td>9</td></tr>  
   <tr><td>또치</td><td>아프리카</td><td>10</td></tr>  
</table>
</body>
</html>
```

- border-bottom 하면 아래부분만 그려지게끔 함.

- 원래는 같은 열의 제일 긴 애 기준으로 그려지는데, th1 은 가로 10px, th2은 가로 30px로 함.
- :nth-of-type(2)  는 가상 선택자라고 함.



http://localhost:8000/edu/cssexam/exam8.html

```shell
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title>CSS 학습</title>
		<style>
			* {
				border : 1px dotted red;
			}
		</style>
	</head>
	<body>
   		<h1>레이아웃 나누기</h1>
		<em>오늘은 즐거운 목요일</em><br>
		<strong>고르세용</strong><br>
		<mark>먹고싶은거</mark>
		<ul>
			<li>메뉴1</li>
			<li>메뉴2</li>
			<li>메뉴3</li>
			<li>메뉴4</li>
		</ul>
		<h2>제목1</h2>
		<p>내용1</p>
		<h2>제목2</h2>
		<p>내용2</p>
		<h3>홈페이지 정보(바닥 글)</h3>
	</body>
</html>
```

'*' : 모든 태그에 적용

em 태그: 이탤릭체 (기울임꼴) -> 행바꿈이 자동으로 일어나지 않기 때문에 행바꿈 원하면 br 태그 붙이기

strong 태그: 굵게 강조

br 태그 는 종료 태그가 없은 단일 사이드 태그인데,  <!---<br>--->또는 <!---<br/>--->

mark 태그 : 형광펜 표시

ul 태그 : 순서없는 리스트



# HTML5 문서 구조

## 기존 레이아웃 방식

- 모든 레이아웃 영역을 <div> 태그를 사용하므로 세부적인 구별이 어려움

- div 태그의 id 속성값으로 의미를 표시하거나 class 속성값으로 의미를 표현

## 시맨틱 레이아웃 방식

- div 태그 대신 여러 시맨틱 태그로 변경하여 표시
- 아이디(또는 클래스) 이름들을 표준 시맨틱 태그로 정의함으로써 문서의 의미 구조를 명확하고 간결하게 표현하도록 개선

![image-20210118103115604](C:\Users\jinsujeong\AppData\Roaming\Typora\typora-user-images\image-20210118103115604.png)

http://localhost:8000/edu/cssexam/exam8_1.html

http://localhost:8000/edu/cssexam/exam8_2.html

```shell
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>CSS 학습</title>
<style>
   header {
      border : 1px dotted red;
   }
   footer {
      border : 1px dotted orange;
   }
   section {
      border : 1px dotted blue;     
   }
   article {
      border : 1px dotted green;
   }
   nav {
      border : 1px dotted magenta;
   }
   aside {
      border : 1px dotted brown;
   }
</style> 
</head>
<body>
   <header>
      <h1>레이아웃 나누기</h1>
      <em>오늘은 즐거운 목요일</em>
   </header>
   <nav>
      <strong>고르세용</strong><br>
      <mark>먹고싶은거</mark>
      <ul>
         <li>메뉴1</li>
         <li>메뉴2</li>
         <li>메뉴3</li>
         <li>메뉴4</li>
      </ul>
   </nav>
   <section>
      <article>
         <h2>제목1</h2>
         <p>내용1</p>
      </article>
      <article>
         <h2>제목2</h2>
         <p>내용2</p>
      </article>
   </section>
   <footer>
      <h3>홈페이지 정보(바닥 글)</h3>
   </footer>
</body>
</html>
```

이름을 부여하여 태그 만듦.

#### <**HTML5에서 문서의 구조를 정의하는 태그들**>

![image-20210118103352564](C:\Users\jinsujeong\AppData\Roaming\Typora\typora-user-images\image-20210118103352564.png)



**header**
**header**는 주로 머리말, 제목을 표현하기 위해 쓰인다.

**nav**
네비게이션이라고 불린다. 콘텐츠를 담고 있는 문서를 사이트간에 서로 연결하는 릿크의 역할 을 담당한다. 주로 메뉴에 사용되고 위치에 영향을 받지 않아 어디에서든 사용이 가능하다.

**section**
<body>영역은 콘텎트를 <Header>,<section>,<footer>의 3가지 공간에 저장하는데 그 중 <section>은 본문 콘텎트를 담고 있다. <section>앆에 <section>을 넣는 것도 가능하다.

**article**

**section**이 콘텐트를 분류한다면 **article**태그 안에는 실질적인 내용을 넣는다. 뉴스로 예를 들면 정치/ 연예/ 사회의 대분류는 **section**이고, 정치의 기사내용과 연예의 기사내용들을 **article**에 넣는 것이다.

**aside**
사이드바라고 부르기도 하며, 본문 이외의 내용을 담고 있는 시맨틱 태그입니다. 주로 본문 옆에 광고를 달거나 릿크들을 이 공간에 넣어 표현한다.
**footer**
화면의 구조 중 제일 아래에 위치하고, 회사소개 / 저작권 / 약관 / 제작정보 들이 들어갂다. 연락처는 <address>태그를 사용하여 표시한다.
**div**

**div**는 HTML5에 와서 글자나 사진등 콘텐트들을 묶어서 CSS 스타일을 적용시킬 때 사용한다.



http://localhost:8000/edu/cssexam/exam8_3.html

```
float : left;
```

```
float : right;
```

```
clear : both;
```

```shell
<style>
       * {
      margin : 0
   }

   header {
      width : 100%;
      height : 100px;
      background-color : yellow;
   }
   nav {
      width : 30%;
      height : 500px;
      float : left;
      background-color : pink;
   }
   section {
      width : 70%;
      height : 500px;
      float : right;
      background-color : skyblue;
   }
   article {
      width : 80%;
      height : 200px;
      background-color : magenta;
      margin-left : auto;
      margin-right : auto;
   }
   footer {
      width : 100%;
      height : 50px;    
      clear : both;
      background-color : lightgray;
   }

</style>
</head>
```

**float**는 width만큼 공간을 잡고 왼쪽(오른쪽)으로 가라.

**clear** - 플로팅 해제 기법 : 왼쪽 오른쪽 모두 floating 된 요소를 지정 해제



http://localhost:8000/edu/cssexam/exam8_4.html

```
<link rel="stylesheet"  href="mystyle.css">
```

끌어오고자하는 css 파일 이름(같은 폴더에 있어야함.) , rel : 관계는 어떻게 되는지

css 파일을 독립적으로 만들어서 불러오는 경우임.



http://localhost:8000/edu/cssexam/exam9.html







http://localhost:8000/edu/cssexam/exam10.html

```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        p:nth-child(2) {
            color : red;
        }
        p:nth-of-type(2) {
            color : blue;
        }
       section > h1 {
            color : green;
        }
       section h1 {
            background-color : pink;
        }
        img {
            width : 150px;
        }
        img[src$=gif] {
            border : 1px dotted red;
        }
    </style>
</head>
<body>
<div>
<h3>어린 왕자</h3>
<p>1장 </p>
<p>2장 </p>
</div>
<section>
    <h1>섹션제목</h1>
    <article>
        <h1>아티클제목</h1>
    </article>
</section>
<img src="/edu/images/1.jpg">
<img src="/edu/images/r1.gif">
</body>
</html>
```



```
p:nth-child(2) {
    color : red;
}
```

부모의 자식으로서 두번째인 p태그

```
p:nth-of-type(2) {
    color : blue;
}
```

p태그 중에 두번째



```
section h1 {
     background-color : pink;
```

자식 자손 모두 찾아서 적용

```
section > h1 {
     color : green;
 }
```

section의 자식에 해당하는 h1 만 적용







```
vertical-align : middle;
```

이미지에도 가운데로 적용해줘.

