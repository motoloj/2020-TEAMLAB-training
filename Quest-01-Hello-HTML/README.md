# 2020-TEAMLAB-training
# Quest 01. Hello, HTML


## Introduction
* HTML은 HyperText Markup Language의 약자로, 웹 브라우저에 내용을 표시하기 위한 가장 기본적인 언어입니다. 이번 퀘스트를 통해 HTML에 관한 기초적인 사항들을 알아볼 예정입니다.

## Topics
* 브라우저의 역사
  * Mosaic
  * Netscape
  * Internet Explorer
  * Firefox
  * Chrome
  * Safari (for iOS)
  * Edge
  
* HTML 표준의 역사
  * HTML 4.01
  * XHTML 1.0, XHTML 1.1
  * XHTML 2.0
  * HTML5
    * HTML 5.3
    
* HTML 문서의 구조
* HTML 문서의 엘리먼트
  * Semantic elements
  * Block-level elements vs Inline elements

## Resources
* [MDN - HTML](https://developer.mozilla.org/ko/docs/Web/HTML)
* [모던 웹 디자인을 위한 HTML5+CSS3 입문](http://www.yes24.com/24/Goods/15683538?Acode=101), 한빛미디어
* [웹 디자인 2.0 고급 CSS](http://www.yes24.com/24/Goods/2808075?Acode=101), 에이콘출판사
* [StatCounter Global Stats](http://gs.statcounter.com/)

## Quest
* [이 그림](github.png)은 github의 웹사이트 레이아웃입니다. 이 레이아웃의 정보를 HTML 문서로 표현해 보세요.
* CSS를 전혀 사용하지 않고, 문서의 구조가 어떻게 되어 있는지를 파악하여 구현해 보세요.
  * [CSS Naked Day](http://meiert.com/en/blog/20150319/css-naked-day/)는 매년 4월 9일에 CSS 없는 웹 페이지를 공개하여 내용과 마크업에 집중한 HTML 구조의 중요성을 강조하는 행사입니다.
* 폴더에 있는 `skeleton.html` 파일을 바탕으로 작업해 보시면 됩니다.

# Checklist
## Question 1) HTML 4.x 이후의 HTML 표준의 변천사는 어떻게 되나요?

 <br/>
 
 1991년부터 1998년까지, HTML은 버전 1에서 버전 4로 발전했으며 4버전부터 멀티미디어와 스타일시트를 지원하기 시작했습니다.<br/>
 2000년에는 월드 와이드 웹 컨소시엄(W2C)에서 XHTML 1.0이 등장했습니다. <br/>2008년에 최초의 HTML5공개 초안이 발표되었고 XHTML의 개발이 중단되었습니다. <br/>
 
 < XHTML, HTML5 >
 XHTML: Extensible Hypertext Markup Language
 - XML의 응용이다.
- XHTML과 HTML은 분리된 표준이다.
- XHTML은 조금 더 엄격한 기준의 HTML이라고도 볼 수 있는데, 전통 컴퓨터를 벗어난 이동 기기에서 부정확한 HTML을 지원하는데 필요한 자원이 부족하기 때문에 엄격한 버전의 HTML의 필요성이 대두되었다.
- XHTML 1.0: HTML 4.01을 XML로 다시 규정한 것이다.
- XHTML 1.1: 모듈 기반의 XHTML이다.
- XHTML과 HTML을 적절히 합친 듯한 HTML5가 등장했다.
- XML에서 JSON으로 데이터 포멧의 주도권이 넘어가게 되었다.

HTML5
- HTML5는 WorldWideWeb의 콘텐츠를 구조화하고 표현하는 데 사용되는 마크업 언어이며, HTML표준의 다섯번째이자 현재 버전입니다.
- HTML 4.01, XHTML 1.0, DOM 레벨 2 HTML에 대한 차기 표준 제안이다.
- 비디오, 오디오 등의 부가기능과 최신 멀티미디어 콘텐츠를 액티브x 없이 브라우저에서 쉽게 볼 수 있게 하는 것을 목적으로 한다.


HTML 4.01 이전에는 CSS는 HTML 안에 embedded된 형식이었다. 그렇기 때문에 여러 개의 페이지가 있으면 각각의 페이지마다 CSS를 모두 입력해주어야 했고, 반복된 CSS도 굉장히 많았다.
<br/>
HTML 4.01 이후로는 외부의 스타일 시트가 도입되었다.파일 형태로 스타일 시트를 작성하고, HTML 안에 삽입하는 방식이다.
<br/>
html의 새로운 요소는 다음과 같습니다.
1. 새로운 의미론적 요소들 :  header , footer , article , section
2. 번호, 날짜, 시간, 일정 및 범위 같은 새로운 속성이 생겼습니다.
3. 새로운 그래픽 요소 : svg 와 canvas .
4. 새로운 멀티미디어 요소 : audio 및 video .

HTML5는 input, geolocation을 나타내는 등의 많은 양의 새로운 HTML Tags를 도입했다.

*예시<br/>
 * Email: form tag 밖에서도 사용이 가능하며, email 타입에 사용되며 validation check가 되는 tag이다.<br/>
 * Password: form tag의 한 종류로 비밀번호를 입력에 사용되는 tag이다. 사용자에게 입력한 내용이 직접적으로 보여지지 않고 다른 형태의 이미지가 보이게 된다.<br/>
 * Audio: 웹페이지에서 오디오를 삽입할 때 사용할 수 있는 태그이다.<br/>
 * Semantic: HTML에서 구조를 표현할 때 사용할 수 있는 tag이다.예를 들어 header, footer와 같은 것들이 있다.<br/>
 * Section: HTML 문서의 구조를 표현할 때 사용할 수 있는 tag의 한 종류이고, 웹페이지의 구역을 나타낼 때 사용된다.<br/>
  
<html, Xhtml, html 5 요약비교표><br/>
|구분|HTML|XHTML|HTML5|
|---------|-----------------|----------------------|---------------------|
|특징|- SGML 기반의 마크업 언어<br/>  - 문법이 엄격하지 않음<br/>  - 시스템이나 운영체제에 독립적<br/>  - 확장성 부족함<br/> |- XML 기반의 마크업 언어<br/>  - HTML4.01과 유사한 사용법<br/>  - 반드시 XHTML 문법을 지켜야 함<br/>  - CSS와 HTML의 분리로 유지보수 용이<br/> - 경량의 로딩속도|- 시맨틱 마크업 언어<br/>  - 문법이 엄격하지 않음<br/>  - 편리한 웹폼 기능 등의 기능 제공<br/>  - 웹어플리케이션 작성이 용이<br/>  → CSS & JavaScrript<br/>  - 오디오·비디오·그래픽 처리,<br/> 위치정보 제공 등 다양한 기능 제공)|
|등장배경|문서를 구조적으로 표현하기 위한 마크업언어에서 파생|HTML의 표현 제한사항<br/> → 각종 미디어파일, 다양한 브라우저 등에 대한 사용자 요구에 의해 등장|HTML에 익숙해진 사용자들을 위해  XHTML보다 <br/>HTML을 발전시키는 방식을  채택 (WHATWG에서 규격 만듦)
|"(DOCTYPE)  선언"|(!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/dtdtype.dtd") |(!DOCTYPE HTML PUBLIC "-//W3C//DTD XHTML 1.0//EN" "http://www.w3.org/TR/xhtml1-dtdtype.dtd")|(!DOCTYPE html)|


## Question 2) MS와 IE는 왜 역사에 오점을 남기게 되었을까요?<br/>

- MS는 IE6 당시에 높은 시장 점유율을 가진 독점시장 상태로 기능 개발을 중단하고 <br/>
 개발팀을 해체했었습니다.<br/>
- 파이어폭스의 점유율이 증가하자 다시 개발팀을 소집했었으나 <br/>
 아래와 같은 이유로 점유율을 잃어가고 결국 IE는 역사의 뒤안길로 사라져가고 있습니다.

 - IE는 크롬과 비교해서 속도, 기능, 디자인 등에서 꽤 많은 차이가 난다. <br/>
 하지만 가장 큰 차이점은 보안과 관련한 이슈이다.
 - 릴리즈 주기가 매우 길어서 최신 웹 표준의 지원과 버그 수정이 굉장히 느립니다.<br/>
 IE는 메모리의 개체에 부적절하게 엑세스될 경우, 원격 코드 실행 취약점이 존재하고 <br/>
 이 취약점으로 인해 메모리가 손상되면 해커들은 악성 코드를 실행시킬 수 있다.

 - IE의 취약한 보안에 대해서는 MS도 인정했지만 이 문제를 고치거나 패치할 수 없다고 합니다.
 그래서 MS는 Internet Explorer의 사용 중지를 권장하고, Microsoft Edge를 내놓았다.

 ## Question 3) `<section>`과 `<div>`, `<header>`, `<footer>`, `<article>` 엘리먼트의 차이점은 무엇인가요?<br/>
 
 1. section은 독립적인 구역을 표현할 때 사용된다.

 2. header는 제목과 같은 내용을 담을 때 사용된다. 소개하거나 네비게이션의 역할에 사용되기도 하며, 로고, 검색창 등을 사용할 때도 쓰인다.

 3. div는 division, 컨텐츠의 구획을 구분할 때 사용된다. 기본적으로 적합한 sematice tag가 없을 때, 사용된다.

 4. footer는 보통 페이지의 맨 밑에 있는 구역에 사용되는 태그이다. copyright나 링크, 관련 문서와 같은 각 페이지의 공통된 정보들을 담는데 활용된다.

 5. article은 자체적으로 구성이 되어있는 콘텐츠 덩어리를 묶을 때 사용된다. 독립적으로 존재할 수 있어야 하며 재사용될 수 있다.
 
 
## Question 4) 블럭 레벨 엘리먼트와 인라인 엘리먼트의 차이는 무엇일까요?<br/>
 
 
 * 화면 전체를 사용하는 태그 => block element<br/>
 * 화면의 일부를 차지하는 태그 => inline level element<br/>
 
- 블록 레벨 엘리먼트: 기본적으로 부모 엘리먼트의 가로 길이에 맞춰 최대 가로 길이를 가지며, 항상 새로운 줄을 차지한다. 그래서 하나의 블록을 형성한다.
 1. 새로운 줄에서 시작합니다.
 2. 좌우 양쪽으로 최대한 늘어나 가능한 모든 너비를 차지합니다.
 3. 다른 블록 레벨 요소와 인라인 요소들을 포함할 수 있습니다.
 4. 블록 레벨 요소 자체를 text-align을 활용해 가운데 정렬할 수 없습니다.
 5. 블록 레벨 요소 자체를 Vertical-align을 활용해 수직 정렬할 수 없습니다.
 
  ex) p, h1~h6, ul, ol, pre, dl, div, noscript, blockquote, form, hr, table, fieldset, address<br/>
  
- 인라인 엘리먼트: 태그 안에 있는 콘텐츠의 크기만큼의 구획을 가진다. 블록 레벨 엘리먼트가 항상 새로운 줄을 차지한다면, 인라인 엘리먼트는 그렇지 않다.
 1. 새로운 줄을 만들지 않습니다.
 2. 필요한 너비만 차지합니다.
 3. 다른 인라인 요소를 포함할 수 있습니다. ( 인라인 요소가 블록 레벨 요소를 포함하는 건 웹 표준에 어긋납니다 )
 4. height가 적용되지 않습니다.
 5. width가 적용되지 않습니다
 
 ex) samp, kbd, var, cite, abbr, acronym, a, img, object, br, scrip, map, q, sub, sup, span, bdo, input, select, textarea, label, button
  
 기타 다른 차이점은, block-level element는 inline-level element를 포함할 수 있지만 반대의 경우는 불가능합니다.
 추가로 블록 레벨과 인라인 요소의 분류는 HTML 명세 4.01까지 사용됐습니다. 이런 이진적 구분은 HTML5부터 보다 복잡한 콘텐츠 카테고리 집합으로 대체됐습니다. 
 "인라인" 카테고리는 구문 콘텐츠와 적당히 짝지을 수 있지만 "블록 레벨" 카테고리는 어느 HTML5 콘텐츠 카테고리와도 정확히 일치하지 않습니다. 
 그러나 블록 레벨과 인라인 요소를 조합하면 플로우 콘텐츠에 대응합니다. 대화형 콘텐츠 등 추가 카테고리도 존재합니다.
