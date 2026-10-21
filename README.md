## 1. JavaScript 자료형 (Data Types)
* **`number`** : 정수와 실수를 모두 포함하는 숫자 타입
* **`string`** : 따옴표(`'`, `"`, `` ` ``)로 감싸진 문자열 텍스트
* **`boolean`** : 참(`true`)과 거짓(`false`)을 나타내는 논리 타입
* **`null`** : 비어 있는 상태를 의도적으로 명시한 값
* **`undefined`** : 변수는 선언되었으나 아직 값이 할당되지 않은 상태

```javascript
// [JS 실습 사례]
let age = 25;           // number
let name = "Alice";     // string
let isSubscribed = true;// boolean
let emptyValue = null;  // null
let notDefined;         // undefined
```
> 🔹 <font color="blue">Python 비교 : 파이썬은 정수(int)와 실수(float)를 구분하며, boolean은 첫 글자가 대문자인 True, False를 씁니다. null 대신 None을 사용하고, undefined 개념은 존재하지 않습니다.</font>
```python
# <font color="blue">[Python 실습 사례]</font>
# <font color="blue">age = 25                # int</font>
# <font color="blue">price = 19.99           # float</font>
# <font color="blue">name = "Alice"          # str</font>
# <font color="blue">is_subscribed = True    # bool</font>
# <font color="blue">empty_value = None      # NoneType</font>
```

---

## 2. JavaScript 변수 선언
* **`let`** : 변수 값을 추후에 변경(재할당)할 수 있는 선언 방식
* **`const`** : 한 번 할당하면 값을 바꿀 수 없는 상수(Constant) 선언 방식

```javascript
// [JS 실습 사례]
let count = 10;
count = 20; // 가능 (재할당 가능)

const PI = 3.14;
// PI = 3.14159; // 에러 발생 (상수 재할당 불가)
```
> 🔹 <font color="blue">Python 비교 : 변수 선언 키워드(let, const)가 없으며 모두 자유롭게 재할당 가능합니다. 문법적인 상수가 없어 관례상 대문자로 표기하여 상수로 취급합니다.</font>
```python
# <font color="blue">[Python 실습 사례]</font>
# <font color="blue">count = 10</font>
# <font color="blue">count = 20  # 가능 (언제나 재할당 가능)</font>
# <font color="blue">PI = 3.14   # 재할당은 가능하나 관례상 상수로 취급</font>
```

---

## 3. JavaScript 연산 방법
* **`+`, `-`, `*`, `/`** : 기본 사칙연산
* **`%`** : 나눗셈의 몫을 제외한 **나머지 연산**
* **`Math`** : 수학적 계산을 처리하는 **내장 객체**

```javascript
// [JS 실습 사례]
let remainder = 10 % 3;        // 1
let rounded = Math.round(4.6); // 5 (반올림)
let absolute = Math.abs(-10);  // 10 (절대값)
```
> 🔹 <font color="blue">Python 비교 : 정수 몫만 구할 때는 // 연산자를 따로 사용합니다. 수학 연산은 기본 내장 함수를 쓰거나 복잡한 계산은 import math 모듈을 불러와서 처리합니다.</font>
```python
# <font color="blue">[Python 실습 사례]</font>
# <font color="blue">remainder = 10 % 3        # 1</font>
# <font color="blue">quotient = 10 // 3         # 3 (정수 몫 연산자)</font>
# <font color="blue">rounded = round(4.6)       # 5</font>
# <font color="blue">absolute = abs(-10)        # 10</font>
```

---

## 4. JavaScript 비교 연산
* **`<`, `>`, `<=`, `>=`** : 값의 대소 비교
* **`==` (동등 연산자)** : 값만 비교 (타입이 달라도 표기 형태가 같으면 참으로 인정)
* **`===` (일치 연산자)** : 값과 데이터 타입까지 엄격하게 비교 **(실무 권장)**
* **`typeof`** : 데이터의 자료형을 확인하는 키워드

```javascript
// [JS 실습 사례]
console.log(5 == '5');  // true  (자동 형변환 발생)
console.log(5 === '5'); // false (타입이 달라 거짓)
console.log(typeof 5);  // "number"
```
> 🔹 <font color="blue">Python 비교 : 파이썬의 기본 == 연산자는 자바스크립트의 ===처럼 데이터 타입까지 엄격하게 비교하는 것이 기본 원칙입니다. 타입 확인은 type() 함수를 사용합니다.</font>
```python
# <font color="blue">[Python 실습 사례]</font>
# <font color="blue">print(5 == '5')  # False (파이썬은 타입 자동 변환을 하지 않음)</font>
# <font color="blue">print(type(5))   # <class 'int'></font>
```

---

## 5. JavaScript 논리 연산
* **`&&`** : **and 연산자** (모든 조건이 참일 때 참 반환)
* **`||`** : **or 연산자** (조건 중 하나라도 참이면 참 반환)
* **`!`** : **not 연산자** (부정 연산자, 참/거짓의 논리 상태를 뒤집음)

```javascript
// [JS 실습 사례]
let isAdult = true;
let hasTicket = false;

console.log(isAdult && hasTicket); // false
console.log(isAdult || hasTicket); // true
console.log(!isAdult);             // false
```
> 🔹 <font color="blue">Python 비교 : 특수 기호 대신 직관적이고 가독성이 좋은 문자 키워드인 and, or, not을 그대로 사용합니다.</font>
```python
# <font color="blue">[Python 실습 사례]</font>
# <font color="blue">is_adult = True</font>
# <font color="blue">has_ticket = False</font>
# <font color="blue">print(is_adult and has_ticket)  # False</font>
# <font color="blue">print(is_adult or has_ticket)   # True</font>
# <font color="blue">print(not is_adult)             # False</font>
```

---

## 6. JavaScript 문자열 연산
* **`+` (이어붙이기)** : 문자열끼리 결합하거나, 문자열과 다른 자료형을 연결
* **`템플릿 리터럴`** : 백틱(`` ` ``)과 `${변수명}`을 활용한 문자열 결합
* **`number + string`** : 숫자와 문자열을 더하면 숫자가 문자로 자동 변환되어 결합

