forEach: Model
---

아래의 요구사항을 기반으로 Frontend의 기본 패키지구조, 공통 파일, 기본 설정 파일을 생성해주세요.

프로젝트 생성 순서

frontend 폴더 생성 → frontend 하위 패키지 구조 생성 → React + Vite 기반 설정 파일 생성 → React 실행

frontend 패키지 구조
frontend 하위 패키지 구조를 생성할때 아래의 구조로 생성해야합니다:
```
/frontend                  # 통합 프론트엔드 프로젝트 (React + Vite + TypeScript)
  /public
    /favicon.ico          # 파비콘
  /src
    /components
      /common             # 전역 공통 컴포넌트
        /Layout.tsx       # 공통 레이아웃 컴포넌트
        /Loading.tsx      # 로딩 컴포넌트
    /pages                # 페이지 컴포넌트 (React Router 기반)
      /HomePage.tsx       # 메인 홈페이지 (BC별 네비게이션 포함)
    /services             # API 및 비즈니스 로직
      /api
        /client.ts        # Axios 클라이언트 기본 설정
        /interceptors.ts  # API 인터셉터
        /types.ts         # API 관련 타입
    /types                # TypeScript 타입 정의
      /common.types.ts    # 공통 타입 정의
      /api.types.ts       # API 관련 타입
    /utils                # 유틸리티 함수
      /constants.ts       # 상수 정의 (API 엔드포인트 등)
    /theme                # Material-UI 테마 설정
      /index.ts           # 통합 테마 설정
    /App.tsx              # 루트 App 컴포넌트
    /main.tsx             # Vite 엔트리포인트
    /index.css            # 전역 스타일
    /vite-env.d.ts        # Vite 타입 정의
  package.json            # NPM 패키지 설정
  vite.config.ts          # Vite 빌드 도구 설정
  tsconfig.json           # TypeScript 설정
  .gitignore              # Git 무시 파일
  ```

유의 사항
1. 기본 파일 생성의 경우 Node22에서도 호환되는 React기반의 프로젝트를 생성하여 실행에 오류가 발생하지 않는 수준으로 생성되어야한다.
2. 패키지 구조 기반 파일을 생성할 때, HomePage.ts의 경우 초기 기본 구성만 되도록 생성해야한다.
