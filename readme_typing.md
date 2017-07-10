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

### 01 선형방정식 Linear Equations

+ $Ax=b$에서 $x$를 구해야 한다.
+ $Ax$란 행렬 $A$의 모든 칼럼들의 linear combination을 뜻한다.

### 02~03 Ax=b를 푸는 방법 (1) 가우스 소거법

+ $Ax=b \Rightarrow Ux=b'$
+ 행렬 $A$를 $U$형태로 바꾼 후 back substitution을 적용하여 $x$를 하나씩 구한다.

### 04 첨가 행렬 Augmented Matrix

+ $Ax=b \Rightarrow [A \ | \ b] \Rightarrow [U \ | \ b'] \Rightarrow Ux = b'$
+ 가우스 소거법을 진행할 때 첨가행렬을 사용하면 간편하게 연산할 수 있다.

### 05~06 Ax=b를 푸는 방법 (2) 가우스-조던 소거법

+ 역행렬을 구하는 방법이다.
+ $AA^{-1}=I \Rightarrow A[x \ y \ z] = [e_1 \ e_2 \ e_3] \Rightarrow U[x \ y\ z] = [e_1' \ e_2' \ e_3'] \Rightarrow I[x \ y \ z] = [e_1'' \ e_2'' \ e_3'']$
+ 역행렬을 구했으니 $Ax=b$의 양변에 역행렬을 곱하면 $x$를 한꺼번에 구할 수 있다.
+ $Ax=b \Rightarrow A^{-1}Ax=A^{-1}b \Rightarrow x = A^{-1}b$

### 07 A = LU Factorization

+ $Ax=b \Rightarrow Ux=b'$으로 바꿔주기 위해 $E$(Elimination)를 곱해준다.
+ $E_{3}E_{2}E_{1}A = U \Rightarrow A = E_{1}^{-1}E_{2}^{-1}E_{3}^{-1}U \Rightarrow A = LU $ ($E$는 항상 $L$ 형태를 유지하므로)
+ 행렬 $A$는 $LU$로 분해된다.

### 08 Ax=b를 푸는 방법 (3) 칼럼 스페이스

+ '**해가 존재하는지 존재하지 않는지 판별할 수 있는 방법**'이다.
+ $Ax=b$에서 $A^{-1}$이 존재하지 않을 때, 해가 있는지 없는지 어떻게 알 수 있을까.
+ 공간의 관점으로 접근하면 된다.
+ $Ax$는 하나의 벡터 공간인데 행렬 $A$의 칼럼들이 $span$하여 만드는 공간이므로 칼럼 스페이스 $C(A)$라고 부른다.
+ $C(A)$에 $b$가 속하면 해가 있는 것이고, 속하지 않으면 해가 없는 것이다.

### 09 Example :: 칼럼 스페이스 묘사하기

$(1) \ I =
\begin{bmatrix}
1 & 0\\
0 & 1
\end{bmatrix}
$

+ 행렬 $I$의 칼럼벡터는 2차원이다.
+ 2차원 칼럼벡터 2개가 independent하다.
+ 행렬 $I$의 칼럼벡터로 모든 2차원 공간을 만들 수 있다.
+ $C(I) \rightarrow R^{2}$

$(2) \ A =
\begin{bmatrix}
1 & 2\\
2 & 4
\end{bmatrix}
$

+ 행렬 $A$의 칼럼벡터는 2차원이다.
+ 2차원 칼럼벡터 2개가 서로 dependent하다.
+ 2차원에서 칼럼벡터 1개는 line을 만들어낸다.
+ $C(A) \subset R^{2}$

$(3) \ B =
\begin{bmatrix}
1 & 2 & 0 \\
0 & 0 & 4
\end{bmatrix}
$

+ 행렬 $B$의 칼럼벡터는 2차원이다.
+ 2차원 칼럼벡터 3개 중 2개가 서로 dependent하다.
+ 2차원에서 칼럼벡터 2개는 모든 2차원 공간을 만든다.
+ $C(B) \rightarrow R^{2}$

### 09 Problem :: C(A)를 고려하여 Ax=b를 만족시키는 적절한 b 만들기

$20.(a) \ \begin{bmatrix}
1 & 4 & 2 \\
2 & 8 & 4 \\
-1 & -4 & -2
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
x_3
\end{bmatrix}
=
\begin{bmatrix}
b_1 \\
b_2 \\
b_3
\end{bmatrix}
$

+ $C(A)$는 3차원 벡터 3개가 모두 dependent하다.
+ $C(A)$는 3차원 공간의 line이다.
+ $b$는 반드시 $C(A)$에 속해야 하므로 $[1 \ 2 \ {-}1]$과 같은 선상에 있으면 된다.
+ $\therefore b = [b_1 \ 2b_1 \ {-}b_1]$

$20.(b) \ \begin{bmatrix}
1 & 4 \\
2 & 9 \\
-1 & -4
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2
\end{bmatrix}
=
\begin{bmatrix}
b_1 \\
b_2 \\
b_3
\end{bmatrix}
$

+ $C(A)$는 3차원 벡터 2개가 서로 independent하다.
+ $C(A)$는 3차원 공간에서 2차원 plane이다.
+ 행렬 $A$의 칼럼벡터를 $[a_1 \ a_2 \ a_3]$라고 할 때, $a_1$과 $a_3$의 비율은 고정되고 $a_2$만 움직인다.
+ $b$는 반드시 $C(A)$에 속해야 하므로 $b_1$과 $b_3$의 비율만 고정시키면 된다.
+ $\therefore b_3 = -b_1$

### 10 널스페이스의 정의

+ $N(A)$: $Ax=0$을 만족시키는 모든 벡터 $x$의 집합을 공간으로 표현한 것
+ $N(A) \subseteq R^{n}$: 벡터 $x$는 $n$차원이므로 널스페이스는 $R^{n}$의 subspace가 된다.
+ 행렬 $A$의 역행렬(invertible matrix)이 존재하면 $Ax=0$의 유일한 해는 $x=0$이므로 free variable은 존재하지 않고 $N(A)=Z$가 된다.

### 10 Example :: 널스페이스 구하는 방법

$(3) \ U =
\begin{bmatrix}
1 & 2 & 2 & 3 \\
0 & 0 & 4 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix}$

+ pivot 칼럼은 1번째와 3번째이다.
+ free variable이 2개이므로 speicla solution도 2개 존재한다.
+ free variable에 1과 0을 대입해서 special solution을 만들 수 있다.
+ $x_2, x_4$에 $(1,0)$을 대입하면 $x_3=0, x_1=-1$이 나온다. $s_1 = (-1,1,0,0)$
+ $x_2, x_4$에 $(0,1)$을 대입하면 $x_3=-1, x_1=-1$이 나온다. $s_2 = (-1,0,-1,1)$
+ $N(U)$는 $s_1$과 $s_2$의 linear combination이다.
+ free 칼럼인 $x_2, x_4$에는 어떤 값을 넣어도 상관 없으므로 다음과 같다.
+ $\therefore x = x_2 \begin{bmatrix}
-1 \\
1 \\
0 \\
0
\end{bmatrix} + x_4 \begin{bmatrix}
-1 \\
0 \\
-1 \\
1
\end{bmatrix} = \begin{bmatrix}
-x_2-x_4 \\
x_2 \\
-x_4\\
x_4
\end{bmatrix}$

### 10 Reduced Row Echelon Matrix

$(1) \ U =
\begin{bmatrix}
1 & 1 & 2 & 3 \\
0 & 0 & 4 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix} \Rightarrow E = \begin{bmatrix}
1 & 1 & 0 & 1 \\
0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0
\end{bmatrix}
$

