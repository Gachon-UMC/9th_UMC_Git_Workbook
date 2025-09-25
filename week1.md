\## 1주차: TypeScript 기초 정리



\## TypeScript



TypeScript는 JavaScript에 타입 시스템을 추가한 언어로, 컴파일 시점에 타입 검사를 할 수 있게 도와준다.

이로 인해 코드 안정성이 높아지고 유지보수가 쉬워짐



---



\## 🔍 주요 개념

\### 1. TypeScript

* 매개변수 타입 : 매개변수 이름 뒤에 ': 타입' 형식으로 작성
* 반환 타입 : 매개변수 목록 ( )뒤에 ': 타입'을 붙여서 함수가 어떤 값을 반환할 지 명시
* 여러가지 타입

&nbsp;	- 숫자 : number

&nbsp;	- 문자열 : string

&nbsp;	- 참 / 거짓 불 값 : boolean

&nbsp;	- 값 없음 : null

&nbsp;	- 값이 아직 할당되지 않음 : undefined

&nbsp;	- 고유한 값 : symbol

&nbsp;	-  매우 큰 정수 : bigint

&nbsp;	- 객체 표현 : object 



\### 2. 배열타입, 튜플타입

* 배열 타입 

&nbsp;	- string \[ ] : 배열 요소가 문자열임을 간단히 표시하는 방법

&nbsp;	- Array<string> : 제네릭 문법을 활용해서 타입을 지정하는 방법

* 튜플 타입 : 배열과 비슷하지만 각 요소의 타입과 순서가 고정되어 있음

&nbsp;	- 예시 : const tuple \[string, boolean, number] = \["모리", ture, 21]



\### 3. Interface 객체 타이핑

* Merging Interfaces : TypeScript에서는 \*\*같은 이름을 가진 여러 인터페이스가 선언되면 자동으로 병합\*\*

&nbsp;	- 특징 : 자동 병합, 확장성, 타입 안정성 유지

* 네임스페이스 : 코드를 \*\*모듈화하고 그룹화해서 관리\*\*할 수 있는 방법

&nbsp;	- 특징 : 코드 조직화, 자동 병합, 전역 오염 방지

