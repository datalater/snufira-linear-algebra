ⓒ JMC 2017

**COURSE**  
\- 서울대학교 4차산업혁명 아카데미  
\- 인공지능 에이전트 과정  
\- 기계학습 기초수학, 김종권 교수님

**SOURCE**  
\- Introduction to Linear Algebra, Strang  
\- [MIT 선형대수학 Strang 교수 강의 OCW](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8)  
\- 김종권 교수님 수업 자료

---

## Ch.1 Introduction to Vectors

### Linear Combination이란 무엇인가

+ combining **vector addition** with **scalar multiplication**
+ 벡터 더하기와 스칼라 곱하기를 결합한 것
+ `cv + dw`

###

---

## Introduction

### Linear Algebra의 목적

+ Linear equation 형태를 가진 문제를 푸는 것

> **Note:** Linear equation : 선형방정식, 일차방정식

### Linear Equation을 표현하는 방법

$\begin{array}{lcl} 2x+5y & = & 1 \\ x+3y & = & 2 \end{array}$

+ `Ax= b`
    + A : 연립방정식의 계수(coefficient)를 행렬로 표현한 것
    + x : 연립방정식의 미지수(unknowns)를 벡터로 표현한 것
    + b : 연립방정식의 상수를 벡터로 표현한 것

### Picture of Linear Equation ::: (1) Row picture

$\begin{bmatrix} 2 & 5 \\ 1 & 3 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$

+ row에 있는 방정식을 바라본다.
+ 방정식을 하나씩 그래프에 나타낸다.

> **Note:** row 관점으로 바라보기 때문에 첫번째 방정식부터 다음 방정식까지 차례대로 그래프에 나타낸다.

### Picture of Linear Equation ::: (2) Column picture

$x\begin{bmatrix} 2 \\ 1 \end{bmatrix} + y\begin{bmatrix} 5 \\ 3 \end{bmatrix} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$

+ column에 있는 unknown에 곱해진 계수를 바라본다.
+ 계수를 벡터로 나타낸다.
+ unknown이 곱해진 벡터의 합이 특정 벡터 값이 나오도록 요구한다.
+ 적절한 linear combination of columns를 찾도록 요구한다.
+ column vector를 하나씩 그래프에 나타낸다.

> **Note:** linear combination : 특정 벡터 값을 도출하기 위해 벡터 더하기와 스칼라 곱하기를 결합하는 것

### Row computation vs. Column computation

+ `Ax = b`

$\begin{bmatrix} 2 & 5 \\ 1 & 3 \end{bmatrix} \begin{bmatrix} 1 \\ 2 \end{bmatrix} =  1\begin{bmatrix} 2 \\ 1 \end{bmatrix} + 2\begin{bmatrix} 5 \\ 3 \end{bmatrix} = \begin{bmatrix} 12 \\ 7 \end{bmatrix}$

+ Ax is a combination of the columns of A.
+ (matrix-vector multiplication) Ax는 A의 칼럼의 linear combination이다.

---
