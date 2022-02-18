### 2회독 중

https://www.youtube.com/channel/UCFTMvQIeO94gru6JDn0seDw



[ 깃헙 토큰 생성하는 과정 ]

1. Git Setting - Emails - Keep my email addresses private 해제
2. Git Setting - Public profile - Public email 설정
3. Git Setting - Developer setting - Personal access tokens - Generate new token
   (체크구간!) 기간 90일정도 / workflow / gist / user / delete_repo까지 체크해주고 생성할 것
   (주의!) 반드시 안전한 곳에 기입해 둘 것, 권한은 바꿀 수 있지만 토큰을 잊어버리면 삭제하고 다시 만들어야 한다.

---

ㅇ Git은 인증에 Git Credential Manager를 사용하고 있다. 흠..

---

[ Source Tree 설치 ]
도구 - 옵션 - 인증 - Git 인증 Basic - 토큰 기입 - 설정 초기화(setting as Default)

> **로그인 기입**
>
> 아이디     : 아이디(@메일생략)
> 비밀번호 : 토큰 기입

※ 이 과정에서 '유효한 소스 경로/url 이 아닙니다' 문제 발생
해결시도(1) 소스트리 재설치
해결시도(2) 자격 증명 관리자 제거
해결시도(3) 내장 Git 재설치 - https://devbirdfeet.tistory.com/66

---





# SourceTree

Git GUI 버전


## Reverse hunk / Discard hunk

=> 코드뭉치 되돌리기 /  코드뭉치 버리기  -  작업을 진행한 파일이 커밋하기 전 상태로 한번 되돌린다. 보통 작업을 하다가 잘 못 생성할 경우 이것을 사용한다.





# Commit

### ㅇ 커밋 주의사항

커밋에는 주의사항이 있습니다.

1. 반드시 한 번에 하나의 논리적 작업만을 커밋합니다.
2. 커밋 메시지를 잘 적어야 합니다.

특히 커밋 메시지는 미래의 여러분과 다른 개발자를 위해서 꼼꼼히 적어야 합니다.



### ㅇ 커밋 메시지 작성법

1. 첫 줄에 간단하지만 명확하게 내용을 씁니다.
2. 한 줄 비우고
3. 자세한 내용을 적습니다.





# branch

- 브랜치 (branch): 기능 변경을 하고 싶을 때 생성 및 사용
  - HEAD branch : 현재 브랜치
- 머지 (merge): 한 브랜치의 내용을 다른 브랜치에 반영
  - 브랜치 삭제 : merege 이후 branch delete 가능
- 체크아웃 (checkout): 저장소에서 특정 커밋이나 브랜치로 돌아가고 싶을 때 사용 - 소스트리는 더블클릭 만으로 체크아웃을 할 수 있다.
- 충돌시 해결법 : 수동으로 해결 ( 충돌 해결 tool도 존재하긴 함 )
  - visual studio 사용시 merge 충돌 발생시 '붉은색 ! 표시' 생성 
  - '내것'으로 및 '저장소'로 해결시 오류 발생 - Staging Area로 올라가지 않고 강제 초기화 발생 ( 이유를 알 수 없음 )

![충동 해결 오류](C:\Users\서영호\OneDrive\문서\07. 프로그래밍\01. 공부 루틴 프로젝트\Core 3 - 공부법 및 사용툴, 고전서\Git&GitHub\5. 호눅스 코드스쿼드 Git\충동 해결 오류.png)

![충동 해결 오류2](C:\Users\서영호\OneDrive\문서\07. 프로그래밍\01. 공부 루틴 프로젝트\Core 3 - 공부법 및 사용툴, 고전서\Git&GitHub\5. 호눅스 코드스쿼드 Git\충동 해결 오류2.png)





## 초기화 & 되돌아가기 ( reset )

- ```
  git reset --hard
  ```

   이것에 해당하는 명령으로 커밋을 되돌리기 한다.

   * **[장점]** 쉽다.
  * **[단점1]** **[주의!]** 이전 커밋은 사라짐 ( push로 '원격저장소' 저장된 상태에서는 사라지지 않는다 )
  * **[단점2]** **[주의!]** reset이후 main을 새로 commit할 경우 origin과 다른 트리로 생성되기 때문에 문제가 발생한다.
    * **[단점2 해결법1]** 강제 푸시 해야 한다.  ( push는 `force` 옵션을 선택해야 함 )
          `git push --force` 를 CLI를 통해 사용 ( SourcTree에서도 설정을 통해 실행 가능 )
    * **[단점2 해결법2]** origin과 merge해서 해결한다.





## 초기화 & 되돌아가기 ( with branch )

되돌가려는 부분에 브랜치를 생성하여 되돌아간다. ( reset 오사용으로 인한 '이전 커밋이 사라짐' 방지할 수 있다. )
마지막에 push 사용시 merge를 통해 해결한다.

**[단점]** 코드트리가 지저분해 진다.
