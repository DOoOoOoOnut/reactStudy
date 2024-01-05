# REACT STUDY 24/01/03
## Node JS 설치하기
* 설치 완료 후 `window+R`->`cmd`
* `node -v`, `npm -v` 설치 버전 확인


## 클라이언트 사이드 프레임워크 Client-side Javascript framework
* 웹 애플리케이션
* 복잡한 기능 쉽게 구축- 프레임워크 소프트웨어

## 프레임워크의 종류
* Angular -> Google의 Angular 팀이 개발 후 2016년에 공식 출시한 프레임워크(Type Script)
* vue -> AngularJS 프로젝트에서 기반하여 Evan You가 2014년 출시한 프레임워크(HTML)
* React -> Facebook에서 2013년 출시한 프레임워크.(JSX)
* Jquery -> John Resig에 의해 2006년 개발되어 공식 발표된 DOM 이벤트처리를 간편하게 해주는 프레임워크(HTML)

## REACT란?
* 전세계적으로 인기있는 프론트엔드 자바스크립트 라이브러리
* 리액트를 사용하면 빠르고 효율적이며 유지보수가 쉬운 UI를 개발할 수 있다
싱글 페이지 애플리케이션~ 모바일 에플리케이션~ 웹 개발 등에 폭넓게 사용

## 리액트의 장점
1. 가상 DOM 사용 : 실제 DOM이 아닌 가상 DOM 사용으로 성능, 효율성 향상
2. 컴포넌트 기반 : 재사용성이 높고 유지보수가 쉽다.
3. 활발한 커뮤니케이션 : 전세계적으로 많은 개발자가 사용하여 다양한 라이브러리와 도구가 제공되어 개발생산성이 올라간다.

## 웹 개발에서 사용되는 접근 방식 개념 이해하기

### SSR(Server Side Rending)
* 웹 페이지 접속 시 서버에 요청받아 클라이언트로 화면을 출력하는 전통적인 렌더링 방식 , 속도가 느린 단점.
* 클라이언트 요청 시 전통적인 방식으로 서버에서 HTML을 생성해 브라우저(클라이언트)로 전송한다. 초기 로딩속도는 빠르나 새로운 페이지로 이동할 때마다 HTML을 생성해 최종적으로 렌더링속도가 느려질 수 있다.

### CSR(Client Side Rendering)
* 자바스크립트 제외한 HTML과 CSS 먼저 로딩하는 방식, 초기 로딩속도가 빠르고 사용자 경험이 좋다.
* 초기 로딩속도가 빠르고 상호작용할 때마다 필요한 부분만 업데이트되어 빠른 사용자 경험 가능.
자바스크립트가 맣은 웹앱같은 겨우에는 자바스크립트 로딩 파일이 많으므로 SSR에 비해 느릴 수 있다.
초기 HTML은 서버에서 제공하고 추가 콘텐츠는 자바스크립트를 통해 렌더링된다.

### SPA(Single Page Application)
* 초기에 모든 동적 리소스를 로드하고 이후 필요한 데이터만 비동기적으로 불러와 동적으로 처리한다. 

### SSG(Static Site Generation)
* 정적 사이트

### 동기적 페이지
* 페이지가 이동될 때마다 모든 데이터를 불러오는 방식
### 비동기적 페이지
* 페이지를 이동할 때마다 페이지가 새로고침되지 않고 필요한 데이터만 불러오는 방식

## Package 여러 개의 자바스크립트 파일을 실행, 관리하는 단위 패키지
* 하나의 프로젝트에서 여러 자바스크립트 파일을 NodeJS를 이용해 실행할 때는 패키지 형태로 구성한다.

## Component 컴포넌트 기반의 UI 라이브러리(Component-Based UI Library)
* 페이지 기반 모든 요소 나눠서 개발 후 완성된 컴포넌트를 조립하여 페이지 구성 (aka.퍼즐)
* 웹 서비스를 개발할 때는 컴포넌트 여러 개 생성 & 조합하여 제작하게 된다.

## 성능 저하를 최소화한 Virtual DOM(가상 돔) = Node JS
* 컴포넌트 변경 > 가상 DOM Update > 컴포넌트 변경 > 가상 DOM Update > ... > 실제 DOM Update
* 진짜 서버에 올리기 전 미리보기하여 결과 체크할 수 있음 -> 이후 서버에 최종 업로드하여 완성

## 보일러 플레이트 Create React App (CRA)
* 복잡한 설정 없이 프로젝트를 생성할 수 있는 개발 도구

#24/01/05
## JSX 문법 
* HTML과 JS를 직접 연결해 사용할 수 있는 XML.
* {}묶어서 사용

## 주의사항
### 1. 객체 자료형 렌더링 오류
* 원시 자료형(숫자, 문자, 논리, null, undefined)을 제외한 값을 사용하면 오류 발생.
* -> 객체, 배열, BOM, DOM은 오류
### 2. 닫기 태그 필수
* HTML 규칙 상 닫기태그가 존재하지 않더라도 JSX에서는 반드시 닫기 태그를 표시해야 한다.
* <img><br><input> -> <img/><br/><input/>
### 4. 스타일 작성법
* 인라인 스타일링 -> `<main style={{"border:"5px solid black"}}>`
=> 스타일 규칙이 많을 시 복잡성이 높아져 가독성이 떨어질 수 있다.
* 외부 스타일 파일 분리 (script도 동일) -> `import 'url'`
=> 스타일 파일 분리 및 구성만 잘해준다면 파일 관리에 뛰어나고 가독성이 좋다

---

## 환경설정
* src > App.js와 index.js는 기본 세팅이므로 지우면 안됨.
### index.js
* `import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);`
### App.js
* `function App() {
  return (
    <div className="App">
      
    </div>
  );
}

export default App;`

## React 파일 연결
* 리액트는 src 개발환경 내에서 html파일을 생성하지 않고 모두 js 파일로 생성돼서 개발된다.
js는 원칙적으로 자바스크립트 작성파일이기 떄문에 리액트에서KTML을 js 내에서 표현하려면 function 함수를 먼저 생성하여 작성해야 한다. 함수 내에 HTML을 작성하면 JSX 문법과 함꼐 자바스크립트와 HTML을 사용할 수 있어 효율적이다.
* 다른 js파일로 작성되어 있는 컴포넌트를 불러오려면
해당 컴포넌트 맨 하단에 "export default 컴포넌트명"으로 내보내는 리액트가 작성되어 있어야 한다.
* 그 후 내보낸 컴포넌트를 받는 js 파일에서
import 명령으로 import 받는컴포넌트명 from '해당파일경로'로 작성해서 컴포넌트를 받아 사용하게 된다.
* -> 내보낼 파일에 export default 이름 / 보낼 파일에 import 이름 from 경로
* 이후 App 컨포넌트 내부의 return 반환 컴포넌트에 <이름 /> 형식으로 작성 -> 해당 이름 컴포넌트의 데이터가 index로 이동되어 node 서버에 나타나게 됨.
* 컴포넌트 == aka.함수// 리액트에서는 컴포넌트라고 부름.

