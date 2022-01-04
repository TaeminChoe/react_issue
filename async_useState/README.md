## state 동기화

![Untitled](https://user-images.githubusercontent.com/92558961/148014587-e2fced54-8b2b-44a1-8e89-e17c8767ecd5.png)

- 15: setToDoList를 통해 입력 받은 todo를 todoList state에 갱신하고자 함
- 22: 갱신된 toDoList를 확인하고자 콘솔로그에 출력

결과.

![Untitled (1)](https://user-images.githubusercontent.com/92558961/148014616-9c168e1c-b312-44d2-99b4-bc58e2c5651d.png)

![Untitled (2)](https://user-images.githubusercontent.com/92558961/148014619-b2b6cb30-6740-4828-94ce-8f39a9e81f20.png)

- 예상 결과 : todo를 입력하고 enter로 submit할 때마다 toDoList에 반영되어 출력
- 출력 결과 : toDoList에 재때 반영되지 않아 todo입력이 밀려 있음.

원인 

- react는 virtual DOM을 이용해 일괄 처리 형식으로 DOM에 접근하게 되기 때문에, 개발자의 의도에 맞지 않게 값 변경이 이뤄지지 않을 수 있다.
- useState는 비동기식으로 처리가 되기 때문이다.

해결 방법

- useEffect를 활용해 toDoList에 변경에 따라 콘솔에 출력하면, 해결할 수 있다.

![Untitled (3)](https://user-images.githubusercontent.com/92558961/148014629-ec18c7b9-b87e-4ed8-857e-aa0729383055.png)

참조: https://jihyee.tistory.com/9?category=0
