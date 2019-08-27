# react-redux-portal
  webpack + react + redux

# build command
    npm start : start local node server + npm run dev
    npm run build : prod build
    npm run dev : dev build
    npm run lint : check eslint
    npm test : run test by jest
    npm run analyze : analyze bundle file
    npm run eslint-check : check lint & prettier formatting rules
    npm run storybook : run storybook

# 폴더구조
    Apis : 외부 자원에 접근하기 위한 인터페이스 정의 
    Components : 리액트 컴포넌트
      -Atoms
        웹 구성의 기본 블록 컴포넌트 (example : input, label …)※ 현재 project에선 대부분이 도입하여 사용중인 UI-Component가 대체
      -Molecules
        atom을 조합하여 사용한 구조화된 컴포넌트 (example : form input+label …)단일책임의 원칙을 준수하며, 한가지 기능단위로 수행
        ※ additional inner rules
          atomic design 기조와 별개로 molecules의 경우, presentational 성격을 지향하였다.  (물론 아닌 것들도 있다!)
          - state가 없게
          - component props로만 동작하도록 설계
      -Organisms
         molecule/atom들을 결합하여 형성 (example : GNB/LNB, account status selectbox)
         독립적이고, 호환가능하며, 재사용 가능하게 만들어야함
         ※ additional inner rules
          업무영역을 포함하는 컴포넌트로, 독자적인 비즈니스 기능 수행이 가능하도록 설계
          자체 state가 관리됨. 글로벌 상태 사용도 되도록 유기체부터 사용을 지향
      -Templates
        레이아웃 역할을 담당 (example : home, contents layer)
        atom/molecules/organisms의 배치형태를 관리한다.
        배치될 component영역이 비어져있고, component크기와 위치를 결정하며, props로 componen를 받아 render 하는 역할
      -Pages
        앞선 component들을 모두 사용하여 구성됨
        하나의 page view를 이루는 component
    Constants : 상수
    I18n : 국제화처리를 위한 리소스
    Modules : 외부 모듈 (Adaptor Pattern 성격)
    Redux : 전역 상태 관리
    Utils : 유틸성/공유 메소드

# 국제화
    react-intl - https://github.com/formatjs/react-intl
    
# UI component
    reactstrap - Stateless React Components for Bootstrap 4. https://reactstrap.github.io/
    editor - react-quill (https://github.com/zenoamaro/react-quill)
    table- React-virtualized (https://github.com/bvaughn/react-virtualized)