+ 행렬 $U$는 pviot 아래에만 0을 가지면 된다.
+ 행렬 $E$는 **pivot 위에도 0을 가져야 한다**.
+ 행렬 $E$의 pivot 칼럼($(1,0,0), \ (0,1,0)$)을 붙여 놓으면 단위행렬 $I$가 된다.

### 11 Ax=0을 푸는 방법 (1) Rx=0으로 푼다

+ 행렬 $A$를 Row Reduced Echelon Form으로 바꾸면 행렬 $R$은 단위행렬과 영행렬 로우로 구성된다.
+ 행렬 $R$의 형태는  $R = \begin{bmatrix}
I & F \\
0 & 0
\end{bmatrix}
$이다.
+ 그러면 널스페이스 $N = \begin{bmatrix}
-F \\
I
\end{bmatrix}
$를 즉시 구할 수 있다.

### 11 행렬 R은 단위행렬과 영행렬 로우로 구성된다

+ 행렬 $A$를 행렬 $R$ 형태로 바꾸고 나면
+ $r \ by \ r$ 단위행렬 $I$가 존재하며
+ 가장 밑에는 $m-r$개의 영행렬 로우가 존재한다.

### 11 rank가 r이면 special solution은 n-r개이다

+ 행렬 $A$가 $m \ by \ n$이고 $rank$가 $r$일 때
+ 벡터 $x$는 $n$차원이고 pivot variable은 이미 $r$개 이므로
+ 나머지 $n-r$이 free variabel의 개수이자 special solution의 개수가 된다.

### 11 Example :: 행렬 R에서 바로 N을 구하는 방법

$(1) \ R = \begin{bmatrix}
1 & 3 & 0 & 2 & -1 \\
0 & 0 & 1 & 4 & 3 \\
0 & 0 & 0 & 0 & 0
\end{bmatrix}
$

+ pivot variable은 $x_1, x_3$이고, free variable은 $x_2, x_4, x_5$이다.
+ special solution의 개수는 3개이고 벡터 $x$는 5차원이므로 행렬 $N$은 5 by 3이다.

$(2) \ F = \begin{bmatrix}
3 & 2 & -1 \\
0 & 4 & 3 \\
0 & 0 & 0
\end{bmatrix}
$

+ $F$를 미리 구해둔다.

$(3) \ N = \begin{bmatrix}
(1) & \\
(2) & \\
(3) & \\
(4) & \\
(5) &
\end{bmatrix} = \begin{bmatrix}
-F \\
I
\end{bmatrix}
$

+ special solution의 개수는 3개이고 벡터 $x$는 5차원이므로 행렬 $N$은 5 by 3이다.
+ special solution을 구하듯이 $x_2, x_4, x_5$부터 (1, 0, 0), (0, 1, 0), (0, 0, 1)을 대입한다.

$(4) \ N = \begin{bmatrix}
(1) & \\
(2) & 1 & 0 & 0 \\
(3) & \\
(4) & 0 & 1 & 0 \\
(5) & 0 & 0 & 1
\end{bmatrix} = \begin{bmatrix}
-F \\
I
\end{bmatrix}
$

+ 나머지 칸은 $-F$로 채운다.

$(5) \therefore \ N = \begin{bmatrix}
(1) & -3 & -2 & 1 \\
(2) & 1 & 0 & 0 \\
(3) & 0 & -4 & -3 \\
(4) & 0 & 1 & 0 \\
(5) & 0 & 0 & 1
\end{bmatrix} = \begin{bmatrix}
-F \\
I
\end{bmatrix}
$


---
---
---

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

## 12 Ax=b에 대한 Complete Solution (3.4)

### Ax=b를 Rx=d 형태로 바꾸기

#### b = (b1, b2, b3)로 일반화하기

$(1) \ \begin{bmatrix}
1 & 3 & 0 & 2 & | & b_1 \\
0 & 0 & 1 & 4 & | & b_2 \\
1 & 3 & 1 & 6 & | & b_3
\end{bmatrix} \Rightarrow \begin{bmatrix}
1 & 3 & 0 & 2 & | & b_1 \\
0 & 0 & 1 & 4 & | & b_2 \\
0 & 0 & 0 & 0 & | & b_3-b_1-b_2
\end{bmatrix} = [R \ | \ d]
$

