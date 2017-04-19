# HTML

## `<!DOCTYPE html>`
This declaration is an instruction. It tells the browser what type of document to expect, along with what version of HTML is being used in the document. `<!DOCTYPE html>` must be the first line of code in all of your HTML documents.

**Note**: If you don't use the doctype declaration, your HTML code will likely still work, however, it's risky. Right now, the browser will correctly assume that you are using HTML5, as HTML5 is the current standard. In the future, however, a new standard will override HTML5. Future browsers may assume you're using a different, newer standard, in which case your document will be interpreted incorrectly.

## `<html>` `</html>`
Anything between <html> and </html> will be considered HTML code.

## HTML terms
### angle brackets
`<` `>`
### HTML element
HTML code that lives inside angle brackets(`<`, `>`)

### opening tag
HTML tag used to start an HTML element
ex) `<p>`
### closing tag
HTML tag used to end an HTML element
ex) `</p>`

(HTML terms를 보여주는 이미지 삽입)

## `<head>` `<title>` `</title>` `</head>`
The <head> element will contain information about the page that isn't displayed directly on the actual web page.

## `<body>` `</body>`
Once the file has a body, many different types of content can be added within the body, like text, images, buttons, and much more.

### `<h1>` `</h1>` `<h2>` `</h2>` ... `<h6>` `</h6>`
제목(heading)

### `<p>` `</p>`
본문(paragraph)

### `<ul> <li> </li> <li> </li> </ul>`
순서없는 목록(unordered lists)

### `<ol> <li> </li> <li> </li> </ol>`
순서있는 목록(ordered list)

### `<a href="주소" target="속성">anchor제목</a>`
a는 anchor의 약자. Similar to hyperlink.
href는 hyper reference의 약자로 '주소'를 찾아준다는 의미이다.

#### 네임 앵커(anchor)
어떤 특정 위치에 책갈피를 지정하고, 그 지정된 곳으로 이동하는 것을 네임앵커라고 한다.
`<a name = "책갈피이름">`으로 책갈피를 지정하고, `<a href="#책갈피이름">`으로 지정한 "책갈피이름"위치로 이동한다.

#### link와 anchor의 차이점
찾아본 바로는, `<head>`에서 쓰는 게 `<link>`, `<body>`에서 쓰는게 `<a>`이다.

The anchor element is used to link to **another page**.
`<a href="index.html">Home</a>`

The link tag is used to link to **external style sheets**.

```xml
<head>
	<link rel="stylesheet" type="text/css" href="theme.css">
</head>
```

#### target의 속성
- `target = "_self"` : 현재 자신의 페이지가 바뀐다. default
- `target = "_parent"` : 부모의 페이지에서 이동한다.
- `target = "_top"` : 최고 상단 페이지가 이동한다.
- `target = "_blank"` : 새로운 창을 띄워서 이동한다.

### `<a href="#" target="속성"><img src="이미지파일링크주소" alt="이미지의 묘사내용"/></a>`

#### alt
alt는 alternate(대체하다)의 약자. 다시 말해 이미지의 대안을 나타낸다. 이 이미지는 외부의 주소이기 때문에, 주소가 잘못되었거나 해당 위치의 서버에 문제가 있다면 이미지를 못 읽어 올 수 있다. 이럴 때 이 alt 속성의 내용이 해당 이미지를 대체하여 나타낸다.

이미지가 제대로 로드가 될 경우에는 이 속성 값이 브라우저에서 보이지 않기 때문에 이 속성을 무시하는 경향이 있지만, 반드시 써야 할 속성이다. 왜냐하면, 이 alt속성은 이미지를 보지 못하는 분들이 보기 때문이다.

### `<br/>`
line break

### `<!--` `-->`
comments.
```xml
<!-- This is a comment that the browser will not display. -->
```

## Boilerplate code
(boilerplate code 이미지 삽입)
The term "boilerplate code" is used to describe the basic HTML code required to begin creating a web page. Without all of the elements in the boilerplate code, you'll risk starting without the minimum requirements considered to be best practice.