---
title: "[Python] basic"
subtitle: "Print, Data Types, Variable, Math Expression, Increment and Decrement a Number, Advanced Math Expressions, Concatenating Text Strings"
categories:
  - Python
tags:
  - [Python, Blog]
toc: true
toc_sticky: true
toc_label: "목차"
---


## 1. Print

파이썬에서 화면에 출력을 하고자 할때는 __print__ 명령어를 사용할 수 있습니다. 예를 들어, "Hello World!" 를 화면에 출력하고자 할때는 다음 코드를 실행하면 됩니다.
```python
print("Hello World!")
```

<iframe src="https://trinket.io/embed/python/f55f2d774b?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
**print**의 정확한 문법은 다음과 같습니다.

+ 먼저 __print__ 라는 function(함수) 이름이 위치
+ 그리고 괄호가 위치
+ 괄호 안에 따옴표가 위치
+ 마지막으로 따옴표 안에 출력하고자 하는 string(문자열)이 위치

<img class="img-fluid" src="/img/posts/print.jpg" alt="print-image">
<hr>


## 2. Data Types

파이썬에서는 다음과 같은 데이터 타입들이 존재 합니다.
### 2-1. String
string은 문자열을 나타내는 data type 입니다.
+ 두개의 따옴표 ("") 사이에 있는 문자열을 string 이라고 합니다.
+ 파이썬이 string 을 출력할때 따옴표들은 제외하고 출력하게 됩니다.
+ 따옴표들은 단순히 print의 괄호 안에 들어가는 값들이 string 이라고 알려주는 역할을 할 뿐입니다.

### 2-2. Integer
정수 값을 이야기 합니다. ex) 1, 2, 100
### 2-3. Float
소수점 숫자를 이야기 합니다. ex) 2.0, 3.7, 9.99
### 2-4. Complex Numbers
실수와 허수를 포함하고 있는 복소수를 이야기 합니다. 파이썬에서는 j를 사용하여 허수를 표현합니다. ex) 1+3j, 2-4j
### 2-5. Boolean
True 나 False 이 2가지 값만 가지고 있으면 조건문에서 많이 사용됩니다.
data type을 알수 없을 때 type을 쓰면 data type을 알수 있습니다.
<iframe src="https://trinket.io/embed/python/f06153b6e3?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

## 3. Variables

### 3-1. 변수 선언 방법
변수는 어떻게 만들까? 다음 예와 같은 name, a, b, c를 변수라고 한다.
name = "송은우
+ a = 1
+ b = "python"
+ c = [1, 2, 3]

<img class="img-fluid" src="/img/posts/variable.jpg" alt="variable">
변수가 지정되면 print문에 실제 값 대신 변수를 사용할 수 있습니다.

<iframe src="https://trinket.io/embed/python/34f1b0503e?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

### 3-2. 변수 이름 법칙
+ 변수 이름은 영어 알파벳과 숫자 그리고 underscore(_) 으로만 구성해야 합니다.
+ 변수 이름 첫글자는 알파벳이나 underscore(_)로만 시작해야 합니다.
+ 숫자로 시작될 수 없습니다.
+ 영어 알파벳은 대문자와 소문자가 구분이 됩니다.
+ 올바른 변수 이름 : name, _name, my_name, myName
+ 잘못된 변수 이름: 7name, my name