+ $Ax=b$를 $[A \ | \ b]$와 같이 augmented matrix 형태로 바꿔준다.
+ 행렬 $A$를 Row Reduced Form인 $R$로 바꿔주고 $b$ 칼럼도 같이 연산해준다.
+ 마지막 영행렬 로우를 통해 $b_3-b_1-b_2=0$임을 알 수 있다.

### Example :: Particular Solution 구하기

$(1) \ Ax = b  \Rightarrow
\begin{bmatrix}
1 & 3 & 0 & 2 \\
0 & 0 & 1 & 4 \\
1 & 3 & 1 & 6
\end{bmatrix} \begin{bmatrix}
x_1 \\
x_2 \\
x_3 \\
x_4
\end{bmatrix} = \begin{bmatrix}
1 \\
6 \\
7
\end{bmatrix} \Rightarrow \begin{bmatrix}
1 & 3 & 0 & 2 & | & 1 \\
0 & 0 & 1 & 4 & | & 6 \\
1 & 3 & 1 & 6 & | & 7
\end{bmatrix} = [A \ | \ b]
$

+ $Ax=b$를 $[A \ | \ b]$와 같이 augmented matrix 형태로 바꿔준다.

$(2) \ \begin{bmatrix}
1 & 3 & 0 & 2 & | & 1 \\
0 & 0 & 1 & 4 & | & 6 \\
0 & 0 & 0 & 0 & | & 0
\end{bmatrix} = [R \ | \ d]
$

+ 행렬 $A$를 Row Reduced Form인 $R$로 바꿔주고 바뀐 $b$값을 $d$로 써준다.
+ pivot variable은 $x_1, x_3$이 되고 free variable은 $x_2, x_4$가 된다.

$(3) \ \begin{bmatrix}
1 & 3 & 0 & 2 \\
0 & 0 & 1 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix} \begin{bmatrix}
(x_1) & \\
(x_2) & \\
(x_3) & \\
(x_4) &
\end{bmatrix} = \begin{bmatrix}
1 \\
6 \\
0
\end{bmatrix}
$

+ $Rx=d$ 형태로 복원시켜주고
+ **free variable $x_2, x_4$에 0을 대입한다**.

$(4) \ \begin{bmatrix}
1 & 3 & 0 & 2 \\
0 & 0 & 1 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix} \begin{bmatrix}
(x_1) & \\
(x_2) & 0 \\
(x_3) & \\
(x_4) & 0
\end{bmatrix} = \begin{bmatrix}
1 \\
6 \\
0
\end{bmatrix}
$

+ **나머지 pivot 칼럼은 단위행렬 $I$이므로 $d$에 있는 값을 그대로 써주면 된다**.
+ $x_1 = 1, \ x_3=6$

$(5) \ \begin{bmatrix}
1 & 3 & 0 & 2 \\
0 & 0 & 1 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix} \begin{bmatrix}
(x_1) & 1 \\
(x_2) & 0 \\
(x_3) & 6 \\
(x_4) & 0
\end{bmatrix} = \begin{bmatrix}
1 \\
6 \\
0
\end{bmatrix}
$

+ $Rx=d$를 만족시켜주는 $x$를 particular solution, 즉 $x_{particular}$라고 한다.
+ $x_{particular} = x_{p} = \begin{bmatrix}
1 \\
0 \\
6 \\
0
\end{bmatrix}$

+ $Ax=b$를 만족시키는 particular solution을 구했으니, $Ax=0$을 만족시키는 special solution을 구한다.

### Example :: Special Solution (Nullspace) 구하기

$(6) \ R = \begin{bmatrix}
1 & 3 & 0 & 2 \\
0 & 0 & 1 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix}, \ F = \begin{bmatrix}
3 & 2\\
0 & 4
\end{bmatrix} \Rightarrow N \begin{bmatrix}
(x_1) & \\
(x_2) & 1 & 0 \\
(x_3) & \\
(x_4) & 0 & 1
\end{bmatrix} \Rightarrow N \begin{bmatrix}
(x_1) & -3 & -2 \\
(x_2) & 1 & 0 \\
(x_3) & 0 & -4 \\
(x_4) & 0 & 1
\end{bmatrix}
$

+ $x_{nullspace} = x_{n} = x_2 \begin{bmatrix}
-3 \\
1 \\
0 \\
0
\end{bmatrix} + x_4 \begin{bmatrix}
-2 \\
0 \\
-4 \\
1
\end{bmatrix}
$

### Example :: Complete Solution 구하기

$(7) \ x = x_p + x_n = \begin{bmatrix}
1 \\
0 \\
6 \\
0
\end{bmatrix} + x_2 \begin{bmatrix}
-3 \\
1 \\
0 \\
0
\end{bmatrix} + x_4 \begin{bmatrix}
-2 \\
0 \\
-4 \\
1
\end{bmatrix}
$

+ $x_p$와 $x_n$을 더하면 $Ax=b$에 대한 Complete Solution인 $x$를 구할 수 있다.

### Full column rank (m>n) 행렬 R의 형태

+ Full column rank가 되려면 대각선보다 칼럼 벡터가 많아야 하므로 tall and thin하다.
+ $R = \begin{bmatrix} I \\ 0 \end{bmatrix} =
\begin{bmatrix} (n \ by \ n) \ I \\ (m-n) \ rows \ of \ zeros \end{bmatrix}$

### Full column rank (m>n) 행렬 R의 성질

+ 모든 칼럼이 pivot이므로 free variable이나 speical solution이 존재하지 않는다.
+ special solution이 존재하지 않으므로 $N(A)$는 $x=0$만을 포함한다.
+ $Ax=b$에서 $b$가 $C(A)$에
  + 속한다면 하나의 해 $x_p$만 존재하게 되고
  + 속하지 않는다면 해는 존재하지 않는다.