```javascript
// [JS 실습 사례]
let name = "Alice";
console.log(`Hello, ${name}!`); // "Hello, Alice!"
console.log(10 + "20");        // "1020" (오류 없이 문자열로 결합)
```
> 🔹 <font color="blue">Python 비교 : 문자열과 숫자를 + 연산자로 더하면 TypeError가 발생하므로 str(10)처럼 명시적으로 형변환을 해야 합니다. 문자열 내 변수 삽입은 f-string(f"{변수}") 문법을 씁니다.</font>
```python
# <font color="blue">[Python 실습 사례]</font>
# <font color="blue">name = "Alice"</font>
# <font color="blue">print(f"Hello, {name}!")     # f-string 문법</font>
# <font color="blue"># print(10 + "20")           # TypeError 에러 발생</font>
# <font color="blue">print(str(10) + "20")        # "1020" (명시적 형변환)</font>
```

---

## 7. JavaScript 조건문
* **`if`** : 조건이 참일 때 실행할 코드 블록
* **`else if`** : 앞선 조건이 거짓일 때, 새로운 조건을 검사
* **`else`** : 모든 조건이 거짓일 때 최종적으로 실행할 코드 블록

```javascript
// [JS 실습 사례]
let point = 85;

if (point >= 90) {
    console.log("A");
} else if (point >= 80) {
    console.log("B"); // 실행됨
} else {
    console.log("C");
}
```
> 🔹 <font color="blue">Python 비교 : else if 대신 축약어인 elif 키워드를 사용합니다. 코드 블록을 중괄호 {} 대신 콜론(:)과 공백 들여쓰기로 구분하는 것이 차이점입니다.</font>
```python
# <font color="blue">[Python 실습 사례]</font>
# <font color="blue">point = 85</font>
# <font color="blue">if point >= 90:</font>
# <font color="blue">    print("A")</font>
# <font color="blue">elif point >= 80:     # elif 사용</font>
# <font color="blue">    print("B")</font>
# <font color="blue">else:</font>
# <font color="blue">    print("C")</font>
```

---

## 8. JavaScript 반복문
* **`for`** : 지정된 횟수나 인덱스 조건에 따라 루프 반복
* **`while`** : 조건식이 참(true)인 동안 계속해서 반복

```javascript
// [JS 실습 사례]
for (let i = 0; i < 3; i++) {
    console.log(i); // 0, 1, 2 출력
}

let count = 0;
while (count < 3) {
    console.log(count);
    count++;
}
```
> 🔹 <font color="blue">Python 비교 : for i in range(3): 구조를 사용하여 범위를 지정하거나 연속된 자료형 내부를 순회합니다. 파이썬에는 ++ 증감 연산자가 없으므로 += 1을 사용합니다.</font>
```python
# <font color="blue">[Python 실습 사례]</font>
# <font color="blue">for i in range(3):</font>
# <font color="blue">    print(i)          # 0, 1, 2 출력</font>
# <font color="blue">count = 0</font>
# <font color="blue">while count < 3:</font>
# <font color="blue">    print(count)</font>
# <font color="blue">    count += 1        # += 1 사용</font>
```

