## Transitions

    어떤 상태에서 다른 상태로의 변화! 를 보내주는 애니매이션이다

1.  transtion은 state가 없는 요소에 붙어야한다

        처음 생긴곳에 있어야한다
        state에 transition을 준다면 변화를 준것(예를들면 hover라면 마우스를 갖다 댄것)을 그만할경우(마우스를 뗄경우)
        원래상태로 바로 돌아간다

2.  transtion 에 변화를 준것들은 state에 들어있는것들이 기준이 되어 바뀌는것이다
    바뀌는 것들에 한정하여 transition 이 일어날 수 있다

ease-in function : 브라우저에게 변화하는 방법을 알려주는 역할

- linear - 변화 그래프가 직선
- ease-in - 시작과 끝이 빠름
- ease-out - 시작과 끝이 느림
- ease-in-out - 시작이 빠르고 끝이 느림

all : 변화 요소를 한번에 다룬다.

- 따로 다루고 싶으면 각각 써주면 됨

cubic-bezier(0, 0, 0, 0); 으로 직접 설정할수도 있다.

이런식으로 할 수 있음

```css
a {
  color: wheat;
  background-color: tomato;
  border-radius: 5px;
  transition: color 1s cubic-bezier(0.6, 0, 0.735, 0.045), border-radius 5s
      ease-in-out, background-color 10s ease-out;
}
```
