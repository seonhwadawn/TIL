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


