# 3.1 Sucesiones superoscilantes

**Definición 3.1.1.** Una sucesión generalizada de Fourier es una sucesión de la forma
$$
Y_{n,a}(x)=\sum_{j=0}^n C_j(n,a)\exp(ik_j(n)x) 
$$
donde $a>0$, $n\in \mathbb N$ y los $C_j(n,a),k_j(n)$ son números reales.

**Comentario 3.1.2.** Una sucesión de sumas parciales de Fourier es un caso particular.

**Definición. 3.1.3.** Sean $a>0,\alpha>0$. Una sucesión generalizada de Fourier $(Y_n(x))$  como la de la definición 3.1.1. se dice superoscilante si

1. $|k_j(n)|\leq \alpha$ para todo $n$ y para todo $j$.
2. Existe un compacto $K\subset \mathbb R$ no vacío,  que llamaremos conjunto de superoscilación, de modo que $Y_n(x)\to \exp(ig(a)x)$ uniformemente en $K$, donde $g(a)$ es una función continua de $a$ tal que $|g(a)|≥\alpha$. 

Obviamente una sucesión de sumas parciales de Fourier no es superoscilante pues no satisfacen el primer punto de la definición 3.1.3.

Se puede considerar un escenario diferente.

**Definición 3.1.4.** Sea $\displaystyle f(x)= \sum_{j=0}^\infty d_j\exp(ia_jx)$ donde $a_j,d_j\in\mathbb R$ para todo $j=0,1,\dots$. Diremos que la sucesión 
$$
S_n(x)=\sum_{j=0}^n C_j(n)\exp(ik_j(n)x)
$$
con $C_j(n),k_j(n)\in\mathbb R$ es $f$-superoscilante si existe un índice $J$ de modo que $\displaystyle \sup_{n,j}|k_j(n)|<a_J$ y además la sucesión $(S_n(x))$ convergen uniformemente a $f$ en algún conjunto compacto no vacío de $\mathbb R$.

**Comentario 3.1.5.** Me lo salto. No entiendo bien lo que quiere decir.

**Comentario 3.1.6.** Me lo salto. No entiendo lo que quiere decir.

El ejemplo fundamental de sucesión superoscilante en el sentido de la Definición $3.1.3$  es el siguiente
$$
\boxed{F_n(x,a)=\left(\cos\left(\frac{x}{n}\right)+ia\sin\left(\frac{x}{n}\right)\right)^n}
$$
donde $a>1, n\in\mathbb N$ y $x\in\mathbb R$.

Observemos que $F_n(x)$ se puede escribir así
$$
F_n(x,a)=\left(\frac{1+a}{2}\exp(ix/n)+\frac{1-a}{2}\exp(-ix/n)\right)^n
$$
simplemente poniendo a $\cos(x/n)$ y $\sin(x/n)$ en términos de la exponencial compleja usando las fórmulas
$$
\cos(\theta)=\frac{\exp(i\theta)+\exp(-i\theta)}{2}, \,\, \sin(\theta)=\frac{\exp(i\theta)-\exp(-i\theta)}{2i}
$$
**Teorema 3.1.7.** Sea $a>1$. Sea $n\in\mathbb N$. Consideremos $\displaystyle F_n(x,a)=\left(\cos(x/n)+ia\sin(x/n)\right)^n$. 

1. $\displaystyle \lim_{n\to +\infty}F_n(x,a)=\exp(iax)$ para todo $x\in\mathbb R$.

2. $\displaystyle F_n(x,a)=\sum_{j=0}^n C_j(n,a)\exp(i(1-2j/n)x)$ donde los coeficientes de Fourier $C_j(n,a)$ vienen dados por la fórmula
   $$
   C_j(n,a)=\frac{(-1)^j}{2^n}\binom{n}{j}(a+1)^{n-j}(a-1)^j.
   $$

3. Para cada $p\in\mathbb N$ se tiene la siguiente relación entre los coeficientes de Taylor y los de Fourier

