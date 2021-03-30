## GFM-how to use
- GFM의 표준 Markdown에 대한 확장 부분의 사용법

Table (extension)
GFM은 table 추가 리프 블록 유형을 사용할 확장을 .

테이블 단일 헤더 행 구성된 행과 열 데이터의 배열이다하는 구분자 행 데이터 및 제로 이상의 데이터 열로부터 헤더를 분리.

각 행은 인라인 이 구문 분석되고 파이프 ( |)로 구분 된 임의의 텍스트를 포함하는 셀로 구성됩니다 . 읽기의 명확성을 위해 선행 및 후행 파이프도 권장되며 그렇지 않으면 파싱 모호성이 있습니다. 파이프와 셀 내용 사이의 공간이 잘립니다. 블록 수준 요소는 테이블에 삽입 할 수 없습니다.

분리 행은 그 내용 만 하이픈 (있는 세포로 구성 -), 및 선택적으로, 선행 또는 후행 콜론 ( :), 또는 양쪽 각각 오른쪽, 또는 중심 정렬을 나타내도록 왼쪽.

예 198
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
한 열의 셀은 길이가 일치 할 필요가 없지만 일치하는 경우 읽기가 더 쉽습니다. 마찬가지로 선행 및 후행 파이프를 사용하면 일관성이 없을 수 있습니다.

예제 199
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
다른 인라인 범위 내부를 포함하여 이스케이프 처리하여 셀의 콘텐츠에 파이프를 포함합니다.

예제 200
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
테이블은 첫 번째 빈 줄 또는 다른 블록 수준 구조의 시작에서 나뉩니다.

예제 201
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
예 202
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
헤더 행 은 셀 수의 구분 기호 행 과 일치해야합니다 . 그렇지 않으면 테이블이 인식되지 않습니다.

예제 203
| abc | def |
| --- |
| bar |
 
<p>| abc | def |
| --- |
| bar |</p>
테이블 행의 나머지 부분은 셀 수에 따라 다를 수 있습니다. 헤더 행의 셀 수보다 적은 수의 셀이있는 경우 빈 셀이 삽입됩니다. 더 큰 경우 초과는 무시됩니다.

예 204
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
본문에 행이 없으면 <tbody> HTML 출력에 가 생성됩니다.

예 205
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
