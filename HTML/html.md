## HTML

HTML은 Hyper Text Markup Language의 줄임말

### 문서타입

- HTML의 기본 구조는 웹 문서를 작성할 때 반드시 들어가야 하는 기본적인 내용으로 크게는 문서 타입 정의와 <html>요소로 구분
- 문서 타입정의는 보통 DTD라 부름
- 문서 버젼을 알려주는 선언문, 반드시 최상단 선언되어야함.

## HTML 태그

- 태그는 HTML을 이루고 있는 구성 요소로서 많은 종류의 태그들이 존재
- 종류가 다양한 만큼 의미에 맞는 태그를 사용하여 브라우저가 잘 이해할 수 있도록 (시멘틱 마크업) 하는 것이 매우 중요합니다.
- HTML 버젼이 업그레이드 되면서 추가/삭제되기도 함, 현재 130개 정도 태그 존재

<b> : bold 태그는 글자를 굵게 표현
<i> : italic 태그는 글자를 기울여서 표현
<u> : underline 태그는 글자의 밑줄을 표현
<s> : strike 태그는 글자의 중간선을 표현 (예전에 존재했던 strike 태그와는 다른 태그로, strike 태그는 폐기되어 더는 사용 X.)
<a> : 앵커, a태그등 여러이름으로 불림. 링크 만들기 위해 반드시 href속성을 가지고 있어야함, 안에 같이 들어가는target은 어디에 리소스를 표시할지 정할때 씀

### div & span

div(division) 태그는 블록 레벨 태그.
블록 레벨 요소는 기본적으로 한 줄을 생성해서 내용을 표현
span은 인라인 레벨 태그, 블록레벨 요소의 한 줄에서 표현되는 요소.

<ul> : ul(unordered list) 태그는 순서가 없는 리스트를 표현할 때 사용
<ol> : ol(ordered list) 태그는 순서가 있는 리스트를 표현할 때 사용
<dl> : dl(definition/description list) 태그는 용어와 그에 대한 정의를 표현할 때 사용.
- <dl>은 용어와 설명이 하나의 세트로 항목을 이루고 하나 이상의 항목으로 리스트가 이루어지는 구조
* <dt> : 용어를 나타내는 태그
* <dd> : 용어에 대한 정의 또는 설명을 나타내는 태그

### table

<!-- 고생정말 많이한 애증의 ... -->

표는 셀(내용이 들어가는 하나의 칸)
표의 행(가로 방향)을 row, 열(세로 방향)을 column.

<table> : 표를 나타내는 태그
<tr> : 행을 나타내는 태그
<th> : 제목 셀을 나타내는 태그
<td> : 셀을 나타내는 태그

하나의 테이블은 하나 이상의 <tr>로 이루어져 있고, <tr>은 셀을 나타내는 <th>, <td>를 자식으로 가지게 됨
표 구성시 : 위 => 밑, 좌 => 우 작성

<caption>: 표의 제목을 나타내는 태그
<thead>: 제목 행을 그룹화하는 태그
<tfoot>: 바닥 행을 그룹화하는 태그
<tbody>: 본문 행을 그룹화하는 태그

### textarea

<textarea>에는 텍스트 상자의 크기를 조절하는 rows, cols 이 있음.

cols : 가로 크기를 조절하는 속성(한 줄에 들어가는 글자의 수, 수치의 의미는 평균적인 글자의 너비로 정확히 글자 수X.)
rows : 세로 크기를 조절하는 속성(화면에 보여지는 줄 수)

## 콘텐츠 모델

HTML5에는 요소들이 가지고 있는 성격에 따라 요소의 종류를 정의하는 규칙이 있음.
요소는 규칙 준수를 해야하며, 반드시 권고안을 따라야함
비슷한 성격의 모델들끼리 모은것이 콘텐츠 모델

### 7가지 분류

1. Metadata Content
2. Flow Content
3. Sectioning Content
4. Heading Content
5. Phrasing Content
6. Embedded Content
7. Interacitve Content

### Meta data

" base, link, meta, noscript, script, style, title "

Metadata에는 스타일, 동작을 설정하거나 다른 문서와의 관계 등 정보를 포함하는 요소들이 포함
메타 태그, 타이틀 태그, 스타일 태그, 링크 태그가 이에 해당, 대부분 <head>내에 들어간다는 것이 특징

### Flow

" a, abbr, address,map>area, article, aside,audio, b, bdo, blockquote,br, button,
canvas, cite, code, datalist, del, details, dfn, div, dl, em, embed,
fieldset, figure, footer, form, h1 ~ h6, header, hgroup, hr, i, iframe, img,
input, ins, kbd, keygen, label, map, mark, math, menu, meter, nav, noscript, object, ol,
output, p, pre, progress, q, ruby, samp, script, section, select, small, span, strong,
style[scoped], sub, sup, svg, table, textarea, time, ul, var, video, wbr "

문서의 자연스러운 흐름에 의해 배치되는 요소들.
Metadata에 해당하는 일부 태그들만 Flow에서 제외되며 요소 대부분이 Flow에 포함

### Sectioning

" article, aside, nav, section "

Sectioning에는 문서의 구조와 관련된 요소들이 포함.

HTML5에서 새로 생긴 <article>, <aside>, <nav>, <section> 등이 포함되며 이 태그들은 문서의 구조, 아웃라인에 영향.

### Heading

" h1, h2, h3, h4, h5, h6 "

Heading에는 각 section의 header를 정의하는 heading 태그가 포함

### Phrasing

"a, abbr, map>area, audio, b, bdo, br, button, canvas, cite, code, datalist, del, dfn, em, embed,
i, iframe, img, input, ins, kbd, keygen, label, map, mark, math, meter, noscript, object, output,
progress, q, ruby, samp, script, select, small, span, strong, sub, sup, svg, textarea, time,
var, video, wbr"

Phrasing에는 문서의 텍스트 또는 텍스트를 꾸며주는 문단 내부 레벨로 사용되는 요소들이 포함

### Embedded

" audio, canvas, embed, iframe, img, math, object, svg, video "

Embedded에는 외부 콘텐츠를 표현하는 요소들이 포함되며 오디오나 비디오, 이미지 등 멀티미디어 관련 요소들이 이에 해당

### Interactive

" a, audio[controls], button, details, embed, iframe, img[usemap], input, keygen, label, menu,
object[usemap], select, textarea, video[controls] "

Interactive에는 사용자와 상호작용을 하는 요소들이 포함되며 대표적으로 form 요소들이 이에 해당
