- [x] 策略模式
- [x] 观察者模式
- [x] 装饰者模式
- [x] 工厂模式
  - [x] 工厂方法
  - [x] 抽象工厂
- [x] 单件模式
- [x] 命令模式
- [x] 适配器模式
- [x] 模版方法模式 
- [x] 状态模式
- [x] 代理模式
- [x] 迭代器模式、组合模式 
- [x] 复合模式（模式中的模式） 
  - MVC：V 与 C - 策略模式；M 与 V/C - 观察者模式；V 内 - 组合模式

## 设计模式语言仓库

- Python 设计模式：[faif/python-patterns](https://github.com/faif/python-patterns)
- Golang 设计模式：[tmrts/go-patterns](https://github.com/tmrts/go-patterns)

## 模式定义

问题 + 情境 + 解决方案。

## 模式分类1

### 创建型

涉及将对象实例化。该类型提供一个方法，将客户从需要实例化的对象中解耦。

- 单例
- 工厂

### 行为型

涉及类和对象如何交互和分配职责。

### 结构型

让你把类和对象组合到更大的结构中。

## 模式分类2

### 类模式

描述类之间的关系如何通过继承定义。

### 对象模式

描述对象之间的关系，通过组合定义。

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
