1. 라이프사이클(함수형, 클래스형)

※ 리액트는 클래스형과 함수형으로 컴포넌트를 생성할 수 있는데, 주로 함수형 컴포넌트가 많이 사용된다.

클래스형은 사용하지 않는다고 리액트에서 공식 발표를 했다고 한다.

함수형 컴포넌트의 가장 큰 장점은 간단하게 함축적인 프로그래밍이 가능하다는 것이다.

※ 클래스형 라이프사이클

- render() 메소드와 Component 상속이 필수이다.

- state, props 사용이 불편하고, 많은 메모리 사용한다는 단점이 있다.

※ 함수형 라이프사이클

- 간편한 컴포넌트 선언 및 프로그래밍이 가능하고 React Hook을 사용한다.

- state와 생명주기(Life Cycle) 메소드를 별도로 구현해야 한다. => useState, useEffect 사용

2. React Hooks

- 함수형태의 컴포넌트에서 사용되는 몇가지 기술을 Hook이라고 부른다.

- 함수형 컴포넌트에서도 상태 관리를 할 수 있는 useState, 그리고 렌더링 직후 작업을 설정하는 useEffect 등
  의 기능 등이 있다.

※ 클래스형 컴포넌트를 함수형 컴포넌트로 바꿔야하는 이유!

- react를 배우는 데에 있어서 클래스는 큰 진입장벽이었다. 코드의 재사용성과 코드 구성을 어렵게 만들고, this의 사용이나 이벤트 핸들러의 등록 등 기본적인 JS 문법 사항을 알아야 다룰 수 있기 때문이다. 또한 클래스는 잘 축소되지 않고, reloading을 깨지기 쉽고 신뢰하기 어렵게 만든다. 따라서 react의 최신 기술들이 클래스형 컴포넌트에 효과적으로 적용되지 않았다.

- 클래스의 문법이 어렵다.
- 축소가 어렵다.
- reloading의 신뢰성이 떨어진다.
- 최신 기술의 적용이 효과적이지 않다.

→ 이러한 클래스의 단점들을 함수형 컴포넌트로 커버할 수 있다. 하지만 클래스 컴포넌트의 장점인 state 사용이나 life cycle을 직접 다루는 등의 기능을 사용하지 못한다. 이를 해결하기 위해 Hook이 등장했다.

- Hook은 함수형 컴포넌트가 클래스형 컴포넌트의 기능을 사용할 수 있도록 해주는 기능이다.

- useState와 useEffect를 사용하여 특징적으로 state와 lifecycle과 같은 기능을 사용 가능하게 해준다.