+ 보통 연립방정식의 해를 풀려면 equation의 수가 최소 unknown의 수만큼 있어야 한다.
+ $m > n$이라는 것은 equation의 수가 unknown보다 많은 것이므로 조건이 넘치는 '**overdetermined**'라고 표현한다.

### Full row rank (m<n) 행렬 R의 형태

+ Full row rank가 되려면 대각선보다 로우 벡터가 많아야 하므로 short and wide하다.
+ 


---

## 11 랭크와 Row Reduced Form (3.3)

### 랭크에 대한 첫 번째 정의

+ $rank$ : 행렬 $A$의 pivot의 개수
+ $rank$ : $Ax=b$에서 중복되는 방정식을 제외한 필수적인 방정식의 수
+ 행렬 $A$에서 linear한 칼럼이나 로우만 추려낸 개수를 의미한다.
+ $rank$가 1일 때 pivot 로우를 제외한 모든 로우는 0이 된다.

### rank one 행렬에서 널스페이스와의 관련성 이끌어내기

#### 1) Elimination으로 pivot 로우, pivot 칼럼 가려내기

$(1) \ A =
\begin{bmatrix}
1 & 3 & 10 \\
2 & 6 & 20 \\
3 & 9 & 30
\end{bmatrix} \Rightarrow \ U =
\begin{bmatrix}
1 & 3 & 10 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{bmatrix}
$

+ rank one 행렬을 elimination하면 pivot 로우를 제외한 모든 로우가 0이 된다.
+ rank one 행렬을 elimination하면 모든 칼럼은 pivot 칼럼의 스칼라곱이 된다.
+ 따라서 rank one 행렬 $A$의 $C(A)$는 1차원이다.

#### 2) 널스페이스를 만드는 벡터 x 가려내기

$(2) \ A =
\begin{bmatrix}
1 & 3 & 10 \\
2 & 6 & 20 \\
3 & 9 & 30
\end{bmatrix} = \begin{bmatrix}
1 \\
2 \\
3
\end{bmatrix} \begin{bmatrix}
1 & 3 & 10
\end{bmatrix}
$

+ 행렬 $A$를 칼럼 * 로우 형태로 나타낼 수 있다.
+ $A = uv^{T}$ (pivot 칼럼 * **pivot 로우**)

$(3) \ Ax = 0 \Rightarrow u(v^{T}x) = 0 \Rightarrow v^{T}x = 0
$

+ $u$는 0이 아니므로 $v^{T}x$가 반드시 0이 되어야 한다.
+ 두 벡터의 곱이 0이라는 것은 두 벡터가 직교한다는 것을 뜻한다.
    + 널스페이스에 존재하는 모든 벡터 $x$는 로우 스페이스에 존재하는 pivot 로우 벡터인 $v$와 반드시 직교한다.
    + 그래프로 나타낸다면 : 로우 스페이스 = line, nullspace = perpendicular plane이 된다.

$(4) \ v^{T}x = \begin{bmatrix}
1 & 3 & 10
\end{bmatrix} \begin{bmatrix}
x_1 \\
x_2 \\
x_3
\end{bmatrix} = 0
$

+ $v^{T}$의 값을 알고 있으니 $x_1, x_2, x_3$의 값을 구할 수 있다.
+ 단, 해는 무수히 많으므로 free variable에 값을 먼저 대입하는 방식으로 special solution을 구한다.
+ free variable인 $x_2, x_3$에 각각 $(1,0), (0,1)$을 대입하면 된다.
+ $s_1 = \begin{bmatrix}
-3 \\
1 \\
0
\end{bmatrix} , \ s_2 = \begin{bmatrix}
-10 \\
0 \\
1
\end{bmatrix}
$

$(5)$ **널스페이스는 로우 스페이스와 직교한다.**

+ special solution의 linear combination으로 널스페이스를 구할 수 있다.
+ 널스페이스 $x + 3y + 10z = 0$ plane은 pivot 로우 벡터인 $(1,3,10)$과 직교한다.

### 랭크에 대한 두 번째 정의

+ $rank$ : pivot column 또는 pivot row의 수 (벡터 관점)

### 랭크에 대한 세 번째 정의

+ $rank$ : 칼럼 스페이스의 또는 로우 스페이스의 차원 (space 관점)
+ $rank(r)$를 알면 자연스럽게 널스페이스도 알게 된다. ($n-r$)


### 행렬 R에서 널스페이스를 바로 구하는 방법

#### 1) pivot 칼럼과 모든 값이 0으로 구성된 로우

$(1) \ R = \begin{bmatrix}
1 & 3 & 0 & 2 & -1 \\
0 & 0 & 1 & 4 & 3 \\
0 & 0 & 0 & 0 & 0
\end{bmatrix}
$

+ 행렬 $A$를 $U$형태로 만든 후 pivot 위에 있는 값도 0으로 만들어서 $R$형태로 만들었다.
+ 행렬 $R$의 pivot 칼럼은 pivot의 값만 1이고 나머지는 0이다.
+ 따라서 r($rank$)개의 pivot 칼럼을 모아두면 r by r의 단위행렬 $I$를 발견할 수 있다.
+ 모든 값이 0으로 구성된 로우는 $m-r$개이다.

#### 중간 정리 :: 행렬 R은 단위행렬과 영행렬 로우로 구성된다

+ 행렬 $A$를 행렬 $R$ 형태로 바꾸고 나면
+ $r \ by \ r$ 단위행렬 $I$가 존재하며
+ 가장 밑에는 $m-r$개의 영행렬 로우가 존재한다.

#### 2) R의 형태를 일반화하기

