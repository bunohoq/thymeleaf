Thymeleaf Examples – README (Developer Style)
---------------------------------------------

Spring + Thymeleaf 기본 문법을 체계적으로 학습하기 위한 예제 모음입니다.
변수 표현식부터 반복문, 조건문, URL 처리, 조각 페이지까지
타임리프의 핵심 기능을 파일 단위로 정리했습니다.


[ 프로젝트 구조 ]

templates/
  ├── m1.html   # 변수 표현식
  ├── m2.html   # 메시지(i18n)
  ├── m3.html   # 연산자
  ├── m4.html   # HTML 속성 조작
  ├── m5.html   # 콘텐츠(text/utext/inline)
  ├── m6.html   # 숫자/날짜 포맷
  ├── m7.html   # 링크 표현식
  ├── m8.html   # 조건문/반복문/status
  ├── m9.html   # 조각 페이지(fragment)
  └── inc/
       ├── sub1.html
       └── sub2.html


[ 예제 상세 ]

1) m1 – Variable / Selection Expression  
   - ${} 변수 표현식  
   - DTO/Map 접근  
   - th:object + *{} 선택 변수 표현식

2) m2 – Spring Messages (i18n)
   - messages.properties 문자열 관리  
   - 다국어 처리  
   - 메시지 포맷팅

3) m3 – Operators
   - 산술/비교/논리/삼항  
   - 문자열 결합  
   - 파이프 | | 표현  
   - Elvis(?:) 연산자

4) m4 – HTML Attribute Manipulation
   - th:value, th:checked, th:selected  
   - th:style  
   - HTML 속성 우선순위 이해

5) m5 – Text / UText / Inline
   - th:text vs th:utext  
   - [[...]] / [(...)]  
   - th:inline="javascript"

6) m6 – Number & Date Formatting
   - #numbers.formatInteger / formatDecimal  
   - #dates.format  
   - 날짜 요소(year, monthName 등)

7) m7 – URL Expression
   - @{ } 로 URL 빌드  
   - 쿼리 파라미터 바인딩  
   - PathVariable 처리  
   - 문자열 방식과 비교

8) m8 – Conditional / Loop / Status
   - th:if, th:unless, th:switch  
   - th:each 반복  
   - status(index, count, size, even/odd)  
   - <th:block>  
   - 주소록 테이블 렌더링

9) m9 – Fragment(include)
   - th:fragment  
   - th:insert / th:replace  
   - Fragment 파라미터 전달



[ 실행 방법 ]

Spring Boot 기준:
http://localhost:8080/m1
http://localhost:8080/m2
...
http://localhost:8080/m9

각 URL은 TestController에 매핑된 페이지로 연결됩니다.



[ Today I Learned (TIL) ]

- 타임리프는 HTML 속성 기반 템플릿 엔진이며, th:* 구조가 핵심이다.
- 출력 방식(escaped/unescaped) 차이를 정확히 이해했다:  
  th:text, th:utext, [[ ]], [( )].
- URL 빌딩은 @{ } 방식이 가장 안전하다.  
  문자열 결합 없이 파라미터 인코딩까지 자동 처리됨.
- 반복문 + status 조합은 실무에서 매우 유용하다.  
  index, count, 짝/홀수 여부 등 다양한 상태값 제공.
- Fragment를 이용해 레이아웃·조각 페이지 구조를 구성할 수 있다.
- JSP 대비 HTML 친화적이며 유지보수성이 높다.



[ Summary ]

이 레포지토리는 타임리프의 핵심 기능을 빠르게 정리하고,
스프링 MVC 프로젝트에서 즉시 활용 가능한 템플릿 패턴을 제공하기 위해 작성되었다.
