# Center CSS

## Horizontal Center Inline Text/Link

```
.center-children {
  text-align: center;
}
```

## Center Block Level Element

```
.center-me {
  margin: 0 auto;
}
```

## Center Multiple Block Elements

```
.inline-block-center div {
  display: inline-block;
  text-align: left;
}
```


## Center Horizontal and Vertical Element with unknown width/height

```
.parent {
  position: relative;
}

.child {
  width: 300px;
  height: 100px;
  padding: 20px;

  position: absolute;
  top: 50%;
  left: 50%;

  margin: -70px 0 0 -170px;
}
```

[Source](https://css-tricks.com/centering-css-complete-guide/)