$(2) \ R' = \begin{bmatrix}
1 & 0 & 3 & 2 & -1 \\
0 & 1 & 0 & 4 & 3 \\
0 & 0 & 0 & 0 & 0
\end{bmatrix}
$

+ 패턴을 발견하기 위해 $R$ 형태에서 pivot 칼럼(col1, col3)과 free 칼럼을 분리해서 보자.
+ pivot 칼럼은 단위행렬 $I$를 만든다.
+ $rank$가 2이므로 $3-2=1$개의 영행렬 로우가 존재한다.
+ 나머지 free 칼럼의 형태를 $F$라고 해보자.

$(3) \ R = \begin{bmatrix}
I & F \\
0 & 0
\end{bmatrix}
$

+ 행렬 $A$를 $R$ 형태로 만들면 단위행렬 $I$와 free 칼럼의 값 $F$의 형태를 보인다.
+ 그리고 여기서 $Rx=0$을 만드는 벡터 $x$의 널스페이스 즉, $N$ 값을 구할 수 있다.

$(4) \ Rx = \begin{bmatrix}
I & F \\
0 & 0
\end{bmatrix} \begin{bmatrix}
x_1 \\
x_2
\end{bmatrix} = 0
$

+ 위 식을 만족시키려면 $x_1 = -F$, $x_2 = I$가 되어야 한다.

$ (5) \therefore \ N = \begin{bmatrix}
-F \\
I
\end{bmatrix}
$

+ 따라서 $N$은 $-F$와 $I$로 구성된다.

### rank가 r이면 special solution은 n-r개이다

+ 행렬 $A$가 $m \ by \ n$이고 $rank$가 $r$일 때
+ 벡터 $x$는 $n$차원이고 pivot variable은 이미 $r$개 이므로
+ 나머지 $n-r$이 free variabel의 개수이자 special solution의 개수가 된다.

### Example :: 행렬 R에서 바로 N을 구하는 방법

$(1) \ R = \begin{bmatrix}
1 & 3 & 0 & 2 & -1 \\
0 & 0 & 1 & 4 & 3 \\
0 & 0 & 0 & 0 & 0
\end{bmatrix}
$

+ pivot variable은 $x_1, x_3$이고, free variable은 $x_2, x_4, x_5$이다.
+ special solution의 개수는 3개이고 벡터 $x$는 5차원이므로 행렬 $N$은 5 by 3이다.

$(2) \ F = \begin{bmatrix}
3 & 2 & -1 \\
0 & 4 & 3 \\
0 & 0 & 0
\end{bmatrix}
$

+ $F$를 미리 구해둔다.

$(3) \ N = \begin{bmatrix}
(1) & \\
(2) & \\
(3) & \\
(4) & \\
(5) &
\end{bmatrix} = \begin{bmatrix}
-F \\
I
\end{bmatrix}
$

+ special solution의 개수는 3개이고 벡터 $x$는 5차원이므로 행렬 $N$은 5 by 3이다.
+ special solution을 구하듯이 $x_2, x_4, x_5$부터 (1, 0, 0), (0, 1, 0), (0, 0, 1)을 대입한다.

$(4) \ N = \begin{bmatrix}
(1) & \\
(2) & 1 & 0 & 0 \\
(3) & \\
(4) & 0 & 1 & 0 \\
(5) & 0 & 0 & 1
\end{bmatrix} = \begin{bmatrix}
-F \\
I
\end{bmatrix}
$

+ 나머지 칸은 $-F$로 채운다.

$(5) \therefore \ N = \begin{bmatrix}
(1) & -3 & -2 & 1 \\
(2) & 1 & 0 & 0 \\
(3) & 0 & -4 & -3 \\
(4) & 0 & 1 & 0 \\
(5) & 0 & 0 & 1
\end{bmatrix} = \begin{bmatrix}
-F \\
I
\end{bmatrix}
$

+ 끝.

**끝.**

---

## 10 널스페이스 (3.2)

### 널스페이스의 정의

+ $N(A)$: $Ax=0$을 만족시키는 모든 벡터 $x$의 집합을 그려낸 공간
+ $N(A) \subseteq R^{n}$: 벡터 $x$는 $n$차원이므로 널스페이스는 $R^{n}$의 subspace가 된다.

### Special solution

+ $Ax=0$을 만족시키는 구체적인 벡터 $x$의 값
+ free variable에 1 또는 0을 대입하여 pivot variable의 값을 구하면 전체 special solution을 구할 수 있다.

### Example :: 널스페이스 묘사하기

$(1) \ A =
\begin{bmatrix}
1 & 2 \\
3 & 8
\end{bmatrix}
$

+ 행렬 $A$를 Elimination하면 각 칼럼은 $(1, 2)$와 $(0, 2)$이다.
+ 행렬 $A$의 모든 칼럼이 pivot 칼럼이므로 special solution은 존재하지 않는다.
+ $Ax=0$을 만족시키는 것은 $x=0$뿐이다.
+ $\therefore N(A) = Z$


$(2) \ B =
\begin{bmatrix}
1 & 2 \\
3 & 8 \\
2 & 4 \\
6 & 16
\end{bmatrix}
$

+ 행렬 $B$를 Elimination하면 각 칼럼은 $(1,0,0,0), \ (2,2,0,4)$이다.
+ 행렬 $B$의 모든 칼럼이 pivot 칼럼이므로 special solution은 존재하지 않는다.
+ $Bx=0$을 만족시키는 것은 $x=0$뿐이다.
+ $\therefore N(B) = Z$

$(3) \ C =
\begin{bmatrix}
1 & 2 & 2 & 4 \\
3 & 8 & 6 & 16
\end{bmatrix}
$

+ 행렬 $C$를 Elimiation하면 $ \ U =
\begin{bmatrix}
1 & 2 & 2 & 4 \\
0 & 2 & 0 & 4
\end{bmatrix}
$가 된다.

