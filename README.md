# GFM-how to use
> GFM의 표준 Markdown에 대한 확장 부분의 사용법에 대하여.

## **<Tables (extension)>**
### -  테이블이란?  
- 테이블은 행과 열이 있는 데이터 배열이다.  

### -  구성  
- 단일 헤더 행  
- 데이터로부터 헤더를 구분하는 구분자 행  
- 0개 이상의 데이터 행

### -  사용법 
- 각 행은 임의 텍스트를 포함하는 셀로 구성되며, 이 셀에서는 인선이 구문 분석되고 **파이프**(|)로 구분된다.  
> 판독의 명확성을 위해 선행 파이프와 후행 파이프가 권장된다.  
- 테이블에 블록 수준 요소를 삽입할 수 없다.  
- **구분자 행**(delimiter row)은 ```오직 하이픈(-)```, ```선행 콜론``` 또는 ```후행 콜론```, 또는 ```둘 다```에 해당하는 셀로 구성되어 각각 왼쪽, 오른쪽 또는 가운데 정렬을 나타낸다.  

## EX 1)  
```
| foo | bar |
| --- | --- |
| baz | bim |
 
<table>
<thead>
<tr>
<th>foo</th>
<th>bar</th>
</tr>
</thead>
<tbody>
<tr>
<td>baz</td>
<td>bim</td>
</tr>
</tbody>
</table>  
```
출력 결과  
| foo | bar |
| --- | --- |
| baz | bim |
 
<table>
<thead>
<tr>
<th>foo</th>
<th>bar</th>
</tr>
</thead>
<tbody>
<tr>
<td>baz</td>
<td>bim</td>
</tr>
</tbody>
</table> 

## EX 2)
```
| abc | defghi |
:-: | -----------:
bar | baz
 
<table>
<thead>
<tr>
<th align="center">abc</th>
<th align="right">defghi</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">bar</td>
<td align="right">baz</td>
</tr>
</tbody>
</table>
```
출력 결과  
| abc | defghi |
:-: | -----------:
bar | baz
 
<table>
<thead>
<tr>
<th align="center">abc</th>
<th align="right">defghi</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">bar</td>
<td align="right">baz</td>
</tr>
</tbody>
</table>  

> 한 열의 셀 길이가 일치 할 필요가 없지만 일치하는 경우 읽기가 더 쉽다.
> 
## EX 3)  
```
| f\|oo  |
| ------ |
| b `\|` az |
| b **\|** im |
 
<table>
<thead>
<tr>
<th>f|oo</th>
</tr>
</thead>
<tbody>
<tr>
<td>b <code>|</code> az</td>
</tr>
<tr>
<td>b <strong>|</strong> im</td>
</tr>
</tbody>
</table>
```
출력 결과  
| f\|oo  |
| ------ |
| b `\|` az |
| b **\|** im |
 
<table>
<thead>
<tr>
<th>f|oo</th>
</tr>
</thead>
<tbody>
<tr>
<td>b <code>|</code> az</td>
</tr>
<tr>
<td>b <strong>|</strong> im</td>
</tr>
</tbody>
</table>  

>이스케이프 처리하여 셀 내용에 파이프를 포함한다.

## EX 4) 
```
| abc | def |
| --- | --- |
| bar | baz |
> bar
 
<table>
<thead>
<tr>
<th>abc</th>
<th>def</th>
</tr>
</thead>
<tbody>
<tr>
<td>bar</td>
<td>baz</td>
</tr>
</tbody>
</table>
<blockquote>
<p>bar</p>
</blockquote>
```
출력 결과  
| abc | def |
| --- | --- |
| bar | baz |
> bar
 
<table>
<thead>
<tr>
<th>abc</th>
<th>def</th>
</tr>
</thead>
<tbody>
<tr>
<td>bar</td>
<td>baz</td>
</tr>
</tbody>
</table>
<blockquote>
<p>bar</p>
</blockquote>  

>테이블이 첫 번째 빈 라인 또는 다른 블록 수준 구조의 시작 부분에서 파손된다.

## EX 5)  
```
| abc | def |
| --- | --- |
| bar | baz |
bar

bar
 
<table>
<thead>
<tr>
<th>abc</th>
<th>def</th>
</tr>
</thead>
<tbody>
<tr>
<td>bar</td>
<td>baz</td>
</tr>
<tr>
<td>bar</td>
<td></td>
</tr>
</tbody>
</table>
<p>bar</p>
```
출력 결과  
| abc | def |
| --- | --- |
| bar | baz |
bar

bar
 
<table>
<thead>
<tr>
<th>abc</th>
<th>def</th>
</tr>
</thead>
<tbody>
<tr>
<td>bar</td>
<td>baz</td>
</tr>
<tr>
<td>bar</td>
<td></td>
</tr>
</tbody>
</table>
<p>bar</p>  

## EX 6)  
```
| abc | def |
| --- |
| bar |
 
<p>| abc | def |
| --- |
| bar |</p>
```
출력 결과  
| abc | def |
| --- |
| bar |
 
<p>| abc | def |
| --- |
| bar |</p>  

>헤더 행 은 셀 수의 구분 기호 행과 일치해야한다. 그렇지 않으면 테이블이 인식되지 않는다.

## EX 7)  
```
| abc | def |
| --- | --- |
| bar |
| bar | baz | boo |
 
<table>
<thead>
<tr>
<th>abc</th>
<th>def</th>
</tr>
</thead>
<tbody>
<tr>
<td>bar</td>
<td></td>
</tr>
<tr>
<td>bar</td>
<td>baz</td>
</tr>
</tbody>
</table>
```
출력 결과  
| abc | def |
| --- | --- |
| bar |
| bar | baz | boo |
 
<table>
<thead>
<tr>
<th>abc</th>
<th>def</th>
</tr>
</thead>
<tbody>
<tr>
<td>bar</td>
<td></td>
</tr>
<tr>
<td>bar</td>
<td>baz</td>
</tr>
</tbody>
</table>  

>테이블 행의 나머지 부분은 셀 수에 따라 다르다.
>- 헤더 행의 셀 수보다 ```적은``` 수의 셀이 있는 경우 : 빈 셀이 삽입된다.
>- 헤더 행의 셀 수보다 ```많은``` 수의 셀이 있는 경우 : 초과는 무시된다.

## EX 8)
```
| abc | def |
| --- | --- |
 
<table>
<thead>
<tr>
<th>abc</th>
<th>def</th>
</tr>
</thead>
</table>
```  
출력 결과  
| abc | def |
| --- | --- |
 
<table>
<thead>
<tr>
<th>abc</th>
<th>def</th>
</tr>
</thead>
</table>  

>본문에 행이 없는 경우 HTML 출력에 ```<tbody>```가 생성되지 않는다.
