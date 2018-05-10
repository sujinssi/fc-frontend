
# 1주차-180510(수)


## [2] Pseudo, algo, data(최우영강사님) 

- 다음주 월요일 퀴즈

## 1. Pseudocode

- 프로그램이나 알고리즘이 수행할 내용을 인간이 이해할 수 있는 언어로 표현하는것. 가짜코드. 
- Pseudocode는 프로그램을 설계할 때 밑그림의 역할을 하게 된다. 목적과 수행과정이 명확해서 코드 수정과 분해가 편리하다. 우리가 하는 코드는 절차지향적이다. 지금 쓰고 있는 객체지향은 좀 다르다. 절차지향은 순서대로 흐르는 느낌이라면, 객체지향은 프로그램에서 중요하다고 생각되는 것 먼저 처리.
-  pseudocode자체가 주석이 될 수 있다. 

* 배포할 때 comment 지우는 툴도 있다. 배포할 때는 지우고 배포하는게 일반적. 
* 그래도 주석다는 습관은 가지면 협업하는데 도움이 된다.
* 자신이 작성할 언어의 스타일에 맞춰서 작성하면 좋다. 

- 슈도코드로 fizzbuss를 만들어보자! : 1 부터 n 까지 반복하면서, 3의 배수는 "fizz" 5의 배수는 "buzz" 15의 배수는 "fizzbuzz" 나머지는 숫자

[내가 한  것]
1. 사용자로부터 숫자 하나를 받아 n에 할당한다
2. 1부터 사용자로부터 입력받은 숫자(number)까지 출력한다
3. A가 3의 배수일 때 “fizz”를 출력
- A를 3으로 나눴을 때 나머지가 0이면 “fizz”를 출력한다
- 3으로 나눴을 때 나머지가 0이 아니면 들어온 값을 그대로 리턴한다
3. b가 5의 배수일때 “buzz”를 출력
- b를 5로 나눴을 때 나머지가 0이면 “buzz”를 출력한다
- 5로 나눴을 때 나머지가 0이 아니면 들어온 값을 그대로 리턴한다
4. C가 15의 배수일 때 “fizz buzz”를 출력한다.
- C를 15로 나눴을 때 나머지가 0이면 “fizz buzz”를 출력한다.
- c를 15로 나눴을 때 나머지가 0이 아니면 들어온 숫자를 그대로 출력한다. 

[강사님 코드]
1. 사용자로부터 숫자 하나를 받아 n에 할당한다
2. 1부터 n까지 숫자를 진행시키면서,
    1. 만약 해당 숫자가 15의 배수라면 “fizzbuzz”를 출력 (큰 공배수 먼저 써야함)
    2. 만약 해당 숫자가 3의 배수라면 “fizz”를 출력
    3. 만약 해당 숫자가 5의 배수라면 “buzz”를 출력
    4. 만약 1,2,3의 경우를 만족시키지 못한경우 해당 숫자를 출력한다

-> *순서를 15, 5, 3으로 바꿔주면 더 효율적.* 컴퓨터가 코드를 좀 더 적은 횟수로 읽기 때문. 
3은 33번 읽고 5는 20번읽는데 양 많은 것을 올려주면 좋다. 적은 숫자가 내려가니까.

1. get integer from user ==> num, i == 1
2. WHILE i is less than or equal to num
3. if i is divisible by 15, print "fizzbuzz"
4. if i is divisible by 3, print "fizz"
5. if i is divisible by 5, print "buzz"
6. else, print i

```
num = input("get number for fizzbuzz: ")
i = 1
for i in range(1,100+1):
	if i % 3 == 0:
		print("fizz")
	elif i % 5 == 0:
		print("buzz")
	elif i % 15 == 0:
		print("fizzbuzz")
	else:
		print(i)
```

[부가가치세]
- 내가 짠 코드
1. 사용자에게 물건의 가격과 국가코드를 받는다
2. 국가 코드가 한국일 경우,
    1. a += a*0.1, print a
3. 국가 코드가 Japan,
    1. B += b*0.08, print b
4. 국가코드 USA,
    1. print “It depends on states.”
5. 국가코드 UK,
    1. C += c*0.2, print c

