> **02.18.**

# Git

## revert ( 커밋 되돌리기 )

현재 커밋을 보존하면서 과거 버전으로 되돌아가는 방법이다.
SourceTree에서 우클릭 '커밋 되돌리기' 사용 

**[단점] [주의!]** 충돌 날 가능성이 매우 높다. 다소 어렵다.

**[TIP①]** revert로 여러 커밋을 되돌리기!

- 최신부터 순서대로 revert를 반복 적용하면 된다.

**[TIP②]**특정 커밋 하나만 취소 하기!

- 직접 선택해서 revert를 하면 된다.

  **[주의!]** 충돌이 날 가능성이 있습니다. 
  			그러니 이왕이면 순서대로 revert를 진행하는 것이 좋다.

<br>

<br>

<br>

---

### [ branch checkout 조건 ]

브랜치를 만들고 체크아웃을 통해 변경하려고 하면 현재 작업디렉토리가 깨끗해야 합니다. 

<br/>

<br/>

# 임시 저장 하는법

**[상황]** commit 하지 않은 코드를 작업 중 부득이하게 다른 브랜치로 checkout 해야하는 상황 발생

<br/>

  ## [해결1] 이전 커밋 덮어쓰기 ( 미지막 커밋 정정 )

**[주의!] 강제 푸시를 필요할 수 있다.**

<br/>

1. 일단 커밋한다.
2. [커밋옵션] - [마지막 커밋 정정]

* **강제푸시를 하는 경우**

  branch를 푸시한 경우 위와 같은 작업을 할 경우 새로운 브랜치가 생기기 때문에 강제 푸시를 해야 한다. 그러니 <u>임시 commmit 같은 경우 서버에 보내면 안된다.</u>

<br/>

<br/>

## [해결2] stash ★

스태시를 사용하면 임시 저장 공간에 현재 작업 내용이 저장됩니다. 
이 내용을 스태시라고 하고 언제든지 다시 복구할 수 있습니다.

**[주의!]**  새로운 파일 있다면 일단 Staging area에 올린후 stash한다.

<br>

<br>

# rebase ( 재배치 )

merge 처럼 두 브랜치를 합칠 때 사용한다.
**[주의!]** 브랜치 재배치 병합 중에는 브랜치 삭제가 안된다?? (**확인필요**) 
            단순 병합에도 해당하는 것 같기도 하고?

<br/>

### 사용법

1. '현재 변경사항을 (A브랜치)에 재배치' 클릭

2. 충돌

   **[주의!]** 충돌 해결 방식이 기존에 방식과 다릅니다 

3. 변경해주고 statging area 올리기

4. (다시) '현재 변경사항을 (A브랜치)에 재배치' 클릭 - '재배치 계속' 클릭 

   * 이 상황은 CLI에서 rebase continue에 해당한다.

5. 마지막으로 '현재 브랜치로 (A브랜치) 병합' 클릭

<br/>

### 장점

- 깔끔한 트리 정리

### 단점

- 위험하다 - 충돌 가능성이 더 높다.
- 이미 원격에 있는 브랜치를 rebase 하면 안 된다!

<br>

<br>

## 좋은 커밋의 단위

- 커밋은 자주 합시다!
- 원자적으로 쪼갤 수 없는 단위 (주로 함수 등)의 의미있는 개발을 했다면 커밋을 합시다.

<br>

<br><br>

<br>

<br>

<br>

# **HTML**

- 저작권이 없는 **퍼블릭 도메인(Public Domain)**으로 앞으로도 사라지지 않을 기술이다.

<br/>

**준비물**

* 웹브라우저

* 에디터 및 IDE ( Atom, brackets, Visual Studio Code )

<br/>

<br/>

## TAG ①

* 검색어 : html ㅁㅁㅁㅁ tag
* Web Docs sites : https://developer.mozilla.org/en-US/

`<meta charset="utf-8">>` : 언어

`<strong></strong>` : Strong Importance element(진하게)
`<u></u>` : Underline element(밑줄)
`<s></s>` : The Strikethrough element(취소줄)
`<h1></h1>` : Heading elements level 1(제목1)

* 생활코딩 왈) **난이도**가 **쉬운 것은 중요**하지만 어려운 것은 지엽적인 것이다. 그러니 집중하자.

<br/>

<br/>

## TAG ②

* 태그 사이트별 통계 : https://www.advancedwebranking.com/seo/html-study/

* 통계를 기반으로 중요한 것 부터 공부하기 ( HTML에 대략 150개 정도 태그가 있지만 필요한 부분은 정해져 있다. )

`<br>` : The Line Break element(줄 바꿈)

`<p></p>`  : The Paragraph element (단락)

`<img src="Hello.jpg">` : The Image Embed element (이미지)
												 Source Attribute (src / 소스 속성) 

<br>

<br>

## TAG 기타 

* css 맛보기 : `<p style="margin-top:45px;">`
* 휴머니즘 : 웹 접근성을 통해 소외된계층에게 정보를 전달하는 사다리
* `H1`태그를 의미에 맞게 적절히 사용해야 하는 이유 : 검색엔진의 SEO에 영향을 끼친다.
  * 검색엔진은 제목 태그의 정보를 더 높게 친다.

<br><br>

## parent / child

태그간의 부모 자식 관계를 가지는 경우가 있다.

`<parent>`
    `<child></child>`
`</parent>`

<br>

#### 리스트의 경우

* ul : unordered list  /  ol : ordered list

```html
<ul>
  <li>1. HTML</li>
  <li>2. CSS</li>
  <li>3. JavaScript</li>
</ul>
```

```html
<ol>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ol>
```

<br>

#### 표의 경우

* `<table>` 태그의 경우 3개가 같이 간다.

`<table>`
   `<tr>`
       `<td>head</td>`
       `<td>98.1%</td>`
    `</tr>` 
   `<tr>`
       `<td>body</td>`
       `<td>97.9%</td>`
    `</tr>`
    `<tr>`
        `<td>html</td>`
        `<td>97.9%</td>`
    `</tr>`
`</table>`