+ 행렬 $C$의 3번째, 4번째는 free 칼럼이므로 special soution이 2개 존재한다.
+ $x_3$과 $x_4$에 각각 $(1, 0)$과 $(0, 1)$을 대입한다.
+ $N(C)$를 구성하는 $ \ s_1 =
\begin{bmatrix}
-2 \\
0 \\
1 \\
0
\end{bmatrix}
$과 $ \ s_2 =
\begin{bmatrix}
0 \\
-2 \\
0 \\
1
\end{bmatrix}
$를 구할 수 있다.

+ $N(C)$는 $s_1$과 $s_2$의 linear combination이 된다.

### R.R.E.F (Reduced Row Echelon Form)

$$ \ U =
\begin{bmatrix}
1 & 2 & 2 & 4 \\
0 & 2 & 0 & 4
\end{bmatrix} \ \Rightarrow \ R =
\begin{bmatrix}
1 & 0 & 2 & 0 \\
0 & 1 & 0 & 2
\end{bmatrix}
$$

+ RREF 형태에서는 단위행렬 $I$의 형태가 나온다.
+ $Rx=0$의 형태를 만들어 놓으면 special solution을 찾는 것이 훨씬 쉬워진다.
+ $R$의 각 칼럼에 $x_1, x_2, x_3, x_4$를 곱하고 각 행의 합이 0이 나오도록 만든다.
+ $x_1 + 2x_3 = 0, \ x_2 + 2x_4 =0$
+ $N(R)$를 구성하는 $ \ s_1 =
\begin{bmatrix}
-2 \\
0 \\
1 \\
0
\end{bmatrix}
$과 $ \ s_2 =
\begin{bmatrix}
0 \\
-2 \\
0 \\
1
\end{bmatrix}
$를 구할 수 있다.

### N(A) = Z의 아주 중요한 의미

+ 행렬 $A$의 모든 칼럼들이 independent하다는 것을 뜻한다.
+ independent에 대한 아이디어는 추후 논의한다.

### Example :: Ax=0에 대한 Complete solution을 구하는 방법

$(1) \ A =
\begin{bmatrix}
1 & 2 & 2 & 3 \\
2 & 2 & 8 & 10 \\
3 & 3 & 10 & 13
\end{bmatrix}$

+ 1번째 pivot은 1번째 칼럼의 $a_{11}$이다.
+ pivot 아래에 있는 값들을 모두 0으로 소거해준다.

$(2) \ A =
\begin{bmatrix}
1 & 2 & 2 & 3 \\
0 & 0 & 4 & 4 \\
0 & 0 & 4 & 4
\end{bmatrix}$

+ 2번째 pivot은 3번째 칼럼의 $a_{23}$이다.
+ pivot 아래에 있는 값을 0으로 소거해준다.

$(3) \ U =
\begin{bmatrix}
1 & 2 & 2 & 3 \\
0 & 0 & 4 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix}$

+ pivot 칼럼은 1번째와 3번째이다.
+ 칼럼은 4개인데 pivot 칼럼은 2개이므로 solution은 여러 개이다.
+ free 칼럼인 2번째와 4번째에 곱해질 free variable에 0과 1을 대입해서 special solution을 만들 수 있다.
+ $x_2, x_4$에 $(1,0)$을 대입하면 $x_3=0, x_1=-1$이 나온다. $s_1 = (-1,1,0,0)$
+ $x_2, x_4$에 $(0,1)$을 대입하면 $x_3=-1, x_1=-1$이 나온다. $s_2 = (-1,0,-1,1)$
+ free 칼럼인 $x_2, x_4$에는 어떤 값을 넣어도 상관 없으므로 다음과 같다.
+ $\therefore x = x_2 \begin{bmatrix}
-1 \\
1 \\
0 \\
0
\end{bmatrix} + x_4 \begin{bmatrix}
-1 \\
0 \\
-1 \\
1
\end{bmatrix} = \begin{bmatrix}
-x_2-x_4 \\
x_2 \\
-x_4\\
x_4
\end{bmatrix}$

### Reduced Row Echelon Matrix

$(1) \ U =
\begin{bmatrix}
1 & 1 & 2 & 3 \\
0 & 0 & 4 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix} \Rightarrow E = \begin{bmatrix}
1 & 1 & 0 & 1 \\
0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0
\end{bmatrix}
$

+ 행렬 $U$는 pviot 아래에만 0을 가지면 된다.
+ 행렬 $E$는 **pivot 위에도 0을 가져야 한다**.
+ 행렬 $E$의 pivot 칼럼($(1,0,0), \ (0,1,0)$)을 붙여 놓으면 단위행렬 $I$가 된다.

### Example :: 널스페이스 묘사하기 :: R vs E

$(1) \ U =
\begin{bmatrix}
1 & 5 & 7\\
0 & 0 & 9
\end{bmatrix}
$

+ 2번째 칼럼이 free 칼럼이므로 $x_2$가 free variable이다.
+ $x_2$에 1을 대입해본다.
+ $s_1 = (-5, 1, 0)$이 나온다.
+ $N(A)$는 $R^{3}$의 line이 된다.

$(2) \ U =
\begin{bmatrix}
1 & 5 & 7\\
0 & 0 & 9
\end{bmatrix} \Rightarrow \begin{bmatrix}
1 & 5 & 7\\
0 & 0 & 7
\end{bmatrix} \Rightarrow \begin{bmatrix}
1 & 5 & 0\\
0 & 0 & 7
\end{bmatrix} \Rightarrow R = \begin{bmatrix}
1 & 5 & 0\\
0 & 0 & 1
\end{bmatrix} = rref(U)
$

+ 2번째 칼럼에서 pivot을 발견할 수 없으니 3번째 칼럼으로 간다.
+ 3번째 칼럼의 pivot 위치의 값 9를 1로 만든다.
+ $x_2$에 1을 대입해본다.
+ 더 쉽게 $s_1 = (-5, 1, 0)$이 나온다.
+ $N(A)$는 $R^{3}$의 line이 된다.

