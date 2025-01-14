
| Rule     | Derivative                                                       |
| -------- | ---------------------------------------------------------------- |
| Constant | $\begin{flalign}(C)'=0\end{flalign}$                             |
| Power    | $\begin{flalign}(x^n)'=nx^{n-1}\end{flalign}$                    |
| Inverse  | $\begin{flalign}(\frac{1}{x})'=-\frac{1}{x^2}\end{flalign}$      |
| Addition | $\begin{flalign}(f+g)'=f'+g'\end{flalign}$                       |
| Product  | $\begin{flalign}(f\cdot g)'=f'g+fg'\end{flalign}$                |
| Quotient | $\begin{flalign}(\frac{f}{g})'=\frac{gf'-fg'}{g^2}\end{flalign}$ |
# Trigonometric Functions

| Direct                                                | Inverse                                                  |
| ----------------------------------------------------- | -------------------------------------------------------- |
| $\begin{flalign}\frac{dsinx}{dx}=cosx\end{flalign}$   | $\begin{flalign}\frac{dcscx}{dx}=-cscxcotx\end{flalign}$ |
| $\begin{flalign}\frac{dcosx}{dx}=-sinx\end{flalign}$  | $\begin{flalign}\frac{dsecx}{dx}=secxtanx\end{flalign}$  |
| $\begin{flalign}\frac{dtanx}{dx}=sec^2x\end{flalign}$ | $\begin{flalign}\frac{dcotx}{dx}=csc^2x\end{flalign}$    |

| Direct                                                                          | Inverse                                                                          |
| ------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| $\begin{flalign}\frac{dsin^{-1}x}{dx}=\frac{1}{\sqrt{1-x^2}}\end{flalign}$      | $\begin{flalign}\frac{dsin^{-1}x}{dx}=-\frac{1}{\sqrt{1-x^2}}\end{flalign}$      |
| $\begin{flalign}\frac{dtan^{-1}x}{dx}=\frac{1}{1+x^2}\end{flalign}$             | $\begin{flalign}\frac{dtan^{-1}x}{dx}=-\frac{1}{1+x^2}\end{flalign}$             |
| $\begin{flalign}\frac{dsec^{-1}x}{dx}=\frac{1}{\|x\|\sqrt{x^2-1}}\end{flalign}$ | $\begin{flalign}\frac{dsec^{-1}x}{dx}=-\frac{1}{\|x\|\sqrt{x^2-1}}\end{flalign}$ |
## Recitation Techniques
derivative of a trigonometric co-function always is negative
### sin and cos
derivative = clockwise
integral = counterclockwise
```mermaid
flowchart LR
    -cosx <--> -sinx
    -cosx <--> sinx
    sinx <--> cosx
    -sinx <--> cosx
```

### the rest
The derivative of the function is the product of the other cells in the row

|     |     |     |
| :---: | :---: | :---: |
| tan | sec | sec |
| cot | csc | csc |

The derivative of the co-function of a trigonometric functional inverse is always the negative of its direct function