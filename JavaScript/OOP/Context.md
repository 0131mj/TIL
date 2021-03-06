# Value Context vs Identifier Context

> " 객체지향은 값을 사용하지 않는다. "

```javascript
const a = {
    a:3,
    b:5
}

const b = {
    a:3,
    b:5
}

console.log(a === b) // identifier Context
console.log(JSON.stringify(a) === JSON.stringify(b))// value Context
```

- 객체지향은 Value Context를 기조로 하고, 함수형 프로그래밍은 Identifier Context를 기조로 한다.
- 객체지향은 철저하게 값 컨텍스트를 배제한다. 
- 객체지향에서 값을 쓸 수 있는 유일한 순간은, 생성자에서 값을 받을 때 뿐이다.



## value context

- 끝없는 복사본을 만든다.
- 상태 변화에 안전하다. (하지만 새로운 값을 만들기 때문이므로 보장하지 않는다.)
- 연산을 기반으로 로직을 전개



## Identifier context

- 하나의 원본
- 상태 변화를 내부에서 책임짐
- 메시지를 기반으로 로직을 전개



# 객체지향의 필수조건

```javascript
const EssentialObject = class{
    
    /* hide state*/
    #name="";
    #screen = "";
    
    constructor(name){
        this.#name = name;        
    }

	camoflage(){
        this.#screen = (Math.random() * 10).toString(16).replace(".", "");
    }

	/* encapsulation */
	get name(){
        return this.#screen || this.#name;
    }
}
```

### hide state

### encapsulation

- 추상화 : 바깥에서는, name 이 내부적으로 어떤 값을 사용해서 보내는지 (원래 이름인지 위장된 스크린의 이름인지) 알 수 없다.





# Isolation of change : 격리

격리벽 세우기 : 오염되지 않는 시스템