## 4. Math Expressions
기본 수학 연산들은 다음과 같습니다.
+ [4-1. 더하기](#4-1-더하기)
+ [4-2. 빼기](#4-2-빼기)
+ [4-3. 곱하기](#4-3-곱하기)
+ [4-4. 나누기](#4-4-나누기)
+ [4-5. 정수 나누기](#4-5-정수-나누기)
+ [4-6. 나머지](#4-6-나머지)

### 4-1. +(더하기)
~~~python
num1 = 7
num2 = 10
num3 = num1 + num2
~~~
num3의 값은 7 + 10, 즉 17이 됩니다.


### 4-2. -(빼기)
~~~python
num1 = 7
num2 = 10
num3 = num1 - num2
~~~
num3의 값은 7 - 10, 즉 3이 됩니다.

### 4-3. *(곱하기)
~~~python
num1 = 7
num2 = 10
num3 = num1 * num2
~~~
num3의 값은 7 * 10, 즉 70이 됩니다.

### 4-4. /(나누기)
~~~python
num1 = 7
num2 = 10
num3 = num1 / num2
~~~
num3의 값은 7 / 10, 즉 0.7이 됩니다.
<iframe src="https://trinket.io/embed/python/5d3d4b979c?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


### 4-5. //(정수 나누기)
파이썬에는 나누기의 값이 정수로 떨어지지 않는 경우 반내림으로 해서 정수의 값만 리턴하는 정수 나누기가 있습니다. 정수 나누기는 나누기 심볼을 2번 연속으로 사용하면 됩니다.
~~~python
num1 = 7
num2 = 2
num3 = num1 // num2
~~~
num3의 값은 7 / 2 = 3.5 입니다. 하지만 7 // 2 = 3 이 됩니다.
<iframe src="https://trinket.io/embed/python/e197a99f97?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


### 4-6. __%__(나머지)
~~~python
num1 = 6
num2 = 5
num3 = num1 % num2
~~~
num3의 값은 6 % 5 = 1 입니다.
<iframe src="https://trinket.io/embed/python/14f51b260f?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

## 5. Increment and Decrement a Number

### 5-1. Increment a Number
+ 파이썬 증감 연산자는 일반적인 ++ 과 다르게 += 연산자를 사용합니다.
+ -= 연산자를 사용하여 변수의 값을 1 감소시킬 수 있습니다.
<iframe src="https://trinket.io/embed/python/d380f92c6c?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


### 5-2. Decrement a Number
+ 파이썬 증감 연산자는 일반적인 -- 과 다르게 -= 연산자를 사용합니다.
+ -= 연산자를 사용하여 변수의 값을 1 감소시킬 수 있습니다.
<iframe src="https://trinket.io/embed/python/3d4f2310f5?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

## 6. Advanced Math Expressions

파이썬은 기본적인 수학 연산 표현 이외에도 다음과 같은 상급 수학 연산 표현 또한 지원하고 있습니다.

### 6-1. \*=
\*= 는 곱하기를 실행한 후의 값을 변수에 저장합니다.
~~~python
num1 = 10
num1 *= 2
print(num1)
~~~
num1의 값은 10 * 2 = 20 입니다.
<iframe src="https://trinket.io/embed/python/14f51b260f?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe><br><br>

### 6-2. /=
/= 는 곱하기를 실행한 후의 값을 변수에 저장합니다.
~~~python
num1 = 10
num1 /= 2
print(num1)
~~~
num1의 값은 10 / 2 = 5 입니다.
<iframe src="https://trinket.io/embed/python/888644d32b?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

### 6-3. **
** 는 제곱값을 구할때 사용합니다.
~~~python
num1 = 10 ** 2
print(num1)
~~~
num1의 값은 10 ** 2 = 100 입니다.
<iframe src="https://trinket.io/embed/python/0fb2e1c328?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

## 7. Order of Operators

파이썬 수학 연산 표현들의 순서는 다음과 같습니다.</p>
+ __( )__
+ __**__
+ __*, /, %__
+ __+, -__

만일 실행되는 순서가 동일한 연산들이 있을 경우 (예를 들어 곱하기 와 나누기), 먼저 나오는 연산이 먼저 실행됩니다.
여기서 중요하게 기억해야 하는 점은 괄호 입니다. 괄호안에 포함된 연산은 항상 먼저 실행됩니다.
<iframe src="https://trinket.io/embed/python/e0d579b01e?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

## 8. Concatenating Text Strings

### 8-1. Concatenating Text Strings
숫자와 마찬가지로 string 도 더할 수 있습니다. 이를 string concatenation 이라고 합니다. 2개 혹은 그 이상의 문자열들을 잇는걸 뜻합니다. 예를 들어, 이전에는 "Hello, World!" 를 출력하기 위해서는 다음과 같이 구현했습니다.
~~~python
print("Hello, World")
~~~
하지만, 다음 처럼 구현 할 수도 있습니다.
~~~python
print("Hello, " + "World")
~~~
위에서 보았듯이 string 을 잇기 위해서 + 을 사용하면 됩니다.
예를 들어, 저장한 변수를 사용해서 출력 하고 싶을 경우에는 string concatenation 을 사용하면 편리합니다.
~~~python
name = "shawn"
print("Hello, " + name)
~~~
<iframe src="https://trinket.io/embed/python/880557cb63?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

### 8-2. 복잡한 string concatenation
string concatenation 을 하는 방법에는 + 이외에도 다른 방법도 있습니다. 특히 길고 복잡한 문자열 인 경우에는 + 보다는 다른 방법을 사용하는게 효과적입니다. 그 중 가장 편리한 방법중 하나가 바로 literal string interpolation 입니다.
~~~python
name = input()
print(f"Hello, {name}")
~~~
literal string interpolation 을 사용하려면 다음의 문법을 지켜야 합니다:
+ 먼저 따옴표 앞에 f 를 붙여야 합니다.
+ 치환 하고 싶은 변수 (혹은 변수가 아니어도 됩니다. 예를 들어 함수 호출이 될 수도 있습니다) 를 {}를 사용해서 표시합니다.

## 9. Significant Whitespace
---
Whitespace 란 바로 들여쓰기(indention)을 이야기 합니다. 다른 언어에서는 들여쓰기가 필수사항은 아닙니다. 단순히 코드의 가독성을 높이기 위해서 사용하는 수준입니다. 하지만 파이썬에서는 들여쓰기는 요구사항 입니다. 들여쓰기를 통해 코드의 종속성을 나타냅니다.
<img class="img-fluid" src="/img/posts/whitespace.jpg" alt="whitespace">
들여쓰기의 칸 수는 일반적으로 4칸입니다. (2칸을 사용하는 개발자도 있습니다.) 대부분 tab 사이즈를 space 4칸으로 설정해서 tab으로 들여쓰기를 합니다.
