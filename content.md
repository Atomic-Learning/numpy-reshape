You can use `reshape()` to create a new view of an array with a different shape, as long as the total number of values stays the same.

```py-cell
import numpy as np

a = np.arange(12).reshape([2, 2, 3])

print(a.ndim)
print(a.shape)
print(a)
```

The new shape must contain the same number of entries as the original array. If it does not, NumPy raises an error.

```py-cell
import numpy as np

a = np.arange(7).reshape([2, 3])
```

This page focuses on the reshaping step itself. The exercise page uses this idea together with array construction.