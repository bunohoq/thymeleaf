🌿 Thymeleaf 기본 예제 모음
--------------------------------------------

Spring + Thymeleaf 문법을 정리하며 만든 예제 페이지 모음입니다.
기본 문법부터 반복문, 조건문, URL 처리, 조각 페이지까지
타임리프의 핵심 기능을 단계별로 학습할 수 있도록 구성되어 있습니다.


📁 프로젝트 구조
--------------------------------------------
templates/
 ├── m1.html   # 변수 표현식
 ├── m2.html   # 스프링 메시지(국제화)
 ├── m3.html   # 연산자
 ├── m4.html   # HTML 속성 조작
 ├── m5.html   # 콘텐츠 조작(text/utext/inline)
 ├── m6.html   # 숫자·날짜 포맷팅
 ├── m7.html   # 링크 표현식(URL)
 ├── m8.html   # 제어 속성 + 반복문 + 상태값
 ├── m9.html   # 조각 페이지(fragment)
 └── inc/
      ├── sub1.html
      └── sub2.html


📘 예제 상세 설명
--------------------------------------------

1️⃣ m1 — 변수 표현식 (Variable Expression)
 - ${} 로 컨트롤러에서 전달된 값 출력
 - DTO / Map 접근
 - 선택 변수 표현식 *{}
 - th:object 활용

2️⃣ m2 — 스프링 메시지(Internationalization)
 - messages.properties 문자열 사용
 - 다국어 / 공통 문구 관리
 - 메시지 포맷팅

3️⃣ m3 — 연산자
 - 산술 / 비교 / 논리 / 삼항 연산자
 - 문자열 결합
 - 파이프(| |) 표현
 - Elvis(?:) 연산자

4️⃣ m4 — HTML 속성 조작
 - th:value, th:checked, th:selected
 - 동적 스타일 변경(th:style)
 - 속성 우선순위

5️⃣ m5 — 콘텐츠 조작
 - th:text / th:utext
 - 인라인 표현 [[...]], [(...)]
 - th:inline="javascript"

6️⃣ m6 — 숫자·날짜 포맷
 - #numbers.formatInteger / formatDecimal
 - #dates.format()
 - year / monthName / day 등 날짜 요소 출력

7️⃣ m7 — 링크 표현식(URL Expression)
 - @{ } 로 URL 자동 생성
 - QueryString 바인딩
 - PathVariable 바인딩
 - 문자열 방식과 비교

8️⃣ m8 — 제어 속성 + 반복문(each) + status
 - th:if, th:unless, th:switch/case
 - 리스트 반복 th:each
 - status: index, count, size, even, odd
 - <th:block> 활용
 - 주소록 테이블 렌더링

9️⃣ m9 — 조각 페이지(Fragment)
 - th:fragment 정의
 - th:insert / th:replace
 - Fragment 파라미터 전달
 - include 구조 구성


🚀 실행 방법
--------------------------------------------
Spring Boot 기준:

http://localhost:8080/m1
http://localhost:8080/m2
...
http://localhost:8080/m9

TestController에 매핑된 URL 순서대로 접근 가능합니다.


✏️ 오늘 배운 점 (회고)
--------------------------------------------

✔ 1. 타임리프는 HTML 속성 기반 템플릿 엔진이다.
   - JSP처럼 태그 중심이 아니라 th:* 속성 중심으로 돌아감.

✔ 2. 출력 방식이 여러 가지다.
   - th:text, th:utext, [[...]], [(...)]
   - escape 여부를 상황에 맞게 선택해야 함.

✔ 3. 날짜·숫자 포맷이 간단하다.
   - #numbers, #dates
   - 자바 코드 없이 포맷팅 가능.

✔ 4. URL 표현식(@{})이 강력하다.
   - 문자열 병합 없이 파라미터 자동 인코딩 지원.

✔ 5. switch/case와 each/status가 유용하다.
   - 짝/홀수 스타일링, 인덱스 출력 등 반복문 처리 편리.

✔ 6. Fragment로 include 구조를 깔끔하게 만들 수 있다.
   - 헤더·푸터·메뉴 등 공통 컴포넌트 분리 가능.


🌱 느낀 점
--------------------------------------------
- JSP보다 훨씬 HTML 친화적이라 작업 흐름이 편하다.
- 데이터 바인딩과 조건/반복이 단순해서 유지보수성이 좋다.
- 실제 프로젝트에서도 바로 사용할 수 있을 정도로 구조가 명확하다.
- 오늘 배운 내용을 익혀두면 이후 스프링 개발 속도도 확실히 빨라질 것으로 예상된다.
