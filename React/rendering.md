## 반복되는 컴포넌트

map method를 사용해서 출력한다.
usage
props.item.map(x=>x\*2)

## key?

리액트 입장에서는 새로운 데이터가 담긴 리스트가 추가되어도 걍..거기서 거기로 본다

이때key를 통해 리액트가 개별 아이템을 식별 할 수 있도록 도와주어야 함

결론: map을 사용해서 컴포넌트를 반복시킬거면 key값을(보통은 props.id) 를 꼭 넣어주자

## filter

내장함수 중 하나, 데이터를 필터링 하고싶을때

const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]

형식을 사용하여 데이터 리스트를 반환한다

## 조건부 렌더링

삼항연산자를 활용해서 표현식을 적어둔다
ex: {filteredExpenses.length === 0 ? <p>No Expenes Found</p> : filteredExpenses.map(expense => <ExpenseItem key={expense.id} title={expense.title} amount={expense.amount} date={expense.date} />)}

### 너무 길어요!

그러면 &&을 활용해서 편법을 사용할 수 있다.

### 만약이것도 너무 길다면...

return 전에 변수로 미리 선언한 뒤 코드를 줄일 수 있다. 훨씬 읽기 편해진다. 다만 렌더링 상황에 따라 다르니 잘 생각해서 넣어두자
= lean코드로 작성하기 위한 방법
