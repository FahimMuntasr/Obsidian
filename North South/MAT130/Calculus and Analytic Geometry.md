---
Relations:
  - "[[Discrete Mathematics]]"
  - "[[Introduction to Linear Algebra]]"
---
---
$$\int du = u + C$$
$$\int a\;du = a \int du = au + C$$
$$\int u^r\;du = \frac{u^{r+1}}{r+1} + C, r\neq -1$$
$$\int\frac{du}{u} = \ln|u|+C$$
$$\int e^u\;du = e^u +C$$
$$\int b^u\;du = \frac{b^u}{\ln b} + C,b>0,b\neq -1$$
---
$$\int \sin u\;du=-\cos u +C$$$$\int\cos u\;du=\sin u+C$$
$$\int\sec ^2 u\;du=\tan u+C$$
$$\int\csc ^2 u\;du=-\cot u+C$$
$$\int\sec u\tan u\;du=\sec u+C$$
$$\int\csc u\cot u\;du=-\csc u+C$$
$$\int\tan u\;du=-\ln|\cos u|+C$$
$$\int\cot u\;du=\ln|\sin u|+C$$
---
$$\int\sinh u\;du=\cosh u+C$$
$$\int\cosh u\;du=\sinh u+C$$
$$\int\text{sech}^2\;u\;du=\tanh u+C$$
$$\int\text{csch}^2\;u\;du=-\coth u+C$$
$$\int\text{sech}\;u\tanh u\;du=-\text{sech}\;u+C$$
$$\int\text{csch}\;u\coth u\;du =-\text{csch}\;u+C$$
---
$$\int\frac{du}{\sqrt{a^2-u^2}}=\sin^{-1}\frac{u}{a}+C$$
$$\int\frac{du}{{a^2+u^2}}=\frac{1}{a}\tan^{-1}\frac{u}{a}+C$$
$$\int\frac{du}{u\sqrt{u^2-a^2}}=\frac{1}{a}\sec^{-1}\left|\frac{u}{a}\right |+C$$
$$\int\frac{du}{\sqrt{a^2+u^2}}=\ln(u+\sqrt{u^2+a^2})+C$$
$$\int\frac{du}{\sqrt{u^2-a^2}}=\ln \left| u+\sqrt{u^2-a^2}\right|+C$$
$$\int\frac{du}{a^2-u^2} = \frac{1}{2a}\ln\left|\frac{a+u}{a-u}\right|+C$$
$$\int\frac{du}{u\sqrt{a^2-u^2}}=-\frac{1}{a}\ln\left|\frac{a+\sqrt{a^2-u^2}}{u}\right|+C$$
$$\int\frac{du}{u\sqrt{a^2+u^2}}=-\frac{1}{a}\ln\left|\frac{a+\sqrt{a^2+u^2}}{u}\right|+C$$
---
$$\int f(x)g(x)\;dx = f(x)G(x)\;dx\;-\int f'(x)G(x)\;dx\; ,\;G(x) = \int g(x)\;dx$$
---
$$\int\sin ^n x\;dx=-\frac{\sin ^{n-1}x\cos x}{n}+\frac{n-1}{n}\int\sin^{n-2}x\;dx$$
$$\int\cos^nx\;dx=\frac{\cos^{n-1}x\sin x}{n}+\frac{n-1}{n}\int\cos^{n-2}x\;dx$$
For $\int\sin ^mx\cos ^nx\;dx$ ;
$n$ is odd, $u=\sin x$ , $\cos ^2x=1-\sin ^2x$
$m$ is odd,$u=\cos x$ , $\sin ^2x = 1-\cos ^2x$
$m$ and $n$ is even, $\sin^2x=\frac{1}{2}(1-\cos2x)$, $\cos^2x=\frac{1}{2}(1+\cos2x)$

---

$$\int\tan^n\;dx=\frac{\tan^{n-1}x}{n-1}-\int\tan^{n-2}x\;dx$$
$$\int\sec^nx\;dx=\frac{\sec^{n-2}x\;tanx}{n-1}+\frac{n-2}{n-1}\int\sec^{n-2}x\;dx$$
$$\int\tan x\;dx=\ln|\sec x|+C$$
$$\int\sec x\;dx=\ln|\sec x+\tan x|+C$$
For $\int\tan^mx\sec^nx\;dx$ ;
$n$ is even, $u=\tan x$ , $\sec ^2x=\tan ^2x+1$
$m$ is odd,$u=\sec x$ , $\tan ^2x =\sec ^2x-1$
$m$ is even and $n$ is odd, $\tan ^2x =\sec ^2x-1$

---

$$\sin\alpha\cos\beta=\frac{1}{2}[\sin(\alpha-\beta)+\sin(\alpha+\beta)]$$
$$\sin\alpha\sin\beta=\frac{1}{2}[\cos(\alpha-\beta)-\cos(\alpha+\beta)]$$
$$\cos\alpha\cos\beta=\frac{1}{2}[\cos(\alpha-\beta)+\cos(\alpha+\beta)]$$
---
Trigonometric substitutions;
$\sqrt{a^2-x^2} \rightarrow x=a\sin\theta\rightarrow a^2-a^2\sin ^2\theta\rightarrow a^2(1-\sin ^2\theta)\rightarrow a^2\cos ^2\theta$ 
$\sqrt{a^2+x^2}\rightarrow x=a\tan\theta\rightarrow a^2+a^2\tan ^2\theta\rightarrow a^2(1+\tan ^2\theta)\rightarrow a^2\sec ^2\theta$
$\sqrt{x^2-a^2}\rightarrow x=a\sec\theta\rightarrow a^2\sec ^2\theta -a^2\rightarrow a^2(\sec ^2\theta -1)\rightarrow a^2\tan ^2\theta$
