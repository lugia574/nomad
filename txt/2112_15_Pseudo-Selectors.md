# position

1.  position: fixed

        해당 오브젝이 계속 자리를 유지함 ex) 팝업창, 맨위 메뉴창

2.  position: relative

        처음 위치한곳(부모)을 기준으로 위치를 수정함

3.  position: absolute

        가장 가까운 relative 부모 기준으로 위치를 수정함

    ```html
    <div class="warp">
      <div class="parent">
        <div class="chlid"></div>
      </div>
    </div>
    ```

    ```css
    .warp {
      position: relative;
    }

    .parent {
      position: absolute;
    }

    .chlid {
      position: absolute;
    }
    ```

    이렇다면 chlid의 기준은 **warp** 이 됨

# Pseudo Selectors

좀더 세부적으로 엘리먼트를 선택해 주는 것!

선택의 복잡한 과정을 pseudo selector로 가능함

```css
selector:first-child {
  background-color: tomato;
}
```

- selector:nth-child(2) >> 2번째 selector에 적용

```css
selector:nth-child(2),
selector:nth-child(3) {
}
/*이렇게 여러개도 적용 가능*/
```

- selector:nth-child(even) >> 짝수 selector에 적용
- selector:nth-child(odd) >> 홀수 selector에 적용

```css
selector:nth-child(2n) {
}
selector:nth-child(2n + 1) {
}
/*이렇게도 가능*/
```

p태그 안 span의 inside 글자 색을 바꾸려면

```html
<div>
  <p>
    asdasdasdasdasdasdasdasdasdasdasdasdasdasdasd
    <span>inside</span>
  </p>
  <span>hello</span>
</div>
```

```css
p span {
  color: tomato;
}

/*또는 */

div p span {
  color: tomato;
}
```

반대로 span 태그의 hello만 밑줄을 긋고 싶다면

```css
div > span {
  text-decoration: underline;
}
```

div의 바로 밎 자식

또는

```css
p + span {
  text-decoration: underline;
}
```

p 바로 뒤의 형제 (※ 바로 뒤에 있어야함)

바로 뒤에 있지 않을 경우

```css
p ~ span {
  text-decoration: underline;
}
```

### attribute 특성 선택자

    tag[attribute="value"]을 통해 스타일을 적용시킬 수 있다.
    tag[attribute~="value"]으로 value를 포함하는 모든 tag에
    스타일을 적용 가능

- input:required {} 은 input태그에서 required속성을 갖고 있는거에 대한.

- \*= is 'contains'

        \*= "hello" 라고 하면
        ㅁㄴㅇㄹㄴㅇㄹhelloㅁㄴㅇㄹㄴㅇㄹ 라고 줘도 선택됨

- ~ = is 'exactly'

        ~= "hello" 라고 하면 앞뒤에 공백이 있는 상태에서
        hello 인 경우만 선택됨

- a[href$=".org"]

         "$="는 ".org"로 끝나는 모든 anchor를 선택할 수 있다.
