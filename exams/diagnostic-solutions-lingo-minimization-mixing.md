# 查漏补缺带练：LINGO 编程题（最小化配料问题）

## 题目

把下面线性规划模型写成 LINGO 程序：

```text
min Z = 3x1 + 2x2
s.t.
    x1 + x2 >= 50
    4x1 + 2x2 >= 160
    x1, x2 >= 0
```

## 1. LINGO 程序

```lingo
MODEL:

MIN = 3 * X1 + 2 * X2;

X1 + X2 >= 50;
4 * X1 + 2 * X2 >= 160;

END
```

## 2. 对照关系

数学模型：

```text
min Z = 3x1 + 2x2
```

LINGO：

```lingo
MIN = 3 * X1 + 2 * X2;
```

数学模型：

```text
x1 + x2 >= 50
```

LINGO：

```lingo
X1 + X2 >= 50;
```

数学模型：

```text
4x1 + 2x2 >= 160
```

LINGO：

```lingo
4 * X1 + 2 * X2 >= 160;
```

## 3. 注意

普通连续变量默认非负，所以 `x1,x2>=0` 一般不用在 LINGO 中单独写。

若考试想写，也可以写成：

```lingo
X1 >= 0;
X2 >= 0;
```

但不是必须。

## 4. LINGO 基本模板

```lingo
MODEL:

MAX 或 MIN = 目标函数;

约束1;
约束2;
约束3;

END
```
