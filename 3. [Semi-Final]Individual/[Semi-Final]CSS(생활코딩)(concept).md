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
