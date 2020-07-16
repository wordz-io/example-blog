# Example Blog Post

It is not hard to show that, after applying this transformation `n` times, `a` and `b` will be equal, respectively, to `Fib(n + 1)` and `Fib(n)`. Thus, we can compute Fibonacci numbers iteratively using this procedure

```python
def fib_iter(a, b, count):
  if count == 0:
    return b
  else:
    fib_iter(a + b, a, count - 1)

def fib(n):
  return fib_iter(1, 0, n)

```

This second method for computing `Fib(n)` is a linear iteration. The difference in numbers of steps required by the two methods—one liniear in `n`, one growing as fast as `Fib(n)` itself—is enormous, even for small inputs.

One should not conclude from this that tree-recursive processes are useless. When we consider processes that operate on hierarchically structured data rather than numbers, we will find that tree recursion is a natural and powerful tool.
