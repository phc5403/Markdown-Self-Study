# **[ Markdown Self-Study Note ]**  


## Official_Document를 보면서 정리  


## ▶ CONFIGURATION  
### 1. Line Break(줄 바꿈)   
`<br>`  

### 2. Moveable Type  
뭘 뜻하는지 모르겠다,,  

## ▶ PARAGRAPHS, HEADERS, BLOCKQUOTES  
### 1. Paragraph(단락)  
→ 하나 이상의 빈 줄로 구분된 연속된 텍스트 줄.  
→ 공백 or Tab만 포함된 줄은 공백으로 간주한다.  
`<p> This area is paragraphs.</p>`  <br>
`<p> 단락 내에서는 줄바꿈을 하려면 <br>를 사용해야한다. </p>` <br>
### 2. Headers(헤더)  
→ 헤더는 Setext, atx 두 가지의 Style이 있다.  
♤ Setext-style  
`"<h1> Header </h1>"`  
or  
`"Header"`  
`=`
→ h1을 나타냄.  

`"<h2> Header </h2>"`  
or  
`"Header"`  
`-`  
→ h2을 나타냄.  

A First Level Header
=
A Second Level Header
-
※ 직접 사용해보니, '=' or '-'은 그 윗줄에 "Enter로 구분되어있지 않은 모든 문장"을 Header로 같이 묶어 버린다.  
사용시 주의 할 것.  

♤ ats-style  
`# Header 1 ~ 6 `  
→ '#'을 1 ~ 6개 붙여씀으로써, h1 ~ h6과 동일하게 사용할 수 있다.  
