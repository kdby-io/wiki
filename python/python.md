# python

## Metaclass란
파이썬에서는 클래스도 하나의 인스턴스다. 뭐의 인스턴스냐?의 대답이 metaclass. 클래스의 클래스를 메타클래스라고 한다.  
즉, 인스턴스는 class의 인스턴스고, 클래스는 metaclass의 인스턴스다.

type은 default metaclass다.

```py
>>> class Foobar:
...     pass
>>> type(Foobar)
<class 'type'>
>>> foo = Foobar()
>>> type(foo)
<class '__main__.Foobar'>
>>> isinstance(foo, Foobar)
True
>>> isinstance(Foobar, type)
True
```

type을 이용해 이런식으로 클래스를 만들 수도 있다.
```py
>>> MyClass = type('MyClass', (), {})
>>> MyClass
<class '__main__.MyClass'>
```

custom metaclass는 다음과 같이하면 만들 수 있다.
```py
>>> class Meta(type):
...     pass
>>> class Complex(metaclass=Meta):
...     pass
>>> type(Complex)
<class '__main__.Meta'>
```

*그래서 어디다가 쓰는건데?*
