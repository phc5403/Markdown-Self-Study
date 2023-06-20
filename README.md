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
● Markdown은 최대한 가독성이 좋도록 설계되었음.  
● 이를 위해 전적으로 구두점 문자로 구성되며 구두점 문자는 의미하는 대로 보이도록 신중하게 설계되었음(예를 들면 별표 `*문자*`는 실제로 문자를 강조하는것 처럼 보임).  

### ① INLINE HTML
#### Table
→ HTML 테이블 추가  
→ Markdown 서식 구문은 블록 수준 HTML 태그 내에서 처리되지 않음.  
→ 예를 들어, HTML 블록 내에서 Markdown 스타일 `*emphasis*` 을 사용할 수 없음.  
→ 범위 수준 HTML 태그(`<span>`, `<cite>`, `<del>`)는 Markdown 단락, 목록 항목 또는 헤더의 모든 위치에서 사용할 수 있음.  원하는 경우 Markdown 서식 대신 HTML 태그를 사용할 수 도 있음.  
→ 예를 들어, Markdown의 링크나 이미지 구문 대신, HTML의 `<a>`또는 `<img>` 태그를 사용하고 싶으면 쓰면 됨.  

```
This is a regular paragraph.
<table>
    <tr>
        <td> Foo </td>
    </tr>
</table>

This is another regular paragraph.
```

### ② Automatic Escaping For Special Characters(특수 문자 자동 이스케이프)
● HTML에는 특별 취급하는 두 문자가 있음.  
  1. `<` : 태그를 시작하는 데 사용됨.
  2. '&' : HTML 엔티티를 표시하는 데 사용됨.  
● 위 두 문자를 Literal 문자로 사용하고 싶은 경우, `&lt;`, `&amp;`와 같은 엔티티로 이스케이프 처리해야 함.

● 특히, Ampersand(&, 앰퍼샌드)는 URL 내에서 사용할 때에도, `AT&T` → `AT&amp;T`와 같이 이스케이프 처리해야해서 쓰기 불편함.    
  → 앵커 태그 `<href>` 속성에서 이스케이프 처리를 잊기 쉬워서 HTML 유효성 검사 오류의 가장 일반적인 원인이 되기도 함.   

● **Markdown은 필요한 모든 이스케이프 처리를 해주어 이러한 문자를 자연스럽게 사용할 수 있음.**  
  → HTML 엔티티의 일부로 앰퍼샌드를 사용하면 변경되지 않지만, 그렇지 않다면 `&amp;`로 자동 이스케이프 처리가 됨.  
  → 따라서, 저작권 기호를 쓰고싶다면 `&copy;` = &copy; 처럼 쓰면 되지만, `AT&T`를 작성하는 경우 `AT&amp;T`라고 처리됨.  

● 마찬가지로 Markdown은 인라인 HTML을 지원하므로 HTML 태그의 구분 기호로 `< (꺾쇠 괄호)`를 사용하면 Markdown에서 이를 그대로 취급함.
  → 그러나, `4 < 5` 같이 작성하는 경우 `4 &lt; 5`로 이스케이프 처리가 되버림.  

● Markdown 코드 범위 및 블록 내에서 `<`와 `&`는 항상 자동으로 인코딩 됨. 이렇게 하면 Markdown을 사용하여 HTML 코드에 대해 쉽게 작성 할 수 있음. (HTML 구문으로 작성하려면 모든 단일 `<`와 `&`를 일일이 이스케이프 처리해야 하기 때문)  

## ▶ Block Elements (블록 요소)
### ① Paragraphs and Line breaks (단락 및 줄 바꿈)
● 단락은 단순히 하나 이상의 빈 줄로 구분된 하나 이상의 연속된 텍스트 줄(빈 줄은 빈 줄처럼 보이는 모든 줄이다, 공백이나 탭만 포함된 줄은 공백으로 간주됨). **일반 단락(문자)은 공백이나 탭으로 들여쓰기하면 안 됨!**  

● Markdown 에서는 `<br>`를 **단락의 끝에 공백 2번**을 하면 가능.  

### ② Headers (헤더)
● Markdown은 `Setext`와 `Atx`라는 두 가지 스타일의 헤더를 지원함.  

#### Setext
● `=`와 `-`를 사용하여 밑줄을 표현함.  
```
This is an H1
=============

This is an H2
-------------
```
→ `=`와 `-`는 몇 개든 상관없음.  

