# Quest 02. Hello, CSS


## Introduction
* CSS는 Cascading StyleSheet의 약자입니다. 웹브라우저에 표시되는 HTML 문서의 스타일을 지정하는 (거의) 유일하지만 다루기 쉽지 않은 언어입니다. 이번 퀘스트를 통해 CSS의 기초적인 레이아웃 작성법을 알아볼 예정입니다.

## Topics
* CSS 기초 문법
* CSS를 HTML에 적용하는 세 가지 방법
  * Inline Style
  * `<style>`
  * `<link rel="stylesheet" href="...">`
* 레이아웃을 위해 몇 가지 중요한 속성들
  * `position`
  * `left`/`top`
  * `display`
  * `width`/`height`
  * `display: flex;`
  * `display: grid;`
  * CSS Box Model
* 브라우저별 Developer tools

## Resources
* [MDN - CSS](https://developer.mozilla.org/ko/docs/Web/CSS)
* [모던 웹 디자인을 위한 HTML5+CSS3 입문](http://www.yes24.com/24/Goods/15683538?Acode=101), 한빛미디어
* [웹 디자인 2.0 고급 CSS](http://www.yes24.com/24/Goods/2808075?Acode=101), 에이콘출판사
* [Centering in CSS: A Complete Guide](https://css-tricks.com/centering-css-complete-guide/)
* [A complete guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
* [그리드 레이아웃과 다른 레이아웃 방법과의 관계](https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Grid_Layout/%EA%B7%B8%EB%A6%AC%EB%93%9C_%EB%A0%88%EC%9D%B4%EC%95%84%EC%9B%83%EA%B3%BC_%EB%8B%A4%EB%A5%B8_%EB%A0%88%EC%9D%B4%EC%95%84%EC%9B%83_%EB%B0%A9%EB%B2%95%EA%B3%BC%EC%9D%98_%EA%B4%80%EA%B3%84)

## Quest
* 아래의 그림들은 모두 전체적으로 창의 크기에 꽉 차야 하며, 창의 크기가 일정 크기 이상일 경우 전체 창 크기가 어떻게 바뀌되더라도 그림에 맞게 각 박스의 크기가 조절되어야 합니다.
* **주의사항**
  * HTML 파일은 수정하면 안됩니다.
  * `float` 속성과 `calc()`함수를 사용하지 않고 해 보세요!
* [이 그림](layout1.png)을 flexbox를 쓰지 않고 구현해 보세요. [`skeletons/layout1.html`](skeletons/layout1.html) 파일에 링크된 [`skeletons/layout1.css`](skeletons/layout1.css)파일을 수정하면 됩니다.
* [이 그림](layout2.png)을 flexbox를 쓰지 않고 구현해 보세요. [`skeletons/layout2.html`](skeletons/layout2.html)  파일에 링크된 [`skeletons/layout2.css`](skeletons/layout2.css) 파일을 수정하면 됩니다.
* [이 그림](layout3.png)을 flexbox를 쓰지 않고 구현해 보세요. [`skeletons/layout3.html`](skeletons/layout3.html)  파일에 링크된 [`skeletons/layout3.css`](skeletons/layout3.css) 파일을 수정하면 됩니다.
* 위와 같은 그림을 flexbox를 써서 구현해 보세요. [`skeletons/layout4.html`](skeletons/layout4.html)  파일에 링크된 [`skeletons/layout4.css`](skeletons/layout4.css) 파일을 수정하면 됩니다.

## Checklist
* Question 1) CSS를 HTML에 적용하는 세 가지 방법의 장단점은 무엇인가요?
  1. inline style
    * 장점: inline과 다르게 내용과 스타일이 분리되어 있기 때문에 어느정도 재사용이 가능하고 일괄 변경, 적용 등이 가능
    * 단점: 한 개의 HTML 문서 안에서는 재사용이 가능하지만 다른 HTML 문서에는 적용시킬 수 없다. 즉, 문서마다 작성해야 하기 때문에 문서가 많아질 수록 비효율적이다.
  2. `<style>`
    * 장점: inline과 다르게 내용과 스타일이 분리되어 있기 때문에 어느정도 재사용이 가능하고 일괄 변경, 적용 등이 가능하다.
    * 단점: 한 개의 HTML 문서 안에선는 재사용이 가능하지만 다른 HTML 문서에는 적용시킬 수 없다. 즉, 문서마다 작성해야 하기 때문에 문서가 많아질 수록 비효율적이다.
  3. `<link rel="stylesheet" href="...">`
    * 장점: 하나의 스타일 시트만 만들어놓아도 여러 개의 HTML 문서에 적용시킬 수 있다.
    * 단점: 독립적인 스타일 시트 파일이기 때문에 작업을 계속하면서 지속적으로 유지, 보수를 해야 하며 규모가 커질 수록 복잡해질 가능성이 있다.

`<style>`과 `<link rel="stylesheet" href="...">`의 장, 단점을 모두 사용할 수는 없을까. `<link>`를 사용하게 되면 재사용성은 매우 높아질 수 있지만 결국 네트워크를 활용하기 때문에 그만큼의 성능 상 문제가 생길 여지가 있다. 그러나 `<style>`의 경우, 재사용성의 측면에서 매우 비효율적이다. 사실 그렇기 때문에 webpack이라는 것을 사용한다고 볼 수 있다. 굳이 css만 한정된 이야기는 아니다. 코드의 재사용성은 극대화하하면서도 모든 코드를 한 개의 문서로 통합하면서 네트워크 사용을 최소화한다. 

* Question 2) 여러 개의 CSS 규칙이 한 개의 대상에 적용될 때, 어떤 규칙이 우선순위를 가지게 되나요?
  * 각각의 CSS 적용 방식에는 점수가 있어서 그 점수가 높은 순서대로 우선 순위를 가지게 된다.
    * Inline Style: 1000점
    * ID:           100점
    * Class:        10점
    * 속성선택자:      10점
    * 가상클래스속성:   10점
    * 태그선택자:      1점
    * 전체선택(/*):   0점
  
 ` <div id="foo" class="foo1 foo2 foo3 ... foo20">안녕</div>`

  #foo {
   color: blue;
   }

   .foo1.foo2.foo3.....foo20 {
   color: red;
   }

  위와 같은 코드가 있다고 가정해보자. 위의 `div`의 "안녕"은 빨간색이 될까, 파란색이 될까.
점수 상으로는 빨간색이 되어야 맞다. 그러나 정답은 파란색.
점수는 개념 상의 설명을 위한 것이고, 실제로 하위 우선 순위의 점수가 높아도 상위 우선 순위의 이상으로 갈 수는 없다.

* Question 3) 어떤 박스가 `position: absolute;`인 속성을 갖는다면, 그 위치의 기준점은 어디가 되나요?
  * position 속성은 웹 문서 안 요소들을 어떻게 배치할 지를 정하는 속성입니다. position 속성을 이용하면 텍스트나 이미지를 원하는 위치로 배치할 수 있고 어떤 방식으로 놓을 지를 결정할 수 있습니다.
  |-------|---------------------|
  |static|요소를 문서 흐름에 맞추어 배치.|
  |relative|이전 요소(주로 부모 요소)에 자연스럽게 연결하여 위치를 지정.|
  |absolute|원하는 위치를 지정해 배치. |
  |fixed|지정한 위치에 고정하여 배치.|
  |sticky|위치에 따라서 동작방식이 달라짐. 요소가 임계점(scroll 박스 기준) 이전에는 relative와 같이 동작. 그 이후에는 fixed와 같이 동작.|

  * .parent 선택자에 position:absolute 없는 경우 : 브라우저 창 기준.
  * .parent 선택자에 position:absolute 있는 경우 : 부모 요소 기준.
  * `position: absolute` 는 이름과 같이 절대적인 위치에 둘 수 있습니다.
   어떤 기준으로 절대적이냐 하면, 특정 부모에 대해 절대적으로 움직이게 됩니다. 부모 중에 position이 relative, fixed, absolute 하나라도 있으면 
   그 부모에 대해 절대적으로 움직이게 됩니다. 일반적으로 absolute를 쓸 경우, 절대적으로 움직이고 싶은 부모에게 position: relative; 를 부여하면 됩니다.

  * 만일 부모가 static인 경우, document body를 기준으로 하여 좌표 프로퍼티대로 위치하게 됩니다. 따라서 부모 요소를 배치의 기준으로 삼기 위해서는 
    부모 요소에 relative를 정의하여야 합니다.
    이때 다른 요소가 먼저 위치를 점유하고 있어도 뒤로 밀리지 않고 덮어쓰게 됩니다. (참고: 이런 특성을 부유 또는 부유 객체라 합니다.)
    `absolute 선언 시, block 레벨 요소의 width는 inline 요소와 같이 content에 맞게 변화되므로 적절한 width를 지정하여야 합니다.`
  * `position: relative`와 `position:absolute`의 차이점을 좀 더 구체적으로 살펴보겠습니다.

    `relative`는 기본 위치(static으로 지정되었을 때의 위치)를 기준으로 좌표 프로퍼티(top, bottom, left, right)를 사용하여 위치를 이동시킵니다. 
    따라서 무조건 부모를 기준으로 위치하게 됩니다.

     `absolute`는 부모에 static 이외의 position 프로퍼티가 지정되어 있을 경우에만 부모를 기준으로 위치하게 됩니다. 만일 부모, 조상이 모두 static인 
     경우, document body를 기준으로 위치하게 됩니다.
     따라서 absolute 프로퍼티 요소는 부모 요소의 영역을 벗어나 자유롭게 어디든지 위치할 수 있습니다.

* Question 4) 가로나 세로로 여러 개의 박스가 공간을 채우되, 그 중 한 개의 박스만 가변적인 크기를 가지고 나머지 박스는 고정된 크기를 갖게 하려면 어떻게 해야 할까요?
   * `position.absolute`를 사용한다.
	
* Question 5) `float` 속성은 왜 좋지 않을까요?
  1. 기본적으로 이미지 정렬을 위해 등장한 CSS 스타일이지만 레이아웃 정렬에도 많이 사용했다. 그렇기 때문에 불편한 사항들이 있다.
  2. `overflow: visible`인 경우, 부모 요소의 크기가 자동으로 늘어나지 않는다. (position: absolute와 비슷하게 렌더링) 
  3. `float`속성은 `clear`하지 않는 이상 계속해서 상속이 된다.

 화면의 플로우와 코드의 플로우는 가능하면 동일한 것이 좋다. 하지만 `float`를 쓴다는 것은 화면에서 띄워 애초에 플로우를 무시해버린다. 물론 역량에 따라 플로우 맞게 짤 수는 있다.

* Question 6) Flexbox(Flexible box)와 CSS Grid의 차이와 장단점은 무엇일까요?
  Flexbox: flexbox는 기본적으로 1차원 레이아웃을 위해 만들어졌다. Row or Column.

    * 장점: 모든 방향으로 정렬이 가능하고, reverse도 가능하다. Container로 사용할 경우, 하위 item들을 정렬하기가 매우 수월하다.
    * 단점: 퍼포먼스 이슈가 있다.

   Grid: grid는 2차원 레이아웃을 위해 만들어졌다. Row and Column

    * 장점: prototyping할 때 매우 쉽고 효율적으로 간단하게 작성하여 2차원의 레이아웃을 관리할 수 있다.
    * 단점: 모든 브라우저에서 지원하는 것이 아니다.

차이점: flexbox는 행과 열을 매우 효율적으로 정렬하고 구성할 수 있기 때문에 비교적 작은 단위의 레이아웃에 적합하고, grid는 2차원의 레이아웃을 효율적으로 정렬할 수 있으므로 조금 더 큰 단위의 레이아웃을 구성할 때 사용하면 좋다.
