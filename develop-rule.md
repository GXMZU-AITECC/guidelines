# B · 开发规范

## B1 开发流程

1. 首先 `fork` 仓库
2. 在你 fork 的仓库里从 `develop` 拉出新分支（命名见 B2）
3. 在分支中写好之后，向主仓库的 `develop` 提交 PR（提交规范见 **C 章**）

## B2 分支命名

1. `feature/...` —— 新增功能
2. `bugfix/...` —— 修复 Bug
3. 分不清是修 Bug 还是新功能时，优先使用 `feature/...`

## B3 代码注释

函数需要写详细的注释，说清楚具体功能、参数和返回值，方便别人阅读和维护。

参考写法：

```python
def evaluate(self, expression: str, mode: str) -> Union[int, float]:
    """计算表达式并返回数值结果。

    参数:
        expression: 要计算的数学表达式字符串
        mode: 当前计算模式，如 "Standard" 或 "Programmer"

    返回:
        计算结果的整型或浮点数值
    """
    if not expression:
        raise ValueError("Empty expression")

    use_int_div = (mode == "Programmer")
    return self._compute(expression, use_int_div)
```

## B4 可运行

提交代码前确保代码可运行。