#### Atx
● 줄 시작 부분에서 헤더 수준 1 ~ 6에 해당하는 1 ~ 6개의 해시 문자를 사용함.  
```
# This is an H1
## This is an H2
###### This is an H6

### This is H3 ###### 
```
→ 마지막 줄 처럼 헤더를 닫을 수는 있지만, **열린 해시의 수에 따라 헤더 수준이 결정**되므로 닫는 해시는 열린 해시의 수와 일치할 필요조차 없다(=장식용).  

### ③ BlockQuotes (인용구)
● Markdown은 블록 인용에 이메일 스타일 `>` 문자를 사용함.  

● Markdown은 간편하게 Hard-wrapped된 단락의 첫 줄 앞에만 `>`를 넣을 수 있음.  

```
> 이것은 두 개의 단락이 있는 블록 인용문입니다. Life is short, You need Python. 인생은 짧으니, 당신은 파이썬이 필요하다. Bruce Eckel.

> Programming isn't about what you know; it's about what you can figure out. 프로그래밍은 무엇을 알고 있는가에 대한 것이 아니다. 그것은 당신이 무엇을 알아낼 수 있는 가에 대한 것이다. Chris Pine(크리스 파인). 
```
↳ 위 예시는 이렇게 보인다.  

> The only way to learn a new programming language is by writing programs in it. 새로운 프로그래밍 언어를 배우는 유일한 방법은 그 언어로 프로그램을 만드는 것이다. Dennis Ritchie(데니스 리치, C언어 창시자).

> In some ways, programming is like painting. You start with a blank canvas and certain basic raw materials. You use a combination of science, art, and craft to determine what to do with them. 어떤 면에서 프로그래밍은 그림그리는 것과 같다. 당신은 특정한 기본 재료들과 빈 캔버스에서 시작한다. 그것들을 가지고 무엇을 할지 경정하기 위해서 당신은 과학, 기술, 기예의 조합을 사용한다. Andrew Hunt(앤드류 헌트).

● BlockQuotes는 다음 수준을 추가하여 중첩할 수 있다.  
```
> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
```
↳ 위 예시는 이렇게 보인다.  

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

● BlockQuotes는 헤더, 목록 및 코드 블록을 비롯한 다른 Markdown 요소를 포함할 수 있다.  
```
> ## This is a header.
>
> 1.   This is the first list item.
> 2.   This is the second list item. (숫자 뒤의 공백 3칸은 상관없는듯?)
>
> Here's some example code:
>
>     return shell_exec("echo $input | $markdown_script");

```
↳ 위 예시는 이렇게 보인다.  

> ## This is a header.
>
> 1.   This is the first list item.
> 2. This is the second list item.
>
> Here's some example code:
>
>     return shell_exec("echo $input | $markdown_script");

### ④ LISTS (목록)
● Markdown은 정렬된 목록(번호 매기기)과 정렬되지 않은 목록(글머리 기호)을 지원함.  

● 순서가 지정되지 않은 목록은 `*`, `+`, `-`을 리스트 마커로 상호 교환하여 사용함.  
```
* Red
* Green
* Blue

+ Red
+ Green
+ Blue

- Red
- Green
- Blue
```

● 순서가 있는 목록은 숫자 다음에 마침표를 사용함.  
```
1. Bird
2. McHale
3. Parish
```

● 목록을 표시하는 데 사용한 실제 숫자는 Markdown이 생성하는 HTML 출력에 영향을 미치지 않음(**최상위 숫자부터 자동으로 넘버링 됨!**).
```
3. Bird
1. McHale
8. Parish
```
↳ 위 예시는 이렇게 보인다.  

3. Bird
1. McHale
8. Parish

● 목록을 보기 좋게 `*   문자열`처럼 들여쓰기로 묶을 수 있긴함.  
```
*   Bird
*   Magic
```

→ 내부적으로 HTML로 바뀌는 내용은?
```
<ul>
<li> Bird </li>
<li> Magic </li>
</ul>
```
↳ 위 예시는 이렇게 보인다.  

*   Bird
*   Magic

● 하지만, **목록 항목이 빈 줄로 구분되면 Markdown은 HTML을 출력에서 항목을 `<p>`태그로 자동으로 묶는다!** 
```
* Bird

* Magic
```

→ 내부적으로 HTML로 바뀌는 내용은?
```
<ul>
<li> <p> Bird </p> </li>
<li> <p> Magic </p> </li>
</ul>
```

