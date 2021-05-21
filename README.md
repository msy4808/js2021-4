# 문성운 [201840117]
## [5월18일]
>### Process 객체

- argv : 실행 매개 변수를 나타냄
- env  : 컴퓨터 환경과 관련된 정보를 나타냄
- version : Node.js 버전을 나타냄
- versions : Niode.js와 종속된 프로그램 버전을 나타냄
- arch : 프로세서의 아키텍처를 나타냄
- platform : 플랫폼을 나타냄

```jsx
console.log('- process.env : ' + process.env);
console.log('- process.version : ' + process.version);
console.log('- process.versions : ' + process.versions);
console.log('- process.arch : ' + process.arch);
console.log('- process.platform : ' + process.platform);
console.log('- process.memoryUsage() : ' + process.memoryUsage());
console.log('- process.uptime() : ' + process.uptime());
```

### os 객체

- hostname() : 운영체제의 호스트 이름을 리턴
- type() : 운영체제의 이름을 리턴
- platform() : 운영체제의 플랫폼을 리턴
- arch() : 운영체제의 아키텍처를 리턴
- release() : 운영체제의 버전을 리턴
- uptime() : 운영체제가 실행된 시간을 리턴
- loadavg() : 로드 에버리지 정보를 담은 배열을 리턴
- totalmem() : 시스템의 총 메모리를 리턴
- freemem() : 시스템의 사용 가능한 메모리를 리턴
- cpus() : CPU의 정보를 담은 객체를 리턴
- getNetworkInterfaces() : 네트워크 인터페이스의 정보를 담은 배열을 리턴

```jsx
var os = require('os');

console.log(os.tmpdir());
console.log(os.type());

var cpus = os.cpus();

for(var i = 0; i < cpus.length; i++) {
	console.log("CPU[" + (i+1) + "]");
	console.log("model: " + cpus[i].model);
	console.log("speed: " + cpus[i].speed);
}
```
### Url 모듈의 메소드

- parse(urlStr [, ParseQueryString = false, slashesDenoteHost = false]) : URL 문자열을 URL 객체로 변환하여 리턴
- format(urlObj) : URL 객체를 URL 문자열로 변환하여 리턴
- resolve(from,to) : 매게 변수를 조합하여 완전한 URL 문자열을 생성해 리턴




## [5월11일]
>표준 내장 객체<br>
기본적으로 제공하는 객체들<br>
내장되어있는 함수를 사용할 수 있다<br>
대표적으로 날짜관련 객체인 Date()가있는데<br>
그 안에 함수인 getHours()등등을 사용할 수 있다<br>

>let date = new Date(); 객체선언<br>
console.log(date.getMonth()); 현재 월 출력 ==> 4가 출력됨<br>
4가 출력되는 이유는 인덱스값으로 카운트하기때문에 0부터 시작<br>

>Object 객체<br>
자바스크립트의 최상위 객체<br>
생성<br>
var object={<br>
    name:"성운",<br>
    age:23<br>
}; <br>
Object 객체의 메소드<br>
constructor() : 객체의 생성자 함수를 나타냄<br>
hasOwnProperty(name) : 객체가 name 속성을 가지고 있는지 확인<br>
isPrototypeof(object) : 객체가 object의 프로토타입인지 검사<br>
propertyIsEnumerable(name) : 반복문으로 열거 가능 여부 확인<br>
toLocaleString() : 객체를 호스트 환경에 맞는 언어의 문자열로 변경<br>
toString() : 객체를 문자열로 변경<br>
valueOf()  : 객체의 값을 표시<br>


>String 객체<br>
문자열을 표현할 때 사용하는 객체<br>
String 객체의 속성<br>
length() : 문자열의 길이를 표시<br>

>예외처리<br>
기본적인 예외처리는 if문으로 해당 데이터가 undefinded인지 확인<br>

>고급예외처리<br>
try-catch문으로 처리<br>

>try{<br>
예외가 발생될 가능성이 있는 부분<br>
}catch{<br>
try에서 예외가 발생되면 처리할 부분<br>
}finally{<br>
예외랑 상관없이 무조건 실행되는 부분 <br>
}<br>

## [4월13일]
>함수<br>

>익명 함수<br>
이름을 붙이지 않고 함수 생성<br>
let <함수 이름> = function () {};<br>

>선언적 함수<br>
이름을 붙여 함수를 생성<br>

>화살표 함수<br>
() => {}<br>
'하나의 표현식을 리턴하는 함수'를 만들 때는 중괄호 생략 가능<br>

>함수의 기본 형태<br>
function <함수 이름>(매개변수) {<br>
    <함수 코드><br>
}<br>

>함수 매개 변수 초기화<br>
실행하면 undefined가 출력됨<br>

>콜백 함수<br>
함수의 매개 변수로 전달되는 함수<br>

>표준 내장 함수<br>
자바스크립트에서 기본적으로 지원하는 함수<br>

>숫자 변환 함수<br>
parselnt() = 문자열을 정수로 변환<br>
parseFloat() = 문자열을 실수로 변환<br>

>타이머 함수<br>
'특정 시간 후에' 또는 '특정 시간마다' 실행<br>
시간은 밀리초로 지정. 1초를 나타내려면 1000(밀리초)을 입력<br>

>타이머 제거 함수<br>
clearInterval()함수 특정 시간마다 실행하던 함수 호출을 정지<br>

## [4월 06일]
>반복문<br>
for문<br>
for(초기식;조건식;증감식){<br>
    실행할 코드<br>
}<br>
while문<br>
while(조건식){ 조건식에 true를 넣으면 무한루프<br>
    실행할 코드<br>
}<br>
>배열<br>
선언방식<br>
let 변수이름 = [데이터1,데이터2];<br>

>선언할때 데이터를 안넣으면<br>
변수[인덱스값] = 넣을 데이터;<br>
로 넣을 수 있다<br>

>데이터에 숫자와 문자열뿐 아니라 변수도 넣을 수 있다<br>

## [3월 30일]
>조건문에 대해서 배움<br>

>if문<br>
>if(조건문){<br>
    실행할 코드<br>
    }<br>
가장 기본적인 형태<br>
조건을 만족하면 코드를 실행함<br>
else if문<br>
if(조건문){<br>
    실행할 코드<br>
}else if(조건문){<br>
    실행할 코드<br>
}<br>
else if문은 한가지 조건이 아닌 다수의 조건을 비교할때 사용<br>

>switch문<br>
switch (비교할 값){<br>
    case "값" :<br>
    실행할 문장<br>
    break;<br>
    case "값" :<br>
    실행할 문장<br>
    break;<br>
    case "값" :<br>
    실행할 문장<br>
    break;<br>
    default:<br>
    실행할 문장<br>
    break;<br>
}<br>
값을 비교하여 해당 값이 있는 case를 실행함<br>
아무 값도 안맞는경우 default문을 실행<br>
위에서부터 순차적으로 내려오기에 break;로 실행후 빠져나와야함<br>

>삼항 연산자<br>
계산식 ? 참 : 거짓<br>
자주 사용하진 않지만 계산식의 값이 참과 거짓일경우로 출력값이 다름<br>




## [3월 23일]
>자바 스크립트의 기본 자료형을 배움<br>
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