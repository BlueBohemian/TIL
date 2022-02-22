# HTML

<br>

### 자주 쓰이는 태그

```html
<!DOCTYPE html>
<meta charset = "UTF-8">
<a href = "naver.com/html" target="_blank" title="무슨 링크인지 알려줌"></a>
```

1. DOCTYPE
   - DOCTYPE은 문서의 유형을 정의하기 위해 사용하는 선언문(DTD / Document Type Definition)이다. 웹 문서의 시작을 알려주며 `<html>` 태그보다 먼저 선언한다. DOCTYPE은 웹 브라우저에서 처리할 문서가 HTML이며 어떠한 버전으로 사용하였으니 해당 방식대로 해석하라는 의미를 갖는다.
2. meta charset = "UTF-8"
   * 웹 브라우저나 컴퓨터가 HTML파일을 웹브라우저에서 표시될 수 있도록 변환하는 처리작업 즉 인코딩을 해야한다. 그 **인코딩** 방식을 알려주는 태그이다.

3. target = "_blank"
   * 새 창 띄우기

<br>

### 기타

웹의 메소포타미아 : http://info.cern.ch

<br>

<br>

## (실습) 개인 웹사이트 완성하기

1. index.html **(필수)**
2. html.html
3. css.html
4. javascript.html

* 지금까지 배운 내용을 활용하여 개인 컴퓨터에서 작동하는 웹사이트를 만든다.

<br>

<br>

### 인터넷 연결하기

1. 실제 사이트 ( index.html )
2. 웹 브라우저 ( 클라이언트 )
   - request - 요청
3. 웹 서버 ( 서버 ) or 웹 호스팅
   * response - 응답

---

# CSS

<br>

## 이유 찾기

### CSS 탄생 이유

원래 HTML에 있던 디자인 기능을 CSS라는 개념으로 분리시켜 디자인 기능을 더욱 강화시키고, 유지보수와 협업을 편리하게 만들었다.

1. 유지 보수
2. 가독성
3. 디자인 전문화

<br>

<br>

### CSS 배워야 하는 이유

ㅇ 디자인을 위한 도구와 기술을 통한 확장성

* 논리적인 과정을 거쳐 만들어지는 것을 배워야 더 확장된 디자인을 만들 수 있다. 

ㅇ 협업 능력 향상
     - 디자이너, 프런트엔드 등

<br>

<br>

## 사용법

### CSS 사용하는 방법

* **[핵심] 선택자와 속성**

<br>

1. style tag ( 선택자 사용 )

```css
<style>
	a {
		color:red;
		text-decoration:none;     <!--밑줄이 없어진다.-->
	}
	h1{
            font-size:45px;
            text-align:center;
        }
</style>
```

| Selector        | 선택자   |
| --------------- | -------- |
| **Declaration** | **선언** |
| **Property**    | **속성** |
| **Value**       | **값**   |

<br>

2. style property

```
<style="color:red; text-decoration:none;">
```

* 세미콜론(;) 으로 구분해서 사용한다.

<br>

3. 검색 키워드
   ex) css text size property

<br>

<br>

### 클래스 및 아이디

* 우선순위 : id > class > tag
  * 포괄적인 것보다 구체적인 것을 우선순위로 가진다. ( 제외를 위해 )
  * 클래스는 2개까지도 지정할 수 있지만 사용을 권장하지 않는다.
  * 그외에 코드와 가장 가까이에 있는 코드가 우선순위를 가진다.
* 검색 키워드
  ex) css selector

```html
<style>
            #active {
                color:red;
            }
            .saw {
                color:gray;
            }
            a {
                color:black;
                text-decoration: none;
            }
            h1 {
                font-size:45px;
                text-align:center;
            }
</style>
```

```html
<a href="SquidGame.html" class="saw"><li>오징어게임</li></a>
<a href="HELLBOUND.html" class="saw" id="active"><li>지옥</li></a>
```

* '.saw'가 아닌 'saw'를 지정할 경우 클래스 saw가 아닌 태그 saw를 지정하게 되니 주의하자. 







[ 프런트엔드 영역 ]

※ CSS 끝이 없다.

~심화~

# Sass(SCSS)

# Flex / Grid

# Canvas 





