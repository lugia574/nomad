###시간과 말풍선 위치를 바꾸는 방법

    같은 요소가 반복될 때, 간단한 수정만으로 추가하기 위해서는
    class를 하나 더 추가해서 css에 적어준다.
    flex children에는 order 기능이 있다.
    display방식을 바꿀 수 있음.

1.  .message-row--own .message**time {
    order: 0;
    margin-right: 5px;
    }
    .message-row--own .message**bubble {
    order: 1;
    margin-right: 0px;
    }

flex children에게 사용할 수 있다. 자식 수가 많으면 어렵다.

    하나는 order : 0, 1, 2 ... 와 같이 순서를 정해주는 방식이다.
    하지만, flex children이 많아지면 코드를 많이 써야한다.

2.  간단하고 쿨한방법
    .message-row--own .message\_\_info {
    flex-direction: row-reverse;
    }

         두 번째 방식은 flex-direction : row-reverse를 이용해 반전시키는 방법이다.

### forwards

display:none;(눈에보이는화면만 없앰)

visibility:hidden;(기능까지 숨김, 마우스클릭 가능)

만약 없애고 싶다면 Javascript(뇌) 필요. html로는 무시(골격)정도만 가능.

animation-delay: #s

    will-change는 애니메이션이 좀 더 부드럽게 동작할 수 있게 한다. → 브라우저에게 어떤 것이 변할 것인지 예고해주는 것


    will-change는 그래픽 카드를 이용해서 애니메이션을 가속화 한다.

뭐냐 왜 바꾼게 깃헙 io 에는 반영이 안되냐
