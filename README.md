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
