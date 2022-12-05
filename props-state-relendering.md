<!-- <state와 props의 차이>
props처럼 App 컴포넌트의 렌더링 결과물에 영향을 주는 데이터를 갖고 있는 객체
props는 컴포넌트에 전달되는 반면 state는 컴포넌트 안에서 관리된다.
props를 사용했는데도 state를 사용하는 이유는 사용하는 쪽과 구현하는 쪽을 철저하게 분리시켜서 양쪽의 편의성을 각자 도모하는 것에 있다.

<사용하는 법>
state객체를 사용하고 싶다면 컴포넌트를 생성할 때 가장 윗부분에 constructor() 함수를 적어준다.
컴포넌트 생성자에서 super를 호출하기 전에는 this를 사용할 수 없기 때문이다. -->

class App extends Component { constructor(props) { super(props); this.state={
Subject:{title:'WEB',sub:'월드와이드웹!'} } } render() { return (

<div className="App">
  <Subject title="{this.state.subject.title}" sub="{this.state.subject.sub}">
  </Subject>
</div>
); }

<!-- <state와 props의 차이점>
    화면에 출력되는 내용은 완전히 똑같지만, props 데이터를 사용자에게 노출되는 부분에 직접 적는 것이 아니라 S
    tate를 통해 참조했다는 차이가 있다. 즉, 사용자가 알 필요가 없는 데이터를 내부에서 은닉하는 것.
    즉, 캡슐화를 통해 코드를 리펙토링 하는 것이 좋은 사용성을 만드는 핵심이다. -->

class App extends Component { render() { return (

<div className="App">
  <Subject title="WEB" sub="월드와이드웹!"></Subject>
</div>
); } }
<!-- 위 코드는 State를 사용해 수정하기 전, 즉 Props만 사용했을 때 App 컴포넌트의 모습이다. -->

<!-- <리렌더링이 되는 조건>
    state 변경이 있을 때
-   react 에서 유동적인 데이터를 저장하기 위해서 state 라는 것을 이용한다.
    이때 state 값을 바꿔주기 위해서는 state 를 직접 조작해서는 안되고 setState() 메서드를 이용해 주어야한다. 왜냐하면 리액트는 state 의 변경이 감지되면 리렌더링을 해주는 데 메서드를 사용하지 않고 직접 바꿔주게 되면 리액트가 state 의 변경을 감지하지 못하게 된다.
    새로운 props이 들어올 때
-   전달받은 props 값이 업데이트 됬다면 리 렌더링 된다.
    부모 컴포넌트가 렌더링 될 때
-   새로운 prop 이 들어오지 않더라도 부모컴포넌트가 리렌더링 된다면 자식컴포넌트 역시 리렌더링이 된다.

 -->
