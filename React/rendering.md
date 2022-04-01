## 반복되는 컴포넌트

map method를 사용해서 출력한다.
usage
props.item.map(x=>x\*2)

## key?

리액트 입장에서는 새로운 데이터가 담긴 리스트가 추가되어도 걍..거기서 거기로 본다
key없이 state를이용해 새로운 데이터를 추가해서 map을 돌리면

리액트는 map된 모든 아이템을 훑어보고 > 맽 밑에 새로운 div를추가 한 다음> array를 한칸씩 밀어 짝지어주게 되는데,
결론적으로는 돌아가긴 하지만 성능적인 관점에서는 나쁘고, 버그를 일으킬 가능성이 높다. (해당 array값이 맞지 않게 되거나, 사용자 데이터 array가
한칸씩 밀리거나..끔찍!)

이때key를 통해 리액트가 개별 아이템을 식별 할 수 있도록 도와주어야 한다.

결론: map을 사용해서 컴포넌트를 반복시킬거면 key값을(보통은 props.id같이 식별 가능한 고유의 값) 를 꼭 넣어주자

## filter

내장함수 중 하나, 데이터를 필터링 하고싶을때

const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]

형식을 사용하여 데이터 리스트를 반환한다

## 조건부 렌더링

특정조건일때 미리 설정한 다른 출력값을 렌더링 해 두는것

보통은? 

삼항연산자를 활용해서 표현식을 적어둔다
ex: {filteredExpenses.length === 0 ? <p>No Expenes Found</p> : filteredExpenses.map(expense => <ExpenseItem key={expense.id} title={expense.title} amount={expense.amount} date={expense.date} />)}

### 너무 길어요!

그러면 &&을 활용해서 편법을 사용할 수 있다.

### 만약이것도 너무 길다면...

return 전에 변수로 미리 선언한 뒤 코드를 줄일 수 있다. 훨씬 읽기 편해진다. 다만 렌더링 상황에 따라 다르니 잘 생각해서 넣어두자
= lean코드로 작성하기 위한 방법
