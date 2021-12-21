## Transformations

    한 요소를 말 그대로 변형시킬수 있음

transformation은 box element를 변형시키지 않는다.
즉, 옆에 sibling들에게 영향을 끼치지 않는다.
margin, padding이 적용되지 않는다.
일종의 3D transformation이기 때문이다.

margin이나 padding을 주기위해서 tarnslateX, trnasLateY 를 사용하는것이 아니다!

다른 요소의 box를 변형시키지 않고 원하는 요소를 이동시키기 위해서 사용하는 것이다.

trransformation 은 페이지의 픽셀의 다른 부분에서 일어난다.
transformatino은 box차원에서 일어나지 않는다.
tronsformation 을 결합 가능하다!

CSS의 3D는 GPU로 돌아간다 즉 3D작업을 할 수 있다
transformation 은 이것 역시 엄청나게 많은 document가 있다 확인해서 combine할 수 있다

transition 과 transformation 을 합친다면 아름다운 애니매이션을 만들 수 있다

```css
img {
  width: 300px;
  height: 550px;
  border: 10px solid black;
  border-radius: 50%;
  transition: transform 1s ease-in-out;
}
img:hover {
  transform: rotateY(520deg) scale(0.5);
}
```

##
