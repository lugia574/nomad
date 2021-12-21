## Animations

### conin flip

1.  from to 방법

    @keyframes 애니메이션 이름 {
    from{

        }
        to {

        }

    }

    사용하기
    img {
    animation : 애니메이션 이름 재생시간 옵션
    }
    무한으로 반복되게 하려면 뒤에 infinite를 붙여준다.

```css
@keyframes sexyboom {
  from {
    transform: rotateX(0);
  }
  to {
    transform: rotateX(360deg) translateX(100px);
  }
}
img {
  width: 300px;
  height: 550px;
  border: 10px solid black;
  border-radius: 50%;
  animation: sexyboom 5s ease-in-out infinite;
}
```

이렇게 하면

to 의 translateX(100px) 때문에

x축으로 100px만큼 갔다가 바로 끊기고

0px 에서 다시 시작해서 어색함

2. % 방법

```css
@keyframes sexyboom {
  0% {
    transform: rotateX(0);
  }
  50% {
    transform: rotateX(360deg) translateX(100px);
  }
  100% {
    transform: rotateX(0);
  }
}
img {
  width: 300px;
  height: 550px;
  border: 10px solid black;
  border-radius: 50%;
  animation: sexyboom 5s ease-in-out infinite;
}
```
