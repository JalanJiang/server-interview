## 设计模式语言仓库

- Python 设计模式：[faif/python-patterns](https://github.com/faif/python-patterns)
- Golang 设计模式：[tmrts/go-patterns](https://github.com/tmrts/go-patterns)

## 设计原则

1. 将变化之处独立
2. 针对接口编程，而不是针对实现编程
3. 多用组合，少用继承

## 行为模式 Behavioral Patterns

### 策略模式

> Strategy behavioral design pattern enables an algorithm's behavior to be selected at runtime.
> It defines algorithms, encapsulates them, and uses them interchangeably.

定义了**算法族**，分别封装起来，让它们之间可以互相替换，让算法的变化独立于使用算法的客户。

以鸭子类 `class Duck` 为例，它实现了鸭子叫声 `quack()` 方法与鸭子飞 `fly()` 方法。但不是所有鸭子都会叫、都会飞，比如我的小黄鸭。

因此，我们把「叫」和「飞」的行为拆分出来，分别为它们定义两个接口 `QuackBehavior` 和 `FlyBehavior`（即：拆分出了「算法族」）。这样一来，不同的**鸭子行为**就特别去实现这两个接口的方法，产生不同的叫声、飞行方法。

例如有个小黄鸭，给它的叫声定义一个类：

```
class 小黄鸭的叫法 implements QuackBehavior {
    public void quack() {
        并不会叫
    }
}
```

在鸭子类中加入 `QuackBehavior` 和 `FlyBehavior` 两个实例变量：

```
class Duck {
    QuackBehavior quackBehavior

    public void performQuack() {
        // 不同的 quackBehavior 产生了不同的叫声
        quackBehavior.quack()
    }
}
```

让小黄鸭继承 Duck：

```
class 小黄鸭 extends Duck {
    构造函数() {
        // 设置这个实例变量
        quackBehavior = new 小黄鸭的叫法()
    }
}
```

如果要在运行时改变 `quackBehavior` 可以添加一个 setter 函数。
