tailwindcss 를 설치하면서 프로젝트 생성을 했음.

로직같은 경우는 css같은 외형이 필요가 없음

작업 {
  - 사이트 레이아웃 설계
  - tailwindcss를 이용한 레이아웃 꾸미기
  - 더미 데이터를 이용한 로직 짜보기
  - 데이터 베이스 관리를 위한 db 정하기 , SQL, DB , Session ,Cookie
  - 도메인, 서버호스팅 공부
  - 광고 및 ui 를 만들기 위한 포토샵 사용
}

데이터베이스(SQL):

SQLite: SQLite는 경량의 서버리스 데이터베이스로, 별도의 데이터베이스 서버가 필요하지 않습니다. SQL 문법을 사용하여 데이터를 다루며, 파일 형태로 저장되어 쉽게 관리할 수 있습니다. 앱이나 웹사이트의 작은 규모 프로젝트에 적합합니다.

서버 호스팅:
Heroku: Heroku는 배우기 쉬우면서도 개발자 친화적인 클라우드 플랫폼으로, 앱을 손쉽게 배포하고 관리할 수 있습니다. 간단한 명령어로 앱을 빠르게 배포할 수 있어서 학습 곡선이 낮습니다.

백엔드 프레임워크:
Express.js: Express.js는 Node.js 기반의 경량 백엔드 웹 프레임워크로, 라우팅, 미들웨어 지원 등을 제공합니다. 초보자도 쉽게 시작할 수 있으며, 자유도가 높아 많은 자료와 예제를 찾을 수 있습니다.
Flask: Flask는 Python 기반의 경량 백엔드 웹 프레임워크로, 간단한 구조와 직관적인 문법으로 배우기 쉽습니다. Python에 익숙하다면 더욱 쉽게 시작할 수 있습니다.

프론트엔드 프레임워크:
Vue.js: Vue.js는 배우기 쉬운 프론트엔드 프레임워크로, 가볍고 간단한 구조를 가지고 있습니다. React나 Angular보다 학습 곡선이 낮아 초보자에게 적합합니다.


디렉토리 구조:
Nuxt.js는 기본적으로 몇 가지 특정한 디렉토리 구조를 가지고 있습니다. 주요 디렉토리는 다음과 같습니다:

pages: 라우트와 뷰를 포함하는 페이지 컴포넌트를 저장하는 곳입니다.
components: Vue.js 컴포넌트들을 저장하는 디렉토리입니다.
layouts: 페이지에 레이아웃을 제공하는 컴포넌트를 저장하는 디렉토리입니다.
assets: 스타일시트, 이미지 등의 자원을 저장하는 디렉토리입니다.
기본 페이지 생성:
Nuxt.js에서는 pages 디렉토리에 있는 파일들이 자동으로 라우트로 매핑됩니다. 예를 들어, pages/index.vue는 웹 애플리케이션의 루트 URL인 /에 대응됩니다. 따라서 필요한 페이지들을 pages 디렉토리에 추가하고 구성할 수 있습니다.

Nuxt.js와 Tailwind CSS 연동:
Nuxt.js에서 Tailwind CSS를 사용하려면, 생성한 프로젝트의 CSS 파일에 Tailwind CSS 스타일을 import해야 합니다. 프로젝트의 assets 디렉토리에 styles.css 파일을 생성하고 다음과 같이 Tailwind CSS 스타일을 추가합니다:

css
Copy code
/* assets/styles.css */
@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';
페이지 및 컴포넌트 생성:
Nuxt.js에서는 pages 디렉토리에 있는 파일들이 페이지로 매핑되며, components 디렉토리에 있는 파일들이 재사용 가능한 Vue 컴포넌트로 사용됩니다.

예를 들어, 간단한 홈페이지를 만들기 위해 다음과 같이 파일들을 생성합니다:

pages/index.vue: 메인 홈페이지를 위한 페이지 컴포넌트
components/Header.vue: 사이트의 헤더 컴포넌트
components/Footer.vue: 사이트의 푸터 컴포넌트
Tailwind CSS 클래스 사용:
Tailwind CSS는 많은 유틸리티 클래스를 제공하여 쉽게 디자인을 구성할 수 있습니다. 예를 들어, 다음과 같이 pages/index.vue 파일에서 Tailwind CSS 클래스를 사용할 수 있습니다:

html
Copy code
<!-- pages/index.vue -->
<template>
  <div>
    <header class="bg-blue-500 py-4">
      <h1 class="text-white text-4xl text-center">Welcome to My Site</h1>
    </header>
    <main class="container mx-auto py-8">
      <p class="text-gray-800 text-lg">Hello, this is a simple Nuxt.js and Tailwind CSS site!</p>
    </main>
    <footer class="bg-gray-300 py-4">
      <p class="text-center">© 2023 My Site. All rights reserved.</p>
    </footer>
  </div>
</template>