### Ax=0 (m<n)에 대한 통찰

+ 와이드 스크린처럼 가로가 세로보다 훨씬 긴 직사각형 행렬 $A$를 상상해본다.
+ pivot의 개수는 행의 개수나 열의 개수를 초과할 수 없다. (대각선이므로)
+ pivot은 최대 $m$개이고 free variable은 $n-m$개이므로 special solution이 최소 1개 이상 존재한다.
+ 따라서 $x=0$이 아닌 해가 반드시 존재한다.

### invertible matrix와 free variables

+ 역행렬이 존재한다면 $Ax=0$의 유일한 해는 $x=0$이다.
+ $x=0$이면 $N(A)=Z$이므로 free variables가 없다는 뜻이다.

**끝.**

---

## 09 Ax=b와 공간, 칼럼 스페이스

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

+ 벡터 공간에 속하는 임의의 벡터들로 만들어내는 공간을 부분 공간(subspace)이라고 한다.
+ 즉, 벡터들의 linear combination이 부분 공간(subspace)을 만들어낸다.
+ 다르게 말하면 임의의 벡터들이 $span$한 것을 subspace라고 한다.
+ subspace에 속하는 벡터들을 linear combination한 결과 또한 당연히 subspace에 속한다.

### Subspace 구분법과 OX 퀴즈

#### 구분법

+ subspace에 속하는 벡터들을 linear combination한 결과가 subspace에 속하지 않으면 그것은 subspace가 아니다.

#### OX 퀴즈

+ A plane in $R^{3}$ that misses the origin : (x)
  + plane에 속하는 $v$에 0을 곱한 결과가 plane에 속하지 않기 때문이다.
+ The quarter-plane : (x)
  + (2, 3)에 -1을 곱한 결과가 1사분면에 속하지 않기 때문이다.

### 칼럼 스페이스 Column Space

+ $Ax=b$에서 $A^{-1}$이 존재하지 않을 때, 해가 있는지 없는지 어떻게 알 수 있을까.
+ 공간의 관점으로 접근하면 된다.
+ $Ax$는 하나의 벡터 공간인데 행렬 $A$의 칼럼들이 $span$하여 만드는 공간이므로 칼럼 스페이스 $C(A)$라고 부른다.
+ $C(A)$에 $b$가 속하면 해가 있는 것이고, 속하지 않으면 해가 없는 것이다.

> **Note:** $C(A)$에는 행렬 $A$의 칼럼뿐만 아니라 linear combination의 결과인 $Ax$까지 포함하고 있다.

### 칼럼 스페이스의 subspace

+ 행렬 $A$가 m by n 행렬일 때, 행렬 $A$의 칼럼들은 $m$차원 벡터이다.
+ $m$차원 벡터칼럼은 $R^{m}$에 속한다.
+ 따라서 $C(A)$는 $R^{m}$의 subspace이다.

### Ax=b를 만족시키는 b 만들기

+ $b_k$가 행렬 $A$의 $k$번째 칼럼 $a_k$의 linear combination이 되도록 한다.
+ not yet

### C(A)가 full vector space가 되느냐 subspace가 되느냐

+ 행렬 $A$의 $m$차원 칼럼벡터가 $m$차원을 가득 채우면 full vector space ($R^{m}$)가 되고 그렇지 못하면 $R^{m}$의 subspace가 된다.

### Example :: 칼럼 스페이스 묘사하기

$(1) \ I =
\begin{bmatrix}
1 & 0\\
0 & 1
\end{bmatrix}
$

+ 행렬 $I$의 칼럼벡터는 2차원이다.
+ 행렬 $I$의 칼럼벡터는 2개가 independent하다.
+ 행렬 $I$의 칼럼벡터로 모든 2차원 공간을 만들 수 있다.
+ $C(I) \rightarrow R^{2}$

$(2) \ A =
\begin{bmatrix}
1 & 2\\
2 & 4
\end{bmatrix}
$

+ 행렬 $A$의 칼럼벡터는 2차원이다.
+ 행렬 $A$의 칼럼벡터들은 서로 dependent하다.
+ 2차원에서 칼럼벡터 1개는 line을 만들어낸다.
+ $C(A) \subset R^{2}$

$(3) \ B =
\begin{bmatrix}
1 & 2 & 0 \\
0 & 0 & 4
\end{bmatrix}
$

+ 행렬 $B$의 칼럼벡터는 2차원이다.
+ 행렬 $B$의 칼럼벡터는 2개가 서로 dependent하다.
+ 2차원에서 칼럼벡터 2개는 모든 2차원 공간을 만든다.
+ $C(B) \rightarrow R^{2}$

### Problem :: C(A)를 고려하여 Ax=b를 만족시키는 적절한 b 만들기

$20.(a) \ \begin{bmatrix}
1 & 4 & 2 \\
2 & 8 & 4 \\
-1 & -4 & -2
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
x_3
\end{bmatrix}
=
\begin{bmatrix}
b_1 \\
b_2 \\
b_3
\end{bmatrix}
$

+ $C(A)$는 3차원 공간의 line이다.
+ $b$는 반드시 $C(A)$에 속해야 하므로 $[1 \ 2 \ {-}1]$과 같은 선상에 있으면 된다.
+ $\therefore b = [b_1 \ 2b_1 \ {-}b_1]$

$20.(b) \ \begin{bmatrix}
1 & 4 \\
2 & 9 \\
-1 & -4
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2
\end{bmatrix}
=
\begin{bmatrix}
b_1 \\
b_2 \\
b_3
\end{bmatrix}
$

+ $C(A)$는 3차원 공간에서 2차원 plane이다.
+ 행렬 $A$의 칼럼벡터를 $[a_1 \ a_2 \ a_3]$라고 할 때, $a_1$과 $a_3$의 비율은 고정되고 $a_2$만 움직인다.
+ $b$는 반드시 $C(A)$에 속해야 하므로 $b_1$과 $b_3$의 비율만 고정시키면 된다.
+ $\therefore b_3 = -b_1$

