### Confusion matrix
>在机器学习中，将预测的类别和真实类别放在一个二维表中。可以方便地查看分错的类别。

#### Example1:


```python
from sklearn.metrics import confusion_matrix
y_true = [2, 0, 2, 2, 0, 1]
y_pred = [0, 0, 2, 2, 0, 2]
confusion_matrix(y_true, y_pred)

array([[2, 0, 0],
       [0, 0, 1],
       [1, 0, 2]])

```
解释：这里省略了其标签：[0,1,2]

| -||Pred|||
|----------|:-------------:|------:|-------:|
|-|| 0 |  1| 2|
|True|0| 2|    0   |   0 |
||1| 0 | 0 |    1 |
||2| 1| 0 |    2 |

```python
y_true = ["cat", "ant", "cat", "cat", "ant", "bird"]
y_pred = ["ant", "ant", "cat", "cat", "ant", "cat"]
confusion_matrix(y_true, y_pred, labels=["ant", "bird", "cat"])

array([[2, 0, 0],
       [0, 0, 1],
       [1, 0, 2]])
```
| -||Pred|||
|----------|:-------------:|------:|-------:|
|-|| ant |  bird| cat|
|True|ant| 2|    0   |   0 |
||bird| 0 | 0 |    1 |
||cat| 1| 0 |    2 |
