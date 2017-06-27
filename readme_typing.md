ⓒ JMC 2017

**COURSE**  
\- 서울대학교 4차산업혁명 아카데미  
\- 인공지능 에이전트 과정  
\- 기계학습 기초수학, 김종권 교수님

**SOURCE**  
\- Introduction to Linear Algebra, Strang (The most desired way to learn)  
\- [MIT 선형대수학 Strang 교수 강의 ](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8)  
\- [KOCW 건국대 이향원 교수 강의](http://www.kocw.net/home/search/kemView.do?kemId=1039395)  
\- 김종권 교수님 수업 자료

**RESUME**  
\- KOCW : `3.2 00:00~`  
\- TEXTBOOK : `p.125`

---

## One-Sentence Summary

### 0. 선형방정식 Linear Equations

+ $Ax=b$에서 $x$를 구해야 한다.
+ $Ax$란 행렬 $A$의 모든 칼럼들의 linear combination을 뜻한다.

### 1. 가우스 소거법 Gaussian Elimination

+ 가우스 소거법은 선형방정식을 풀기 위해 사용한다.
+ $Ax=b$의 형태를 $Ux=b'$의 형태로 바꿔주는 것이 가우스 소거법이다.

### 2. 첨가 행렬 Augmented Matrix

+ $Ax=b \Rightarrow [A \ | \ b] \Rightarrow [U \ | \ b'] \Rightarrow Ux = b''$
+ 가우스 소거법을 진행할 때 첨가행렬을 사용하면 편안하게 연산할 수 있다.

### 3. 가우스-조던 소거법으로 역행렬 구하기 Inverse Matrix Using Gauss-Jordan Elimination

1. $AA^{-1} = I$ ......................................... $A^{-1} = [x \ y \ z]$.
2. $A[x \ y \ z] = I$ .................................... $I = [e_1 \ e_2 \ e_3]$
3. $[Ax \ Ay \ Az] = [e_1 \ e_2 \ e_3]$
4. $Ax = e_1, \ Ay = e_2, \ Az = e_3$ ........ $[A \ | \ e_1], \ [A \ | \ e_2], \ [A \ | \ e_3]$
5. $[A \ | \ e_1 \ e_2 \ e_3]$ .....................................행렬 $A$를 가우스 소거법으로 $U$로 만든다.
6. $[U \ | \ e_1' \ e_2' \ e_3']$ .................................... 행렬 $U$를 가우스-조던 소거법으로 $I$로 만든다.
7. $[I \ | \ e_1'' \ e_2'' \ e_3'']$
8. $I[x \ y \ z] = [e_1'' \ e_2'' \ e_3''] $
9. $\therefore A^{-1} = [x \ y \ z] = [e_1'' \ e_2'' \ e_3'']$

### 4. A = LU Factorization

+ $Ax=b \Rightarrow Ux=b''$으로 바꿔주기 위해 $E$(Elimination)를 곱해준다.
+ $E_{3}E_{2}E_{1}A = U \Rightarrow A = E_{1}^{-1}E_{2}^{-1}E_{3}^{-1}U \Rightarrow A = LU $
+ 행렬 $A$는 $LU$로 분해된다.

### 5. Ax=b와 Subspaces

+ $Ax=b$에서 $x$는 존재할 수도 있고 존재하지 않을 수도 있다.
+ $Ax$를 공간으로 나타냈을 때 그 공간 안에 $b$가 포함되면 solution을 구한 것이다.
+ 만약 행렬 $A$가 만드는 공간이 3차원의 Subspace인 plane이라면, b가 그 plane에 포함될 확률은 매우 낮을 것이다.
  + 3차원 공간에서 plane은 두께가 0이며 차지하는 비율이 매우 작다.

### 6. Ax=b와 C(A)

+ $Ax=b$에서 $x$는 존재할 수도 있고 존재하지 않을 수도 있다.
  + $C(A)$에 $b$가 속하면 $x$는 존재한다.
  + $C(A)$에 $b$가 속하지 않으면 $x$는 존재하지 않는다.

### . C(A)와 N(A)

+ $C(A)$ : 행렬 $A$의 모든 칼럼($m$차원 벡터)들의 linear combination을 모아 놓은 집합
+ $N(A)$ : $Ax=0$을 만족시키는 모든 $x$($n$차원 벡터)를 모아 놓은 집합

### . Ax=b와 C(A)의 관계

+ 선형방정식 $Ax=b$를 푸는 것은 $b$를 행렬 $A$의 모든 칼럼들의 linear combination으로 표현하겠다는 것과 같다.
+ 행렬 $A$의 모든 칼럼들의 linear combination을 모아 놓은 것이 바로 $C(A)$이다.
+ $C(A)$로 $b$를 만들어낼 수 있다면 $x$를 구한 것이고, 그렇지 못하다면 해가 존재하지 않는 것이다.





---

## 03 Vector spaces and Subspaces (5) N(A) & Complete solution to Ax=b

### N(A)를 표현하는 방법 Describing N(A)





---

## 03 Vector spaces and Subspaces (5) 부분공간

### 부분공간의 조건 Subspace

$$(1) \ u + v \in S, \ \forall u, v \in S$$
$$(2) \ cv \in S, \ \forall v \in S$$

+ (1) $S$에 속하는 어떤 벡터들의 linear combinaion한 결과 벡터도 $S$에 속해야 한다.
+ (2) $S$에 속하는 벡터에 스칼라곱한 결과 벡터도 $S$에 속해야 한다.
+ 위 두 가지 조건을 모두 만족하면 Subspace가 된다.
+ Subspace는 항상 영 벡터를 포함하고 있다.

### 행렬에 의해 정의되는 Subspace 4가지

```
1. C(A)
2. N(A)
```

### C(A) :: Column space of A (m by n)

$$\begin{array}{rcl} C(A) & = & \{Ax \ | \ \forall x \in R^{n} \} \\ & = &
\{[a_1 \ a_2 \ \cdot \cdot \ a_n] \begin{bmatrix}
x_1 \\
x_2 \\
\cdot \\
\cdot \\
x_n
\end{bmatrix}
| \ \forall x \in R^{n} \} \\
& = & \{ x_1a_1 + \cdot \cdot + x_na_n, \ \forall x \in R^{n} \} \end{array}$$

+ 행렬 $A$의 모든 칼럼들의 linear combination을 모아 놓은 집합
+ 행렬 $A$의 각 칼럼은 $m$차원 벡터이므로 $C(A)$는 $R^{m}$의 Subspace이다.
  + $x_1a_1 + \cdot \cdot + x_na_n \in R^{m}$

### 몇 차원 Subspace인지 구하는 방법

+ 안에 들어간 벡터가 몇 차원인지 구하면 된다.

### N(A) :: Null space of A (m by n)

$$\begin{array}{rcl} N(A) & = & \{x \in R^{n} \ | \ Ax = 0 \} \end{array}$$

+ 행렬 $A$에 '**오른쪽**'에 곱해졌을 때 $Ax=0$을 만드는 $n$차원 $x$ 벡터들을 모아 놓은 집합
+ $x$는 $n$차원이므로 $N(A)$는 $R^{n}$의 Subspace이다.

### 실생활에서 쓰이는 C(A), N(A)

$$\begin{bmatrix}
a_1 \\
a_2 \\
\cdot \\
\cdot \\
a_m
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
\cdot \\
\cdot \\
x_n
\end{bmatrix}
=
\begin{bmatrix}
y_1 \\
y_2 \\
\cdot \\
\cdot \\
y_m
\end{bmatrix}$$

+ MRI (자기공명영상, Magnetic Resonance Imaging)
  + 우리 몸 속의 이미지를 보려고 한다.
  + 우리 몸 속에 대한 이미지를 $n$차원 벡터 $x$라고 하자.
  + 미지수가 $n$개이므로 방정식도 최대 $n$개 필요하다.
  + 이미지의 크기가 1024*1024라면 대략 $10^6$, 백만 개의 방정식이 필요하다.
  + 그런데 **이미지에 해당하는 벡터 $x$가 특정 성질을 만족하면 방정식을 $n$보다 훨씬 더 적은 $m$개만 구해도 벡터 $x$를 정확하게 풀어낼 수 있다**.
  + 그러한 기술을 compressed sensing이라 한다.
  + 이러한 성질을 따질 때 $C(A)$와 $N(A)$를 사용하게 된다.

**끝.**

---

## 03 Vector spaces and Subspaces (4) 벡터 공간, 부분 공간, 칼럼 스페이스

### 칼럼벡터와 공간의 의미

+ 공간 : **모든** 벡터(all column vectors)를 모아 놓은 집합
+ $R^{n}$ : (모든) $n$차원 칼럼벡터 $v$로 구성되는 공간
+ $R^{2}$ : (모든) 2차원 칼럼벡터 $v$로 구성되는 공간 = $xy$ plane
+ $R^{1}$ : (모든) 1차원 칼럼벡터 $v$로 구성되는 공간 = Linear

### 공간에 속하는 벡터

+ (4, $\pi$) is in $R^{2}$
+ (1, 1, 0, 1, 1) is in $R^{5}$

### 벡터의 연산과 벡터 공간 Vector space

+ 벡터를 원소로 가지는 집합을 벡터 공간이라 한다.
+ 벡터 공간 $V$에 속하는 벡터들을 연산한 결과 벡터 또한 $V$에 속한다.

### 벡터 공간 예시

+ $M$ : 2 by 2 행렬의 벡터 공간
  + $M$에 속하는 요소를 연산하면 항상 $M$에 속하게 된다.
+ $Z$ : 영 벡터로 구성되는 벡터 공간

### 벡터 공간과 부분 공간 Subspaces

+ 벡터 공간에 속하는 벡터들로 만들어내는 공간을 부분 공간(subspace)이라고 한다.
+ 즉, 벡터들의 linear combination이 부분 공간(subspace)을 만들어낸다.
+ subspace에 속하는 벡터들을 linear combination한 결과 또한 당연히 subspace에 속한다.

### subspace 구분법과 OX 퀴즈

#### 구분법

+ subspace에 속하는 벡터들을 linear combination한 결과가 subspace에 속하지 않으면 그것은 subspace가 아니다.

#### OX 퀴즈

+ A plane in $R^{3}$ that misses the origin : (x) not a subspace
  + plane에 속하는 $v$에 0을 곱한 결과가 plane에 속하지 않기 때문이다.
+ The quarter-plane : (x) not a subspace
  + (2, 3)에 -1을 곱한 결과가 1사분면에 속하지 않기 때문이다.

### 칼럼 스페이스 Column Space

+ $Ax=b$에서 $A^{-1}$이 존재하지 않을 때, 해가 있는지 없는지 어떻게 알 수 있을까.
+ 벡터 공간의 의미로 접근하면 된다.
+ $Ax$는 하나의 벡터 공간인데 행렬 $A$의 칼럼들로 구성되는 공간이므로 칼럼 스페이스 $C(A)$라고 부른다.
+ $C(A)$에 $b$가 속하면 해가 있는 것이고, 속하지 않으면 해가 없는 것이다.

> **Note:** $C(A)$에는 행렬 $A$의 칼럼뿐만 아니라 linear combination의 결과인 $Ax$까지 포함하고 있다.

### 칼럼 스페이스의 subspace

+ 행렬 $A$가 m by n 행렬일 때, 행렬 $A$의 칼럼들은 $m$차원 벡터이다.
+ $m$차원 벡터칼럼은 $R^{m}$에 속한다.
+ 따라서 $C(A)$는 $R^{m}$의 subspace이다.

@@@RESUME: `TEXTBOOK p.125 (To repeat, the attianable ~)`

**끝.**

---

## 02 Solving Linear Equations (3) 가우스 소거법을 행렬 간 곱셈으로 치환하는 방법

### 가우스 소거법을 행렬 간 곱셈으로 치환하기 Elimination as Matrix Mutliplication

```
1. pivot과 multiplier의 연산을 행렬 간 곱셈으로 나타낸다.
```

$$(1) \ \begin{array}{lcr} 2x_{1}+3x_{2} & = & 5 \\ 6x_{1}+12x_{2} & = & 10 \end{array}$$
$$(2) \ \begin{bmatrix}
2 & 3 \\
6 & 12
\end{bmatrix}
\begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix}
=
\begin{bmatrix}
5 \\
10
\end{bmatrix}$$
$$(3) \ \begin{bmatrix}
2 & 3 \\
0 & 3
\end{bmatrix}
\begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix}
=
\begin{bmatrix}
5 \\
-5
\end{bmatrix}$$

+ $(2) Ax = b$에서 $(3) Ux = b'$을 만드는 과정을 행렬 간 곱셈으로 나타낼 수 있다.

$$(2) \ \begin{bmatrix}
2 & 3 \\
6 & 12
\end{bmatrix}
\begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix}
=
\begin{bmatrix}
5 \\
10
\end{bmatrix}$$