● 목록 항목은 여러 단락으로 구성될 수 있다. 목록 항목의 각 후속 단락은 `4개의 공백 또는 하나의 탭`으로 들여쓰기 되어야 함.  
```
1. Life is short, You ne
    ed Python.

    인생은 짧고, 당신은 파이썬이 필요하다.

2. Life is long, You don't need Python.
```
↳ 위 예시는 이렇게 보인다. (**need의 띄어쓰기 처리된 것 유의**) 

1. Life is short, You ne
    ed Python.

    인생은 짧고, 당신은 파이썬이 필요하다.

2. Life is long, You don't need Python.

● 다른 예시  
```
*   This is a list item with two paragraphs.

    This is the second paragraph in the list item. You're
only required to indent the first line. Lorem ipsum dolor
sit amet, consectetuer adipiscing elit.

*   Another item in the same list.
```
↳ 위 예시는 이렇게 보인다.  

*   This is a list item with two paragraphs.

    This is the second paragraph in the list item. You're
only required to indent the first line. Lorem ipsum dolor
sit amet, consectetuer adipiscing elit.

*   Another item in the same list.

● 목록 항목 내에 **인용구**를 넣으려면 인용구의 `>` 구분 기호를 들여쓰기 해야 함.  
```
*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.
```
↳ 위 예시는 이렇게 보인다.  

*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.

● 목록 항목 내에 **코드 블록**을 넣으려면 코드 블록을 **두 번** 들여써야 함(공백 8개 or 탭 2개).  
```
*   A list item with a code block:

        <code goes here>
```
↳ 위 예시는 이렇게 보인다.  

*   A list item with a code block:

        <code goes here>

● 실수로 정렬된 목록은 마침표를 `\`로 이스케이프하여 트리거할 수 있다!
```
1986. What a great season1.  
1986\. What a great season2.  
1986. What a great season3.  
```
↳ 위 예시는 이렇게 보인다.  

1986. What a great season1.  
1986\. What a great season2.  
1986. What a great season3.  
↳ 항목의 넘버링을 건너 뛰고, 띄어쓰기도 다르게 되어있다.  

### ⑤ Code Blocks (코드 블록)  ★★★★★★ 작동 X ★★★★★★★★★
● 일반 단락으로 구성하는 대신 코드 블록의 줄을 문자 그대로 해석함.  

● Markdown은 코드 블록을 `<pre>`와 `<code>` 태그로 감싼다.  

● Markdown에서 코드 블록을 생성하려면 블록의 모든 줄을 **최소 4개의 공백 또는 1개의 탭**으로 들여쓰기하면 된다.  

```
This is a normal paragraph:
    This is a code block. 
```
↳ 위 예시는 이렇게 보인다.  

This is a normal paragraph:  
  This is a code block.  

● Markdown 내부에서 변환된 모습.  
```
<p> This is a normal paragraph: </p>
<pre><code> This is a code black. </pre></code>
```

Here is an example of AppleScript:  
    tell application "Foo"  
        beep  
    end tell  

<p>Here is an example of AppleScript:</p>

<pre><code>tell application "Foo"
    beep
end tell
</code></pre>

● 코드 블록은 들여쓰기되지 않은 행에 도달할 때까지와 계속됩니다.  
코드 블록 내에서 `&`와 `<`, `>`는 자동으로 HTML 엔티티로 변환됩니다.  

● 이렇게하면 Markdown을 사용하여 예제 HTML 소스 코드를 포함하는 것이 매우 쉬워집니다.  
붙여넣고 들여쓰기만 하면 Markdown이 `&`와 `<`, `>`를 인코딩하는 번거로움을 처리합니다.  

```
    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>
```
↳ 위 예시는 이렇게 보인다.  

    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>

<pre><code>&lt;div class="footer"&gt;
    &amp;copy; 2004 Foo Corporation
&lt;/div&gt;
</code></pre>

    
### ⑥ Horizontal Rules (수평적 규칙)


## ▶ Span Elements (스팬 요소)
### ① Links (연결)
### ② Emphasis (중요성)
### ③ Code (암호? 코드?)
### ④ Images (이미지)

## ▶ Miscellaneous (여러가지 잡다한)
### ① Backslash Escapes (백슬래시 이스케이프)
### ② Automatic Links (자동 링크)




↳ 위 예시는 이렇게 보인다.  
