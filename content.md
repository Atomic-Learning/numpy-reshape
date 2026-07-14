You can use the `numpy.reshape()` function to create a new view of an array with a different shape, as long as the total number of values stays the same.

```py-cell
import numpy as np

x = np.arange(12)

print(x.ndim)
print(x.shape)
print(x)

y = x.reshape([3, 4])

print(y.ndim)
print(y.shape)
print(y)
```

# View Implications

As the result of `reshape()` is a view of the original array, any changes made to the new array will also be reflected in the original array, and vice-versa

```py-cell
import numpy as np

x = np.arange(12)
y = x.reshape([3, 4])

x[0] = 100
y[1, 1] = 200

print(x)
print(y)
```

# Size Requirements

The new shape must contain the same number of entries as the original array. If it does not, NumPy raises an error.

```py-cell
import numpy as np

x = np.arange(7)

y = x.reshape([3, 2])
```