$$
F_n^{(p)}(0,a)=\sum_{j=0}^n C_j(n,a)\left(i\left(1-\frac{2j}{n}\right)\right)^p
$$

**Demostración del Teorema 3.1.7.**  Para demostrar (1) fijemos $x\in\mathbb R$. Escribimos
$$
F_n(x,a)=\exp(n\log(\cos(x/n)+ia\sin(x/n)))
$$
siendo $\log$ el logaritmo principal.  Tenemos en cuenta que $\log(\cos(x/n)+ia\sin(x/n))$ es un infinitésimo equivalente a $(\cos(x/n)-1)+ia\sin(x/n)$ cuando $n\to+\infty$ y por lo tanto
$$
\begin{aligned}
\lim_{n\to+\infty} n\log(\cos(x/n)+ia\sin(x/n))&=\lim_{n\to+\infty} n((\cos(x/n)-1)+ia\sin(x/n))\\
&=\lim_{n\to +\infty} n((\cos(x/n)-1)+ia\lim_{n\to +\infty} n\sin(x/n)\\
&=0+iax
\end{aligned}
$$
ya que $\cos(x/n)-1$ es un infinitésimo equivalente a $-(x/n)^2/2$ cuando $n\to+\infty$ y $\sin(x/n)$ es un infinitésimo equivalente a $x/n$ cuando $n\to+\infty$.

Para demostrar (2) usamos la fórmula del binomio de Newton
$$
\left(\frac{1+a}{2}\exp(ix/n)+\frac{1-a}{2}\exp(-ix/n)\right)^n=\frac{1}{2^n}\sum_{j=0}^n (-1)^j\binom{n}{j}(a+1)^{n-j}(a-1)^j\exp(i(1-2j/n))
$$
Y por último (3) es directo por derivación. $\square$

**Teorema 3.1.8.** Sea $M>0$. La sucesión $(F_n(x,a))$ converge uniformemente a $\exp(iax)$ en el intervalo $[-M,M]$.

**Demostración del Teorema 3.1.8.** Tenemos que demostrar que
$$
\lim_{n\to+\infty}\sup_{|x|\leq M}|F_n(x,a)-\exp(iax)|= 0
$$
Teorema 3.1.9. La sucesión $(F_n(x,a))$ no converge uniformemente a $\exp(iax)$ en $\mathbb R$.

**Demostración del Teorema 3.1.9.** Sea $a\in\mathbb R\setminus \mathbb Z$. Basta observar que si $x_n=n\pi$ entonces
$$
|F(x_n,a)-\exp(iax_n)|=|(\pm 1)^n -\exp(ian\pi)|\not\to 0
$$
Si $a\in\mathbb Z$ podemos tomar $x_n=n\pi/2$. $\square$

Comentario 3.1.10. El teorema 3.1.7. demuestra que bajo ciertas condiciones cualquier función que pueda ser representada como una serie de Fourier de exponenciales puede en realidad ponerse como límite de una sucesión superoscilante. Este comentario hay que estudiarlo porque  lo que dice no está tan claro.

Comentario 3.1.11. Observemos que para todo número natural $n$ se tiene 
$$
1=F_n(0,a)=\sum_{j=0}^n C_j(n,a)
$$
y también
$$
ia=F_n'(0,a)=\sum_{j=0}^n C_j(n,a)i\left(1-\frac{2j}{n}\right)
$$
de donde 
$$
a=\sum_{j=0}^n C_j(n,a)\left(1-\frac{2j}{n}\right)
$$
**Teorema 3.1.12.** Para cualesquiera $a,x\in\mathbb R$ y para cualesquiera  $n,p\in\mathbb N$  se tiene que
$$
F_n^{(p)}(x,a)=\sum_{k_1,k_2,\dots,k_n=0 \\ k_1+k_2+\dots+k_n=p}^p \frac{p!}{k_1!k_2!\dots k_n!}g^{(k_1)}\dots g^{(k_n)}
$$
**Demostración del Teorema 3.1.12.**

