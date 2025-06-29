# Nomad Coders-Vanilla JS
**강의명: 노마드 코더_바닐라 JS로 크롬 앱 만들기**
<br>
강의를 듣고 코드 및 내용을 정리합니다
<br>
<br>
<br>
<br>
## 브라우저와 JS(동작 흐름)
1. **JS는 브라우저에 설치되어**있기 때문에 브라우저를 사용하면 따로 다운받을 필요 없이 사용할 수 있다.

2. **브라우저는 HTML 파일(.html)을 실행**하고 CSS파일, JS파일 등은 HTML파일에 연결되어 실행된다.
   - CSS는 head에서, JS는 body에서 호출
     <br>
     ```html
     <!DOCTYPE html>
     <html lang="en">
     <head>
         <meta charset="UTF-8">
         <meta name="viewport" content="width=device-width, initial-scale=1.0">
         <link rel="stylesheet" href="style.css" />
         <title>Momentum</title>
     </head>
     <body>
         <script src="app.js"></script>
     </body>
     </html>   
     ```
<br>
<br>

## 타입과 변수
- **console.log()**: 콘솔에 ()안의 내용을 출력. 숫자(integer, float..), 문자열(string..) 등
  <br>
  1. 숫자는 그대로 입력하면 되고 문자열의 경우 "" 또는''안에 작성한다.
  2. 두 데이터를 연결해 출력하고 싶을 경우 '+'를 사용하여 연결한다.
    ```javascript
    console.log("hello"+79);
    ```
1. 숫자나 문자열 등을 바로 사용할 수 있지만 수정 등의 경우에 반복되는 작업을 줄이기 위해 변수를 사용한다.
   ```javascript
   console.log(5+3)
   console.log(5*3)
   console.log(5/3)
   ```
   위 코드에서 5와 3대신에 6과 4를 사용해야 한다면 각 줄의 5와 3을 직접 6과 4로 수정해야한다.
   ```javascript
   const a = 5;
   const b = 3;
   console.log(a+b)
   console.log(a*b)
   console.log(a/b)
   ```
   위 코드처럼 a와 b라는 변수를 만들어 숫자를 대입하면 a와 b의 수정만으로(a에 6을 대입하고 b에 4를 대입) 각 연산에 사용되는 숫자를 바꿀 수 있다.
   변수 선언에 관한 내용은 아래에 추가 설명
   
2. JS는 보통 변수의 이름을 camelCase로 작성한다.(python의 경우 snake_case)
 
3. **변수 선언**은 **const**와 **let**으로 할 수 있다.
   <br>
   **const** : 상수(constant)를 의미하며 데이터를 입력하면 값이 바뀔 수 없다.
   <br>
   **let** : const와 다르게 입력한 데이터를 이후에 바꿀 수 있다.
   <br>
   ```javascript
   const a = 5;
   a = 3   //수정불가
   let a = 5;
   a = 3   //수정가능
   ```
   **일반적으로 const를 사용하며 데이터 변경이 필요한 경우에 let을 사용한다.**
   <br>
  *언어는 계속 업데이트 or 패치가 일어남. const, let이전에는 var를 사용. var는 언제나 입력된 데이터를 수정할 수 있다. 이후 const와 let으로 변경되지 않는 데이터와 변경 가능한 데이터를 구분하여 사용.*

4. 변수 사용 방법
   <br>
   ```javascript
   const num = 1;   //int
   
   const name = "myName"   //String
   
   const myArray = ["popcorn", 1, 2, "a"];    //array
   
   const myObject = {   //Object
      name: "myName",
      birthday: 1012,
      }
   myObject.name = "notMyName"   //property 변경
   myObject.weight = 50;   //property 추가
   ```
   *const로 선언했지만 수정이 가능한 이유: Object를 수정하는것과 내부를 수정하는것은 다름.<br>Object 내부를 수정하는건 ok, Object 자체를 변경하는건 x<br>ex) myObject = false;, my Object = "me";  ->불가능*
<br>
<br>

## 메서드
1. 메서드 선언 방법
   <br>
   function 메서드명(매개변수1, 매개변수2,...){    //매개변수 생략 가능
   <br>
   ...    //동작
   <br>
   }
   <br>
   ```javascript
   function sayHello(name){
      console.log("Hello My name is" + name);
   }
   
   sayHello("lilikim");   //호출
   ```
   <br>
2. 객체(Object)안의 메서드 선언
   <br>
   메서드명: function(agr1, arg2,...){
   <br>
   ...    //동작
   <br>
   }
   <br>
   ```javascript
   const player = {
       name: "lilikim",
       sayHello: function(otherName){
       console.log("Hello my other name is" + "otherName);
       },
   };

   player.sayHello("lin");   //호출
   ```
   <br>
   

