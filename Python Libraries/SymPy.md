```python
import sympy as sym
```

# Evaluation
```python
print(sym.pi.evalf(digit))
print(sym.N(expression, digit))
```

# Symbols
```python
x, y, z = sym.symbols('x y z')
u = 2*x - 7*y + z**2
```

# Expansion
			  
```python
x = sym.symbols('x')
f = (x + 5)*(x - 3)
print(sym.expand(f))
```
## Trigonometry
```python
a, b = sym.symbols('a b')
f = sym.cos(a+b)
print(sym.expand(f, trig=True))
```