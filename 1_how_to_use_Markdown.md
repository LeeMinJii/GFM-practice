# **<야 너도 MARKDOWN 할 수 있어>**  
- markdown 기본 구문을 익혀보자. 
  
목차

----

1. [제목](#1.-제목)
2. [단락](#2.-단락)
3. [줄 바꿈](#3.-줄바꿈)
4. 강조
5. 인용구
6. 목록
7. 코드
8. 수평 규칙
9. 링크
10. 이미지
11. 이스케이프 문자
12. HTML
 
----  
#1. 제목
# **1. 제목**  
> 1. 제목을 만들려면 단어나 구 앞에 #을 추가한다. 만들고 싶은 제목의 크기에 따라 #을 한개부터 여섯개까지 달 수 있다.  
>- 주의사항 :  #뒤에 반드시 공백이 있어야함.  
```ex)    # Here's a Heading (O)  /   #Here's a Heading (X)```
>>-  #1개 : 아주 큰 크기의 제목
>>-  #2개 : 조금 큰 크기의 제목  
>>-  #3개 : 보통 크기의 제목  
>>-  #4개 : 조금 작은 크기의 제목  
>>-  #5개 : 아주 작은 크기의 제목  
>>-  #6개 : 굉장히 작은 크기의 제목  
## 예)  

```
    <Markdown>	                      <HTML>	              
# Heading level 1	        <h1>Heading level 1</h1>	
```
```출력 결과 ``` 
# 제목 1

```
    <Markdown>	                      <HTML>
## Heading level 2	        <h2>Heading level 2</h2>	
```
```출력 결과```
## 제목 2

---

```
    <Markdown>	                      <HTML>
### Heading level 3	        <h3>Heading level 3</h3>	
```
```출력 결과```
### 제목 3

---

```
    <Markdown>	                      <HTML>
#### Heading level 4	    <h4>Heading level 4</h4>	
```
```출력 결과```
#### 제목 4

---

```
    <Markdown>	                      <HTML>
##### Heading level 5	    <h5>Heading level 5</h5>	
```
```출력 결과```
##### 제목 5

---

```
    <Markdown>	                      <HTML>
###### Heading level 6	    <h6>Heading level 6</h6>	
```
```출력 결과```
###### 제목 6

---


> 2. 제목을 만드는 또 다른 방법은 텍스트 아래 줄에 ===혹은 ---을 추가하는 것이다.
> 

## 예)
```
  <Markdown>              	<HTML>	
Heading level 1
===============	     <h1>Heading level 1</h1>	
```
```출력 결과 ``` 

Heading level 1
===============	

```
  <Markdown>              	<HTML>	
Heading level 2
---------------	     <h2>Heading level 2</h2>	
```
```출력 결과 ``` 

Heading level 2
---------------	 

---


# **2. 단락**
> 단락을 만들려면 빈 줄을 사용하여 텍스트 줄을 분리한다.  
### 예)
```
<Markdown>
I really like using Markdown.

I think I'll use it to format all of my documents from now on.
__________________________
<HTML>
<p>I really like using Markdown.</p>

<p>I think I'll use it to format all of my documents from now on.</p>	
```
```출력 결과  ```  
I really like using Markdown.

I think I'll use it to format all of my documents from now on.

---


>- 주의사항 : 공백이나 탭으로 문단을 들여쓰지 않아야 한다.
```
ex) 
Don't put tabs or spaces in front of your paragraphs.

Keep lines left-aligned like this. (O)

ex)
    This can result in unexpected formatting problems.

  Don't add tabs or spaces in front of paragraphs. (X)
```
# **3. 줄 바꿈**
>줄을 바꾸려면 두 개 이상의 공백으로 선을 끝내고 엔터를 입력한다.
### 예)
```
<Markdown>
This is the first line.  
And this is the second line.
<HTML>
<p>This is the first line.<br>
And this is the second line.</p>
```
```출력 결과  ```  
This is the first line.  
And this is the second line.

---

>- 주의사항 : 대부분의 경우에 마크 업 언어는 줄 끝에 아무것도 필요하지 않다.  

``` 호환성을 위해 [공백+엔터] 대신 <br> HTML 태그를 이용하기도 한다. ```
```
ex) First line with two spaces after.  
And the next line.

First line with the HTML tag after.<br>
And the next line. (O)

ex) First line with a backslash after.\
And the next line.

First line with nothing after.
And the next line. (X)
```

---

# **4. 강조**

> **1. 굵게**  
> 단어나 구 전후에 두 개의 별표 또는 밑줄을 추가하여 글자를 굵게 만들어 단어를 강조한다.  
>- 공백은 없도록 한다.  
>- 문자 중간에는 별표는 사용가능 하되, 밑줄은 사용불가능하다.  
```ex)  Love**is**bold (O)	 Love__is__bold (X)```
### 예) 
```
        <Markdown>	                   <HTML>	
I just love **bold text**.	I just love <strong>bold text</strong>.	
```
출력 : I just love **bold text**.

---

```
       <Markdown>	                   <HTML>	
 I just love __bold text__.	I just love <strong>bold text</strong>.	
```
출력 : I just love **bold text**. 

---

```
<Markdown>	         <HTML>
Love**is**bold	Love<strong>is</strong>bold	
```
출력 : Love**is**bold

---

> **2. 기울임꼴**  
> 단어나 구 전후에 하나의 별표 또는 밑줄을 추가하여 글자를 기울여 단어를 강조한다.  
>- 공백은 없도록 한다.  
>- 문자 중간에는 별표는 사용가능 하되, 밑줄은 사용불가능하다.  
```ex)  A*cat*meow (O)	 A_cat_meow (X)```  
### 예)
```
           <Markdown>	                                <Html>
Italicized text is the *cat's meow*.	Italicized text is the <em>cat's meow</em>.  
```
출력 : Italicized text is the *cat's meow*.  

---

```
<Markdown>	                   <Html>
Italicized text is the _cat's meow_.	Italicized text is the <em>cat's meow</em>.	  
```
출력 : Italicized text is the _cat's meow_.  

---

```
<Markdown>	           <Html>
A*cat*meow	      A<em>cat</em>meow  
```  
출력 : A*cat*meow

---

> **3. 굵고 기울임꼴**  
> 단어나 구 전후에 세 개의 별표 또는 밑줄을 추가하여 글자를 굵게 함과 동시에 기울여 단어를 강조한다. 
>- 공백은 없도록 한다.  
>- 문자 중간에는 별표는 사용가능 하되, 밑줄은 사용불가능하다.  
```ex)  This is really***very***important text. (O)	 This is really___very___important text. (X)```  
### 예)
```
           <Markdown>	                               <Html>
This text is ***really important***.	 This text is <strong><em>really important</em></strong>.
```
출력 : This text is ***really important***.  

---

```
           <Markdown>	                               <Html>
This text is ___really important___.	 This text is <strong><em>really important</em></strong>.  
```
출력 : This text is ___really important___.

---

```
           <Markdown>	                               <Html>
This text is __*really important*__.	 This text is <strong><em>really important</em></strong>.  
```  
출력 : This text is __*really important*__.  

---

```
          <Markdown>	                               <Html>
This text is **_really important_**.	 This text is <strong><em>really important</em></strong>.  
```
출력 : This text is **_really important_**.  

---

```
          <Markdown>	                               <Html>
This is really***very***important text.	 This is really<strong><em>very</em></strong>important text.  
```
출력 : This is really***very***important text.  

---

# **5. 인용구**
```단락 앞에 >을 추가하여 인용구를 만든다.```
### 예)
```
> Dorothy followed her through many of the beautiful rooms in her castle.
```
출력 결과
> Dorothy followed her through many of the beautiful rooms in her castle.  

---


```1. 여러 단락이 있는 인용구  ```
- 단락 사이에 빈 줄에 >을 추가한다.
### 예)
```
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```
출력 결과    
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

---

```2. 중첩 인용구```
- 중첩할 단락 앞에 >>을 추가한다.
### 예)
```
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```
출력 결과  
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

---

```3. 다른 요소가 있는 인용구```
- 인용구는 다른 마크다운 서식 요소를 포함할 수 있다. 대표적으로 > - 을 이용하는 방법이 있다.
### 예)
```
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
```
출력 결과  
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.

---

# **6. 목록**
> **1. 정렬된 목록**  
>>정렬 된 목록을 만들려면 숫자 뒤에 마침표(.)가 있는 항목을 추가한다.
> - 숫자 순서대로 일 필요는 없지만 목록은 숫자 1로 시작해한다.
>- 중첩 된 목록을 만들려면 하나 이상의 항목을 들여 쓴다.
## 예)
```
<Markdown>	
1. First item   
2. Second item
3. Third item
4. Fourth item	
___________
<HTML>
<ol>
<li>First item</li>
<li>Second item</li>
<li>Third item</li>
<li>Fourth item</li>
</ol>
```
```출력 결과 ``` 
1. First item   
2. Second item
3. Third item
4. Fourth item	
   
---

```
<Markdown>
1. First item
1. Second item
1. Third item
1. Fourth item	
___________
<HTML>
<ol>
<li>First item</li>
<li>Second item</li>
<li>Third item</li>
<li>Fourth item</li>
</ol>
```
```출력 결과  ```
1. First item
1. Second item
1. Third item
1. Fourth item	

---

```
<Markdown>
1. First item
8. Second item
3. Third item
5. Fourth item	
___________
<HTML>
<ol>
<li>First item</li>
<li>Second item</li>
<li>Third item</li>
<li>Fourth item</li>
</ol>
```
```출력 결과  ```
1. First item
2. Second item
3. Third item
4. Fourth item	

---

```
<Markdown>
1. First item
2. Second item
3. Third item
    1. Indented item
    2. Indented item
4. Fourth item
___________
<HTML>
<ol>
<li>First item</li>
<li>Second item</li>
<li>Third item
<ol>
<li>Indented item</li>
<li>Indented item</li>
</ol>
</li>
<li>Fourth item</li>
</ol>
```
```출력 결과```  
1. First item
2. Second item
3. Third item
    1. Indented item
    2. Indented item
4. Fourth item

---

> - 주의 사항 : 호환성을 위해 ' ) '가 아닌 ' . '만을 사용한다.
```
ex) 
1. First item
2. Second item (O)
ex) 
1) First item
2) Second item (X)
```

---


> **2. 정렬되지 않은 목록**  
> > 정렬되지 않은 목록을 만들려면 항목 앞에 대시 (-), 별표 (*) 또는 더하기 기호 (+)를 추가 한다.
>- 중첩 된 목록을 만들려면 하나 이상의 항목을 들여 쓴다.
## 예)
```
<Markdown>
- First item
- Second item
- Third item
- Fourth item
___________
<HTML>
<ul>
<li>First item</li>
<li>Second item</li>
<li>Third item</li>
<li>Fourth item</li>
</ul>
```
```출력 결과```  
- First item
- Second item
- Third item
- Fourth item

---

```
<Markdown>
* First item
* Second item
* Third item
* Fourth item
___________
<HTML>
<ul>
<li>First item</li>
<li>Second item</li>
<li>Third item</li>
<li>Fourth item</li>
</ul>
```
```출력 결과```  
* First item
* Second item
* Third item
* Fourth item

---

```
<Markdown>
+ First item
+ Second item
+ Third item
+ Fourth item
___________
<HTML>
<ul>
<li>First item</li>
<li>Second item</li>
<li>Third item</li>
<li>Fourth item</li>
</ul>
```
```출력 결과```  
+ First item
+ Second item
+ Third item
+ Fourth item

---

```
<Markdown>
- First item
- Second item
- Third item
    - Indented item
    - Indented item
- Fourth item
___________
<HTML>
<ul>
<li>First item</li>
<li>Second item</li>
<li>Third item
<ul>
<li>Indented item</li>
<li>Indented item</li>
</ul>
</li>
<li>Fourth item</li>
</ul>
```
```출력 결과```  
- First item
- Second item
- Third item
    - Indented item
    - Indented item
- Fourth item

---

> - 주의 사항 : 호환성을 위해 기호를 혼합하여 사용하지 않는다.
```
ex) 
- First item
- Second item
- Third item
- Fourth item (O)
ex) 1) First item
2) Second item (X)
```

---

> ***3. 목록에 요소 추가***
> > 목록의 연속성을 유지하면서 다른 요소를 추가하려면 요소를 공백 4 개 또는 탭 1 개로 들여 쓴다.

 ```단락```
```
*   This is the first list item.
*   Here's the second list item.

    I need to add another paragraph below the second list item.

*   And here's the third list item.
```
출력 결과  
*   This is the first list item.
*   Here's the second list item.

    I need to add another paragraph below the second list item.

*   And here's the third list item.

---

```인용구```
```
*   This is the first list item.
*   Here's the second list item.

    > A blockquote would look great below the second list item.

*   And here's the third list item.
```
출력 결과  
*   This is the first list item.
*   Here's the second list item.

    > A blockquote would look great below the second list item.

*   And here's the third list item.

---

```코드 블록  (공백 4 개 또는 탭 1 개로 만든다.)```
```
1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.
```

출력 결과  
1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.

---

```이미지```
```
1.  Open the file containing the lion image.
2.  See the cute lion.

    ![Tux, the Linux mascot](lion.jpg)

3.  Close the file.
```
출력 결과  
1.  Open the file containing the Linux mascot.
2.  Marvel at its beauty.

    ![Tux, the Linux mascot](lion.jpg)

3.  Close the file.

---

```목록 (정렬되지 않은 목록을 정렬 된 목록에 중첩하거나 그 반대로 할 수 있다.)```
```
1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item
```
출력 결과  
1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item

---

# **7. 코드**

>단어나 구를 코드로 나타내려면 **백틱** ( ` )으로 묶는다.
### 예)
```
<Markdown>  
At the command prompt, type `nano`.
___________
<HTML>
At the command prompt, type <code>nano</code>.
```
출력 결과  
At the command prompt, type `nano`

---

>- 백틱 ( ` )에서 빠져나오기
>> 코드로 표시하려는 단어나 구에 하나 이상의 백틱이 포함되어있는 경우 단어나 구를 이중 백틱 ( `` )으로 묶어 빠져나오게 한다.
### 예)
```
<Markdown>  
``Use `code` in your Markdown file.``
___________
<HTML>
<code>Use `code` in your Markdown file.</code>
```
출력 결과  
``Use `code` in your Markdown file.``

---

 # **8. 수평 규칙**
>수평선을 만들려면 3 개 이상의 별표 (***), 대시 (---) 또는 밑줄 (___)을 한 줄에 단독으로 사용한다.  
>- 출력은 모두 같다. 

>-  **주의 사항 : 호환성을 위해 수평 규칙 앞뒤에 빈 줄을 넣는다.**

## 맞는 예)
```
Try to put a blank line before...

---

...and after a horizontal rule. (O)
```


## 틀린 예)
```
Without blank lines, this would be a heading.
---
Don't do this!  (X)
```
---


# **9. 링크**
>링크를 만들려면 링크 텍스트를 대괄호[]로 묶은 다음 바로 뒤에 URL을 소괄호()로 묶는다.
### 예)
```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com).
```
```출력 결과 ```  
My favorite search engine is [Duck Duck Go](https://duckduckgo.com).

---

>**1. 제목 추가**  
>>제목을 추가하려면 URL 뒤 괄호로 묶는다.
### 예)
```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").
```
```  출력 결과  ```  
My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").

---

> **2. URL 및 이메일 주소**
>>URL 또는 이메일 주소를 링크로 빠르게 바꾸려면 각도 대괄호<>로 묶는다.
### 예)
```
<https://www.markdownguide.org>
<fake@example.com>
```
```  출력 결과```    
<https://www.markdownguide.org>  
<fake@example.com>

---

> **3. 링크 서식 지정**
>- 링크를 강조하려면 괄호와 괄호 전후에 별표( * )를 추가한다.   
>- 링크를 코드로 나타내려면 괄호에 백틱( ` )을 추가한다.
### 예)
``` 
I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).
``` 
출력 결과  
I love supporting the **[EFF](https://eff.org)**.  
This is the *[Markdown Guide](https://www.markdownguide.org)*.  
See the section on [`code`](#code).

---

> **4. 참조 스타일 링크**  
> 참조 스타일 링크는 마크다운에서 URL을 쉽게 표시하고 읽을 수 있는 특별한 종류의 링크이다.

## **<링크의 첫 번째 부분 서식 지정>**
참조 스타일 링크의 첫 번째 부분은 두 세트의 대괄호로 형식이 지정된다.
- 첫 번째 대괄호 세트는 링크 된 것으로 표시되어야하는 텍스트를 둘러 싼다.   
- 두 번째 대괄호 세트는 문서의 다른 곳에 저장하는 링크를 가리키는 데 사용되는 레이블을 표시한다.


```예)``` 
``` 
[hobbit-hole][1]
[hobbit-hole] [1]  -> 사이에 공백 사용 가능
``` 
- **주의 사항** : 두 번째 대괄호 세트의 레이블은 대소 문자를 구분하지 않으며 문자, 숫자, 공백 또는 구두점을 포함 할 수 있다. 
## **<링크의 두 번째 부분 서식 지정>**
다음 예시와 같이 형식이 지정된다.  
``` 예)``` 
``` 
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit lifestyles)
[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"
[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit lifestyles'
[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)

*위 형식들은 링크의 두 번째 부분에 대해 거의 모두 동일함.
``` 
- 이 링크의 두 번째 부분은 마크 다운 문서의 아무 곳에 나 배치 할 수 있다.  
## <부품 조합의 예>
```URL을 단락에 대한 표준 URL 링크 로 추가하는 예시)```
``` 
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"), and that means comfort.
``` 
``` 이에 불필요한 기능을 삭제한 URL형식 지정의 예시)```
``` 
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"), and that means comfort.
``` 
두 예시의 출력 결과는 다음으로 같다.  
>In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"), and that means comfort.  

[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"

  
 ``` 링크의 HTML : <a href="https://en.wikipedia.org/wiki/Hobbit#Lifestyle" title="Hobbit lifestyles">hobbit-hole</a> ``` 

>- **링크 주의 사항 : URL 중간에 공백이 있어서는 안된다.**  
``` ex)[link](https://www.example.com/my%20great%20page) (O) /  [link](https://www.example.com/my great page) (X)``` 

---

# **10. 이미지**
> **1. 이미지  추가**  
>이미지를 추가하려면 느낌표(!), 대괄호[] 안에 대체 텍스트, 소괄호()에 이미지의 경로 URL을 추가한다. 
>- 선택적으로 괄호 안의 URL 뒤에 ""을 이용해 제목을 추가 할 수 있다.
### 예)
```
![My dog is so cute!](dog.jpg "My Cute Dog")
```
출력 결과
![My dog is so cute!](dog.jpg "My Cute Dog")

---

> **2. 이미지 연결**  
이미지에 링크를 추가하려면 이미지의 마크 다운을 괄호로 묶은 다음 괄호를 이용해 링크를 추가한다.
### 예)
```
[![Sunflower in Jeju](sunflower.jpg "Shiprock, beautiful sunflower")](https://search.naver.com/search.naver?where=image&sm=tab_jum&query=sunflower)
```
출력 결과  
[![Sunflower in Jeju](sunflower.jpg "Shiprock, beautiful sunflower")](https://search.naver.com/search.naver?where=image&sm=tab_jum&query=sunflower)

---

# **11. 이스케이프 문자**
>Markdown 문서에서 텍스트 서식을 지정하는 데 사용되는 리터럴 문자를 표시하기 위해 문자 앞에 **백 슬래시** ( \ )를 추가한다.

## <이스케이프 문자의 종류>
```
문자  이름
-------------------
\	백슬래시
`	백틱(코드에서 백틱을 벗어나는 것 참조)
*	별표
_	밑줄
{ }	중괄호
[ ]	대괄호
< >	각도 브래킷
( )	괄호
#	파운드 기호
+	플러스 기호
-	마이너스 기호(하이픈)
.	점
!	느낌표
|	파이프(테이블에서 파이프를 탈출하는 것 참조)
```

### 이스케이프 문자 사용 예시)  
```
\* Without the backslash, this would be a bullet in an unordered list.
```
```출력 결과```   
\* Without the backslash, this would be a bullet in an unordered list.  

---

# **12. HTML**
>**HTML태그의 사용**  
>- 많은 Markdown 응용 프로그램을 사용하면 Markdown 형식의 텍스트에서 HTML 태그를 사용할 수 있다.  
>- Markdown 구문보다 특정 HTML 태그를 선호하는 경우에 유용하게 쓰인다.  
ex) 예를 들어 어떤 사람들은 이미지에 HTML 태그를 사용하는 것이 더 쉽다고 생각한다.  
>- HTML을 사용하면 텍스트 색상 지정 또는 이미지 너비 변경과 같이 요소의 속성을 변경해야 할 때도 유용하다.

### 예)  
```
This **word** is bold. This <em>word</em> is italic.
```
```출력 결과 ```  
This **word** is bold. This <em>word</em> is italic.

---


>-  **주의 사항** 
>>- 모든 Markdown 응용 프로그램이 문서에서 HTML을 지원하는 것은 아니다.
>>- 블록 수준 HTML 태그 내에서는 Markdown 구문을 사용할 수 없다.   
```ex) <p>italic and **bold**</p> 는 작동하지 않는다.```
>>- 빈 라인을 이용하여 주변 콘텐츠에서 ```<div><table><pre><p>```와 같은 블록 수준 HTML 요소를 분리해야하며 서식을 방해할 수 있으므로 탭이나 공백으로 태그를 들여쓰지 않도록 한다.

---

GFM의 표준 Markdown에 대한 확장 부분의 사용법 [GitHub repository URL](https://github.com/LeeMinJii/how_to_use_Markdown/blob/fe2690b954ea89a5b12c7588cbeef2ac7de43d2e/2_how_to_use_Markdown.md)