---

## 9. JavaScript 배열 (Array)
* **`array 사용법`** : 대괄호(`[]`)를 사용해 여러 데이터를 순서대로 저장하는 자료형
* **`array의 활용`** : 크기 확인(`.length`) 및 요소 추가(`.push()`) 등의 배열 제어

```javascript
// [JS 실습 사례]
let fruits = ["사과", "바나나"];
fruits.push("오렌지"); // 배열 끝에 데이터 추가

console.log(fruits[1]);     // "바나나" (0부터 시작하는 인덱스 접근)
console.log(fruits.length); // 3 (배열 크기 확인)
```
> 🔹 <font color="blue">Python 비교 : 배열과 매칭되는 개념을 리스트(List)라고 부르며, 요소를 끝에 추가할 때는 .append()를 사용하고 리스트의 크기를 구할 때는 len() 함수를 사용합니다.</font>
```python
# <font color="blue">[Python 실습 사례]</font>
# <font color="blue">fruits = ["사과", "바나나"]</font>
# <font color="blue">fruits.append("오렌지")   # append 사용</font>
# <font color="blue">print(fruits[1])         # "바나나"</font>
# <font color="blue">print(len(fruits))       # 3 (len 함수 사용)</font>
```

---

## 10. JavaScript 객체 자료형 (Object)
* **`object 선언`** : 중괄호 `{}` 내부에 키(Key)와 값(Value)의 쌍으로 구조화된 데이터 정의
* **`object 다루기`** : 점 표기법(`.`)을 통한 속성 읽기/추가/수정/삭제 및 존재 여부(`in`) 확인

```javascript
// [JS 실습 사례]
let user = { name: "John", age: 30 };

console.log(user.name);      // "John" (점 표기법으로 읽기)
user.job = "Developer";      // 동적으로 새로운 속성 추가
delete user.age;             // 속성 제거
console.log('name' in user); // true (속성 존재 여부 확인)
```
> 🔹 <font color="blue">Python 비교 : 객체에 상응하는 자료구조를 딕셔너리(Dictionary)라고 부릅니다. 점 표기법(user.name)은 불가능하며 반드시 대괄호(user["name"])로만 접근해야 합니다. 제거 시에는 del 키워드를 씁니다.</font>
```python
# <font color="blue">[Python 실습 사례]</font>
# <font color="blue">user = { "name": "John", "age": 30 }</font>
# <font color="blue">print(user["name"])      # 대괄호 표기법만 가능 (user.name 불가)</font>
# <font color="blue">user["job"] = "Developer" # 속성 추가</font>
# <font color="blue">del user["age"]          # del 키워드로 제거</font>
# <font color="blue">print("name" in user)    # True</font>
```

---

# JavaScript vs Python 기초 개념 비교 정리

| 핵심 개념 | JavaScript (자바스크립트) | Python (파이썬) |
| :--- | :--- | :--- |
| **변수 선언 키워드** | `let`, `const` 필요 | 키워드 없음 (변수명에 바로 할당) |
| **상수 선언 제한** | `const`로 강력한 제한 가능 | 문법적 상수 없음 (관례상 대문자 표기) |
| **비어있는 값** | `null` / `undefined` 구분 | `None` 하나로 통일 |
| **논리 연산자** | `&&`, `\|\|`, `!` (기호 사용) | `and`, `or`, `not` (영단어 사용) |
| **동등/일치 연산** | `==` (값만 비교), `===` (타입까지 비교) | `==` (값과 타입 엄격히 모두 비교) |
| **타입 확인** | `typeof` 키워드 | `type()` 함수 |
| **숫자 + 문자 연산** | 숫자가 자동으로 문자로 변환되어 결합 | `TypeError` 발생 (명시적 형변환 필수) |
| **문자열 내 변수 삽입**| 템플릿 리터럴 (백틱 + `${변수}`) | f-string (`f"{변수}"`) |
| **구문 영역 구분** | 중괄호 `{}` 블록 형태 | 콜론(`:`) 및 들여쓰기 (Indentation) |
| **조건문 중간 분기** | `else if` | `elif` |
| **선형 순서 자료구조** | 배열 (`Array`) / 크기는 `.length` | 리스트 (`List`) / 크기는 `len()` |
| **키-값 쌍 자료구조** | 객체 (`Object`) / 점 표기법(`.`) 지원 | 딕셔너리 (`Dictionary`) / 대괄호만 가능 |
