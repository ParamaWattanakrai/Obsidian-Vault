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
```python
sol = sym.expand(expression)
```
$$\begin{flalign}
(x+5)(x-3)=x^2 + 2x - 15&&
\end{flalign}$$
```python
x = sym.symbols('x')
f = (x + 5)*(x - 3)
print(sym.expand(f)) #x**2 + 2*x - 15
```
## Trigonometry
```python
sol = sym.expand(expression, Trig=True)
```
$$\begin{flalign}
cos(a+b)=-sin(a)sin(b)+cos(a)cos(b)&&
\end{flalign}$$
```python
a, b = sym.symbols('a b')
f = sym.cos(a+b)
print(sym.expand(f) #cos(a + b)
print(sym.expand(f, trig=True)) #-sin(a)*sin(b) + cos(a)*cos(b)
```

# Factorization
```python
sol = sym.factor(expression)
```
$$\begin{flalign}
6x^3+11x^2-16x-21=(x + 1)(2x-3)(3x+7)&&
\end{flalign}$$
```python
x = sym.symbols('x')
f = 6*x**3 + 11*x**2 - 16*x - 21
print(sym.factor(f)) #(x + 1)*(2*x - 3)*(3*x + 7)
```

# Simplification
$$\begin{flalign}
\frac{x+2y}{\frac{2}{x}+\frac{1}{y}}=xy&&
\end{flalign}$$
```python
x, y = sym.symbols('x y')
f = (x + 2*y)/(2/x + 1/y)
print(sym.simplify(f)) #x*y
```

# Limit
```python
sol = sym.limit(expression, variable, value)
```
$$\begin{flalign}
\lim_{x\to a}\frac{x^2-a^2}{x-a}=2a&&
\end{flalign}$$
```python
x, a = symbols('x a')
f = (x**2 - a**2)/(x - a)
sol = sym.limit(f, x, a) #2*a
```

# Differentiation
```python
sol = sym.diff(expression, variable, order)
```

$$\begin{flalign}
\frac{d^2}{dx}2x^3+7x^2+3x+5=2(6x+7)&&
\end{flalign}$$
```python
x = sym.symbols('x')
y = 2*x**3 + 7*x**2 - 3*x + 5
sol = sym.diff(y, x, 2)
print(sol) #order of differentiation
```

# Integration
## Indefinite Integration
```
sol = sym.integrate(expression, variable)
```

$$\begin{flalign}
\int \frac{1}{1+x^2}\,dx=tan^{-1}x&&
\end{flalign}$$
```python
x = sym.symbols('x')
f = 1/(1 + x**2)
print(sym.integrate(f, x))
```
$$\begin{flalign}
\int x^2\sqrt{x-1}\,dx=\frac{2(x-1)^\frac{1}{2}}{105}(15x^3-13x^2-4x-8)&&
\end{flalign}$$
```python
x = sym.symbols('x')
f = x**2*sym.sqrt(x - 1)
print(sym.integrate(f, x)) #Piecewise((2*x**3*sqrt(x - 1)/7 - 2*x**2*sqrt(x - 1)/35 - 8*x*sqrt(x - 1)/105 - 16*sqrt(x - 1)/105, Abs(x) > 1), (2*I*x**3*sqrt(1 - x)/7 - 2*I*x**2*sqrt(1 - x)/35 - 8*I*x*sqrt(1 - x)/105 - 16*I*sqrt(1 - x)/105, True))
print(sym.simplify(sym.integrate(f, x))) #Piecewise((2*sqrt(x - 1)*(15*x**3 - 3*x**2 - 4*x - 8)/105, (x > 1) | (x < -1)), (2*I*sqrt(1 - x)*(15*x**3 - 3*x**2 - 4*x - 8)/105, True))
```
## Definite Integration
```python
sol = sym.integrate(expression, (var1, lower1, upper1), (var2, lower2, upper2), ...)
```

$$\begin{flalign}
\int_1^2\int_3^4\int_5^6 x^3y^2z\,dx\,dy\,dz=\frac{2035}{8}&&
\end{flalign}$$
```python
x, y, z = sym.symbols('x y z')
f = x**3*y**2*z
print(sym.integrate(f, (x, 1, 2), (y, 3, 4), (z, 5, 6))) #2035/8
```

# Series
```python
expression.series(var, x0=center, n=order)
```

$$\begin{flalign}
e^x\approx 1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+\frac{x^4}{4!}+\cdots\approx 1+x+\frac{x^2}{2}+\frac{x^3}{6}+\frac{x^4}{24}+\cdots&&
\end{flalign}$$
```python
x = sym.symbols('x')
f = sym.exp(x)
print(f.series(x, x0=0, n=5)) #1 + x + x**2/2 + x**3/6 + x**4/24 + O(x**5)
print(f.series(x, x0=0, n=5).removeO()) #x**4/24 + x**3/6 + x**2/2 + x + 1
```

# Sum
```python
sol = sym.Sum(expression, (variable, lower, upper)).doit()
```

$$\begin{flalign}
\sum\limits_{n=0}^{10}2^n=2047&&
\end{flalign}$$
```python
n = sym.symbols('n')
f = 2**n
sol = sym.Sum(f, (n, 0, 10))
print(sol) #Sum(2**n, (n, 0, 10))
print(sol.doit()) #2047
```
$$\begin{flalign}
\sum\limits_{n=1}^{\infty}\frac{1}{(3n-2)(3n+1)}=\frac{1}{3}=0.\overline{3}&&
\end{flalign}$$
```python
n = sym.symbols('n')
f = 1/((3*n-2)*(3*n+1))
sol = sym.Sum(f, (n, 1, sym.oo))
print(sol) #Sum(1/((3*n - 2)*(3*n + 1)), (n, 1, oo))
print(sol.doit()) #1/3
print(float(sol)) #0.3333333333333333
```

# Lambdify
```python
function = sym.lambdify(variable, experssion)
```

```python
x = sym.symbols('x')
f = sym.exp(x)
sol = f.series(x, x0=0, n=5).removeO()

f_numeric = sym.lambdify(x, f, 'numpy')
taylor_numeric = sym.lambdify(x, sol, 'numpy')
```
# Sources
https://docs.sympy.org/latest/reference/index.html

#DataScience
#ProgrammingLanguages/Python/Libraries