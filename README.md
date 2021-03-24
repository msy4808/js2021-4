# 문성운 [201840117]
## [3월 23일]
>오늘 배운 내용 요약 <br>
자바 스크립트의 기본 자료형을 배움<br>
다른 언어들과 다르게 let로 선언 후 사용하면 그에 맞는 자료형으로 변형<br>

>증감 연산자에 대해 배움<br>
자바와 C언어와 같은 연산자<br>

>typeof란 자료형 확인 연산자가 있는데 실제로 크게 쓰이지는 않음<br>
typeof "확인할 자료형"<br>
ex)typeof 10, typeof "자료형"<br>

>강제 자료형 변환이 가능한 함수가 있음<br>
종류로는 Nember(), String(), Boolean()이 있음<br>

>사용법은<br>
console.log(Number("10")); <--이건 "10"이란 문자열을 숫자로 변경하여 출력하는것<br>
let num = Number("안녕"); <--이건 숫자로 변경이 불가하기에 출력이  NaN이 출력됨<br>


>NaN이란 개념<br>
숫자 자료형이지만 숫자가 아닌것을 의미 isNaN()함수로 NaN인지 확인가능<br>
즉 위에서 선언한 num을 console.log(isNaN(num));을 출력하면 결과로 true가 출력됨<br>

>자동 자료형 변환은 숫자와 문자열 사이에 +를 이용하여 가능<br>
console.log("10" + 10);은 "20"이란 문자열이 출력됨<br>


## [03월 16일]
> 오늘 배운 내용 요약 <br>
이벤트기반의 의미를 배움(재래시장 줄서기) <br>
동기식과 비동기식의 개념을 배움(비동기식 개꿀) <br>
함수와 메소드의 차이 <br>
콘솔과 웹에서 실행하는 기본적인 코드실행 <br>
> 요약<br>
html에서 팝업 띄우기<br>
>  script 태그를 이용<br>
    alert('hello world!');
    웹 브라우저에서 팝업 실행

>head에서 script태그에 옵션을 추가하여 .js파일을 바로 실행<br>
옵션값 : type="text/javascript" src="hello.js"<br>

>js파일을 만들어 콘솔에서 node 파일명.js로 실행<br>
console.log('Hello World...!');<br>

>REPL을 이용한 출력 콘솔에서 node를 입력해서 사용가능<br>
콘솔에서 1+5같이 입력하면 값(6)이 출력됨<br>
또한 let name ="성"+"운";<br>
이처럼 선언가능<br>
let은 변수 선언<br>
name은 변수명<br>

>사칙연산자는 다른 언어들과 동일함