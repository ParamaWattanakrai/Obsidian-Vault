```python
import sympy as sym
```

# Evaluation
```python
print(sym.pi.evalf(digit)) #digit include everything, infront and behind floating point
print(sym.N(expression, digit))
```

# Symbols
```python
x, y, z = sym.symbols('x y z')
u = 2*x - 7*y + z**2
```

# Expansion
$$\begin{flalign}
(x+5)(x-3)=x^2 + 2x - 15&&
\end{flalign}$$			  
```python
x = sym.symbols('x')
f = (x + 5)*(x - 3)
print(sym.expand(f))
```
## Trigonometry
$$\begin{flalign}
cos(a+b)=-sin(a)sin(b)+cos(a)cos(b)&&
\end{flalign}$$
```python
a, b = sym.symbols('a b')
f = sym.cos(a+b)
print(sym.expand(f, trig=True))
```

# Factorization
$$\begin{flalign}
6x^3+11x^2-16x-21=(x + 1)(2x-3)(3x+7)&&
\end{flalign}$$
```python
x = sym.symbols('x')
f = 6*x**3 + 11*x**2 - 16*x - 21
print(sym.factor(f))
```

# Simplification
$$\begin{flalign}
\frac{x+2y}{\frac{2}{x}+\frac{1}{y}}=xy&&
\end{flalign}$$
```python
x, y = sym.symbols('x y')
f = (x + 2*y)/(2/x + 1/y)
print(sym.simplify(f))
```

# Sources
https://docs.sympy.org/latest/reference/index.html

#DataScience
#ProgrammingLanguages/Python/Libraries