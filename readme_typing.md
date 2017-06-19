ⓒ JMC 2017

**COURSE**  
\- 서울대학교 4차산업혁명 아카데미  
\- 인공지능 에이전트 과정  
\- 기계학습 기초수학, 김종권 교수님

**SOURCE**  
\- Introduction to Linear Algebra, Strang  
\- [MIT 선형대수학 Strang 교수 강의 ](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8)  
\- [KOCW 건국대 이향원 교수 강의](http://www.kocw.net/home/search/kemView.do?kemId=1039395)  
\- 김종권 교수님 수업 자료

---

## 02 Solving Linear Equations (4) Transpose와 Symmetric Matrix

@@@resume : 2_2, 00:44:35

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

+ $(2) Ax = b$에서 $(3) ux = b'$을 만드는 과정을 행렬 간 곱셈으로 나타낼 수 있다.

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

+ $(4)$는 다음과 같은 형태로 나타낼 수 있다. $\ E_{21}A = u$

### A = LU, LU Factorization

```
1. 삼각행렬의 대각선이 모두 0이 아니면 역행렬이 존재한다.
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

$$(5) \ E_{21}A = u$$

+ $E_{21}$은 삼각행렬인데 대각선의 값이 모두 0이 아니므로 역행렬이 반드시 존재한다.

$$(6) \ A = E_{21}^{-1}u$$

+ $E_{21}$의 역행렬은 $E_{21}$의 효과를 없애주는 것이다.
+ $E_{21}$의 효과는 $(row_2)' = (row_2) - 3*(row_1)$이다.
+ 효과를 없애주려면 $(row_2)''' = (row_2)' + 3*(row_1)$를 해줘야 한다.

$$(7) \ A = E_{21}^{-1}u = \begin{bmatrix}
1 & 0 \\
3 & 1
\end{bmatrix}u
$$

+ $E_{21}$은 L(Lower Triangluar)이다.

$$(8) \ A = LU$$

+ 이러한 과정을 보고, 행렬 $A$를 $L$ 곱하기 $u$로 `factorization`(분해)를 했다고 말한다.

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
ux = b'
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
Ax = b => ux = b' (b prime)

1) Ax = b
2) Gauss Elimination
3) ux = b
4) back substitution
```

$$\begin{array}{lcl} x_{1}+2x_{2} & = & 5 \\ 2x_{1}+5x_{2} & = & 12 \end{array}$$

+ 방정식을 $Ax=b$로 표현한다.

$$\begin{bmatrix} 1 & 2 \\ 2 & 5 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$$

+ Gauss Elimination으로 행렬 $A$를 $U$(upper triangluar)로 만들어준다.

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
Ax = b => [A | b] => [u | b'] => ux = b'

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

+ 2번째 행과 3번째 행을 바꿔서 $ux=b$ 형태로 만들어준다.

**끝.**

---
