# Data Type

---

프로그래밍을 할 때 쓰이는 숫자, 문자열 등의 자료 형태로 사용하는 그 모든 것을 뜻한다.

## 1. 숫자

- 정수 : 자바의 정수를 표현하기 위한 자료형은 int, long 이다.
(byte, short 등도 있지만 잘 사용하지 않는다.)
    - int와 long의 차이는 표현할 수 있는 숫자의 범위이다.
    
    | 자료형 | 표현범위 |
    | --- | --- |
    | int | -2147483648 ~ 2147483647 |
    | long | -9223372036854775808 ~ 9223372036854775807 |

```java
//변수에 값 할당
int age = 10;
long countMyMoney = 8764827384923849L;
```

 -long 변수에 값을 대입할 때는 대입하는 숫자 값이 int 자료형의 최댓값인 2147483647 보다 큰 경우 위 표현과 같이 L 접미사(또는 소문자 l을 사용하지만, 1이나 I(아이) 와 비슷하게 보이므로 L을 쓰도록 하자!)를 붙여 준다. 접미사를 붙이지 않으면 컴파일 에러가 발생한다.

- 실수 : 자바의 실수를 표현하기 위한 자료형은 float, double 이다.
    - float과 double의 차이 또한 표현할 수 있는 숫자의 범위이다.
    
    | 자료형 | 표현범위 |
    | --- | --- |
    | float | -3.4 * 10^38 ~ 3.4 * 10^38 |
    | double | -1.7 * 10^308 ~ 1.7 * 10^308 |

```java
//변수에 값 할당
float pi = 3.14F;
double morePi = 3.14159265358979323846;
```

-자바에서 실수형은 default가 double이므로 위에서 보듯이 float 변수에 값을 대입할 때 F 접미사를 붙여준다.

마찬가지로 접미사가 없으면 컴파일 에러가 발생한다.

- 8진수와 16진수 : int 자료형을 사용하여 표시한다.
    - 0(숫자)으로 시작하면 8진수, 0x(숫자+알파벳)로 시작하면 16진수가 된다.

```java
int octal = 025;    // 십진수 : 21
int hex = 0x25;    // 십진수 : 37
int moreHex = 0xC;    // 십진수 : 12
```

## 2-1 문자(char)

- **한 개**의 문자 값에 대한 자료형은 char를 이용한다.

```java
char a1 = 'a';
```

-문자값을 변수에 할당할때는 ‘ ‘ 를 사용해야한다.
(프로그램 작성시 char 자료형은 거의 사용할 일이 없다.)

- char는 문자값을 표현하는 방식이 다양하기 때문에 주의해야 한다.

```java
char a1 = 'a';    // 문자로 표현
char a2 = 97;    // 아스키코드로 표현
char a3 = '\u0061';    // 유니코드로 표현

// 출력하게 된다면 모두 a 가 출력된다
```

## 2-2 문자열(String)

- 문자들로 구성된 문장을 뜻한다.

```java
// 리터럴 방법
String a = "Hello Ssafy";
String b = "a";
String c = "123";

// 또는

String a = new String("Hellp Ssafy");
String b = new String("a");
String c = new String("123");
```

-new 키워드는 객체를 만들 때 사용한다. 하지만 첫번째 방법을 사용하는 것 권장.

- 원시 자료형(primitive data type) : int, long, double, float, boolean, char 자료형을 원시 자료형이라고 부른다. 이 자료형들은 new 키워드로 값을 생성할 수 없다. 원시 자료형은 리터럴 표기로만 값을 세팅할 수 있다.
(※ String은 원시 자료형이 아니지만 리터럴로 표기할 수 있게 특별대우 해주는 자료형)
- 문자열 내장 메서드
    - equals : 두개의 문자열이 동일한지 비교하여 결과값을 반환한다.
    (※ == 을 사용할 경우 잘못된 결과를 반환할 수 있다. == 는 두개의 자료형이 동일한 객체인지 판별할 때 사용하기 때문이다.
    따라서 **문자열을 비교할 때는 equals**를 사용하자!)
    - indexOf : 문자열에서 특정 문자열이 시작되는 인덱스를 반환한다.
    - contains : 문자열에서 특정 문자열이 포함되어 있는지의 여부를 반환한다.
    (Boolean 값으로 반환)
    - charAt : 문자열에서 특정 위치의 문자(char)를 반환한다.
    - replaceAll : 문자열 중 특정 문자열을 다른 문자열로 바꾸고 싶을 때 사용한다.
    - substring : 문자열 중 특정 부분을 뽑아낼 경우에 사용한다.
    (python에서 slicing과 유사하다.)
    - toUpperCase, toLowerCase : 문자열을 모두 대문자 또는 소문자로 변경할 때 사용한다.
    - split : 문자열을 특정 구분자로 나누어 문자열 배열로 반환하는 메서드이다.
