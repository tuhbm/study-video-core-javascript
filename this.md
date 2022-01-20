# this

## this 바인딩(this binding)
- this의 바인딩은 함수가 호출될때 결정된다.
    * 호출방식에 따라 달라진다
        - 전역공간에서 호출시
            - window / global
        - 함수로 호출시 
            - ES5 => window / global
            - ES6 => arrow function의 경우는 상위 컨텍스트의 this
        - 메서드로써 호출시
            - 메서드 호출 주체 a.b(); 의 경우 a가 this 
            - this 우회법
                - self 우회법 사용(스코프체인)
                - arrow function 사용
                - apply, call
                    - call
                        - 실행과 동시에 this 바인드
                    - apply
                        - 실행과 동시에 this 바인드
                    - bind
                        - this 바인드 후 실행가능
        - callback으로 넘겨 호출시
            - 기본적으로는 함수내부에서와 동일
            - 실행시점에 따라 변화 => 콜백실행시 call || apply || bind 등을 통해 지정된 this 
        - 생성자 함수로써 호출시(new 연산자 사용)
            - 인스턴스 자신
            
![data type](img/this.PNG)
