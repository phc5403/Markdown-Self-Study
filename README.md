# **[ Markdown Self-Study Note ]**  


## Official_Document를 보면서 정리  

# **☆ Basics**
## ▶ CONFIGURATION  
### 1. Line Break(줄 바꿈)   
→ <br>태그 or 문장의 끝에 공백 2번(이상도 되긴 함)을 적는다.  
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

### 3. Blockquotes (인용구)  
→ HTML의 \<p> 태그.  
`> This is a blockquote.`  
`> ## This is an H2 in a blockquote`  

## ▶ PHRASE EMPHASIS(구문 강조)  
→ '*'와 '_'을 사용하여 구문을 강조할 수 있다.  
→ 각 기호 1개 = 기울임  
→ 각 기호 2개 = 볼드체  
※ 강조할 문구의 시작과 끝에 기호가 붙어있어야 함.  
`*Words are emphasized.*`  
`__Words are strong emphasized__`  

## ▶ LISTS(목록)  
### 1. 순서가 없는 목록(= \<ul> - \<li>).  
→ '*' 및 '+', '-'로 표시함(동일한 표현).  
`* Candy.`  
`+ Gum.`  
`- Booze`  

### 2. 순서가 있는 목록(= \<ol> - \<li>).  
→ '1. Text~', '2. Text~' 등과 같이 표현.  

### 3. List + \<p>  
→ 목록의 요소 사이에 빈 줄을 넣으면 \<p> 처럼 단락을 구분할 수 있고,  
들여쓰기(4) 또는 Tab사용해 단락을 들여서 목록 요소별 다중 항목을 만들 수 있다.   

`* A List item.`  
`  With multiple paragraphs.`  
`* Another item in the list.`  
+ A list item.  
  With multiple paragraphs.  
- Another item in the list.  

\<li> \<p> A list item. \</p>  
\<p> With multiple paragraphs. \</p> \</li>  
→ 위와 동일한 표현이 됨.  

## ▶ LINKS(링크)  
→ Inlines(인라인), Reference(참조) 두가지 Style.  
→ 모두 대괄호를 사용하여 링크로 전환할 텍스트를 구분한다. 
### 1. Inlines  
`This is an [example link] (https://example.com/).`  
[Link Explanation] https://github.com  
→ 추가적으로, 제목을 포함할 수 있다.  
`This is an [example link] (https://github.com "Title is Github.")`  
This is an [Link Explanation] (https://github.com "Title is Github.")  
※ \<a href="https://example.com" title="With a Title"> 과 동일한 표현.  

### 2. Reference  
→ 참조 링크를 사용하면 문서의 다른 위치에서 정의한 이름으로 링크를 참조할 수 있다.  
`I get 10 times more traffic from [Google][1] than from [Naver][2] or [Github][3].`  
`    ` # 한 줄을 띄워야 함!  
`[1]: https://google.com "Google"`  
`[2]: https://naver.com "Naver"`  
`[3]: https://github.com "Github"`  
I get 10 times more traffic from [Goolgle][1] than from [Naver][2] or [Github][3].  

[1]: https://google.com "Google"  
[2]: https://naver.com "Naver"  
[3]: https://github.com "Github"  
  
※ title 속성은 선택 사항이지만  링크 이름에는 문자, 숫자 및 공백이 포함될 수 있으며  
대소문자를 구분하지 않는다.  

## ▶ IMAGES(이미지)  
→ 링크 구문과 유사하게 인라인 & 참조가 있다.  
→ title 속성은 선택사항.  
`![alt text] (/path/to/img.jpg "Title")`  # Inline  

`![alt text]`  
`[id]: /path/to/img.jpg "Title"`  # Reference  

## ▶ CODE(코드)  
→ \`(키보드 틸드키)로 코드 구문을 감싼다.  
→ Ampersands(&), Angle brackets(\< or \>)는 자동으로 HTML 엔티티로 변환된다.  
I strongly recommend against using any `<blink>` tags.

I wish SmartyPants used named entities like `&mdash;`
instead of decimal-encoded entities like `&#8212;`.  

`If you want your page to validate under XHTML 1.0 Strict, you've got to put paragraph tags in your blockquotes:
  "Hello"
  "World!"`

코드 블록안의 모든 줄을 공백 4개 or Tab 1개로 들여쓰기를 하면, 범위가 지정된다.  
`Start`  
`    Content_1`  
`    Content_2`  
`END`  

# **☆ Syntax**
## ▶ OVERVIEW  
→
