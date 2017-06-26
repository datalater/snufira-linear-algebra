ⓒ JMC 2017

**COURSE**  
\- 서울대학교 4차산업혁명 아카데미  
\- 인공지능 에이전트 과정  
\- 기계학습 기초수학, 김종권 교수님

**SOURCE**  
\- Introduction to Linear Algebra, Strang  
\- [MIT 선형대수학 Strang 교수 강의 ](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8 )  
\- [KOCW 건국대 이향원 교수 강의](http://www.kocw.net/home/search/kemView.do?kemId=1039395 )  
\- 김종권 교수님 수업 자료

**RESUME**  
\- `3.1 12:20~`

---

## One-Sentence Summary

### 0. 선형방정식 Linear Equations

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>에서 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 구해야 한다.

### 1. 가우스 소거법 Gaussian Elimination

+ 가우스 소거법은 선형방정식을 풀기 위해 사용한다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>의 형태를 <img src="http://api.gmath.guru/cgi-bin/gmath?Ux%3Db%27"/>의 형태로 바꿔주는 것이 가우스 소거법이다.

### 2. 첨가 행렬 Augmented Matrix

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20%5BA%20%5C%20%7C%20%5C%20b%5D%20%5CRightarrow%20%5BU%20%5C%20%7C%20%5C%20b%27%5D%20%5CRightarrow%20Ux%20%3D%20b%27%27"/>
+ 가우스 소거법을 진행할 때 첨가행렬을 사용하면 편안하게 연산할 수 있다.

### 3. 가우스-조던 소거법으로 역행렬 구하기 Inverse Matrix Using Gauss-Jordan Elimination

1. <img src="http://api.gmath.guru/cgi-bin/gmath?AA%5E%7B-1%7D%20%3D%20I"/> ......................................... <img src="http://api.gmath.guru/cgi-bin/gmath?A%5E%7B-1%7D%20%3D%20%5Bx%20%5C%20y%20%5C%20z%5D"/>.
2. <img src="http://api.gmath.guru/cgi-bin/gmath?A%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20I"/> .................................... <img src="http://api.gmath.guru/cgi-bin/gmath?I%20%3D%20%5Be_1%20%5C%20e_2%20%5C%20e_3%5D"/>
3. <img src="http://api.gmath.guru/cgi-bin/gmath?%5BAx%20%5C%20Ay%20%5C%20Az%5D%20%3D%20%5Be_1%20%5C%20e_2%20%5C%20e_3%5D"/>
4. <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%20%3D%20e_1%2C%20%5C%20Ay%20%3D%20e_2%2C%20%5C%20Az%20%3D%20e_3"/> ........ <img src="http://api.gmath.guru/cgi-bin/gmath?%5BA%20%5C%20%7C%20%5C%20e_1%5D%2C%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_2%5D%2C%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_3%5D"/>
5. <img src="http://api.gmath.guru/cgi-bin/gmath?%5BA%20%5C%20%7C%20%5C%20e_1%20%5C%20e_2%20%5C%20e_3%5D"/> .....................................행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 가우스 소거법으로 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>로 만든다.
6. <img src="http://api.gmath.guru/cgi-bin/gmath?%5BU%20%5C%20%7C%20%5C%20e_1%27%20%5C%20e_2%27%20%5C%20e_3%27%5D"/> .................................... 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>를 가우스-조던 소거법으로 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>로 만든다.
7. <img src="http://api.gmath.guru/cgi-bin/gmath?%5BI%20%5C%20%7C%20%5C%20e_1%27%27%20%5C%20e_2%27%27%20%5C%20e_3%27%27%5D"/>
8. <img src="http://api.gmath.guru/cgi-bin/gmath?I%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%27%27%20%5C%20e_2%27%27%20%5C%20e_3%27%27%5D%20"/>
9. <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ctherefore%20A%5E%7B-1%7D%20%3D%20%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%27%27%20%5C%20e_2%27%27%20%5C%20e_3%27%27%5D"/>

### 4. A = LU Factorization

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20Ux%3Db%27%27"/>으로 바꿔주기 위해 <img src="http://api.gmath.guru/cgi-bin/gmath?E"/>(Elimination)를 곱해준다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?E_%7B3%7DE_%7B2%7DE_%7B1%7DA%20%3D%20U%20%5CRightarrow%20A%20%3D%20E_%7B1%7D%5E%7B-1%7DE_%7B2%7D%5E%7B-1%7DE_%7B3%7D%5E%7B-1%7DU%20%5CRightarrow%20A%20%3D%20LU%20"/>
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>는 <img src="http://api.gmath.guru/cgi-bin/gmath?LU"/>로 분해된다.




---

## 02 Solving Linear Equations (4) 부분공간

### 부분공간과 벡터공간 Subspaces and Vector spaces

`RESUME : 3.1 12:20~`




---

## 02 Solving Linear Equations (3) 가우스 소거법을 행렬 간 곱셈으로 치환하는 방법

### 가우스 소거법을 행렬 간 곱셈으로 치환하기 Elimination as Matrix Mutliplication

```
1. pivot과 multiplier의 연산을 행렬 간 곱셈으로 나타낸다.
```

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%281%29%20%5C%20%5Cbegin%7Barray%7D%7Blcr%7D%202x_%7B1%7D+3x_%7B2%7D%20%26%20%3D%20%26%205%20%5C%5C%206x_%7B1%7D+12x_%7B2%7D%20%26%20%3D%20%26%2010%20%5Cend%7Barray%7D"/></p>
<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%282%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D6%20%26%2012%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_%7B1%7D%20%5C%5C%0Dx_%7B2%7D%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D5%20%5C%5C%0D10%0D%5Cend%7Bbmatrix%7D"/></p>
<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%283%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D0%20%26%203%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_%7B1%7D%20%5C%5C%0Dx_%7B2%7D%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D5%20%5C%5C%0D-5%0D%5Cend%7Bbmatrix%7D"/></p>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?%282%29%20Ax%20%3D%20b"/>에서 <img src="http://api.gmath.guru/cgi-bin/gmath?%283%29%20Ux%20%3D%20b%27"/>을 만드는 과정을 행렬 간 곱셈으로 나타낼 수 있다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%282%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D6%20%26%2012%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_%7B1%7D%20%5C%5C%0Dx_%7B2%7D%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D5%20%5C%5C%0D10%0D%5Cend%7Bbmatrix%7D"/></p>


<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%284%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%20%5C%5C%0D-3%20%26%201%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D6%20%26%2012%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D0%20%26%203%0D%5Cend%7Bbmatrix%7D"/></p>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?%284%29"/>는 다음과 같은 형태로 나타낼 수 있다. <img src="http://api.gmath.guru/cgi-bin/gmath?%5C%20E_%7B21%7DA%20%3D%20U"/>

### A = LU, LU Factorization

```
1. 삼각행렬의 대각선이 모두 0이 아니면 역행렬이 존재한다.

<이유>
- 삼각행렬에 속하는 Elimination 행렬은 곱해진 행렬에 대해 특정 효과를 발휘한다.
- 이 효과를 없애주는 것은 항상 존재하며 그것이 바로 역행렬이 된다.
- 따라서 삼각행렬은 대각선이 모두 0이 아니면 항상 역행렬이 존재한다.
```

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%284%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%20%5C%5C%0D-3%20%26%201%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D6%20%26%2012%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D0%20%26%203%0D%5Cend%7Bbmatrix%7D"/></p>

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%285%29%20%5C%20E_%7B21%7DA%20%3D%20U"/></p>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?E_%7B21%7D"/>은 삼각행렬인데 대각선의 값이 모두 0이 아니므로 역행렬이 반드시 존재한다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%286%29%20%5C%20A%20%3D%20E_%7B21%7D%5E%7B-1%7DU"/></p>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?E_%7B21%7D"/>의 역행렬은 <img src="http://api.gmath.guru/cgi-bin/gmath?E_%7B21%7D"/>의 효과를 없애주는 것이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?E_%7B21%7D"/>의 효과는 <img src="http://api.gmath.guru/cgi-bin/gmath?%28row_2%29%27%20%3D%20%28row_2%29%20-%203*%28row_1%29"/>이다.
+ 효과를 없애주려면 <img src="http://api.gmath.guru/cgi-bin/gmath?%28row_2%29%27%27%27%20%3D%20%28row_2%29%27%20+%203*%28row_1%29"/>를 해줘야 한다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%287%29%20%5C%20A%20%3D%20E_%7B21%7D%5E%7B-1%7DU%20%3D%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%20%5C%5C%0D3%20%26%201%0D%5Cend%7Bbmatrix%7DU%0D"/></p>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?E_%7B21%7D"/>은 L(Lower TriangLUar)이다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%288%29%20%5C%20A%20%3D%20LU"/></p>

+ 이러한 과정을 보고, 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 <img src="http://api.gmath.guru/cgi-bin/gmath?L"/> 곱하기 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>로 `factorization`(분해)를 했다고 말한다.

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

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%281%29%20%5C%20AA%5E%7B-1%7D%3DI"/></p>

+ 어떤 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 역행렬을 곱하면 단위행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>가 나온다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%282%29%20%5C%20A%3DR%5E%7B3*3%7D%2C%20%5C%20A%5E%7B-1%7D%20%3D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%26%20y_1%20%26%20z_1%20%5C%5C%0Dx_2%20%26%20y_2%20%26%20z_2%20%5C%5C%0Dx_3%20%26%20y_3%20%26%20z_3%0D%5Cend%7Bbmatrix%7D%0D%3D%20%5Bx%20%5C%20y%20%5C%20z%5D"/></p>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?x%2C%20y%2C%20z"/>를 구하는 것이 곧 <img src="http://api.gmath.guru/cgi-bin/gmath?A%5E%7B-1%7D"/>을 구하는 것이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?%282%29"/>를 <img src="http://api.gmath.guru/cgi-bin/gmath?%281%29"/>에 적용시키면 다음과 같다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%283%29%20%5C%20AA%5E%7B-1%7D%20%3D%20A%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%20%26%200%20%5C%5C%0D0%20%26%201%20%26%200%20%5C%5C%0D0%20%26%200%20%26%201%0D%5Cend%7Bbmatrix%7D"/></p>

+ 단위행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>의 각 칼럼을 <img src="http://api.gmath.guru/cgi-bin/gmath?e_%7B1%7D%2C%20e_%7B2%7D%2C%20e_%7B3%7D"/>이라고 해보자.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%284%29%20%5C%20%5BAx%20%5C%20Ay%20%5C%20Az%5D%20%3D%20%5Be_%7B1%7D%20%5C%20e_%7B2%7D%20%5C%20e_%7B3%7D%5D%20"/></p>
<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%285%29%20%5C%20Ax%3De_%7B1%7D%2C%20%5C%20Ay%3De_%7B2%7D%2C%20%5C%20Az%3De_%7B3%7D"/></p>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?%285%29"/> 같은 경우 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>의 형태이므로 가우스 소거법을 활용할 수 있다.
+ 그런데 <img src="http://api.gmath.guru/cgi-bin/gmath?%285%29"/>에 있는 3가지 식 모두 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>에 대한 가우스 소거법이므로 똑같이 진행하게 된다.
+ 가우스 소거법의 결과를 결정짓는 것은 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>이므로 한꺼번에 첨가행렬(augmented matrix form)을 활용할 수 있다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%286%29%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_%7B1%7D%5D%2C%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_%7B2%7D%5D%2C%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_%7B3%7D%5D%20"/></p>
<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%287%29%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_%7B1%7D%20%5C%20e_%7B2%7D%20%5C%20e_%7B3%7D%5D"/></p>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?%287%29"/> 식에 가우스 소거법을 적용하면, <img src="http://api.gmath.guru/cgi-bin/gmath?x%2C%20y%2C%20z"/>를 구할 수 있다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%288%29%20%5C%20%5Bu%20%5C%20%7C%20%5C%20e_%7B1%7D%27%20%5C%20e_%7B2%7D%27%20%5C%20e_%7B3%7D%27%5D%20"/></p>

+ 가우스 소거법에서는 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>로 만들었다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%289%29%20%5C%20%5BI%20%5C%20%7C%20%5C%20e_%7B1%7D%27%27%20%5C%20e_%7B2%7D%27%27%20%5C%20e_%7B3%7D%27%27%5D"/></p>
<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%2810%29%20%5C%20I%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_%7B1%7D%27%27%20%5C%20e_%7B2%7D%27%27%20%5C%20e_%7B3%7D%27%27%5D"/></p>

+ 그러나 가우스-조던 소거법에서는 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 단위행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>로 만들어준다.

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

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%5Cbegin%7Barray%7D%7Blcl%7D%20x_%7B1%7D+2x_%7B2%7D%20%26%20%3D%20%26%205%20%5C%5C%202x_%7B1%7D+5x_%7B2%7D%20%26%20%3D%20%26%2012%20%5Cend%7Barray%7D"/></p>

+ 방정식을 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>로 표현한다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%5Cbegin%7Bbmatrix%7D%201%20%26%202%20%5C%5C%202%20%26%205%20%5Cend%7Bbmatrix%7D%20%5Cbegin%7Bbmatrix%7D%20x%20%5C%5C%20y%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%201%20%5C%5C%202%20%5Cend%7Bbmatrix%7D"/></p>

+ Gauss Elimination으로 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>(upper triangLUar)로 만들어준다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%5Cbegin%7Bbmatrix%7D%201%20%26%202%20%5C%5C%200%20%26%201%20%5Cend%7Bbmatrix%7D%20%20%5Cbegin%7Bbmatrix%7D%20x%20%5C%5C%20y%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%205%20%5C%5C%202%20%5Cend%7Bbmatrix%7D"/></p>

+ 다시 방정식으로 나타낸다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%5Cbegin%7Barray%7D%7Brcl%7D%20x_%7B1%7D+2x_%7B2%7D%20%26%20%3D%20%26%205%20%5C%5C%20x_%7B2%7D%20%26%20%3D%20%26%2012%20%5Cend%7Barray%7D"/></p>

+ back substitution을 통해 아래에서부터 미지수의 값을 차례대로 대입하면 쉽게 해를 구할 수 있다.

### 피봇과 멀티플라이어 Pivot and Multiplier

```
Pivot : 소거되지 않는 row의 첫 번째 값
Multiplier : 소거될 row의 첫 번째 값을 Pivot으로 나눈 값
```

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%5Cbegin%7Bbmatrix%7D%201%20%26%202%20%5C%5C%202%20%26%205%20%5Cend%7Bbmatrix%7D%20%5Cbegin%7Bbmatrix%7D%20x%20%5C%5C%20y%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%201%20%5C%5C%202%20%5Cend%7Bbmatrix%7D"/></p>

+ Pivot = 1
+ Multiplier = 2

### 첨가행렬 Augmented Matrix Form

```
Ax = b => [A | b] => [u | b'] => Ux = b'

행렬 A에 칼럼벡터 b를 붙여서 하나의 행렬로 나타낸 것을 첨가행렬이라 한다.

가우스 소거법을 적용하면 A의 row와 b의 row가 같은 연산을 적용 받는다.
어차피 같은 연산을 적용 받으니 행렬 A에 b를 추가하여 첨가행렬로 만들 수 있다.
```

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%203%20%5C%5C%0D2%20%26%202%20%26%204%20%5C%5C%0D3%20%26%207%20%26%209%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_%7B1%7D%20%5C%5C%0Dx_%7B2%7D%20%5C%5C%0Dx_%7B3%7D%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D5%20%5C%5C%0D7%20%5C%5C%0D10%0D%5Cend%7Bbmatrix%7D"/></p>

+ 위 행렬의 형태를 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>라고 할 때
+ 가우스 소거에서 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>는 아무런 관여를 하지 않는다.
+ 가우스 소거의 결과를 결정하는 것은 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>이다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%203%20%26%20%7C%20%26%205%20%5C%5C%0D2%20%26%202%20%26%204%20%26%20%7C%20%26%207%20%5C%5C%0D3%20%26%207%20%26%209%20%26%20%7C%20%26%2010%0D%5Cend%7Bbmatrix%7D%0D"/></p>

+ 따라서 가우스 소거에서 필요 없는 것을 제외하면 하나의 행렬로 나타낼 수 있다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%201%20%26%20%7C%20%26%205%20%5C%5C%0D0%20%26%200%20%26%202%20%26%20%7C%20%26%20-3%20%5C%5C%0D0%20%26%204%20%26%206%20%26%20%7C%20%26%20-5%0D%5Cend%7Bbmatrix%7D%0D"/></p>

+ 가우스 소거를 통해 위와 같은 형태가 만들어진다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%201%20%26%20%7C%20%26%205%20%5C%5C%0D0%20%26%204%20%26%206%20%26%20%7C%20%26%20-5%20%5C%5C%0D0%20%26%200%20%26%202%20%26%20%7C%20%26%20-3%0D%5Cend%7Bbmatrix%7D%0D"/></p>

+ 2번째 행과 3번째 행을 바꿔서 <img src="http://api.gmath.guru/cgi-bin/gmath?Ux%3Db"/> 형태로 만들어준다.

**끝.**

---