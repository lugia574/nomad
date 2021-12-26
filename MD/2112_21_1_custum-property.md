1.  :: placeholder (0:46)

         placeholder의 특성만 바꾸고 싶을 때 사용합니다.

2.  :: selection (1:31)

        클릭해서 긁을 때(1:58) 발생합니다.

3.  :: first-letter

         첫 글자에만 적용됩니다.

4.  ::first-line

        첫 줄에만 작용합니다.

### 17 States 복습 내용

1.  active

         클릭할 때 작동 (예: 버튼 클릭 시 색깔 변함)

2.  hover

         마우스 커서를 올려놓으면 작동 (예: 글자 위에 마우스 커서 올려두면 색상 변함)

3.  focus

         element가 focused된 상태. 3:50 보시면 키보드 탭 버튼으로 이동하면서 생기는 그 모양을 보시면 될 것 같아요.

4.  visited

        방문한 사이트와 관련하여 일어납니다. (예: 애플 링크 눌러서 방문했는데, 다시 보니 해당 링크 색상이 빨강색으로 바뀌어 있음)

5.  focus-within

        focus되는 children이 있으면 작동. mozilla에서 가져온 예시를 들어보겠습니다.

    div: focus-within {background-color: cyan}이면, div의 children이 focus 될 때 {}가 작동합니다.

- form: hover input: focus{} 의 경우엔 두 조건 모두 만족해야 {} 안이 실행됩니다.

## :root

    custum property 변수화

색상같이 여러 태그에 적용하는 것들을 변수 선언해서 관리 하기

```css
:root: {
  --main-color: #489ee3;
}

p {
  background-color: var(--main=color);
}
```