[Eng]
1. Get integer from user ==> price, get text from user => nation
2. If nation == Kor, price += price*0.1, print price
3. if else nation == Jap, price += price*0.08, print price
4. if else nation == USA, print “각 주 별로 상이합니다.”
5. if else nation == UK, price += price*0.2, print price
6. Else, print “잘 못 입력하셨습니다.”


[강사님 짜신 pseudocode 코드]
1. get price of item ==> item_price
2. set tax rate (kor == 0.1, jap == 0.08, usa == "depend on state", uk == 0.2)
3. get contry code(example: kor, jap, usa, uk) ==> contry_code
4. tax_rate is matched price with contry_code
5. sales tax is item_price times tax rate
5. total price is item_price plus sales tax


-------

## 2.  Algorithm

### **"코드를 수행하는 과정"**

알고리즘의 중요성이 점점 대두되고 있다.
목표를 달성하거나 결과물을 생산하기 위해 필요한 과정.
프로그래밍은 절차지향적이기 때문에 알고리즘이 중요한 것.

Clarity // 다이아몬드와 같은 것? 읽었을 때 읽히는 것

----

## **시간복잡성 big o notation**


        1 => constant

        log n => logarithmic

        n => linear

        $n^2$ => quadratic

    O(1) : constant
    값에 대한 키 또는 인엑스를 알고 있을 경우.
    random access와 같이. 바로 떨어지는 것이라 1

    O(log n) : logarithmic
    배열에서 값을 접근할 때(바로 찾아가는 것이 아니라 0번째부터 순차적으로 찾아가는 것.)
    앞 또는 뒤에서 접근이 가능할 경우. (순회가능한 객체)
    그래서 1과 n사이에 있다는 의미에서 log n 

    O(n) : linear
    자료의 수와 시도횟수가 *1:1* 관계인 경우
    (반복문 하나 쓰면 벌어지는 일, n번 반복하기 때문에 n이라고 하는 것)

    ```
    result = 0
    for i in range(1,10+1):
        for j in range(1,j+1):
            result += j
    ```

    O($n^2$): quadratic
    자료의 참조를 이중으로 하게 될 경우
    (이 경우까지 가지 않는게 좋음)

정렬알고리즘 때문에 시간복잡도를 알아본 것
Sort algorithms

----------

* O($n^2$)
    - Bubble sort : 뒤에서부터 요소를 하나 잡은 뒤에 그 전 것과 비교. 1:1로 비교하기 떄문에 비효율적.구현은 쉽지만 최악. 안쓰는게 좋다
    - Selection sort : 가장 작은 것을 선택해서 시작한 시점의 다음에 붙임.
    - Insertion sort

* O(n log n)
    - Merge sort : 섹션을 잘라서 정렬. 피봇을 두고 앞뒤값을 정렬하고 그다음 섹션을 정렬. 두개씩 쪼개 각각을 비교하며 정렬하는 방법. 계속 합치는 방식. 데이터 상테에 영향을 받지 않음
    - Heap sort : 잘라놓은 다음 최대값을 가져와서 집에 넣는 구조. 하나의 부모에 두개의 자식이 있다. heap은 틀. 
    - Quick sort : 정렬알고리즘 중에서 우리가 유일하게 해봐야 할 것. 퀵소트만 구현해보라. 기술면접준비하면서. 평균적으로 가장 빠른 방법. 피벗을 기준으로 큰값, 작은 값을 나눈 뒤, 피벗을 다시 옮겨 수행하는 방법

데이터가 정렬되어 있는 방식에 따라서 전자가 빠를 수도, 후자가 빠를 수도 있다. 

------

## 3. Data Structure(자료구조)

### "데이터를 쌓는 방법"

Data structure is a particular way of organizing data in a computer so that it can be used efficiently.

----

## 웹개발에서 자료구조

Array & Hash(Dictionary) - indexing post

* Array : 관계형 데이터베이스. 엑셀과 같이 테이블. 이중어레이.

* Hash : 

cf. No SQL(테이블처럼 생기지 않은 데이터베이스)

* Tree : DOM rendering performance, reply

    - 상하관계를 규정하기 위한 자료구조. 웹서버에서 넘어올때는 글자로 넘어온다. 브라우저가 랜더링 과정을 거치는데, 파싱하는 과정에서 상하의 구조를 파악하는 것. 브라우저가 효율적으로 파싱할 수 있도록, 하위구조를 인식할 수 있도록 하는 것이 코드를 짜는 것이 좋다. 

