# 변수, 연산자, 반복문

## 변수 Variable

* 초기화
  * 초기화되기 전에 사용되면 에러
  * 이를 방지하기 위해 옵셔널 타입으로 선언함
  * 임시타입이 이를 방지함
* 변수의 활용
  * 사용하거나 할당하거나 두가지 중 하나

## 타입 Type

* 타입 안정성
  * 한번 타입을 선언하면 바꿀 수 없다.
  * js, python은 가능

## 연산자

* 나누기 연산자
  * 나누기 연산자는 정수끼리의 연산일 경우에는 ‘몫’만을 의미함

```swift
Double(5/4) // == 1
Double(5)/Double(4) // == 1.25
```

* 삼항연산자
  * Swift는 단 하나의 삼항연산자를 허용
    * `30 < a < 70` 등은 불가능

```swift
let result = score>70 ? "Pass" : "Fail"
```

*   패턴매칭연산자

    ```swift
    a...b ~= age // 변수가 범위에 속하는지 참거짓 판별
    ```

    * 패턴매칭연산자는 내부적으로 하나씩 대입해 같은지 확인 (?)
    * switch문에서 case 판별할 때 내부적으로 패턴매칭연산자 사용

## 튜플 Tuple

* 튜플과 컬렉션의 차이
  * 튜플은 여러 데이터를 묶어서 하나의 값으로 만듦
  * 컬렉션은 하나의 값이 아니라 각각의 값을 바구니처럼 보관
* named tuple

```swift
// 튜플에 변수명처럼 이름을 붙일 수 있음
let tuple = (name: "홍길동", age: 20, address: "서울")

// tuple.0 == tuple.name
```

## 반복문

* 반복상수
  * let으로 선언되어 있음
  * 반복적으로 변수를 바꿔가는 것처럼 보이지만 반복적으로 상수를 선언하는 것
* for VS while
  * 반복횟수 정해져 있거나, 컬렉션, 범위 이용 → for문
  * 반복횟수가 조건에 따라 바뀔 때 → while문
* 제어전송문
  * continue
    * 만난 시점에서 다음 주기로 넘어감
  * break
    * 만난 시점에서 반복문 자체를 종료