**끝.**

---

## 08 Ax=b를 푸는 방법 (3) 칼럼 스페이스

### 1) 가우스 소거법

+ $Ax=b \Rightarrow Ux=b'$
+ 행렬 $A$를 $U$형태로 바꾼 후 back substituion을 적용하여 $x$를 하나씩 구한다.

### 2) 가우스-조던 소거법

+ '**역행렬을 구하는 방법**'이다.
+ $AA^{-1}=I \Rightarrow A[x \ y \ z] = [e_1 \ e_2 \ e_3] \Rightarrow U[x \ y\ z] = [e_1' \ e_2' \ e_3'] \Rightarrow I[x \ y \ z] = [e_1'' \ e_2'' \ e_3'']$
+ 역행렬을 구했으니 $Ax=b$의 양변에 역행렬을 곱하면 $x$를 한꺼번에 구할 수 있다.
+ $Ax=b \Rightarrow A^{-1}Ax=A^{-1}b \Rightarrow x = A^{-1}b$

### 3) 칼럼 스페이스

+ '**해가 존재하는지 존재하지 않는지 판별할 수 있는 방법**'이다.
+ $Ax=b$에서 $A^{-1}$이 존재하지 않을 때, 해가 있는지 없는지 어떻게 알 수 있을까.
+ 공간의 관점으로 접근하면 된다.
+ $Ax$는 하나의 벡터 공간인데 행렬 $A$의 칼럼들이 $span$하여 만드는 공간이므로 칼럼 스페이스 $C(A)$라고 부른다.
+ $C(A)$에 $b$가 속하면 해가 있는 것이고, 속하지 않으면 해가 없는 것이다.

**끝.**

---

## 07 A = LU Factorization

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

### A = LU (LU Factorization)

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

+ $E_{21}$은 L(Lower triangular)이다.

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

## 06 가우스-조던 소거법으로 역행렬 구하기 Inverse Matrix Using Gauss-Jordan Elimination

### 역행렬을 어떻게 구할까 Inverse Matrix

+ $Ax=b$에서 $x$를 구하는 방법은 행렬 $A$의 역행렬인 $A^{-1}$을 각 항의 왼쪽에 곱하는 것이다.
+ 행렬 $A$의 역행렬을 구하는 방법은 가우스-조던 소거법을 적용하는 것이다.
+ 가우스 소거법은 $Ax=b$를 $Ux=b'$의 형태로 만들지만
+ 가우스-조던 소거법은 $Ax=b$를 $Ix=b''$의 형태로 만든다.
+ 여기서 $b''$은 $A^{-1}b$를 뜻한다.


### 가우스-조던 소거법 Gauss-Jordan Elimination

```
1. AA^{-1} = I                          # 역행렬의 성질 활용
2. A^{-1} = [x y z]                     # 역행렬을 칼럼 벡터로 변환
3. A[x y z] = I                         # Ax=b 형태로 전환
4. [Ax Ay Az] = [e1 e2 e3]              # 단위행렬을 칼럼 벡터로 변환
5. Ax = e1, Ay = e2, Az = e3            # Ax=b 형태로 전환
6. [A | e1], [A | e2], [A | e3]         # 첨가행렬 형태로 전환
7. [A | e1 e2 e3]                       # 첨가행렬 형태로 전환
8. [U | e1' e2' e3']                    # 가우스 소거법 적용
9. [I | e1'' e2'' e3'']                 # 가우스-조던 소거법 적용
10. I[x y z] = [e1'' e2'' e3'']         # 첨가행렬 형태를 원래 상태로 복귀
11. A^{-1} = [x y z] = [e1'' e2'' e3'']
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

## 05 Ax=b를 푸는 방법 (2) 가우스-조던 소거법

### 1) 가우스 소거법

+ $Ax=b \Rightarrow Ux=b'$
+ 행렬 $A$를 $U$형태로 바꾼 후 back substituion을 적용하여 $x$를 하나씩 구한다.

### 2) 가우스-조던 소거법

+ 역행렬을 구하는 방법이다.
+ $AA^{-1}=I \Rightarrow A[x \ y \ z] = [e_1 \ e_2 \ e_3] \Rightarrow U[x \ y\ z] = [e_1' \ e_2' \ e_3'] \Rightarrow I[x \ y \ z] = [e_1'' \ e_2'' \ e_3'']$
+ 역행렬을 구했으니 $Ax=b$의 양변에 역행렬을 곱하면 $x$를 한꺼번에 구할 수 있다.
+ $Ax=b \Rightarrow A^{-1}Ax=A^{-1}b \Rightarrow x = A^{-1}b$

**끝.**

---

## 04 첨가 행렬 Augmented Matrix Form

### 첨가 행렬 Augmented Matrix Form

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

+ 2번째 행과 3번째 행을 바꿔서 $Ux=b'$ 형태로 만들어준다.

**끝.**

---

## 03 가우스 소거법 Gaussian Elimination

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

+ Gauss Elimination으로 행렬 $A$를 $U$(upper triangular)로 만들어준다.

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

**끝.**

---

## 02 Ax=b를 푸는 방법 (1) 가우스 소거법

### 1) 가우스 소거법

+ $Ax=b \Rightarrow Ux=b'$
+ 행렬 $A$를 $U$형태로 바꾼 후 back substituion을 적용하여 $x$를 하나씩 구한다.

**끝.**

---

## 01 선형 방정식 Linear Equations

### 선형 방정식을 어떻게 풀까 Solving Linear Equations

+ $Ax=b$를 선형 방정식이라고 한다.
+ $Ax=b$를 만족시키는 $x$를 찾는 것이 선형 방정식을 푸는 것이다.

**끝.**

---
