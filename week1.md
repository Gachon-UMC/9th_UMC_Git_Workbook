[개인 노션 정리](https://splashy-bovid-12f.notion.site/Week01-2773db583b288063bd00dd4fcef170a2)

## **1. 라이브러리와 프레임워크의 차이**

<hr/>

### **1️⃣ 프레임워크(Framework)란?**

- 소프트웨어의 특정 문제를 해결하기 위해서 상호 협력하는 **클래스와 인터페이스의 집합**
- 원하는 기능 구현에 집중하여 개발할 수 있도록 **일정한 형태와 기능을 갖추고 있는 골격, 뼈대**를 의미
- `프레임워크`는 애플리케이션 개발 시 필수적인 코드, 알고리즘, DB연동과 같은 기능을 위해 **어느정도 구조(뼈대)**를 제공
  → 이러한 구조 위에서 `사용자`가 코드를 작성해서 애플리케이션을 개발
- 공통된 부분은 `프레임워크`가 관리하고, `사용자`는 프레임워크가 정해준 방식대로 클래스, 메소드를 구현
- ex : 앱/서버 등의 구동, 메모리 관리, 이벤트 루프 등

<br>

### **2️⃣ 프레임워크의 기능**

1. **코드 재사용성** : 프레임워크는 공통 기능을 제공하여 코드 재사용에 용이
2. **일정한 구조 제공** : 프레임워크는 **애플리케이션의 구조를 정의**하여 개발자가 그 구조를 따르도록 함
3. **모듈화** : 프레임워크는 **기능을 모듈화**하여 **독립적인 컴포넌트**로 나눌 수 있게 함
4. **생산성 향상** : **반복적인 작업을 자동화**하고 개발 생산성을 높임
5. **유지보수성** : **일관된 코드 구조**를 유지하여 유지보수성을 향상

<br>

### **3️⃣ 프레임워크 예시**

- **Spring Framework** : JAVA 서버 개발
- **Django, Flask :** Python 서버 개발
- **Android :** 안드로이드 앱 개발
- **Angular, Vue.js :** 웹 개발

<br/>
<hr/>

### **1️⃣ 라이브러리(Library)란?**

- 소프트웨어를 개발할 때 **컴퓨터 프로그램이 사용하는 비휘발성 자원의 모임**
- **미리 작성된** 코드, 변수, 함수, 클래스가 포함
- `라이브러리`는 단순 활용 가능한 **도구들의 집합**

<br>

### **2️⃣ 라이브러리의 기능**

1. **코드 재사용성** : 라이브러리는 **특정 작업을 처리하는 코드의 재사용**을 촉진
2. **추상화** : 복잡한 작업을 간단한 **함수 호출로 추상화**
3. **모듈화** : 라이브러리는 **기능별로 모듈화**되어 필요에 따라 가져다 쓸 수 있음
4. **유연성** : 개발자가 필요에 따라 라이브러리를 **선택하여 사용**

<br>

### **3️⃣ 라이브러리 예시**

- **TensorFlow** : 머신러닝과 딥러닝을 위한 Python 라이브러리
- **Pandas** : 데이터 분석과 조작을 위한 Python 라이브러리
- **NumPy** : 수치 계산을 위한 Python 라이브러리
- **jQuery** : HTML 문서 탐색 및 조작, 이벤트 처리, 애니메이션, Ajax를 쉽게 처리할 수 있게 하는 JavaScript 라이브러리

<br>
<hr/>

## **프레임워크 vs 라이브러리**

### **1️⃣ 구조 제공 유무**

- `프레임워크`는 전체 **애플리케이션의 구조를 정의**
  → **일정한 개발 패턴**을 따르게 함
- `라이브러리`는 **특정 기능만 제공**할 뿐 애플리케이션의 전체 ~~구조에는 관여하지 않음~~
  → 개발자 스스로 원하는 방식으로 **구조 설계 가능**
  <br/>

### **2️⃣ 제어의 역전(Inversion of Control)**

### 가장 큰 차이점

- **`제어 흐름에 대한 주도성`이 누구에게/어디에 있는가?**
- 즉, 애플리케이션의 `Flow(흐름)`를 누가 쥐고 있느냐?

### 프레임워크

- `프레임워크`는 그 틀안에 제어 흐름에 대한 **주도성이 내포**
- 사용자는 **프레임워크 안**에 필요한 코드를 구성

### 라이브러리

- `라이브러리`는 **특정 기능만을 제공**할 뿐 어플리케이션의 전체 구조에는 관여하지 않음
- 사용하는 개발자 스스로 원하는 방식으로 **구조를 설계**

<br>
<br>

## 2. `null`과 `undefined`는 어떻게 다르며 `null`이 `object`인 이유는?

---

## `null` vs `undefined`

### 공통점

- `null` 과 `undefined` 모두 `값이 없음` 을 나타내는 자료형

### 차이점

`undefined`

- Javascript에서 **자동으로** 할당되는 값
- 변수는 선언했지만 값을 할당하지 않을 때, 자동으로 `undefined`가 할당

`null`

- **개발자가 의도적**으로 할당하는 값
- 특정 변수가 `값이 없음`을 `명확하게` 표시하기 위해 넣어주는 값

### 비교

- `==` (느슨한 비교)에서는 `null` 과 `undefined`가 같게 처리
- `===` (엄격한 비교)에서는 `null`과 `undefined`는 다르게 처리

### 메모리 관련

`null`

- 개발자가 명시적으로 메모리를 해제하고자 할 때 사용하는 방법.
- 객체를 참조하던 변수를 `null` 로 설정하면, 해당 변수는 더 이상 그 객체를 가리키지 않으므로 **참조가 끊어짐**
- 이렇게 참조가 끊기면 JavaScript 의 GC 에서 **메모리 제거**를 실행

`undefined`

- 메모리 해제외는 관련이 없음.

---

## `typeof null`이 'object' 인 이유?

### 1️⃣ 역사적인 이유

- JavaScript 초창기(1995년)부터 typeof null은 "object"를 반환했다. 이는 **명백한 버그**였지만, 이미 배포된 웹사이트와 코드가 이 동작에 의존하게 되면서 **수정하지 못하고 표준에 남게 된 역사적 유산이다**.
- ECMAScript 명세(ECMA-262)에서도 typeof null === "object"라고 **명시적으로 규정**하고 있습니다. 이유는 단순히 “웹 호환성” 때문이다.
- 실제로 2010년경 typeof null을 "null"로 바꾸자는 제안이 있었지만, 크롬(V8) 엔진에서 실험적으로 바꿨을 때 **수많은 웹사이트가 깨져서** 결국 철회되었다.
- JavaScript 창시자 브렌던 아이크(Brendan Eich)도 “당시 자바(Java)처럼 보이게 만들라는 압박과 촉박한 개발 일정 때문에 이런 세세한 부분까지 챙기지 못했다”고 언급했다. 즉, 빠르게 완성하느라 발생한 실수이자, 그대로 굳어진 버그이다.

### 2️⃣ **JavaScript 내부 동작 원리 (메모리 구조, 타입 태그)**

`초창기` JavaScript 엔진은 **32비트 값** 안에 **타입 태그(type tag)**와 **데이터**를 함께 저장했다.

- **000 (이진수)** → 객체(Object)의 참조값
- **001** → 정수(Integer) 값
- **010** → 실수(Double, 참조로 저장)
- **100** → 문자열(String, 참조로 저장)
- **110** → 불리언(Boolean)

여기서 `null`은 특별히 **NULL 포인터(주소값 0x00)** 로 저장되었다. 즉, 내부적으로는 **객체(Object) 타입 태그(000)** + **참조값 0** 형태였다.

따라서 엔진 입장에서는`null`을 **“객체 참조인데 값이 0인 것”**으로 오인하게 되었고, 그 결과 `typeof null`은 `object`가 되어버린 것이다.

<br>

---

## 3. Javascript가 싱글 스레드 언어이며 비동기 언어인 이유

### 1️⃣ Javascript는 왜 싱글 스레드를 선택했을까?

- `Javascript`는 웹페이지의 보조적인 기능을 수행하기 위해 브라우저에서 동작하는 경량 프로그래밍 언어를 도입하기로 결정하고 만들어진 언어
- **웹사이트를 구현하던 개발자들**에게 `JAVA`라는 언어는 다소 무겁고 어려운 언어였기 때문에, 브랜던 아이크라는 사람을 스카우트하여 ‘자바스크립트’가 탄생되었다.
- `JAVA` 왜 무겁고 어려운 언어라 생각했을까? → **멀티 스레드 모델은 프로그래밍 난이도가 높다.**
- `Javascript`는 멀티 스레드 환경에서 발생할 수 있는 복잡한 시나리오(`ex` 동시성 문제 등)를 신경 쓸 필요가 없다.

### 2️⃣ Javascript 비동기 처리 방식

- 자바스크립트는 싱글 스레드로 동작한다는 것
- 싱글스레드 방식은 한 번에 하나의 태스크만 처리할 수 있다는 것을 의미
- 하지만 브라우저가 동작하는 것을 살펴보면 많은 태스크가 동시에 처리되는 것처럼 느껴진다.
- `ex` `html` 요소가 애니메이션 효과를 통해 움직이면서 이벤트를 처리하기도 하고, `http`요청을 통해 서버로부터 데이터를 가지고 오면서 렌더링하기도 한다.
- 이처럼 자바스크립트의 동시성을 지원하는 것이 **`이벤트루프`**
- `이벤트루프`는 **브라우저에 내장되어 있는 기능 중에 하나이다.**

## <br>

## 4. DOM과 Virtual DOM -> 리액트의 가상DOM이 강한 이유

### 1️⃣ **DOM**이란?

- **DOM**(Document Object Model, 문서 객체 모델)
- 문서 객체란 `HTML`, `head`, `body`와 같은 태그들을 `Javascript`가 이용할 수 있는 객체를 의미
- `div`, `input`, `a` 등이 DOM에 해당

### 2️⃣ 가상 돔(Virtual DOM)의 등장 배경

- 실제 DOM에는 브라우저가 화면을 그리는데 필요한 모든 정보가 들어있어 DOM을 조작하는 작업이 무거움
- 그래서 `React`에서는 실제 DOM의 변경 사항을 빠르게 파악하고 반영하기 위해서 **내부적으로 `가상 DOM`**을 만들어서 관리
- `Virtual DOM`은 DOM의 **요약본**

### 3️⃣ Virtual DOM을 사용해야 하는 이유

- **초기 정적인 웹페이지에 맞계 설계된 DOM**은 정적인 성격
  → 현재 트렌드인 **동적인 웹 애플리케이션**에 사용하려면 **성능 상에 문제**가 발생
- 최근 트렌드인 복잡한 `SPA`에서는 **DOM 조작이 굉장히 빈번**하게 발생하며, 그 변화를 적용하기 위해서는 **브라우저가 많은 연산**을 하게 되고, 결국 전체적인 프로세스가 **비효율적**

### 4️⃣ Virtual DOM의 동작 방식

- `Virtual DOM`을 사용하면 실제 DOM에 접근하며 조작하는 대신, 이를 **추상화**한 자바스크립트 객체를 구성하여 사용
- DOM의 상태를 **메모리에 저장**하고, 변경 전과 변경 후의 **상태를 비교** 한 뒤 **최소한의 내용만 반영**하여 성능 향상
- DOM의 상태를 메모리 위에 계속 올려두고, **DOM에 변경** 있을 경우 **해당 변경 사항만 반영**

## <br>

## 5. 나의 프로젝트 초기 세팅

<aside>

### 디렉토리 구조

```bash
MacBook-Pro-2:my_blog 2sac$ tree
.
├── eslint.config.js
├── index.html
├── node_modules
├── package.json
├── pnpm-lock.yaml
├── postcss.config.js
├── public
├── src
│   ├── api
│   ├── App.css
│   ├── App.tsx
│   ├── assets
│   ├── components
│   │   └── Buttons
│   │       └── Button.tsx
│   ├── index.css
│   ├── main.tsx
│   ├── pages
│   ├── styles
│   └── vite-env.d.ts
├── tailwind.config.ts
├── tsconfig.app.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
```

</aside>
<aside>

### `React Setting with pnpm`

```bash
pnpm create vite
```

```bash
pnpm add -D eslint eslint-config-prettier eslint-plugin-prettier prettier
```

```bash
echo '{
  "semi": true,
  "singleQuote": true,
  "trailingComma": "all",
  "printWidth": 80,
  "tabWidth": 2
}' > .prettierrc
```

### `eslint.config.js`

```bash
import js from '@eslint/js'
import globals from 'globals'
import reactHooks from 'eslint-plugin-react-hooks'
import reactRefresh from 'eslint-plugin-react-refresh'
import tseslint from 'typescript-eslint'
import { defineConfig, globalIgnores } from 'eslint/config'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      js.configs.recommended,
      tseslint.configs.recommended,
      reactHooks.configs['recommended-latest'],
      reactRefresh.configs.vite,
    ],
    languageOptions: {
      ecmaVersion: 2020,
      globals: globals.browser,
    },
  },
])

```

### `.prettierrc`

```bash
{
  "semi": true,
  "singleQuote": true,
  "trailingComma": "all",
  "printWidth": 80,
  "tabWidth": 2
}

```

### `install tailwindcss`

```bash
pnpm add tailwindcss @tailwindcss/vite
```

### `tailwind.config.ts`

```bash
import type { Config } from 'tailwindcss';

const config: Config = {
  content: ['./index.html', './src/**/*.{js,ts,jsx,tsx}'],
  theme: {
    extend: {},
  },
  plugins: [],
};

export default config;
```

### `postcss.config.js`

```bash
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
};
```

</aside>

## <b>

### 참고

- https://idkim97.github.io/2022-08-16-%ED%94%84%EB%A0%88%EC%9E%84%EC%9B%8C%ED%81%AC%20vs%20%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC/
- https://velog.io/@woody_59/undefined%EC%99%80-null-%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90
- https://witch.work/ko/posts/javascript-why-typeof-null-is-object
- https://miracleground.tistory.com/entry/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EB%8A%94-%EC%99%9C-%EC%8B%B1%EA%B8%80-%EC%8A%A4%EB%A0%88%EB%93%9C%EB%A5%BC-%EC%84%A0%ED%83%9D%ED%96%88%EC%9D%84%EA%B9%8C-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4-%EC%8A%A4%EB%A0%88%EB%93%9C-%EB%B9%84%EB%8F%99%EA%B8%B0-%EB%8F%99%EA%B8%B0-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%97%94%EC%A7%84-%EC%9D%B4%EB%B2%A4%ED%8A%B8%EB%A3%A8%ED%94%84
- https://velog.io/@ctdlog/React-DOM%EC%9D%B4%EB%9E%80-Virtual-DOM%EC%9D%84-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94-%EC%9D%B4%EC%9C%A0
