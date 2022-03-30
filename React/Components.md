## 컴포넌트

"Components" are really just a way of thinking about user interfaces. React embraces that concept and gives you tools to build components that you can then combine.

UI 요소를 잘게 쪼갠 것

쪼개는팁

- 기능별로
- UI별로 쪼개서
  나중에 페이지가 12311648개일때 슬기롭게 뽑아다 쓸 수 있게 하자! 초반빌딩이 중요하다.

## Sateful컴포넌트, stateless컴포넌트

보통 컴포넌트를 잘게 쪼개서 사용하는데 컴포넌트도 stateful 컴포넌트와 stateless컴포넌트 두개로 나뉜다.

### State 컴포넌트

말그대로 state를 사용하는 컴포넌트

`class Clock extends React.Component { constructor(props) { super(props); // state 를 생성한다. this.state = {date: new Date()}; } render() { return ( <div> <h1>Hello, world!</h1> {/_ state 의 date 값을 사용한다 _/ } <h2>It is {this.state.date.toLocaleTimeString()}.</h2> </div> ); } }`

### stateless컴포넌트

데이터를 출력하기 위해서만 존재하는 컴포넌트 =state를 사용하지 않는 컴포넌트
애플리케이션을 작게 사용할 수 있는 컴포넌트로 맞추기 때문에 출력용의 기능만 가지는 컴포넌트가 생김. 보통 소수의 컴포넌트만 state를 제어하고, 그걸 props를 통해 pass한다.

`function Clock(props) { return ( <div> <h1>Hello, world!</h1> <h2>It is {this.props.date.toLocaleTimeString()}.</h2> </div> ); }`

