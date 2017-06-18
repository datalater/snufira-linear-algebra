ⓒ JMC 2017

**COURSE**  
\- 서울대학교 4차산업혁명 아카데미  
\- 인공지능 에이전트 과정  
\- 기계학습 기초수학, 김종권 교수님

**SOURCE**  
\- Introduction to Linear Algebra, Strang  
\- [MIT 선형대수학 Strang 교수 강의 OCW](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8)  
\- [KOCW 건국대 이향원 교수 강의](http://www.kocw.net/home/search/kemView.do?kemId=1039395)  
\- 김종권 교수님 수업 자료

---

## 02 Solving Linear Equations

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

+ Gauss Elimination으로 행렬 A를 U(upper triangluar)로 만들어준다.

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
Ax = b => [A | b] => [u | b]

행렬 A에 칼럼 벡터 b를 붙여서 하나의 행렬로 나타낸 것을 첨가행렬이라 한다.
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
+ 가우스 소거에서 x는 아무런 관여를 하지 않는다.
+ 가우스 소거의 결과를 결정하는 것은 행렬 A이다.

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

---