- 문자열 포매팅 : 문자열 안에 어떤 값을 삽입하는 방법이다.
    1. 숫자 바로 대입 : %d, 정수
    2. 문자열 바로 대입 : %s, “문자열”
    3. 숫자 값을 나타내는 변수로 대입 : 변수에 정수를 할당해줬다면 %d, 변수명
    4. 2개 이상의 값 넣기 : 2개의 값 모두 변수에 할당 %d ~~ %s, 정수변수명, 문자열변수명
- 문자열 포맷 코드
    
    
    | 코드 | 설명 | 코드 | 설명 |
    | --- | --- | --- | --- |
    | %s | 문자열 | %o | 8진수 |
    | %c | 문자 | %x | 16진수 |
    | %d | 정수 | %% | ‘%’ 자체 |
    | %f | 부동소수 |  |  |

## 2-3 StringBuffer

- 문자열을 추가하거나 변경 할 때 주로 사용하는 자료형이다.
- StringBuffer의 메서드
    - append : StringBuffer 객체에 문자열을 추가할 수 있다.
    toString()메서드를 StringBuffer 객체에 사용하면 String 자료형으로 변경할 수 있다.
    - insert : 특정 위치에 원하는 문자열을 삽입할 수 있다.
    - substring : String 자료형의 substring 메서드와 동일하게 동작한다.

## 3. 상수집합(Enum)

## 4. 불(Boolean)

- 참 또는 거짓의 값을 갖는 자료형이다.

## 5. 형 변환(Type Casting)

- 자동(묵시적; 암묵적) 형변환이 가능한 방향

![화면 캡처 2023-02-15 163557.jpg](Data%20Type%20af8e272a10c542cfb6d94c100bce05b0/%25ED%2599%2594%25EB%25A9%25B4_%25EC%25BA%25A1%25EC%25B2%2598_2023-02-15_163557.jpg)

- 데이터 형변환
    - 묵시적(암묵적) : 범위가 넓은 데이터 형에 좁은 데이터 형을 대입하는 것이다.
    - 명시적 : 범위가 좁은 데이터 형에 넓은 데이터 형을 대입하는 것이다.

## 6. 연산자

- 단항 연산자
    - 증감 연산자 ++, --
        - 피연산자의 값을 1증가, 감소 시킨다.
        - 전위형 ++i
        - 후위형 i--
    - 부호 연산자 +, -
    - 논리 부정 연산자 !
    - 비트 부정 연산자 ~
    - 형 변환 연산자 (type)
- 산술 연산자
    - 곱하기 연산자 *
    - 나누기 연산자 /
    - 나머지 연산자 %
    - 더하기 연산자 +
    - 빼기 연산자 -
    - 정수와 실수의 연산 = 실수
- 비교 연산자
    - 대소 비교 연산
        - >, >=, <, <=
    - 동등 비교 연산
        - ==
        - !=
    - 객체 타입 비교 연산
        - instanceof
- 논리 연산자
    - &&
        - 논리 곱(AND) : 피연사자 모두가 true일 경우에만 true
    - ||
        - 논리 합(OR) : 피연산자 중 하나라도 true일 경우 true
    - !
        - 논리 부정(NOT) : 피연산자의 결과를 반대로 바꾼다.

## 7. 배열(Array)

- 숫자나 문자열만으로 표현하기 어려운 것들을 **자료형의 집합인 배열**로 해결한다.
- 배열은 자료형 타입 바로 옆에 [] 기호를 사용하여 표현한다.

```java
//홀수들의 집합
int[] nums = {1, 3, 5, 7, 9};

//요일의 집합
String[] days = {"월", "화", "수"};
```

- 위 코드는 1차원 배열이다. 다차원 배열도 가능하다.
- 배열의 길이는 고정되어 있다.