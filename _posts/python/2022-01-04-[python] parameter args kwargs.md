---
layout: post
title: "[python]함수의 인자 형태와 순서"
subtitle: "function parameters, *args, **kwargs"
date: 2022-01-05 15:05:13 -0400
background: '/img/posts/04.jpg'
---


## 1. Positional arguments
가장 기본적인 형태는 순서대로 값이 parameter로 함수에 전해지는 경우입니다.
<img class="img-fluid" src="/img/posts/positional-arguments.jpg" alt="Demo Image">

## 2. Keyword arguments
순서 대신에 parameter 이름으로 맞추어서 값을 전해줄 수 있으며, 이를 keyword argments 라고 합니다.
Keyword arguments 방식으로 parameter 값을 전해주면 실제 parameter 순서가 바뀌어도 괜찮습니다.
<img class="img-fluid" src="/img/posts/keyword-arguments.jpg" alt="function-parameters">
<span class="caption text-muted">위의 경우 처럼 순서에 맞추어서 parameter 값을 전해주지 않을수 있는 방법도 있습니다.</span>
순서가 바뀌어도 괜찮다는 점 말고도 또 가독성도 높아진다는 점도 있습니다.

## 3. Mixing positional arguments and keyword arguments
순서를 맞추어서 parameter 값을 전해주는 positional arguments와 keyword arguments를 혼용하여 사용하는것도 가능합니다.
<img class="img-fluid" src="/img/posts/mixing-positional-arguments.jpg" alt="Mixing positional arguments and keyword arguments">
다만, 여기서 중요한것은 keyword arguments 는 순서가 바뀌어도 상관 없지만 positional arguments 부분은 순서를 지켜줘야 한다는 것입니다.

## 4. Parameter default value
함수의 parameter에 default 값을 정의해 줄 수 도 있습니다. Default 값이 정의된 paramter는 함수가 호출될때 값이 넘겨지 않아도 괜찮습니다. 값이 넘겨지 않은 경우 default 값이 자동으로 넘겨지게 됩니다.
<img class="img-fluid" src="/img/posts/parameter-default-value.jpg" alt="Parameter Default Value">
다만, 조심해야 할점은 default 값이 정의된 parameter가 default 값이 정의 되지 않은 parameter보다 먼저 위치해 있으면 안된다는 점입니다. 만일 default value parameter를 non-default value parameter 앞에 선언하면 syntax error가 납니다.
<iframe src="https://trinket.io/embed/python/603f604826?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
위 코드는 y의 값을 2로 지정해줄 의도였지만 python은 순서대로 값을 넘겨주는데 순서대로 x에게 값을 줘야 할지 값이 정의 되지 않은 y에게 줘야할지 알수 없어서 syntax error가 나게 됩니다.

<iframe src="https://trinket.io/embed/python/3edf866bdc?start=result" width="100%" height="200" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
default 값을 y에게 주면 잘 작동이 되는걸 볼수 있습니다. 앞에 별표는 메모리 주소를 찾아서 값을 읽어준다는 의미이다.
<hr>
## *args
args는 argument를 줄인말로 인자값을 받겠다는 의미이다.
args를 사용하면 key, value를 받는 형식을 제외한 모든 형식을 인자로 받을 수 있다.
인자 양식이 맞으면 여러개의 인자를 받을수 있다.
{% highlight python %}
def func_param_with_var_args(name, *args, age):
    print("name=",end=""), print(name)
    print("args=",end=""), print(args)
    print("age=",end=""), print(age)

func_param_with_var_args("정우성", "01012341234", "seoul", 20)
{% endhighlight %}


```
def func_param_with_var_args(name, *args, age):
    print("name=",end=""), print(name)
    print("args=",end=""), print(args)
    print("age=",end=""), print(age)

func_param_with_var_args("정우성", "01012341234", "seoul", 20)
# "정우성"은 name에 배정되고, '01012341234' 부터 20까지 *args에 배정된다.
```

실행해 보면 TypeError가 난다 이유는 *args 전에 있는 인자에 할당하고 남은 전부를 가져가서 그 뒤에 인자가 할당받을 것이 없어진다
<br>
error 해결 방법으로는
def func_param_with_var_args(name, age, *args):
    print(f"name={name}")
    print(f"args={args}")
    print(f"age={age}")

func_param_with_var_args("정우성", 20, "01012341234", "seoul")
*args를 맨뒤에 넣어주고 age의 값인 20을 순서에 맞게 넣어준다
# 결과

# name=정우성
# args=('01012341234', 'seoul')
# age=20



다른 방법으로는
def func_param_with_var_args(name, *args, age = 20):
    print("name=",end=""), print(name)
    print("args=",end=""), print(args)
    print("age=",end=""), print(age)

func_param_with_var_args("정우성", "01012341234", "seoul")
age를 default value parameter로 만들어주는 것이다
# 결과

# name=정우성
# args=('01012341234', 'seoul')
# age=20

## **kwargs
kwargs는 dictionary 형태로 값을 읽고 이 때 key와 value 값을 가지기 때문에 별표 **두개를 사용한다. kwargs로 값을 받기 위해서는 key값=value값 형식으로 넣어야 한다.
kwarg를 사용하면 key, value를 받는 형식의 인자를 받을 수 있다.
인자 양식이 맞으면 여러개의 인자를 받을수 있다.

def func_param_with_kwargs(name, age, **kwargs, address=0):
    print("name=",end=""), print(name)
    print("age=",end=""), print(age)
    print("kwargs=",end=""), print(kwargs)
    print("address=",end=""), print(address)

func_param_with_kwargs("정우성", "20", mobile="01012341234", address="seoul")
실행해 보면 SyntaxError가 난다 이유는 *args랑 똑같이  **kwargs전에 있는 인자를 할당하고 남은 전부를 가져가서 그 뒤에 인자가 할당받을 것이 없어진다

error 해결 방법은
def func_param_with_kwargs(name, age, address=0, **kwargs):
    print("name=",end=""), print(name)
    print("age=",end=""), print(age)
    print("kwargs=",end=""), print(kwargs)
    print("address=",end=""), print(address)

func_param_with_kwargs("정우성", "20", mobile="01012341234", address="seoul")
**kwargs를 맨뒤에 보내주면 해결이 된다
# 결과

# name=정우성
# age=20
# kwargs={'mobile': '01012341234'}
# address=seoul

<br>
만약 *args와 **kwarg 두개를 함께 쓴다면?

def mixed_params(name="아이유", *args, age, **kwargs, address):
    print("name=",end=""), print(name)
    print("args=",end=""), print(args)
    print("age=",end=""), print(age)
    print("kwargs=",end=""), print(kwargs)
    print("address=",end=""), print(address)

mixed_params(20, "정우성", "01012341234", "male" ,mobile="01012341234", address="seoul")
실행해 보면 SyntaxError가 난다
해결 방법은
def mixed_params(age, name="아이유", *args, address, **kwargs):
    print("name=",end=""), print(name)
    print("args=",end=""), print(args)
    print("age=",end=""), print(age)
    print("kwargs=",end=""), print(kwargs)
    print("address=",end=""), print(address)

mixed_params(20, "정우성", "01012341234", "male" ,mobile="01012341234", address="seoul")
**kwargs를 맨뒤로 보내주고 age를 순서에 맞게 맨앞으로 보내주면 된다
# 결과

# name=정우성
# args=('01012341234', 'male')
# age=20
# kwargs={'mobile': '01012341234'}
# address=seoul