$$(4) \ \begin{bmatrix}
1 & 0 \\
-3 & 1
\end{bmatrix}
\begin{bmatrix}
2 & 3 \\
6 & 12
\end{bmatrix}
=
\begin{bmatrix}
2 & 3 \\
0 & 3
\end{bmatrix}$$

+ $(4)$는 다음과 같은 형태로 나타낼 수 있다. $\ E_{21}A = U$

### A = LU, LU Factorization

```
1. 삼각행렬의 대각선이 모두 0이 아니면 역행렬이 존재한다.

<이유>
- 삼각행렬에 속하는 Elimination 행렬은 곱해진 행렬에 대해 특정 효과를 발휘한다.
- 이 효과를 없애주는 것은 항상 존재하며 그것이 바로 역행렬이 된다.
- 따라서 삼각행렬은 대각선이 모두 0이 아니면 항상 역행렬이 존재한다.
```

$$(4) \ \begin{bmatrix}
1 & 0 \\
-3 & 1
\end{bmatrix}
\begin{bmatrix}
2 & 3 \\
6 & 12
\end{bmatrix}
=
\begin{bmatrix}
2 & 3 \\
0 & 3
\end{bmatrix}$$

$$(5) \ E_{21}A = U$$

+ $E_{21}$은 삼각행렬인데 대각선의 값이 모두 0이 아니므로 역행렬이 반드시 존재한다.

