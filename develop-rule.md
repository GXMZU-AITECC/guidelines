# 开发规范

## 开发流程

1. 首先 `fork` 仓库
2. 然后在你 `fork` 的仓库里添加新分支
   - `bugfix/...` 表示修复bug
   - `feature/...` 表示增加新功能
   - 如果既有修bug又有新功能，优先使用 `feature/...`
3. 当你在分支中写好之后，就可以向主仓库的 `develop` 提交 PR 了（PR 提交规范详见 [pr-rule.md](./pr-rule.md)）

## 代码审计

提交 PR 后，至少需要另外一个人进行审计才能进行合并。

## 代码风格

函数需要写详细的注释，说清楚具体功能、参数和返回值，方便别人阅读和维护。

参考下面这种写法：

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