* Binary Tree Search

    - pagenation -> 다음 페이지로 넘어감. 최신 30개가 모이는 게시판이 있으면 트렌드가 형성되기 쉬움. 
    - 스레드 -> 한 주제에 집중이 가능함. 

    1. Stack(DFS, Depth First Search)

        A stack is an abstract data type that serves as a collection of elements, with two principal operations.

        밑이 닫혀있는 휴지통. 그래서 들어가는 순서와 나가는 순서가 다르다.

        * push: which adds an element to the collection
        * pop: which removes the most recently added element that was not yet removed

        그래서 **"Last In, First Out(LIFO)"**


셀레늄 라이브러리. 웹개발을 끝낸 후 to be a customer 셀레늄이랑 자스 같이 써서 좌석 예매 매크로 가능.


```
function Stack() {
	var items = [];

	this.push = function(element) {
		return items.push(element);
	};

	this.pop = function(){
		return itmes.pop()
	};

};
//stack을 선언한 것

var glass = new Stack();
glass.push('maek-ju');
//1 출력. 1개 쌓였다는 의미
glass.push('so-ju')
//2 출력. 2개 쌓였다는 의미
glass.push();
//"so-ju" 출력. 맨 위에 있던 소주 빼남
glass.pop()
//"maek-ju"출력. 맨 위에 있는 맥주 빼냄.

//peek를 만들어 보자

    this.peek = fuction(){
        return items[items.length1-1]
    }

//peek만든게 되는지 보자

var glass = new Stack();
glass.push('maek-ju');
//1
glass.push('so-ju);
//2
glass.peek();
//'so-ju'

//그럼 이 술잔이 비어있다는 건 어떻게 확인할까? -> 개수가 0일 것.
var glass = new Stack();
glass.push('maek-ju');
//1
glass.push('so-ju);
//2
glass.peek() = function(){
    return items[items.length-1];
};
//'so-ju'


    this.isEmpty = function(){
       itmes.length == 0;
    };

//Empty를 확인해보자.
var glass = new Stack();
glass.isEmpty();
//true
glass.push('maek-ju');
//1
glass.isEmpty();
//false

size, clear, print구현해보자

    this.size = function() {
        return items.length;
    }
    this.clear = function() {
        items= [];
    }
    this.print = functiong(){
            return console.log(items.toString());
    }
    
var glass = new Stack();
glass.size();
// 0 
glass.push('make-ju')
//1
glass.push('soju');
galss.clear();
glass.isEmpty
//true
glass.push('coke');
//1
glass.push('so-ju');
//2
glass.push('maek-ju');
//3
...
```

-----

2. Queue(BFS, Breadth First Search

+ 파이퍼라인 같은 것. 
+ a queue is a particular kind of abstract data type or collection in which the entities in the collection are kept in order.

**"First In First Out"**

* Enqueue : addition of entities to the rear terminal position
* Dequeue : removal of entities from the front terminal position

<pre><code>
var Queue = function() {
    var items = [];

    this.enqueue = function(element) {
        return items.push(element);
    };

    //배열의 첫번째 요소를 제거하는데는 .shift()
    this.dequeue = function(){
        return items.shift();
    }
};

var hyperloop = new Queue();
hyperloop.enqueue('musk');
hyperloop.enqueue('good');
hyperloop.enqueue('mama');hyperloop.enqueue('musk');

hyperloop.dequeue
</pre></code>

stack이랑 Queue의 차이만 알면 됨

* Linked List

    + 자스는 어레첫번째 값을 주고 두번째 값이 들어갈 주소를 준다. **값-다음행선지**를 주는게 linked list.

    + A linked list is **a linear collection** of data elements, in which linear order is not given by their physical placement in memory.

* Tree

    + A tree is an abstract model of a hierarchical structure.
        (hierarchical: arranged in order of rank.)

    + 동그라미를 node, 화살표를  edge라고 함.

* 저 트리를 탐색하는 것을 stack을 쓰느냐, queue를 쓰느냐에 따라 진행방향이 달라짐. 
