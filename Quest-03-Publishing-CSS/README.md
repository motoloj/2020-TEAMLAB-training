# Quest 03. Publishing CSS


## Introduction
* 이번 퀘스트에서는 CSS를 이용해 실제 웹 페이지를 모사해 퍼블리싱하는 것에 도전해볼 예정입니다.

## Topics
* 퍼블리싱을 위해 몇 가지 중요한 속성들
  * `font-*`
  * `text-*`
  * `box-sizing`
  * `:hover`/`:active`

## Resources
* [MDN - CSS](https://developer.mozilla.org/ko/docs/Web/CSS)
* [모던 웹 디자인을 위한 HTML5+CSS3 입문](http://www.yes24.com/24/Goods/15683538?Acode=101), 한빛미디어
* [웹 디자인 2.0 고급 CSS](http://www.yes24.com/24/Goods/2808075?Acode=101), 에이콘출판사
* [Centering in CSS: A Complete Guide](https://css-tricks.com/centering-css-complete-guide/)
* [A complete guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## Checklist
* CSS 퍼블리싱을 할 때, class와 selector들은 어떤 식으로 정리하는 것이 좋을까요?<br>
Answer)
1. 한 페이지 내에서 여러 번 반복될 필요가 있는 스타일은 클래스 선택자를 사용하고, 단 한번 유일하게 적용될 스타일은 ID선택자를 사용하는 것이 좋습니다. 이는 다음과 같은 두 속성의 차이 때문입니다.

2. class속성은 어떤 분류 안에 포함된 요소의 특성을 정의하는 데 사용됩니다.
id속성은 어떤 요소에 대해 유일한 특성을 정의합니다. (HTML 문서에서 특정 id속성값은 오직 하나만 있어야 합니다.)
클래스 선택자는 글자색이나 글자 굵기 등 나중에 다른 곳에도 적용할 수 있는 스타일을 지정하고, ID선택자는 웹 문서 안에서 요소의 배치 방법을 지정할 때 자주 사용합니다.

3. class 속성은 속성값을 두 개 이상 가질 수 있습니다. 그래서 클래스 선택자를 사용하면 한 태그 내에서도 여러종류의 스타일 규칙을 적용할 수 있습니다.

4. ID선택자의 우선순위가 클래스 선택자의 우선순위보다 높습니다. 우선으로 적용되어야 할 스타일을 ID선택자를 사용하여 정의하는 것이 좋습니다.

## Quest
* Quest 01에서 만들었던 HTML을 바탕으로, [이 그림](github.png)의 레이아웃과 CSS를 최대한 비슷하게 흉내내 보세요. 꼭 완벽히 정확할 필요는 없으나 align 등의 속성은 일치해야 합니다.
* **주의사항: 되도록이면 원래 페이지의 CSS를 참고하지 말고 아무것도 없는 백지에서 시작해 보도록 노력해 보세요!**
* 등장하는 아이콘은 GitHub에서 만든 [Octicons](https://octicons.github.com/) 그림 파일입니다. 해당 폰트 파일은 링크를 참조하여 쓰시면 됩니다.

* ttf의 아이콘을 유니코드로 출력시키는 방법:
아래와 같은 코드를 css에서 작성
* 유니코드 참조:https://www.dafontfree.net/freefonts-octicons-f145163.htm

(1)`@font-face{
    font-family: 'octicons';
    src: url(octicons.ttf) format('truetype');
    
}`

(2)`[data-icon]:before{
    font-family: octicons;
    content: attr(data-icon);`
1. 외부 폰트를 읽기위한 코드(1)
2. 코드(2) = 외부 폰트의 유니코드를 아이콘(content)로 출력
3. html에 해당 원하는 유니코드 확인 후 (10진법이면 data-icon="&#10진법", 16진법이면 data-icon="\16진법"를 추가) img 태그를 제외한 태그 인라인에 작성가능<br>