$$(6) \ A = E_{21}^{-1}U$$

+ $E_{21}$의 역행렬은 $E_{21}$의 효과를 없애주는 것이다.
+ $E_{21}$의 효과는 $(row_2)' = (row_2) - 3*(row_1)$이다.
+ 효과를 없애주려면 $(row_2)''' = (row_2)' + 3*(row_1)$를 해줘야 한다.

$$(7) \ A = E_{21}^{-1}U = \begin{bmatrix}
1 & 0 \\
3 & 1
\end{bmatrix}U
$$

+ $E_{21}$은 L(Lower TriangLUar)이다.

$$(8) \ A = LU$$

+ 이러한 과정을 보고, 행렬 $A$를 $L$ 곱하기 $U$로 `factorization`(분해)를 했다고 말한다.

> **Note:** `factorization` : 분해, 소인수분해

### LU Factorization을 하는 이유

```
1. Ax = b         # 우리의 목적은 x를 구하는 것
2. A = LU         # 1번 식에 대한 LU factorization
3. LUx = b        # 1번 식에 A=LU 대입
4. Ux = y         # 임의로 정의
5. Ly = b         # 3번 식에 Ux=y 치환
---------------------------------------------------------------------------
Ax = b
Ux = y            # x를 구하려면 y를 알아야 한다
Ly = b            # Ly=b에서 L은 삼각행렬이므로 y를 쉽게 구할 수 있다
                  # Ly=b에서 구한 y를 Ux=y에 적용하면 x 또한 쉽게 구할 수 있다.
----------------------------------------------------------------------------
Ax = b를 풀기 위해 굳이 LU Factorization을 사용할 필요는 없다.
방정식이 하나일 때는 단순히 가우스 소거법을 사용하는 것이 빠를 것이다.

그러나 만약 b의 값이 계속 변경되는 상황에서 x를 구하려면 LU Factorization을 사용하는 것이 효율적이다.
가우스 소거를 1번 하는 것보다 LU Factorization이 훨씬 더 간단하기 때문이다.

그래서 실제로 컴퓨터 소프트웨어인 Matlab에서는 Ax=b를 LU Factorization으로 푼다고 알려져 있다.
```

**끝.**

---

## 02 Solving Linear Equations (2) 가우스 소거법으로 역행렬을 구하는 방법

### 역행렬을 어떻게 구할까 Inverse Matrix

```
1. 가우스-조던 소거법 적용
```

### 가우스-조던 소거법 Gauss-Jordan Elimination

```
1. AA^{-1} = I                     # 역행렬의 성질 활용
2. A^{-1} = [x y z]                # 역행렬을 칼럼 벡터로 변환
3. A[x y z] = I                    # Ax=b 형태로 전환
4. [Ax Ay Az] = [e1 e2 e3]         # 단위행렬을 칼럼 벡터로 변환
5. Ax = e1, Ay = e2, Az = e3       # Ax=b 형태로 전환
6. [A | e1], [A | e2], [A | e3]    # 첨가행렬 형태로 전환
7. [A | e1 e2 e3]                  # 첨가행렬 형태로 전환
```

$$(1) \ AA^{-1}=I$$

+ 어떤 행렬 $A$의 역행렬을 곱하면 단위행렬 $I$가 나온다.

$$(2) \ A=R^{3*3}, \ A^{-1} =
\begin{bmatrix}
x_1 & y_1 & z_1 \\
x_2 & y_2 & z_2 \\
x_3 & y_3 & z_3
\end{bmatrix}
= [x \ y \ z]$$

+ $x, y, z$를 구하는 것이 곧 $A^{-1}$을 구하는 것이다.
+ $(2)$를 $(1)$에 적용시키면 다음과 같다.

$$(3) \ AA^{-1} = A[x \ y \ z] =
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}$$

+ 단위행렬 $I$의 각 칼럼을 $e_{1}, e_{2}, e_{3}$이라고 해보자.

$$(4) \ [Ax \ Ay \ Az] = [e_{1} \ e_{2} \ e_{3}] $$
$$(5) \ Ax=e_{1}, \ Ay=e_{2}, \ Az=e_{3}$$

+ $(5)$ 같은 경우 $Ax=b$의 형태이므로 가우스 소거법을 활용할 수 있다.
+ 그런데 $(5)$에 있는 3가지 식 모두 행렬 $A$에 대한 가우스 소거법이므로 똑같이 진행하게 된다.
+ 가우스 소거법의 결과를 결정짓는 것은 행렬 $A$이므로 한꺼번에 첨가행렬(augmented matrix form)을 활용할 수 있다.

$$(6) \ [A \ | \ e_{1}], \ [A \ | \ e_{2}], \ [A \ | \ e_{3}] $$
$$(7) \ [A \ | \ e_{1} \ e_{2} \ e_{3}]$$

+ $(7)$ 식에 가우스 소거법을 적용하면, $x, y, z$를 구할 수 있다.

$$(8) \ [u \ | \ e_{1}' \ e_{2}' \ e_{3}'] $$

+ 가우스 소거법에서는 행렬 $A$를 행렬 $U$로 만들었다.

$$(9) \ [I \ | \ e_{1}'' \ e_{2}'' \ e_{3}'']$$
$$(10) \ I[x \ y \ z] = [e_{1}'' \ e_{2}'' \ e_{3}'']$$

+ 그러나 가우스-조던 소거법에서는 행렬 $A$를 단위행렬 $I$로 만들어준다.

### 가우스 소거법 vs. 가우스-조던 소거법 Gauss Elimination vs. Gauss-Jordan Elimination

```
1. 가우스 소거법

Ax = b
[A | b]
[u | b']
Ux = b'
------
>> back substitution을 통해 칼럼 벡터 x의 각 값(unknowns)을 구한다.


2. 가우스-조던 소거법

Ax = b
[A | b]
[u | b']
[I | b'']
Ix = b''
-------
>> 행렬 A의 역행렬 A^{-1}을 구한다.
```

**끝.**

---

## 02 Solving Linear Equations (1) 가우스 소거법

### 선형 방정식을 어떻게 풀까 Solving Linear Equations

```
1. 가우스 소거법 적용
```

### 가우스 소거법 Gauss Elimination

```
Ax = b => Ux = b' (b prime)

1) Ax = b
2) Gauss Elimination
3) Ux = b
4) back substitution
```

$$\begin{array}{lcl} x_{1}+2x_{2} & = & 5 \\ 2x_{1}+5x_{2} & = & 12 \end{array}$$

+ 방정식을 $Ax=b$로 표현한다.

$$\begin{bmatrix} 1 & 2 \\ 2 & 5 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$$

+ Gauss Elimination으로 행렬 $A$를 $U$(upper triangLUar)로 만들어준다.

$$\begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix}  \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 5 \\ 2 \end{bmatrix}$$

+ 다시 방정식으로 나타낸다.

$$\begin{array}{rcl} x_{1}+2x_{2} & = & 5 \\ x_{2} & = & 12 \end{array}$$

+ back substitution을 통해 아래에서부터 미지수의 값을 차례대로 대입하면 쉽게 해를 구할 수 있다.

### 피봇과 멀티플라이어 Pivot and Multiplier

```
Pivot : 소거되지 않는 row의 첫 번째 값
Multiplier : 소거될 row의 첫 번째 값을 Pivot으로 나눈 값
```

$$\begin{bmatrix} 1 & 2 \\ 2 & 5 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$$

+ Pivot = 1
+ Multiplier = 2

### 첨가행렬 Augmented Matrix Form

```
Ax = b => [A | b] => [u | b'] => Ux = b'

행렬 A에 칼럼벡터 b를 붙여서 하나의 행렬로 나타낸 것을 첨가행렬이라 한다.

가우스 소거법을 적용하면 A의 row와 b의 row가 같은 연산을 적용 받는다.
어차피 같은 연산을 적용 받으니 행렬 A에 b를 추가하여 첨가행렬로 만들 수 있다.
```

$$
\begin{bmatrix}
1 & 2 & 3 \\
2 & 2 & 4 \\
3 & 7 & 9
\end{bmatrix}
\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix}
=
\begin{bmatrix}
5 \\
7 \\
10
\end{bmatrix}$$

+ 위 행렬의 형태를 $Ax=b$라고 할 때
+ 가우스 소거에서 $x$는 아무런 관여를 하지 않는다.
+ 가우스 소거의 결과를 결정하는 것은 행렬 $A$이다.

$$
\begin{bmatrix}
1 & 2 & 3 & | & 5 \\
2 & 2 & 4 & | & 7 \\
3 & 7 & 9 & | & 10
\end{bmatrix}
$$

+ 따라서 가우스 소거에서 필요 없는 것을 제외하면 하나의 행렬로 나타낼 수 있다.

$$
\begin{bmatrix}
1 & 1 & 1 & | & 5 \\
0 & 0 & 2 & | & -3 \\
0 & 4 & 6 & | & -5
\end{bmatrix}
$$

+ 가우스 소거를 통해 위와 같은 형태가 만들어진다.

$$
\begin{bmatrix}
1 & 1 & 1 & | & 5 \\
0 & 4 & 6 & | & -5 \\
0 & 0 & 2 & | & -3
\end{bmatrix}
$$

+ 2번째 행과 3번째 행을 바꿔서 $Ux=b$ 형태로 만들어준다.

**끝.**

---
