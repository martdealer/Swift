# 기본개념과 형태

### 개념

***

* `익명함수`
  * 함수의 이름은 재사용 시 호출하기 위한 목적 → 재사용이 필요하지 않은 일회성 함수
* 함수와 완전히 동일하지만 형태만 다르다.
* 함수를 포함하는, 함수보다 큰 개념
* 스위프트는 함수를 `일급객체`로 취급한다
  * 일급객체 취급 == 타입으로 취급 → 변수에 할당, 파라미터, 반환형으로 사용 가능하다.
  * (참고) 프로토콜도 일급객체



### 기본형태

***

```swift
{(a: Int, b: Int) -> Int in

	return a+b

	}
```



### 축약형태 - 타입 생략

***

1. `output type` 생략 가능

```swift
{(a: Int, b: Int) in

	return a+b     // output type 추론 가능 

	}
```

> `output type` 은 추론가능하므로 클로저 사용시 일반적으로 생략



2. `input type` 생략 가능

```swift
let closure1 : (Int, Int) -> Int = {(a,b) in  // input type 추론 가능

	return a+b     // output type 추론 가능
	}
```

> `input type` 은 \[추론 가능한 경우]에만 축약 가능



3. Void → Void 인 경우(단순실행문) `in` 도 생략 가능

```swift
let closure2 = { print("안녕") } 
```
