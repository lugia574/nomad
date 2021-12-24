## MediaQuery

```css
div {
  background-color: teal;
  width: 100px;
  height: 100px;
}

@media screen and (max-width: 600px) {
  div {
    backgrond-color: tomato;
  }
}
```

이렇게 하면 width 600 이하는 div 백그라운드 컬러를 토마토로 바꿔라

```css
@media screen and (min-width: 600px) and (max-width: 750px) {
  div {
    backgrond-color: blue;
  }
}
```

이러면 600~ 750 사이 div 백그라운드 컬러 블루

```css
span {
  font-size: 36px;
}
@media screen and (orientation: landscape) {
  span {
    display: none;
  }
}
```

이러면 화면을 landscape(가로)로 바꾸면 span 태그가 안보이게 됨

Media Queries 주요기능

- min-device-width
- max-device-width
- orientation: landscape
- orientation: portrait
- aspect-ration - 레티나디스플레이 감지가능
- display-mode
- inverted-colors
- lightlevel
- prefers-contrast
- resolution
- monochrome

Media type

- @media screen{}
- @media print{}
