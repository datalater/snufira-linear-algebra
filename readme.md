ⓒ JMC 2017

**COURSE**  
\- 서울대학교 4차산업혁명 아카데미  
\- 인공지능 에이전트 과정  
\- 기계학습 기초수학, 김종권 교수님

**SOURCE**  
\- Introduction to Linear Algebra, Strang (The most desired way to learn)  
\- [MIT 선형대수학 Strang 교수 강의 ](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8 )  
\- [KOCW 건국대 이향원 교수 강의](http://www.kocw.net/home/search/kemView.do?kemId=1039395 )  
\- 김종권 교수님 수업 자료

**RESUME**  
\- KOCW : `3.2 00:00~`  
\- TEXTBOOK : `p.125`

---

## One-Sentence Summary

### 01 선형방정식 Linear Equations

+ <img src="https://latex.codecogs.com/gif.latex?Ax%3Db"/>에서 <img src="https://latex.codecogs.com/gif.latex?x"/>를 구해야 한다.
+ <img src="https://latex.codecogs.com/gif.latex?Ax"/>란 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 모든 칼럼들의 linear combination을 뜻한다.

### 02~03 Ax=b를 푸는 방법 (1) 가우스 소거법

+ <img src="https://latex.codecogs.com/gif.latex?Ax%3Db%20%5CRightarrow%20Ux%3Db%27"/>
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>를 <img src="https://latex.codecogs.com/gif.latex?U"/>형태로 바꾼 후 back substitution을 적용하여 <img src="https://latex.codecogs.com/gif.latex?x"/>를 하나씩 구한다.

### 04 첨가 행렬 Augmented Matrix

+ <img src="https://latex.codecogs.com/gif.latex?Ax%3Db%20%5CRightarrow%20%5BA%20%5C%20%7C%20%5C%20b%5D%20%5CRightarrow%20%5BU%20%5C%20%7C%20%5C%20b%27%5D%20%5CRightarrow%20Ux%20%3D%20b%27"/>
+ 가우스 소거법을 진행할 때 첨가행렬을 사용하면 간편하게 연산할 수 있다.

### 05 Ax=b를 푸는 방법 (2) 가우스-조던 소거법

+ 역행렬을 구하는 방법이다.
+ <img src="https://latex.codecogs.com/gif.latex?AA%5E%7B-1%7D%3DI%20%5CRightarrow%20A%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%20%5C%20e_2%20%5C%20e_3%5D%20%5CRightarrow%20U%5Bx%20%5C%20y%5C%20z%5D%20%3D%20%5Be_1%27%20%5C%20e_2%27%20%5C%20e_3%27%5D%20%5CRightarrow%20I%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%27%27%20%5C%20e_2%27%27%20%5C%20e_3%27%27%5D"/>
+ 역행렬을 구했으니 <img src="https://latex.codecogs.com/gif.latex?Ax%3Db"/>의 양변에 역행렬을 곱하면 <img src="https://latex.codecogs.com/gif.latex?x"/>를 한꺼번에 구할 수 있다.
+ <img src="https://latex.codecogs.com/gif.latex?Ax%3Db%20%5CRightarrow%20A%5E%7B-1%7DAx%3DA%5E%7B-1%7Db%20%5CRightarrow%20x%20%3D%20A%5E%7B-1%7Db"/>

### 06 가우스-조던 소거법으로 역행렬 구하기 Inverse Matrix Using Gauss-Jordan Elimination

1. <img src="https://latex.codecogs.com/gif.latex?AA%5E%7B-1%7D%20%3D%20I"/> ......................................... <img src="https://latex.codecogs.com/gif.latex?A%5E%7B-1%7D%20%3D%20%5Bx%20%5C%20y%20%5C%20z%5D"/>.
2. <img src="https://latex.codecogs.com/gif.latex?A%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20I"/> .................................... <img src="https://latex.codecogs.com/gif.latex?I%20%3D%20%5Be_1%20%5C%20e_2%20%5C%20e_3%5D"/>
3. <img src="https://latex.codecogs.com/gif.latex?%5BAx%20%5C%20Ay%20%5C%20Az%5D%20%3D%20%5Be_1%20%5C%20e_2%20%5C%20e_3%5D"/>
4. <img src="https://latex.codecogs.com/gif.latex?Ax%20%3D%20e_1%2C%20%5C%20Ay%20%3D%20e_2%2C%20%5C%20Az%20%3D%20e_3"/> ........ <img src="https://latex.codecogs.com/gif.latex?%5BA%20%5C%20%7C%20%5C%20e_1%5D%2C%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_2%5D%2C%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_3%5D"/>
5. <img src="https://latex.codecogs.com/gif.latex?%5BA%20%5C%20%7C%20%5C%20e_1%20%5C%20e_2%20%5C%20e_3%5D"/> .....................................행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>를 가우스 소거법으로 <img src="https://latex.codecogs.com/gif.latex?U"/>로 만든다.
6. <img src="https://latex.codecogs.com/gif.latex?%5BU%20%5C%20%7C%20%5C%20e_1%27%20%5C%20e_2%27%20%5C%20e_3%27%5D"/> .................................... 행렬 <img src="https://latex.codecogs.com/gif.latex?U"/>를 가우스-조던 소거법으로 <img src="https://latex.codecogs.com/gif.latex?I"/>로 만든다.
7. <img src="https://latex.codecogs.com/gif.latex?%5BI%20%5C%20%7C%20%5C%20e_1%27%27%20%5C%20e_2%27%27%20%5C%20e_3%27%27%5D"/>
8. <img src="https://latex.codecogs.com/gif.latex?I%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%27%27%20%5C%20e_2%27%27%20%5C%20e_3%27%27%5D%20"/>
9. <img src="https://latex.codecogs.com/gif.latex?%5Ctherefore%20A%5E%7B-1%7D%20%3D%20%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%27%27%20%5C%20e_2%27%27%20%5C%20e_3%27%27%5D"/>

### 07 A = LU Factorization

+ <img src="https://latex.codecogs.com/gif.latex?Ax%3Db%20%5CRightarrow%20Ux%3Db%27"/>으로 바꿔주기 위해 <img src="https://latex.codecogs.com/gif.latex?E"/>(Elimination)를 곱해준다.
+ <img src="https://latex.codecogs.com/gif.latex?E_%7B3%7DE_%7B2%7DE_%7B1%7DA%20%3D%20U%20%5CRightarrow%20A%20%3D%20E_%7B1%7D%5E%7B-1%7DE_%7B2%7D%5E%7B-1%7DE_%7B3%7D%5E%7B-1%7DU%20%5CRightarrow%20A%20%3D%20LU%20"/> (<img src="https://latex.codecogs.com/gif.latex?E"/>는 항상 <img src="https://latex.codecogs.com/gif.latex?L"/> 형태를 유지하므로)
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>는 <img src="https://latex.codecogs.com/gif.latex?LU"/>로 분해된다.

### 08 Ax=b를 푸는 방법 (3) 칼럼 스페이스

+ '**해가 존재하는지 존재하지 않는지 판별할 수 있는 방법**'이다.
+ <img src="https://latex.codecogs.com/gif.latex?Ax%3Db"/>에서 <img src="https://latex.codecogs.com/gif.latex?A%5E%7B-1%7D"/>이 존재하지 않을 때, 해가 있는지 없는지 어떻게 알 수 있을까.
+ 공간의 관점으로 접근하면 된다.
+ <img src="https://latex.codecogs.com/gif.latex?Ax"/>는 하나의 벡터 공간인데 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 칼럼들이 <img src="https://latex.codecogs.com/gif.latex?span"/>하여 만드는 공간이므로 칼럼 스페이스 <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>라고 부른다.
+ <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>에 <img src="https://latex.codecogs.com/gif.latex?b"/>가 속하면 해가 있는 것이고, 속하지 않으면 해가 없는 것이다.

### 09 Example :: 칼럼 스페이스 묘사하기

<img src="https://latex.codecogs.com/gif.latex?%281%29%20%5C%20I%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%5C%5C%0D0%20%26%201%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="https://latex.codecogs.com/gif.latex?I"/>의 칼럼벡터는 2차원이다.
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?I"/>의 칼럼벡터는 2개가 independent하다.
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?I"/>의 칼럼벡터로 모든 2차원 공간을 만들 수 있다.
+ <img src="https://latex.codecogs.com/gif.latex?C%28I%29%20%5Crightarrow%20R%5E%7B2%7D"/>

<img src="https://latex.codecogs.com/gif.latex?%282%29%20%5C%20A%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%5C%5C%0D2%20%26%204%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 칼럼벡터는 2차원이다.
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 칼럼벡터들은 서로 dependent하다.
+ 2차원에서 칼럼벡터 1개는 line을 만들어낸다.
+ <img src="https://latex.codecogs.com/gif.latex?C%28A%29%20%5Csubset%20R%5E%7B2%7D"/>

<img src="https://latex.codecogs.com/gif.latex?%283%29%20%5C%20B%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%200%20%5C%5C%0D0%20%26%200%20%26%204%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="https://latex.codecogs.com/gif.latex?B"/>의 칼럼벡터는 2차원이다.
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?B"/>의 칼럼벡터는 2개가 서로 dependent하다.
+ 2차원에서 칼럼벡터 2개는 모든 2차원 공간을 만든다.
+ <img src="https://latex.codecogs.com/gif.latex?C%28B%29%20%5Crightarrow%20R%5E%7B2%7D"/>

### 09 Problem :: C(A)를 고려하여 Ax=b를 만족시키는 적절한 b 만들기

<img src="https://latex.codecogs.com/gif.latex?20.%28a%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%204%20%26%202%20%5C%5C%0D2%20%26%208%20%26%204%20%5C%5C%0D-1%20%26%20-4%20%26%20-2%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%20%5C%5C%0Dx_3%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0Db_1%20%5C%5C%0Db_2%20%5C%5C%0Db_3%0D%5Cend%7Bbmatrix%7D%0D"/>

+ <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>는 3차원 공간의 line이다.
+ <img src="https://latex.codecogs.com/gif.latex?b"/>는 반드시 <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>에 속해야 하므로 <img src="https://latex.codecogs.com/gif.latex?%5B1%20%5C%202%20%5C%20%7B-%7D1%5D"/>과 같은 선상에 있으면 된다.
+ <img src="https://latex.codecogs.com/gif.latex?%5Ctherefore%20b%20%3D%20%5Bb_1%20%5C%202b_1%20%5C%20%7B-%7Db_1%5D"/>

<img src="https://latex.codecogs.com/gif.latex?20.%28b%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%204%20%5C%5C%0D2%20%26%209%20%5C%5C%0D-1%20%26%20-4%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0Db_1%20%5C%5C%0Db_2%20%5C%5C%0Db_3%0D%5Cend%7Bbmatrix%7D%0D"/>

+ <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>는 3차원 공간에서 2차원 plane이다.
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 칼럼벡터를 <img src="https://latex.codecogs.com/gif.latex?%5Ba_1%20%5C%20a_2%20%5C%20a_3%5D"/>라고 할 때, <img src="https://latex.codecogs.com/gif.latex?a_1"/>과 <img src="https://latex.codecogs.com/gif.latex?a_3"/>의 비율은 고정되고 <img src="https://latex.codecogs.com/gif.latex?a_2"/>만 움직인다.
+ <img src="https://latex.codecogs.com/gif.latex?b"/>는 반드시 <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>에 속해야 하므로 <img src="https://latex.codecogs.com/gif.latex?b_1"/>과 <img src="https://latex.codecogs.com/gif.latex?b_3"/>의 비율만 고정시키면 된다.
+ <img src="https://latex.codecogs.com/gif.latex?%5Ctherefore%20b_3%20%3D%20-b_1"/>

### 10 널스페이스

+ not yet

### ?? C(A)와 N(A)

+ <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/> : 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 모든 칼럼(<img src="https://latex.codecogs.com/gif.latex?m"/>차원 벡터)들의 linear combination을 모아 놓은 집합
+ <img src="https://latex.codecogs.com/gif.latex?N%28A%29"/> : <img src="https://latex.codecogs.com/gif.latex?Ax%3D0"/>을 만족시키는 모든 <img src="https://latex.codecogs.com/gif.latex?x"/>(<img src="https://latex.codecogs.com/gif.latex?n"/>차원 벡터)를 모아 놓은 집합



---

## 03 Vector spaces and Subspaces (5) N(A) & Complete solution to Ax=b

### N(A)를 표현하는 방법 Describing N(A)





---

## 03 Vector spaces and Subspaces (5) 부분공간

### 부분공간의 조건 Subspace

<p align="center"><img src="https://latex.codecogs.com/gif.latex?%281%29%20%5C%20u%20+%20v%20%5Cin%20S%2C%20%5C%20%5Cforall%20u%2C%20v%20%5Cin%20S"/></p>
<p align="center"><img src="https://latex.codecogs.com/gif.latex?%282%29%20%5C%20cv%20%5Cin%20S%2C%20%5C%20%5Cforall%20v%20%5Cin%20S"/></p>

+ (1) <img src="https://latex.codecogs.com/gif.latex?S"/>에 속하는 어떤 벡터들의 linear combinaion한 결과 벡터도 <img src="https://latex.codecogs.com/gif.latex?S"/>에 속해야 한다.
+ (2) <img src="https://latex.codecogs.com/gif.latex?S"/>에 속하는 벡터에 스칼라곱한 결과 벡터도 <img src="https://latex.codecogs.com/gif.latex?S"/>에 속해야 한다.
+ 위 두 가지 조건을 모두 만족하면 Subspace가 된다.
+ Subspace는 항상 영 벡터를 포함하고 있다.

### 행렬에 의해 정의되는 Subspace 4가지

```
1. C(A)
2. N(A)
```

### C(A) :: Column space of A (m by n)

<p align="center"><img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Barray%7D%7Brcl%7D%20C%28A%29%20%26%20%3D%20%26%20%5C%7BAx%20%5C%20%7C%20%5C%20%5Cforall%20x%20%5Cin%20R%5E%7Bn%7D%20%5C%7D%20%5C%5C%20%26%20%3D%20%26%0D%5C%7B%5Ba_1%20%5C%20a_2%20%5C%20%5Ccdot%20%5Ccdot%20%5C%20a_n%5D%20%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%20%5C%5C%0D%5Ccdot%20%5C%5C%0D%5Ccdot%20%5C%5C%0Dx_n%0D%5Cend%7Bbmatrix%7D%0D%7C%20%5C%20%5Cforall%20x%20%5Cin%20R%5E%7Bn%7D%20%5C%7D%20%5C%5C%0D%26%20%3D%20%26%20%5C%7B%20x_1a_1%20+%20%5Ccdot%20%5Ccdot%20+%20x_na_n%2C%20%5C%20%5Cforall%20x%20%5Cin%20R%5E%7Bn%7D%20%5C%7D%20%5Cend%7Barray%7D"/></p>

+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 모든 칼럼들의 linear combination을 모아 놓은 집합
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 각 칼럼은 <img src="https://latex.codecogs.com/gif.latex?m"/>차원 벡터이므로 <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>는 <img src="https://latex.codecogs.com/gif.latex?R%5E%7Bm%7D"/>의 Subspace이다.
  + <img src="https://latex.codecogs.com/gif.latex?x_1a_1%20+%20%5Ccdot%20%5Ccdot%20+%20x_na_n%20%5Cin%20R%5E%7Bm%7D"/>

### 몇 차원 Subspace인지 구하는 방법

+ 안에 들어간 벡터가 몇 차원인지 구하면 된다.

### N(A) :: Null space of A (m by n)

<p align="center"><img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Barray%7D%7Brcl%7D%20N%28A%29%20%26%20%3D%20%26%20%5C%7Bx%20%5Cin%20R%5E%7Bn%7D%20%5C%20%7C%20%5C%20Ax%20%3D%200%20%5C%7D%20%5Cend%7Barray%7D"/></p>

+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>에 '**오른쪽**'에 곱해졌을 때 <img src="https://latex.codecogs.com/gif.latex?Ax%3D0"/>을 만드는 <img src="https://latex.codecogs.com/gif.latex?n"/>차원 <img src="https://latex.codecogs.com/gif.latex?x"/> 벡터들을 모아 놓은 집합
+ <img src="https://latex.codecogs.com/gif.latex?x"/>는 <img src="https://latex.codecogs.com/gif.latex?n"/>차원이므로 <img src="https://latex.codecogs.com/gif.latex?N%28A%29"/>는 <img src="https://latex.codecogs.com/gif.latex?R%5E%7Bn%7D"/>의 Subspace이다.

### 실생활에서 쓰이는 C(A), N(A)

<p align="center"><img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Bbmatrix%7D%0Da_1%20%5C%5C%0Da_2%20%5C%5C%0D%5Ccdot%20%5C%5C%0D%5Ccdot%20%5C%5C%0Da_m%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%20%5C%5C%0D%5Ccdot%20%5C%5C%0D%5Ccdot%20%5C%5C%0Dx_n%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0Dy_1%20%5C%5C%0Dy_2%20%5C%5C%0D%5Ccdot%20%5C%5C%0D%5Ccdot%20%5C%5C%0Dy_m%0D%5Cend%7Bbmatrix%7D"/></p>

+ MRI (자기공명영상, Magnetic Resonance Imaging)
  + 우리 몸 속의 이미지를 보려고 한다.
  + 우리 몸 속에 대한 이미지를 <img src="https://latex.codecogs.com/gif.latex?n"/>차원 벡터 <img src="https://latex.codecogs.com/gif.latex?x"/>라고 하자.
  + 미지수가 <img src="https://latex.codecogs.com/gif.latex?n"/>개이므로 방정식도 최대 <img src="https://latex.codecogs.com/gif.latex?n"/>개 필요하다.
  + 이미지의 크기가 1024*1024라면 대략 <img src="https://latex.codecogs.com/gif.latex?10%5E6"/>, 백만 개의 방정식이 필요하다.
  + 그런데 **이미지에 해당하는 벡터 <img src="https://latex.codecogs.com/gif.latex?x"/>가 특정 성질을 만족하면 방정식을 <img src="https://latex.codecogs.com/gif.latex?n"/>보다 훨씬 더 적은 <img src="https://latex.codecogs.com/gif.latex?m"/>개만 구해도 벡터 <img src="https://latex.codecogs.com/gif.latex?x"/>를 정확하게 풀어낼 수 있다**.
  + 그러한 기술을 compressed sensing이라 한다.
  + 이러한 성질을 따질 때 <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>와 <img src="https://latex.codecogs.com/gif.latex?N%28A%29"/>를 사용하게 된다.

**끝.**

---

## 10 널스페이스



---

## 09 Ax=b와 공간, 칼럼 스페이스

### 칼럼벡터와 공간의 의미

+ 공간 : **모든** 벡터(all column vectors)를 모아 놓은 집합
+ <img src="https://latex.codecogs.com/gif.latex?R%5E%7Bn%7D"/> : (모든) <img src="https://latex.codecogs.com/gif.latex?n"/>차원 칼럼벡터 <img src="https://latex.codecogs.com/gif.latex?v"/>로 구성되는 공간
+ <img src="https://latex.codecogs.com/gif.latex?R%5E%7B2%7D"/> : (모든) 2차원 칼럼벡터 <img src="https://latex.codecogs.com/gif.latex?v"/>로 구성되는 공간 = <img src="https://latex.codecogs.com/gif.latex?xy"/> plane
+ <img src="https://latex.codecogs.com/gif.latex?R%5E%7B1%7D"/> : (모든) 1차원 칼럼벡터 <img src="https://latex.codecogs.com/gif.latex?v"/>로 구성되는 공간 = Linear

### 공간에 속하는 벡터

+ (4, <img src="https://latex.codecogs.com/gif.latex?%5Cpi"/>) is in <img src="https://latex.codecogs.com/gif.latex?R%5E%7B2%7D"/>
+ (1, 1, 0, 1, 1) is in <img src="https://latex.codecogs.com/gif.latex?R%5E%7B5%7D"/>

### 벡터의 연산과 벡터 공간 Vector space

+ 벡터를 원소로 가지는 집합을 벡터 공간이라 한다.
+ 벡터 공간 <img src="https://latex.codecogs.com/gif.latex?V"/>에 속하는 벡터들을 연산한 결과 벡터 또한 <img src="https://latex.codecogs.com/gif.latex?V"/>에 속한다.

### 벡터 공간 예시

+ <img src="https://latex.codecogs.com/gif.latex?M"/> : 2 by 2 행렬의 벡터 공간
  + <img src="https://latex.codecogs.com/gif.latex?M"/>에 속하는 요소를 연산하면 항상 <img src="https://latex.codecogs.com/gif.latex?M"/>에 속하게 된다.
+ <img src="https://latex.codecogs.com/gif.latex?Z"/> : 영 벡터로 구성되는 벡터 공간

### 벡터 공간과 부분 공간 Subspaces

+ 벡터 공간에 속하는 임의의 벡터들로 만들어내는 공간을 부분 공간(subspace)이라고 한다.
+ 즉, 벡터들의 linear combination이 부분 공간(subspace)을 만들어낸다.
+ 다르게 말하면 임의의 벡터들이 <img src="https://latex.codecogs.com/gif.latex?span"/>한 것을 subspace라고 한다.
+ subspace에 속하는 벡터들을 linear combination한 결과 또한 당연히 subspace에 속한다.

### Subspace 구분법과 OX 퀴즈

#### 구분법

+ subspace에 속하는 벡터들을 linear combination한 결과가 subspace에 속하지 않으면 그것은 subspace가 아니다.

#### OX 퀴즈

+ A plane in <img src="https://latex.codecogs.com/gif.latex?R%5E%7B3%7D"/> that misses the origin : (x)
  + plane에 속하는 <img src="https://latex.codecogs.com/gif.latex?v"/>에 0을 곱한 결과가 plane에 속하지 않기 때문이다.
+ The quarter-plane : (x)
  + (2, 3)에 -1을 곱한 결과가 1사분면에 속하지 않기 때문이다.

### 칼럼 스페이스 Column Space

+ <img src="https://latex.codecogs.com/gif.latex?Ax%3Db"/>에서 <img src="https://latex.codecogs.com/gif.latex?A%5E%7B-1%7D"/>이 존재하지 않을 때, 해가 있는지 없는지 어떻게 알 수 있을까.
+ 공간의 관점으로 접근하면 된다.
+ <img src="https://latex.codecogs.com/gif.latex?Ax"/>는 하나의 벡터 공간인데 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 칼럼들이 <img src="https://latex.codecogs.com/gif.latex?span"/>하여 만드는 공간이므로 칼럼 스페이스 <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>라고 부른다.
+ <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>에 <img src="https://latex.codecogs.com/gif.latex?b"/>가 속하면 해가 있는 것이고, 속하지 않으면 해가 없는 것이다.

> **Note:** <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>에는 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 칼럼뿐만 아니라 linear combination의 결과인 <img src="https://latex.codecogs.com/gif.latex?Ax"/>까지 포함하고 있다.

### 칼럼 스페이스의 subspace

+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>가 m by n 행렬일 때, 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 칼럼들은 <img src="https://latex.codecogs.com/gif.latex?m"/>차원 벡터이다.
+ <img src="https://latex.codecogs.com/gif.latex?m"/>차원 벡터칼럼은 <img src="https://latex.codecogs.com/gif.latex?R%5E%7Bm%7D"/>에 속한다.
+ 따라서 <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>는 <img src="https://latex.codecogs.com/gif.latex?R%5E%7Bm%7D"/>의 subspace이다.

### Ax=b를 만족시키는 b 만들기

+ <img src="https://latex.codecogs.com/gif.latex?b_k"/>가 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 <img src="https://latex.codecogs.com/gif.latex?k"/>번째 칼럼 <img src="https://latex.codecogs.com/gif.latex?a_k"/>의 linear combination이 되도록 한다.
+ not yet

### C(A)가 full vector space가 되느냐 subspace가 되느냐

+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 <img src="https://latex.codecogs.com/gif.latex?m"/>차원 칼럼벡터가 <img src="https://latex.codecogs.com/gif.latex?m"/>차원을 가득 채우면 full vector space (<img src="https://latex.codecogs.com/gif.latex?R%5E%7Bm%7D"/>)가 되고 그렇지 못하면 <img src="https://latex.codecogs.com/gif.latex?R%5E%7Bm%7D"/>의 subspace가 된다.

### Example :: 칼럼 스페이스 묘사하기

<img src="https://latex.codecogs.com/gif.latex?%281%29%20%5C%20I%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%5C%5C%0D0%20%26%201%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="https://latex.codecogs.com/gif.latex?I"/>의 칼럼벡터는 2차원이다.
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?I"/>의 칼럼벡터는 2개가 independent하다.
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?I"/>의 칼럼벡터로 모든 2차원 공간을 만들 수 있다.
+ <img src="https://latex.codecogs.com/gif.latex?C%28I%29%20%5Crightarrow%20R%5E%7B2%7D"/>

<img src="https://latex.codecogs.com/gif.latex?%282%29%20%5C%20A%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%5C%5C%0D2%20%26%204%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 칼럼벡터는 2차원이다.
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?A"/>의 칼럼벡터들은 서로 dependent하다.
+ 2차원에서 칼럼벡터 1개는 line을 만들어낸다.
+ <img src="https://latex.codecogs.com/gif.latex?C%28A%29%20%5Csubset%20R%5E%7B2%7D"/>

<img src="https://latex.codecogs.com/gif.latex?%283%29%20%5C%20B%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%200%20%5C%5C%0D0%20%26%200%20%26%204%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="https://latex.codecogs.com/gif.latex?B"/>의 칼럼벡터는 2차원이다.
+ 행렬 <img src="https://latex.codecogs.com/gif.latex?B"/>의 칼럼벡터는 2개가 서로 dependent하다.
+ 2차원에서 칼럼벡터 2개는 모든 2차원 공간을 만든다.
+ <img src="https://latex.codecogs.com/gif.latex?C%28B%29%20%5Crightarrow%20R%5E%7B2%7D"/>

### Problem :: C(A)를 고려하여 Ax=b를 만족시키는 적절한 b 만들기

<img src="https://latex.codecogs.com/gif.latex?20.%28a%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%204%20%26%202%20%5C%5C%0D2%20%26%208%20%26%204%20%5C%5C%0D-1%20%26%20-4%20%26%20-2%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%20%5C%5C%0Dx_3%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0Db_1%20%5C%5C%0Db_2%20%5C%5C%0Db_3%0D%5Cend%7Bbmatrix%7D%0D"/>

+ <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>는 3차원 공간의 line이다.
+ <img src="https://latex.codecogs.com/gif.latex?b"/>는 반드시 <img src="https://latex.codecogs.com/gif.latex?C%28A%29"/>에 속해야 하므로 <img src="https://latex.codecogs.com/gif.latex?%5B1%20%5C%202%20%5C%20%7B-%7D1%5D"/>과 같은 선상에 있으면 된다.
+ <img src="https://latex.codecogs.com/gif.latex?%5Ctherefore%20b%20%3D%20%5Bb_1%20%5C%202b_1%20%5C%20%7B-%7Db_1%5D"/>

<img src="https://latex.codecogs.com/gif.latex?20.%28b%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%204%20%5C%5C%0D2%20%26%209%20%5C%5C%0D-1%20%26%20-4%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0Db_1%20%5C%5C%0Db_2%20%5C%5C%0Db_3%0D%5Cend%7Bbmatrix%7D%0D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%2524C%2528A%2529%2524%25uB294%25203%25uCC28%25uC6D0%2520%25uACF5%25uAC04%25uC5D0%25uC11C%25202%25uCC28%25uC6D0%2520plane%25uC774%25uB2E4.%250D+%2520%25uD589%25uB82C%2520%2524A%2524%25uC758%2520%25uCE7C%25uB7FC%25uBCA1%25uD130%25uB97C%2520%2524%255Ba_1%2520%255C%2520a_2%2520%255C%2520a_3%255D%2524%25uB77C%25uACE0%2520%25uD560%2520%25uB54C%252C%2520%2524a_1%2524%25uACFC%2520%2524a_3%2524%25uC758%2520%25uBE44%25uC728%25uC740%2520%25uACE0%25uC815%25uB418%25uACE0%2520%2524a_2%2524%25uB9CC%2520%25uC6C0%25uC9C1%25uC778%25uB2E4.%250D+%2520%2524b%2524%25uB294%2520%25uBC18%25uB4DC%25uC2DC%2520%2524C%2528A%2529%2524%25uC5D0%2520%25uC18D%25uD574%25uC57C%2520%25uD558%25uBBC0%25uB85C%2520%2524b_1%2524%25uACFC%2520%2524b_3%2524%25uC758%2520%25uBE44%25uC728%25uB9CC%2520%25uACE0%25uC815%25uC2DC%25uD0A4%25uBA74%2520%25uB41C%25uB2E4.%250D+%2520%2524%255Ctherefore%2520b_3%2520%253D%2520-b_1%2524%250D%250D**%25uB05D.**%250D%250D---%250D%250D%2523%2523%252008%2520Ax%253Db%25uB97C%2520%25uD478%25uB294%2520%25uBC29%25uBC95%2520%25283%2529%2520%25uCE7C%25uB7FC%2520%25uC2A4%25uD398%25uC774%25uC2A4%250D%250D%2523%2523%2523%25201%2529%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%250D%250D+%2520%2524Ax%253Db%2520%255CRightarrow%2520Ux%253Db%2527%2524%250D+%2520%25uD589%25uB82C%2520%2524A%2524%25uB97C%2520%2524U%2524%25uD615%25uD0DC%25uB85C%2520%25uBC14%25uAFBC%2520%25uD6C4%2520back%2520substituion%25uC744%2520%25uC801%25uC6A9%25uD558%25uC5EC%2520%2524x%2524%25uB97C%2520%25uD558%25uB098%25uC529%2520%25uAD6C%25uD55C%25uB2E4.%250D%250D%2523%2523%2523%25202%2529%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%250D%250D+%2520%2527**%25uC5ED%25uD589%25uB82C%25uC744%2520%25uAD6C%25uD558%25uB294%2520%25uBC29%25uBC95**%2527%25uC774%25uB2E4.%250D+%2520%2524AA%255E%257B-1%257D%253DI%2520%255CRightarrow%2520A%255Bx%2520%255C%2520y%2520%255C%2520z%255D%2520%253D%2520%255Be_1%2520%255C%2520e_2%2520%255C%2520e_3%255D%2520%255CRightarrow%2520U%255Bx%2520%255C%2520y%255C%2520z%255D%2520%253D%2520%255Be_1%2527%2520%255C%2520e_2%2527%2520%255C%2520e_3%2527%255D%2520%255CRightarrow%2520I%255Bx%2520%255C%2520y%2520%255C%2520z%255D%2520%253D%2520%255Be_1%2527%2527%2520%255C%2520e_2%2527%2527%2520%255C%2520e_3%2527%2527%255D%2524%250D+%2520%25uC5ED%25uD589%25uB82C%25uC744%2520%25uAD6C%25uD588%25uC73C%25uB2C8%2520%2524Ax%253Db%2524%25uC758%2520%25uC591%25uBCC0%25uC5D0%2520%25uC5ED%25uD589%25uB82C%25uC744%2520%25uACF1%25uD558%25uBA74%2520%2524x%2524%25uB97C%2520%25uD55C%25uAEBC%25uBC88%25uC5D0%2520%25uAD6C%25uD560%2520%25uC218%2520%25uC788%25uB2E4.%250D+%2520%2524Ax%253Db%2520%255CRightarrow%2520A%255E%257B-1%257DAx%253DA%255E%257B-1%257Db%2520%255CRightarrow%2520x%2520%253D%2520A%255E%257B-1%257Db%2524%250D%250D%2523%2523%2523%25203%2529%2520%25uCE7C%25uB7FC%2520%25uC2A4%25uD398%25uC774%25uC2A4%250D%250D+%2520%2527**%25uD574%25uAC00%2520%25uC874%25uC7AC%25uD558%25uB294%25uC9C0%2520%25uC874%25uC7AC%25uD558%25uC9C0%2520%25uC54A%25uB294%25uC9C0%2520%25uD310%25uBCC4%25uD560%2520%25uC218%2520%25uC788%25uB294%2520%25uBC29%25uBC95**%2527%25uC774%25uB2E4.%250D+%2520%2524Ax%253Db%2524%25uC5D0%25uC11C%2520%2524A%255E%257B-1%257D%2524%25uC774%2520%25uC874%25uC7AC%25uD558%25uC9C0%2520%25uC54A%25uC744%2520%25uB54C%252C%2520%25uD574%25uAC00%2520%25uC788%25uB294%25uC9C0%2520%25uC5C6%25uB294%25uC9C0%2520%25uC5B4%25uB5BB%25uAC8C%2520%25uC54C%2520%25uC218%2520%25uC788%25uC744%25uAE4C.%250D+%2520%25uACF5%25uAC04%25uC758%2520%25uAD00%25uC810%25uC73C%25uB85C%2520%25uC811%25uADFC%25uD558%25uBA74%2520%25uB41C%25uB2E4.%250D+%2520%2524Ax%2524%25uB294%2520%25uD558%25uB098%25uC758%2520%25uBCA1%25uD130%2520%25uACF5%25uAC04%25uC778%25uB370%2520%25uD589%25uB82C%2520%2524A%2524%25uC758%2520%25uCE7C%25uB7FC%25uB4E4%25uC774%2520%2524span%2524%25uD558%25uC5EC%2520%25uB9CC%25uB4DC%25uB294%2520%25uACF5%25uAC04%25uC774%25uBBC0%25uB85C%2520%25uCE7C%25uB7FC%2520%25uC2A4%25uD398%25uC774%25uC2A4%2520%2524C%2528A%2529%2524%25uB77C%25uACE0%2520%25uBD80%25uB978%25uB2E4.%250D+%2520%2524C%2528A%2529%2524%25uC5D0%2520%2524b%2524%25uAC00%2520%25uC18D%25uD558%25uBA74%2520%25uD574%25uAC00%2520%25uC788%25uB294%2520%25uAC83%25uC774%25uACE0%252C%2520%25uC18D%25uD558%25uC9C0%2520%25uC54A%25uC73C%25uBA74%2520%25uD574%25uAC00%2520%25uC5C6%25uB294%2520%25uAC83%25uC774%25uB2E4.%250D%250D**%25uB05D.**%250D%250D---%250D%250D%2523%2523%252007%2520A%2520%253D%2520LU%2520Factorization%250D%250D%2523%2523%2523%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%25uC744%2520%25uD589%25uB82C%2520%25uAC04%2520%25uACF1%25uC148%25uC73C%25uB85C%2520%25uCE58%25uD658%25uD558%25uAE30%2520Elimination%2520as%2520Matrix%2520Mutliplication%250D%250D%2560%2560%2560%250D1.%2520pivot%25uACFC%2520multiplier%25uC758%2520%25uC5F0%25uC0B0%25uC744%2520%25uD589%25uB82C%2520%25uAC04%2520%25uACF1%25uC148%25uC73C%25uB85C%2520%25uB098%25uD0C0%25uB0B8%25uB2E4.%250D%2560%2560%2560%250D%250D%22/%3E%3C/p%3E%281%29%20%5C%20%5Cbegin%7Barray%7D%7Blcr%7D%202x_%7B1%7D+3x_%7B2%7D%20%26%20%3D%20%26%205%20%5C%5C%206x_%7B1%7D+12x_%7B2%7D%20%26%20%3D%20%26%2010%20%5Cend%7Barray%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%22/%3E%3C/p%3E%282%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D6%20%26%2012%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_%7B1%7D%20%5C%5C%0Dx_%7B2%7D%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D5%20%5C%5C%0D10%0D%5Cend%7Bbmatrix%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%22/%3E%3C/p%3E%283%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D0%20%26%203%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_%7B1%7D%20%5C%5C%0Dx_%7B2%7D%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D5%20%5C%5C%0D-5%0D%5Cend%7Bbmatrix%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%2524%25282%2529%2520Ax%2520%253D%2520b%2524%25uC5D0%25uC11C%2520%2524%25283%2529%2520Ux%2520%253D%2520b%2527%2524%25uC744%2520%25uB9CC%25uB4DC%25uB294%2520%25uACFC%25uC815%25uC744%2520%25uD589%25uB82C%2520%25uAC04%2520%25uACF1%25uC148%25uC73C%25uB85C%2520%25uB098%25uD0C0%25uB0BC%2520%25uC218%2520%25uC788%25uB2E4.%250D%250D%22/%3E%3C/p%3E%282%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D6%20%26%2012%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_%7B1%7D%20%5C%5C%0Dx_%7B2%7D%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D5%20%5C%5C%0D10%0D%5Cend%7Bbmatrix%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D%250D%22/%3E%3C/p%3E%284%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%20%5C%5C%0D-3%20%26%201%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D6%20%26%2012%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D0%20%26%203%0D%5Cend%7Bbmatrix%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%2524%25284%2529%2524%25uB294%2520%25uB2E4%25uC74C%25uACFC%2520%25uAC19%25uC740%2520%25uD615%25uD0DC%25uB85C%2520%25uB098%25uD0C0%25uB0BC%2520%25uC218%2520%25uC788%25uB2E4.%2520%2524%255C%2520E_%257B21%257DA%2520%253D%2520U%2524%250D%250D%2523%2523%2523%2520A%2520%253D%2520LU%2520%2528LU%2520Factorization%2529%250D%250D%2560%2560%2560%250D1.%2520%25uC0BC%25uAC01%25uD589%25uB82C%25uC758%2520%25uB300%25uAC01%25uC120%25uC774%2520%25uBAA8%25uB450%25200%25uC774%2520%25uC544%25uB2C8%25uBA74%2520%25uC5ED%25uD589%25uB82C%25uC774%2520%25uC874%25uC7AC%25uD55C%25uB2E4.%250D%250D%253C%25uC774%25uC720%253E%250D-%2520%25uC0BC%25uAC01%25uD589%25uB82C%25uC5D0%2520%25uC18D%25uD558%25uB294%2520Elimination%2520%25uD589%25uB82C%25uC740%2520%25uACF1%25uD574%25uC9C4%2520%25uD589%25uB82C%25uC5D0%2520%25uB300%25uD574%2520%25uD2B9%25uC815%2520%25uD6A8%25uACFC%25uB97C%2520%25uBC1C%25uD718%25uD55C%25uB2E4.%250D-%2520%25uC774%2520%25uD6A8%25uACFC%25uB97C%2520%25uC5C6%25uC560%25uC8FC%25uB294%2520%25uAC83%25uC740%2520%25uD56D%25uC0C1%2520%25uC874%25uC7AC%25uD558%25uBA70%2520%25uADF8%25uAC83%25uC774%2520%25uBC14%25uB85C%2520%25uC5ED%25uD589%25uB82C%25uC774%2520%25uB41C%25uB2E4.%250D-%2520%25uB530%25uB77C%25uC11C%2520%25uC0BC%25uAC01%25uD589%25uB82C%25uC740%2520%25uB300%25uAC01%25uC120%25uC774%2520%25uBAA8%25uB450%25200%25uC774%2520%25uC544%25uB2C8%25uBA74%2520%25uD56D%25uC0C1%2520%25uC5ED%25uD589%25uB82C%25uC774%2520%25uC874%25uC7AC%25uD55C%25uB2E4.%250D%2560%2560%2560%250D%250D%22/%3E%3C/p%3E%284%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%20%5C%5C%0D-3%20%26%201%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D6%20%26%2012%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D2%20%26%203%20%5C%5C%0D0%20%26%203%0D%5Cend%7Bbmatrix%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D%22/%3E%3C/p%3E%285%29%20%5C%20E_%7B21%7DA%20%3D%20U%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%2524E_%257B21%257D%2524%25uC740%2520%25uC0BC%25uAC01%25uD589%25uB82C%25uC778%25uB370%2520%25uB300%25uAC01%25uC120%25uC758%2520%25uAC12%25uC774%2520%25uBAA8%25uB450%25200%25uC774%2520%25uC544%25uB2C8%25uBBC0%25uB85C%2520%25uC5ED%25uD589%25uB82C%25uC774%2520%25uBC18%25uB4DC%25uC2DC%2520%25uC874%25uC7AC%25uD55C%25uB2E4.%250D%250D%22/%3E%3C/p%3E%286%29%20%5C%20A%20%3D%20E_%7B21%7D%5E%7B-1%7DU%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%2524E_%257B21%257D%2524%25uC758%2520%25uC5ED%25uD589%25uB82C%25uC740%2520%2524E_%257B21%257D%2524%25uC758%2520%25uD6A8%25uACFC%25uB97C%2520%25uC5C6%25uC560%25uC8FC%25uB294%2520%25uAC83%25uC774%25uB2E4.%250D+%2520%2524E_%257B21%257D%2524%25uC758%2520%25uD6A8%25uACFC%25uB294%2520%2524%2528row_2%2529%2527%2520%253D%2520%2528row_2%2529%2520-%25203*%2528row_1%2529%2524%25uC774%25uB2E4.%250D+%2520%25uD6A8%25uACFC%25uB97C%2520%25uC5C6%25uC560%25uC8FC%25uB824%25uBA74%2520%2524%2528row_2%2529%2527%2527%2527%2520%253D%2520%2528row_2%2529%2527%2520+%25203*%2528row_1%2529%2524%25uB97C%2520%25uD574%25uC918%25uC57C%2520%25uD55C%25uB2E4.%250D%250D%22/%3E%3C/p%3E%287%29%20%5C%20A%20%3D%20E_%7B21%7D%5E%7B-1%7DU%20%3D%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%20%5C%5C%0D3%20%26%201%0D%5Cend%7Bbmatrix%7DU%0D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%2524E_%257B21%257D%2524%25uC740%2520L%2528Lower%2520TriangLUar%2529%25uC774%25uB2E4.%250D%250D%22/%3E%3C/p%3E%288%29%20%5C%20A%20%3D%20LU%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%25uC774%25uB7EC%25uD55C%2520%25uACFC%25uC815%25uC744%2520%25uBCF4%25uACE0%252C%2520%25uD589%25uB82C%2520%2524A%2524%25uB97C%2520%2524L%2524%2520%25uACF1%25uD558%25uAE30%2520%2524U%2524%25uB85C%2520%2560factorization%2560%2528%25uBD84%25uD574%2529%25uB97C%2520%25uD588%25uB2E4%25uACE0%2520%25uB9D0%25uD55C%25uB2E4.%250D%250D%253E%2520**Note%253A**%2520%2560factorization%2560%2520%253A%2520%25uBD84%25uD574%252C%2520%25uC18C%25uC778%25uC218%25uBD84%25uD574%250D%250D%2523%2523%2523%2520LU%2520Factorization%25uC744%2520%25uD558%25uB294%2520%25uC774%25uC720%250D%250D%2560%2560%2560%250D1.%2520Ax%2520%253D%2520b%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520%25uC6B0%25uB9AC%25uC758%2520%25uBAA9%25uC801%25uC740%2520x%25uB97C%2520%25uAD6C%25uD558%25uB294%2520%25uAC83%250D2.%2520A%2520%253D%2520LU%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%25201%25uBC88%2520%25uC2DD%25uC5D0%2520%25uB300%25uD55C%2520LU%2520factorization%250D3.%2520LUx%2520%253D%2520b%2520%2520%2520%2520%2520%2520%2520%2520%2523%25201%25uBC88%2520%25uC2DD%25uC5D0%2520A%253DLU%2520%25uB300%25uC785%250D4.%2520Ux%2520%253D%2520y%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520%25uC784%25uC758%25uB85C%2520%25uC815%25uC758%250D5.%2520Ly%2520%253D%2520b%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%25203%25uBC88%2520%25uC2DD%25uC5D0%2520Ux%253Dy%2520%25uCE58%25uD658%250D---------------------------------------------------------------------------%250DAx%2520%253D%2520b%250DUx%2520%253D%2520y%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520x%25uB97C%2520%25uAD6C%25uD558%25uB824%25uBA74%2520y%25uB97C%2520%25uC54C%25uC544%25uC57C%2520%25uD55C%25uB2E4%250DLy%2520%253D%2520b%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520Ly%253Db%25uC5D0%25uC11C%2520L%25uC740%2520%25uC0BC%25uAC01%25uD589%25uB82C%25uC774%25uBBC0%25uB85C%2520y%25uB97C%2520%25uC27D%25uAC8C%2520%25uAD6C%25uD560%2520%25uC218%2520%25uC788%25uB2E4%250D%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520Ly%253Db%25uC5D0%25uC11C%2520%25uAD6C%25uD55C%2520y%25uB97C%2520Ux%253Dy%25uC5D0%2520%25uC801%25uC6A9%25uD558%25uBA74%2520x%2520%25uB610%25uD55C%2520%25uC27D%25uAC8C%2520%25uAD6C%25uD560%2520%25uC218%2520%25uC788%25uB2E4.%250D----------------------------------------------------------------------------%250DAx%2520%253D%2520b%25uB97C%2520%25uD480%25uAE30%2520%25uC704%25uD574%2520%25uAD73%25uC774%2520LU%2520Factorization%25uC744%2520%25uC0AC%25uC6A9%25uD560%2520%25uD544%25uC694%25uB294%2520%25uC5C6%25uB2E4.%250D%25uBC29%25uC815%25uC2DD%25uC774%2520%25uD558%25uB098%25uC77C%2520%25uB54C%25uB294%2520%25uB2E8%25uC21C%25uD788%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%25uC744%2520%25uC0AC%25uC6A9%25uD558%25uB294%2520%25uAC83%25uC774%2520%25uBE60%25uB97C%2520%25uAC83%25uC774%25uB2E4.%250D%250D%25uADF8%25uB7EC%25uB098%2520%25uB9CC%25uC57D%2520b%25uC758%2520%25uAC12%25uC774%2520%25uACC4%25uC18D%2520%25uBCC0%25uACBD%25uB418%25uB294%2520%25uC0C1%25uD669%25uC5D0%25uC11C%2520x%25uB97C%2520%25uAD6C%25uD558%25uB824%25uBA74%2520LU%2520Factorization%25uC744%2520%25uC0AC%25uC6A9%25uD558%25uB294%2520%25uAC83%25uC774%2520%25uD6A8%25uC728%25uC801%25uC774%25uB2E4.%250D%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uB97C%25201%25uBC88%2520%25uD558%25uB294%2520%25uAC83%25uBCF4%25uB2E4%2520LU%2520Factorization%25uC774%2520%25uD6E8%25uC52C%2520%25uB354%2520%25uAC04%25uB2E8%25uD558%25uAE30%2520%25uB54C%25uBB38%25uC774%25uB2E4.%250D%250D%25uADF8%25uB798%25uC11C%2520%25uC2E4%25uC81C%25uB85C%2520%25uCEF4%25uD4E8%25uD130%2520%25uC18C%25uD504%25uD2B8%25uC6E8%25uC5B4%25uC778%2520Matlab%25uC5D0%25uC11C%25uB294%2520Ax%253Db%25uB97C%2520LU%2520Factorization%25uC73C%25uB85C%2520%25uD47C%25uB2E4%25uACE0%2520%25uC54C%25uB824%25uC838%2520%25uC788%25uB2E4.%250D%2560%2560%2560%250D%250D**%25uB05D.**%250D%250D---%250D%250D%2523%2523%252006%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%25uC73C%25uB85C%2520%25uC5ED%25uD589%25uB82C%2520%25uAD6C%25uD558%25uAE30%2520Inverse%2520Matrix%2520Using%2520Gauss-Jordan%2520Elimination%250D%250D%2523%2523%2523%2520%25uC5ED%25uD589%25uB82C%25uC744%2520%25uC5B4%25uB5BB%25uAC8C%2520%25uAD6C%25uD560%25uAE4C%2520Inverse%2520Matrix%250D%250D+%2520%2524Ax%253Db%2524%25uC5D0%25uC11C%2520%2524x%2524%25uB97C%2520%25uAD6C%25uD558%25uB294%2520%25uBC29%25uBC95%25uC740%2520%25uD589%25uB82C%2520%2524A%2524%25uC758%2520%25uC5ED%25uD589%25uB82C%25uC778%2520%2524A%255E%257B-1%257D%2524%25uC744%2520%25uAC01%2520%25uD56D%25uC758%2520%25uC67C%25uCABD%25uC5D0%2520%25uACF1%25uD558%25uB294%2520%25uAC83%25uC774%25uB2E4.%250D+%2520%25uD589%25uB82C%2520%2524A%2524%25uC758%2520%25uC5ED%25uD589%25uB82C%25uC744%2520%25uAD6C%25uD558%25uB294%2520%25uBC29%25uBC95%25uC740%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%25uC744%2520%25uC801%25uC6A9%25uD558%25uB294%2520%25uAC83%25uC774%25uB2E4.%250D+%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%25uC740%2520%2524Ax%253Db%2524%25uB97C%2520%2524Ux%253Db%2527%2524%25uC758%2520%25uD615%25uD0DC%25uB85C%2520%25uB9CC%25uB4E4%25uC9C0%25uB9CC%250D+%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%25uC740%2520%2524Ax%253Db%2524%25uB97C%2520%2524Ix%253Db%2527%2527%2524%25uC758%2520%25uD615%25uD0DC%25uB85C%2520%25uB9CC%25uB4E0%25uB2E4.%250D+%2520%25uC5EC%25uAE30%25uC11C%2520%2524b%2527%2527%2524%25uC740%2520%2524A%255E%257B-1%257Db%2524%25uB97C%2520%25uB73B%25uD55C%25uB2E4.%250D%250D%250D%2523%2523%2523%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%2520Gauss-Jordan%2520Elimination%250D%250D%2560%2560%2560%250D1.%2520AA%255E%257B-1%257D%2520%253D%2520I%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520%25uC5ED%25uD589%25uB82C%25uC758%2520%25uC131%25uC9C8%2520%25uD65C%25uC6A9%250D2.%2520A%255E%257B-1%257D%2520%253D%2520%255Bx%2520y%2520z%255D%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520%25uC5ED%25uD589%25uB82C%25uC744%2520%25uCE7C%25uB7FC%2520%25uBCA1%25uD130%25uB85C%2520%25uBCC0%25uD658%250D3.%2520A%255Bx%2520y%2520z%255D%2520%253D%2520I%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520Ax%253Db%2520%25uD615%25uD0DC%25uB85C%2520%25uC804%25uD658%250D4.%2520%255BAx%2520Ay%2520Az%255D%2520%253D%2520%255Be1%2520e2%2520e3%255D%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520%25uB2E8%25uC704%25uD589%25uB82C%25uC744%2520%25uCE7C%25uB7FC%2520%25uBCA1%25uD130%25uB85C%2520%25uBCC0%25uD658%250D5.%2520Ax%2520%253D%2520e1%252C%2520Ay%2520%253D%2520e2%252C%2520Az%2520%253D%2520e3%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520Ax%253Db%2520%25uD615%25uD0DC%25uB85C%2520%25uC804%25uD658%250D6.%2520%255BA%2520%257C%2520e1%255D%252C%2520%255BA%2520%257C%2520e2%255D%252C%2520%255BA%2520%257C%2520e3%255D%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520%25uCCA8%25uAC00%25uD589%25uB82C%2520%25uD615%25uD0DC%25uB85C%2520%25uC804%25uD658%250D7.%2520%255BA%2520%257C%2520e1%2520e2%2520e3%255D%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520%25uCCA8%25uAC00%25uD589%25uB82C%2520%25uD615%25uD0DC%25uB85C%2520%25uC804%25uD658%250D8.%2520%255BU%2520%257C%2520e1%2527%2520e2%2527%2520e3%2527%255D%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%2520%25uC801%25uC6A9%250D9.%2520%255BI%2520%257C%2520e1%2527%2527%2520e2%2527%2527%2520e3%2527%2527%255D%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%2520%25uC801%25uC6A9%250D10.%2520I%255Bx%2520y%2520z%255D%2520%253D%2520%255Be1%2527%2527%2520e2%2527%2527%2520e3%2527%2527%255D%2520%2520%2520%2520%2520%2520%2520%2520%2520%2523%2520%25uCCA8%25uAC00%25uD589%25uB82C%2520%25uD615%25uD0DC%25uB97C%2520%25uC6D0%25uB798%2520%25uC0C1%25uD0DC%25uB85C%2520%25uBCF5%25uADC0%250D11.%2520A%255E%257B-1%257D%2520%253D%2520%255Bx%2520y%2520z%255D%2520%253D%2520%255Be1%2527%2527%2520e2%2527%2527%2520e3%2527%2527%255D%250D%2560%2560%2560%250D%250D%22/%3E%3C/p%3E%281%29%20%5C%20AA%5E%7B-1%7D%3DI%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%25uC5B4%25uB5A4%2520%25uD589%25uB82C%2520%2524A%2524%25uC758%2520%25uC5ED%25uD589%25uB82C%25uC744%2520%25uACF1%25uD558%25uBA74%2520%25uB2E8%25uC704%25uD589%25uB82C%2520%2524I%2524%25uAC00%2520%25uB098%25uC628%25uB2E4.%250D%250D%22/%3E%3C/p%3E%282%29%20%5C%20A%3DR%5E%7B3*3%7D%2C%20%5C%20A%5E%7B-1%7D%20%3D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%26%20y_1%20%26%20z_1%20%5C%5C%0Dx_2%20%26%20y_2%20%26%20z_2%20%5C%5C%0Dx_3%20%26%20y_3%20%26%20z_3%0D%5Cend%7Bbmatrix%7D%0D%3D%20%5Bx%20%5C%20y%20%5C%20z%5D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%2524x%252C%2520y%252C%2520z%2524%25uB97C%2520%25uAD6C%25uD558%25uB294%2520%25uAC83%25uC774%2520%25uACE7%2520%2524A%255E%257B-1%257D%2524%25uC744%2520%25uAD6C%25uD558%25uB294%2520%25uAC83%25uC774%25uB2E4.%250D+%2520%2524%25282%2529%2524%25uB97C%2520%2524%25281%2529%2524%25uC5D0%2520%25uC801%25uC6A9%25uC2DC%25uD0A4%25uBA74%2520%25uB2E4%25uC74C%25uACFC%2520%25uAC19%25uB2E4.%250D%250D%22/%3E%3C/p%3E%283%29%20%5C%20AA%5E%7B-1%7D%20%3D%20A%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%20%26%200%20%5C%5C%0D0%20%26%201%20%26%200%20%5C%5C%0D0%20%26%200%20%26%201%0D%5Cend%7Bbmatrix%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%25uB2E8%25uC704%25uD589%25uB82C%2520%2524I%2524%25uC758%2520%25uAC01%2520%25uCE7C%25uB7FC%25uC744%2520%2524e_%257B1%257D%252C%2520e_%257B2%257D%252C%2520e_%257B3%257D%2524%25uC774%25uB77C%25uACE0%2520%25uD574%25uBCF4%25uC790.%250D%250D%22/%3E%3C/p%3E%284%29%20%5C%20%5BAx%20%5C%20Ay%20%5C%20Az%5D%20%3D%20%5Be_%7B1%7D%20%5C%20e_%7B2%7D%20%5C%20e_%7B3%7D%5D%20%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%22/%3E%3C/p%3E%285%29%20%5C%20Ax%3De_%7B1%7D%2C%20%5C%20Ay%3De_%7B2%7D%2C%20%5C%20Az%3De_%7B3%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%2524%25285%2529%2524%2520%25uAC19%25uC740%2520%25uACBD%25uC6B0%2520%2524Ax%253Db%2524%25uC758%2520%25uD615%25uD0DC%25uC774%25uBBC0%25uB85C%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%25uC744%2520%25uD65C%25uC6A9%25uD560%2520%25uC218%2520%25uC788%25uB2E4.%250D+%2520%25uADF8%25uB7F0%25uB370%2520%2524%25285%2529%2524%25uC5D0%2520%25uC788%25uB294%25203%25uAC00%25uC9C0%2520%25uC2DD%2520%25uBAA8%25uB450%2520%25uD589%25uB82C%2520%2524A%2524%25uC5D0%2520%25uB300%25uD55C%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%25uC774%25uBBC0%25uB85C%2520%25uB611%25uAC19%25uC774%2520%25uC9C4%25uD589%25uD558%25uAC8C%2520%25uB41C%25uB2E4.%250D+%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%25uC758%2520%25uACB0%25uACFC%25uB97C%2520%25uACB0%25uC815%25uC9D3%25uB294%2520%25uAC83%25uC740%2520%25uD589%25uB82C%2520%2524A%2524%25uC774%25uBBC0%25uB85C%2520%25uD55C%25uAEBC%25uBC88%25uC5D0%2520%25uCCA8%25uAC00%25uD589%25uB82C%2528augmented%2520matrix%2520form%2529%25uC744%2520%25uD65C%25uC6A9%25uD560%2520%25uC218%2520%25uC788%25uB2E4.%250D%250D%22/%3E%3C/p%3E%286%29%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_%7B1%7D%5D%2C%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_%7B2%7D%5D%2C%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_%7B3%7D%5D%20%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%22/%3E%3C/p%3E%287%29%20%5C%20%5BA%20%5C%20%7C%20%5C%20e_%7B1%7D%20%5C%20e_%7B2%7D%20%5C%20e_%7B3%7D%5D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%2524%25287%2529%2524%2520%25uC2DD%25uC5D0%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%25uC744%2520%25uC801%25uC6A9%25uD558%25uBA74%252C%2520%2524x%252C%2520y%252C%2520z%2524%25uB97C%2520%25uAD6C%25uD560%2520%25uC218%2520%25uC788%25uB2E4.%250D%250D%22/%3E%3C/p%3E%288%29%20%5C%20%5Bu%20%5C%20%7C%20%5C%20e_%7B1%7D%27%20%5C%20e_%7B2%7D%27%20%5C%20e_%7B3%7D%27%5D%20%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%25uC5D0%25uC11C%25uB294%2520%25uD589%25uB82C%2520%2524A%2524%25uB97C%2520%25uD589%25uB82C%2520%2524U%2524%25uB85C%2520%25uB9CC%25uB4E4%25uC5C8%25uB2E4.%250D%250D%22/%3E%3C/p%3E%289%29%20%5C%20%5BI%20%5C%20%7C%20%5C%20e_%7B1%7D%27%27%20%5C%20e_%7B2%7D%27%27%20%5C%20e_%7B3%7D%27%27%5D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%22/%3E%3C/p%3E%2810%29%20%5C%20I%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_%7B1%7D%27%27%20%5C%20e_%7B2%7D%27%27%20%5C%20e_%7B3%7D%27%27%5D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%25uADF8%25uB7EC%25uB098%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%25uC5D0%25uC11C%25uB294%2520%25uD589%25uB82C%2520%2524A%2524%25uB97C%2520%25uB2E8%25uC704%25uD589%25uB82C%2520%2524I%2524%25uB85C%2520%25uB9CC%25uB4E4%25uC5B4%25uC900%25uB2E4.%250D%250D%2523%2523%2523%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%2520vs.%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%2520Gauss%2520Elimination%2520vs.%2520Gauss-Jordan%2520Elimination%250D%250D%2560%2560%2560%250D1.%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%250D%250DAx%2520%253D%2520b%250D%255BA%2520%257C%2520b%255D%250D%255Bu%2520%257C%2520b%2527%255D%250DUx%2520%253D%2520b%2527%250D------%250D%253E%253E%2520back%2520substitution%25uC744%2520%25uD1B5%25uD574%2520%25uCE7C%25uB7FC%2520%25uBCA1%25uD130%2520x%25uC758%2520%25uAC01%2520%25uAC12%2528unknowns%2529%25uC744%2520%25uAD6C%25uD55C%25uB2E4.%250D%250D%250D2.%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%250D%250DAx%2520%253D%2520b%250D%255BA%2520%257C%2520b%255D%250D%255Bu%2520%257C%2520b%2527%255D%250D%255BI%2520%257C%2520b%2527%2527%255D%250DIx%2520%253D%2520b%2527%2527%250D-------%250D%253E%253E%2520%25uD589%25uB82C%2520A%25uC758%2520%25uC5ED%25uD589%25uB82C%2520A%255E%257B-1%257D%25uC744%2520%25uAD6C%25uD55C%25uB2E4.%250D%2560%2560%2560%250D%250D**%25uB05D.**%250D%250D---%250D%250D%2523%2523%252005%2520Ax%253Db%25uB97C%2520%25uD478%25uB294%2520%25uBC29%25uBC95%2520%25282%2529%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%250D%250D%2523%2523%2523%25201%2529%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%250D%250D+%2520%2524Ax%253Db%2520%255CRightarrow%2520Ux%253Db%2527%2524%250D+%2520%25uD589%25uB82C%2520%2524A%2524%25uB97C%2520%2524U%2524%25uD615%25uD0DC%25uB85C%2520%25uBC14%25uAFBC%2520%25uD6C4%2520back%2520substituion%25uC744%2520%25uC801%25uC6A9%25uD558%25uC5EC%2520%2524x%2524%25uB97C%2520%25uD558%25uB098%25uC529%2520%25uAD6C%25uD55C%25uB2E4.%250D%250D%2523%2523%2523%25202%2529%2520%25uAC00%25uC6B0%25uC2A4-%25uC870%25uB358%2520%25uC18C%25uAC70%25uBC95%250D%250D+%2520%25uC5ED%25uD589%25uB82C%25uC744%2520%25uAD6C%25uD558%25uB294%2520%25uBC29%25uBC95%25uC774%25uB2E4.%250D+%2520%2524AA%255E%257B-1%257D%253DI%2520%255CRightarrow%2520A%255Bx%2520%255C%2520y%2520%255C%2520z%255D%2520%253D%2520%255Be_1%2520%255C%2520e_2%2520%255C%2520e_3%255D%2520%255CRightarrow%2520U%255Bx%2520%255C%2520y%255C%2520z%255D%2520%253D%2520%255Be_1%2527%2520%255C%2520e_2%2527%2520%255C%2520e_3%2527%255D%2520%255CRightarrow%2520I%255Bx%2520%255C%2520y%2520%255C%2520z%255D%2520%253D%2520%255Be_1%2527%2527%2520%255C%2520e_2%2527%2527%2520%255C%2520e_3%2527%2527%255D%2524%250D+%2520%25uC5ED%25uD589%25uB82C%25uC744%2520%25uAD6C%25uD588%25uC73C%25uB2C8%2520%2524Ax%253Db%2524%25uC758%2520%25uC591%25uBCC0%25uC5D0%2520%25uC5ED%25uD589%25uB82C%25uC744%2520%25uACF1%25uD558%25uBA74%2520%2524x%2524%25uB97C%2520%25uD55C%25uAEBC%25uBC88%25uC5D0%2520%25uAD6C%25uD560%2520%25uC218%2520%25uC788%25uB2E4.%250D+%2520%2524Ax%253Db%2520%255CRightarrow%2520A%255E%257B-1%257DAx%253DA%255E%257B-1%257Db%2520%255CRightarrow%2520x%2520%253D%2520A%255E%257B-1%257Db%2524%250D%250D**%25uB05D.**%250D%250D---%250D%250D%2523%2523%252004%2520%25uCCA8%25uAC00%2520%25uD589%25uB82C%2520Augmented%2520Matrix%2520Form%250D%250D%2523%2523%2523%2520%25uCCA8%25uAC00%2520%25uD589%25uB82C%2520Augmented%2520Matrix%2520Form%250D%250D%2560%2560%2560%250DAx%2520%253D%2520b%2520%253D%253E%2520%255BA%2520%257C%2520b%255D%2520%253D%253E%2520%255Bu%2520%257C%2520b%2527%255D%2520%253D%253E%2520Ux%2520%253D%2520b%2527%250D%250D%25uD589%25uB82C%2520A%25uC5D0%2520%25uCE7C%25uB7FC%25uBCA1%25uD130%2520b%25uB97C%2520%25uBD99%25uC5EC%25uC11C%2520%25uD558%25uB098%25uC758%2520%25uD589%25uB82C%25uB85C%2520%25uB098%25uD0C0%25uB0B8%2520%25uAC83%25uC744%2520%25uCCA8%25uAC00%25uD589%25uB82C%25uC774%25uB77C%2520%25uD55C%25uB2E4.%250D%250D%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%25uC744%2520%25uC801%25uC6A9%25uD558%25uBA74%2520A%25uC758%2520row%25uC640%2520b%25uC758%2520row%25uAC00%2520%25uAC19%25uC740%2520%25uC5F0%25uC0B0%25uC744%2520%25uC801%25uC6A9%2520%25uBC1B%25uB294%25uB2E4.%250D%25uC5B4%25uCC28%25uD53C%2520%25uAC19%25uC740%2520%25uC5F0%25uC0B0%25uC744%2520%25uC801%25uC6A9%2520%25uBC1B%25uC73C%25uB2C8%2520%25uD589%25uB82C%2520A%25uC5D0%2520b%25uB97C%2520%25uCD94%25uAC00%25uD558%25uC5EC%2520%25uCCA8%25uAC00%25uD589%25uB82C%25uB85C%2520%25uB9CC%25uB4E4%2520%25uC218%2520%25uC788%25uB2E4.%250D%2560%2560%2560%250D%250D%22/%3E%3C/p%3E%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%203%20%5C%5C%0D2%20%26%202%20%26%204%20%5C%5C%0D3%20%26%207%20%26%209%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_%7B1%7D%20%5C%5C%0Dx_%7B2%7D%20%5C%5C%0Dx_%7B3%7D%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D5%20%5C%5C%0D7%20%5C%5C%0D10%0D%5Cend%7Bbmatrix%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%25uC704%2520%25uD589%25uB82C%25uC758%2520%25uD615%25uD0DC%25uB97C%2520%2524Ax%253Db%2524%25uB77C%25uACE0%2520%25uD560%2520%25uB54C%250D+%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uC5D0%25uC11C%2520%2524x%2524%25uB294%2520%25uC544%25uBB34%25uB7F0%2520%25uAD00%25uC5EC%25uB97C%2520%25uD558%25uC9C0%2520%25uC54A%25uB294%25uB2E4.%250D+%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uC758%2520%25uACB0%25uACFC%25uB97C%2520%25uACB0%25uC815%25uD558%25uB294%2520%25uAC83%25uC740%2520%25uD589%25uB82C%2520%2524A%2524%25uC774%25uB2E4.%250D%250D%22/%3E%3C/p%3E%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%203%20%26%20%7C%20%26%205%20%5C%5C%0D2%20%26%202%20%26%204%20%26%20%7C%20%26%207%20%5C%5C%0D3%20%26%207%20%26%209%20%26%20%7C%20%26%2010%0D%5Cend%7Bbmatrix%7D%0D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%25uB530%25uB77C%25uC11C%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uC5D0%25uC11C%2520%25uD544%25uC694%2520%25uC5C6%25uB294%2520%25uAC83%25uC744%2520%25uC81C%25uC678%25uD558%25uBA74%2520%25uD558%25uB098%25uC758%2520%25uD589%25uB82C%25uB85C%2520%25uB098%25uD0C0%25uB0BC%2520%25uC218%2520%25uC788%25uB2E4.%250D%250D%22/%3E%3C/p%3E%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%201%20%26%20%7C%20%26%205%20%5C%5C%0D0%20%26%200%20%26%202%20%26%20%7C%20%26%20-3%20%5C%5C%0D0%20%26%204%20%26%206%20%26%20%7C%20%26%20-5%0D%5Cend%7Bbmatrix%7D%0D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uB97C%2520%25uD1B5%25uD574%2520%25uC704%25uC640%2520%25uAC19%25uC740%2520%25uD615%25uD0DC%25uAC00%2520%25uB9CC%25uB4E4%25uC5B4%25uC9C4%25uB2E4.%250D%250D%22/%3E%3C/p%3E%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%201%20%26%20%7C%20%26%205%20%5C%5C%0D0%20%26%204%20%26%206%20%26%20%7C%20%26%20-5%20%5C%5C%0D0%20%26%200%20%26%202%20%26%20%7C%20%26%20-3%0D%5Cend%7Bbmatrix%7D%0D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%25202%25uBC88%25uC9F8%2520%25uD589%25uACFC%25203%25uBC88%25uC9F8%2520%25uD589%25uC744%2520%25uBC14%25uAFD4%25uC11C%2520%2524Ux%253Db%2527%2524%2520%25uD615%25uD0DC%25uB85C%2520%25uB9CC%25uB4E4%25uC5B4%25uC900%25uB2E4.%250D%250D**%25uB05D.**%250D%250D---%250D%250D%2523%2523%252003%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%2520Gaussian%2520Elimination%250D%250D%2523%2523%2523%2520%25uAC00%25uC6B0%25uC2A4%2520%25uC18C%25uAC70%25uBC95%2520Gauss%2520Elimination%250D%250D%2560%2560%2560%250DAx%2520%253D%2520b%2520%253D%253E%2520Ux%2520%253D%2520b%2527%2520%2528b%2520prime%2529%250D%250D1%2529%2520Ax%2520%253D%2520b%250D2%2529%2520Gauss%2520Elimination%250D3%2529%2520Ux%2520%253D%2520b%250D4%2529%2520back%2520substitution%250D%2560%2560%2560%250D%250D%22/%3E%3C/p%3E%5Cbegin%7Barray%7D%7Blcl%7D%20x_%7B1%7D+2x_%7B2%7D%20%26%20%3D%20%26%205%20%5C%5C%202x_%7B1%7D+5x_%7B2%7D%20%26%20%3D%20%26%2012%20%5Cend%7Barray%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%25uBC29%25uC815%25uC2DD%25uC744%2520%2524Ax%253Db%2524%25uB85C%2520%25uD45C%25uD604%25uD55C%25uB2E4.%250D%250D%22/%3E%3C/p%3E%5Cbegin%7Bbmatrix%7D%201%20%26%202%20%5C%5C%202%20%26%205%20%5Cend%7Bbmatrix%7D%20%5Cbegin%7Bbmatrix%7D%20x%20%5C%5C%20y%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%201%20%5C%5C%202%20%5Cend%7Bbmatrix%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520Gauss%2520Elimination%25uC73C%25uB85C%2520%25uD589%25uB82C%2520%2524A%2524%25uB97C%2520%2524U%2524%2528upper%2520triangLUar%2529%25uB85C%2520%25uB9CC%25uB4E4%25uC5B4%25uC900%25uB2E4.%250D%250D%22/%3E%3C/p%3E%5Cbegin%7Bbmatrix%7D%201%20%26%202%20%5C%5C%200%20%26%201%20%5Cend%7Bbmatrix%7D%20%20%5Cbegin%7Bbmatrix%7D%20x%20%5C%5C%20y%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%205%20%5C%5C%202%20%5Cend%7Bbmatrix%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520%25uB2E4%25uC2DC%2520%25uBC29%25uC815%25uC2DD%25uC73C%25uB85C%2520%25uB098%25uD0C0%25uB0B8%25uB2E4.%250D%250D%22/%3E%3C/p%3E%5Cbegin%7Barray%7D%7Brcl%7D%20x_%7B1%7D+2x_%7B2%7D%20%26%20%3D%20%26%205%20%5C%5C%20x_%7B2%7D%20%26%20%3D%20%26%2012%20%5Cend%7Barray%7D%3Cp%20align%3D%22center%22%3E%3Cimg%20src%3D%22https%3A//latex.codecogs.com/gif.latex%3F%250D%250D+%2520back%2520substitution%25uC744%2520%25uD1B5%25uD574%2520%25uC544%25uB798%25uC5D0%25uC11C%25uBD80%25uD130%2520%25uBBF8%25uC9C0%25uC218%25uC758%2520%25uAC12%25uC744%2520%25uCC28%25uB840%25uB300%25uB85C%2520%25uB300%25uC785%25uD558%25uBA74%2520%25uC27D%25uAC8C%2520%25uD574%25uB97C%2520%25uAD6C%25uD560%2520%25uC218%2520%25uC788%25uB2E4.%250D%250D%2523%2523%2523%2520%25uD53C%25uBD07%25uACFC%2520%25uBA40%25uD2F0%25uD50C%25uB77C%25uC774%25uC5B4%2520Pivot%2520and%2520Multiplier%250D%250D%2560%2560%2560%250DPivot%2520%253A%2520%25uC18C%25uAC70%25uB418%25uC9C0%2520%25uC54A%25uB294%2520row%25uC758%2520%25uCCAB%2520%25uBC88%25uC9F8%2520%25uAC12%250DMultiplier%2520%253A%2520%25uC18C%25uAC70%25uB420%2520row%25uC758%2520%25uCCAB%2520%25uBC88%25uC9F8%2520%25uAC12%25uC744%2520Pivot%25uC73C%25uB85C%2520%25uB098%25uB208%2520%25uAC12%250D%2560%2560%2560%250D%250D%22/%3E%3C/p%3E%5Cbegin%7Bbmatrix%7D%201%20%26%202%20%5C%5C%202%20%26%205%20%5Cend%7Bbmatrix%7D%20%5Cbegin%7Bbmatrix%7D%20x%20%5C%5C%20y%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%201%20%5C%5C%202%20%5Cend%7Bbmatrix%7D"/><img src="https://latex.codecogs.com/gif.latex?%0D%0D+%20Pivot%20%3D%201%0D+%20Multiplier%20%3D%202%0D%0D**%uB05D.**%0D%0D---%0D%0D%23%23%2002%20Ax%3Db%uB97C%20%uD478%uB294%20%uBC29%uBC95%20%281%29%20%uAC00%uC6B0%uC2A4%20%uC18C%uAC70%uBC95%0D%0D%23%23%23%201%29%20%uAC00%uC6B0%uC2A4%20%uC18C%uAC70%uBC95%0D%0D+%20"/>Ax=b \Rightarrow Ux=b'<img src="https://latex.codecogs.com/gif.latex?%0D+%20%uD589%uB82C%20"/>A<img src="https://latex.codecogs.com/gif.latex?%uB97C%20"/>U<img src="https://latex.codecogs.com/gif.latex?%uD615%uD0DC%uB85C%20%uBC14%uAFBC%20%uD6C4%20back%20substituion%uC744%20%uC801%uC6A9%uD558%uC5EC%20"/>x<img src="https://latex.codecogs.com/gif.latex?%uB97C%20%uD558%uB098%uC529%20%uAD6C%uD55C%uB2E4.%0D%0D**%uB05D.**%0D%0D---%0D%0D%23%23%2001%20%uC120%uD615%20%uBC29%uC815%uC2DD%20Linear%20Equations%0D%0D%23%23%23%20%uC120%uD615%20%uBC29%uC815%uC2DD%uC744%20%uC5B4%uB5BB%uAC8C%20%uD480%uAE4C%20Solving%20Linear%20Equations%0D%0D+%20"/>Ax=b<img src="https://latex.codecogs.com/gif.latex?%uB97C%20%uC120%uD615%20%uBC29%uC815%uC2DD%uC774%uB77C%uACE0%20%uD55C%uB2E4.%0D+%20"/>Ax=b<img src="https://latex.codecogs.com/gif.latex?%uB97C%20%uB9CC%uC871%uC2DC%uD0A4%uB294%20"/>x$를 찾는 것이 선형 방정식을 푸는 것이다.

**끝.**

---
