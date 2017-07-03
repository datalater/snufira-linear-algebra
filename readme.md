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

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>에서 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 구해야 한다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax"/>란 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 모든 칼럼들의 linear combination을 뜻한다.

### 02~03 Ax=b를 푸는 방법 (1) 가우스 소거법

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20Ux%3Db%27"/>
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>형태로 바꾼 후 back substitution을 적용하여 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 하나씩 구한다.

### 04 첨가 행렬 Augmented Matrix

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20%5BA%20%5C%20%7C%20%5C%20b%5D%20%5CRightarrow%20%5BU%20%5C%20%7C%20%5C%20b%27%5D%20%5CRightarrow%20Ux%20%3D%20b%27"/>
+ 가우스 소거법을 진행할 때 첨가행렬을 사용하면 간편하게 연산할 수 있다.

### 05~06 Ax=b를 푸는 방법 (2) 가우스-조던 소거법

+ 역행렬을 구하는 방법이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?AA%5E%7B-1%7D%3DI%20%5CRightarrow%20A%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%20%5C%20e_2%20%5C%20e_3%5D%20%5CRightarrow%20U%5Bx%20%5C%20y%5C%20z%5D%20%3D%20%5Be_1%27%20%5C%20e_2%27%20%5C%20e_3%27%5D%20%5CRightarrow%20I%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%27%27%20%5C%20e_2%27%27%20%5C%20e_3%27%27%5D"/>
+ 역행렬을 구했으니 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>의 양변에 역행렬을 곱하면 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 한꺼번에 구할 수 있다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20A%5E%7B-1%7DAx%3DA%5E%7B-1%7Db%20%5CRightarrow%20x%20%3D%20A%5E%7B-1%7Db"/>

### 07 A = LU Factorization

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20Ux%3Db%27"/>으로 바꿔주기 위해 <img src="http://api.gmath.guru/cgi-bin/gmath?E"/>(Elimination)를 곱해준다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?E_%7B3%7DE_%7B2%7DE_%7B1%7DA%20%3D%20U%20%5CRightarrow%20A%20%3D%20E_%7B1%7D%5E%7B-1%7DE_%7B2%7D%5E%7B-1%7DE_%7B3%7D%5E%7B-1%7DU%20%5CRightarrow%20A%20%3D%20LU%20"/> (<img src="http://api.gmath.guru/cgi-bin/gmath?E"/>는 항상 <img src="http://api.gmath.guru/cgi-bin/gmath?L"/> 형태를 유지하므로)
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>는 <img src="http://api.gmath.guru/cgi-bin/gmath?LU"/>로 분해된다.

### 08 Ax=b를 푸는 방법 (3) 칼럼 스페이스

+ '**해가 존재하는지 존재하지 않는지 판별할 수 있는 방법**'이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>에서 <img src="http://api.gmath.guru/cgi-bin/gmath?A%5E%7B-1%7D"/>이 존재하지 않을 때, 해가 있는지 없는지 어떻게 알 수 있을까.
+ 공간의 관점으로 접근하면 된다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax"/>는 하나의 벡터 공간인데 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 칼럼들이 <img src="http://api.gmath.guru/cgi-bin/gmath?span"/>하여 만드는 공간이므로 칼럼 스페이스 <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>라고 부른다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>에 <img src="http://api.gmath.guru/cgi-bin/gmath?b"/>가 속하면 해가 있는 것이고, 속하지 않으면 해가 없는 것이다.

### 09 Example :: 칼럼 스페이스 묘사하기

<img src="http://api.gmath.guru/cgi-bin/gmath?%281%29%20%5C%20I%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%5C%5C%0D0%20%26%201%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>의 칼럼벡터는 2차원이다.
+ 2차원 칼럼벡터 2개가 independent하다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>의 칼럼벡터로 모든 2차원 공간을 만들 수 있다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28I%29%20%5Crightarrow%20R%5E%7B2%7D"/>

<img src="http://api.gmath.guru/cgi-bin/gmath?%282%29%20%5C%20A%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%5C%5C%0D2%20%26%204%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 칼럼벡터는 2차원이다.
+ 2차원 칼럼벡터 2개가 서로 dependent하다.
+ 2차원에서 칼럼벡터 1개는 line을 만들어낸다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29%20%5Csubset%20R%5E%7B2%7D"/>

<img src="http://api.gmath.guru/cgi-bin/gmath?%283%29%20%5C%20B%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%200%20%5C%5C%0D0%20%26%200%20%26%204%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?B"/>의 칼럼벡터는 2차원이다.
+ 2차원 칼럼벡터 3개 중 2개가 서로 dependent하다.
+ 2차원에서 칼럼벡터 2개는 모든 2차원 공간을 만든다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28B%29%20%5Crightarrow%20R%5E%7B2%7D"/>

### 09 Problem :: C(A)를 고려하여 Ax=b를 만족시키는 적절한 b 만들기

<img src="http://api.gmath.guru/cgi-bin/gmath?20.%28a%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%204%20%26%202%20%5C%5C%0D2%20%26%208%20%26%204%20%5C%5C%0D-1%20%26%20-4%20%26%20-2%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%20%5C%5C%0Dx_3%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0Db_1%20%5C%5C%0Db_2%20%5C%5C%0Db_3%0D%5Cend%7Bbmatrix%7D%0D"/>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>는 3차원 벡터 3개가 모두 dependent하다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>는 3차원 공간의 line이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?b"/>는 반드시 <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>에 속해야 하므로 <img src="http://api.gmath.guru/cgi-bin/gmath?%5B1%20%5C%202%20%5C%20%7B-%7D1%5D"/>과 같은 선상에 있으면 된다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ctherefore%20b%20%3D%20%5Bb_1%20%5C%202b_1%20%5C%20%7B-%7Db_1%5D"/>

<img src="http://api.gmath.guru/cgi-bin/gmath?20.%28b%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%204%20%5C%5C%0D2%20%26%209%20%5C%5C%0D-1%20%26%20-4%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0Db_1%20%5C%5C%0Db_2%20%5C%5C%0Db_3%0D%5Cend%7Bbmatrix%7D%0D"/>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>는 3차원 벡터 2개가 서로 independent하다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>는 3차원 공간에서 2차원 plane이다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 칼럼벡터를 <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ba_1%20%5C%20a_2%20%5C%20a_3%5D"/>라고 할 때, <img src="http://api.gmath.guru/cgi-bin/gmath?a_1"/>과 <img src="http://api.gmath.guru/cgi-bin/gmath?a_3"/>의 비율은 고정되고 <img src="http://api.gmath.guru/cgi-bin/gmath?a_2"/>만 움직인다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?b"/>는 반드시 <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>에 속해야 하므로 <img src="http://api.gmath.guru/cgi-bin/gmath?b_1"/>과 <img src="http://api.gmath.guru/cgi-bin/gmath?b_3"/>의 비율만 고정시키면 된다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ctherefore%20b_3%20%3D%20-b_1"/>

### 10 널스페이스의 정의

+ <img src="http://api.gmath.guru/cgi-bin/gmath?N%28A%29"/>: <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3D0"/>을 만족시키는 모든 벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>의 집합을 공간으로 표현한 것
+ <img src="http://api.gmath.guru/cgi-bin/gmath?N%28A%29%20%5Csubseteq%20R%5E%7Bn%7D"/>: 벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>는 <img src="http://api.gmath.guru/cgi-bin/gmath?n"/>차원이므로 널스페이스는 <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7Bn%7D"/>의 subspace가 된다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 역행렬(invertible matrix)이 존재하면 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3D0"/>의 유일한 해는 <img src="http://api.gmath.guru/cgi-bin/gmath?x%3D0"/>이므로 free variable은 존재하지 않고 <img src="http://api.gmath.guru/cgi-bin/gmath?N%28A%29%3DZ"/>가 된다.

### 10 Example :: 널스페이스와 Complete solution 구하는 방법

<img src="http://api.gmath.guru/cgi-bin/gmath?%283%29%20%5C%20U%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%202%20%26%203%20%5C%5C%0D0%20%26%200%20%26%204%20%26%204%20%5C%5C%0D0%20%26%200%20%26%200%20%26%200%0D%5Cend%7Bbmatrix%7D"/>

+ pivot 칼럼은 1번째와 3번째이다.
+ free variable이 2개이므로 speicla solution도 2개 존재한다.
+ free variable에 1과 0을 대입해서 special solution을 만들 수 있다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?x_2%2C%20x_4"/>에 <img src="http://api.gmath.guru/cgi-bin/gmath?%281%2C0%29"/>을 대입하면 <img src="http://api.gmath.guru/cgi-bin/gmath?x_3%3D0%2C%20x_1%3D-1"/>이 나온다. <img src="http://api.gmath.guru/cgi-bin/gmath?s_1%20%3D%20%28-1%2C1%2C0%2C0%29"/>
+ <img src="http://api.gmath.guru/cgi-bin/gmath?x_2%2C%20x_4"/>에 <img src="http://api.gmath.guru/cgi-bin/gmath?%280%2C1%29"/>을 대입하면 <img src="http://api.gmath.guru/cgi-bin/gmath?x_3%3D-1%2C%20x_1%3D-1"/>이 나온다. <img src="http://api.gmath.guru/cgi-bin/gmath?s_2%20%3D%20%28-1%2C0%2C-1%2C1%29"/>
+ <img src="http://api.gmath.guru/cgi-bin/gmath?N%28U%29"/>는 <img src="http://api.gmath.guru/cgi-bin/gmath?s_1"/>과 <img src="http://api.gmath.guru/cgi-bin/gmath?s_2"/>의 linear combination이다.
+ free 칼럼인 <img src="http://api.gmath.guru/cgi-bin/gmath?x_2%2C%20x_4"/>에는 어떤 값을 넣어도 상관 없으므로 다음과 같다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ctherefore%20x%20%3D%20x_2%20%5Cbegin%7Bbmatrix%7D%0D-1%20%5C%5C%0D1%20%5C%5C%0D0%20%5C%5C%0D0%0D%5Cend%7Bbmatrix%7D%20+%20x_4%20%5Cbegin%7Bbmatrix%7D%0D-1%20%5C%5C%0D0%20%5C%5C%0D-1%20%5C%5C%0D1%0D%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%0D-x_2-x_4%20%5C%5C%0Dx_2%20%5C%5C%0D-x_4%5C%5C%0Dx_4%0D%5Cend%7Bbmatrix%7D"/>

### 10 Reduced Row Echelon Matrix

<img src="http://api.gmath.guru/cgi-bin/gmath?%281%29%20%5C%20U%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%202%20%26%203%20%5C%5C%0D0%20%26%200%20%26%204%20%26%204%20%5C%5C%0D0%20%26%200%20%26%200%20%26%200%0D%5Cend%7Bbmatrix%7D%20%5CRightarrow%20E%20%3D%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%200%20%26%201%20%5C%5C%0D0%20%26%200%20%26%201%20%26%201%20%5C%5C%0D0%20%26%200%20%26%200%20%26%200%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>는 pviot 아래에만 0을 가지면 된다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?E"/>는 **pivot 위에도 0을 가져야 한다**.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?E"/>의 pivot 칼럼(<img src="http://api.gmath.guru/cgi-bin/gmath?%281%2C0%2C0%29%2C%20%5C%20%280%2C1%2C0%29"/>)을 붙여 놓으면 단위행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>가 된다.

---
---
---

### 실생활에서 쓰이는 C(A), N(A)

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%5Cbegin%7Bbmatrix%7D%0Da_1%20%5C%5C%0Da_2%20%5C%5C%0D%5Ccdot%20%5C%5C%0D%5Ccdot%20%5C%5C%0Da_m%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%20%5C%5C%0D%5Ccdot%20%5C%5C%0D%5Ccdot%20%5C%5C%0Dx_n%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0Dy_1%20%5C%5C%0Dy_2%20%5C%5C%0D%5Ccdot%20%5C%5C%0D%5Ccdot%20%5C%5C%0Dy_m%0D%5Cend%7Bbmatrix%7D"/></p>

+ MRI (자기공명영상, Magnetic Resonance Imaging)
  + 우리 몸 속의 이미지를 보려고 한다.
  + 우리 몸 속에 대한 이미지를 <img src="http://api.gmath.guru/cgi-bin/gmath?n"/>차원 벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>라고 하자.
  + 미지수가 <img src="http://api.gmath.guru/cgi-bin/gmath?n"/>개이므로 방정식도 최대 <img src="http://api.gmath.guru/cgi-bin/gmath?n"/>개 필요하다.
  + 이미지의 크기가 1024*1024라면 대략 <img src="http://api.gmath.guru/cgi-bin/gmath?10%5E6"/>, 백만 개의 방정식이 필요하다.
  + 그런데 **이미지에 해당하는 벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>가 특정 성질을 만족하면 방정식을 <img src="http://api.gmath.guru/cgi-bin/gmath?n"/>보다 훨씬 더 적은 <img src="http://api.gmath.guru/cgi-bin/gmath?m"/>개만 구해도 벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 정확하게 풀어낼 수 있다**.
  + 그러한 기술을 compressed sensing이라 한다.
  + 이러한 성질을 따질 때 <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>와 <img src="http://api.gmath.guru/cgi-bin/gmath?N%28A%29"/>를 사용하게 된다.

**끝.**

---

## 11 랭크와 Row Reduced Form

+ not yet

---

## 10 널스페이스

### 널스페이스의 정의

+ <img src="http://api.gmath.guru/cgi-bin/gmath?N%28A%29"/>: <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3D0"/>을 만족시키는 모든 벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>의 집합을 그려낸 공간
+ <img src="http://api.gmath.guru/cgi-bin/gmath?N%28A%29%20%5Csubseteq%20R%5E%7Bn%7D"/>: 벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>는 <img src="http://api.gmath.guru/cgi-bin/gmath?n"/>차원이므로 널스페이스는 <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7Bn%7D"/>의 subspace가 된다.

### Special solution

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3D0"/>을 만족시키는 구체적인 벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>의 값
+ free variable에 1 또는 0을 대입하여 pivot variable의 값을 구하면 전체 special solution을 구할 수 있다.

### Example :: 널스페이스 묘사하기

<img src="http://api.gmath.guru/cgi-bin/gmath?%281%29%20%5C%20A%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%5C%5C%0D3%20%26%208%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 Elimination하면 각 칼럼은 <img src="http://api.gmath.guru/cgi-bin/gmath?%281%2C%202%29"/>와 <img src="http://api.gmath.guru/cgi-bin/gmath?%280%2C%202%29"/>이다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 모든 칼럼이 pivot 칼럼이므로 special solution은 존재하지 않는다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3D0"/>을 만족시키는 것은 <img src="http://api.gmath.guru/cgi-bin/gmath?x%3D0"/>뿐이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ctherefore%20N%28A%29%20%3D%20Z"/>


<img src="http://api.gmath.guru/cgi-bin/gmath?%282%29%20%5C%20B%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%5C%5C%0D3%20%26%208%20%5C%5C%0D2%20%26%204%20%5C%5C%0D6%20%26%2016%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?B"/>를 Elimination하면 각 칼럼은 <img src="http://api.gmath.guru/cgi-bin/gmath?%281%2C0%2C0%2C0%29%2C%20%5C%20%282%2C2%2C0%2C4%29"/>이다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?B"/>의 모든 칼럼이 pivot 칼럼이므로 special solution은 존재하지 않는다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Bx%3D0"/>을 만족시키는 것은 <img src="http://api.gmath.guru/cgi-bin/gmath?x%3D0"/>뿐이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ctherefore%20N%28B%29%20%3D%20Z"/>

<img src="http://api.gmath.guru/cgi-bin/gmath?%283%29%20%5C%20C%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%202%20%26%204%20%5C%5C%0D3%20%26%208%20%26%206%20%26%2016%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?C"/>를 Elimiation하면 <img src="http://api.gmath.guru/cgi-bin/gmath?%20%5C%20U%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%202%20%26%204%20%5C%5C%0D0%20%26%202%20%26%200%20%26%204%0D%5Cend%7Bbmatrix%7D%0D"/>가 된다.

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?C"/>의 3번째, 4번째는 free 칼럼이므로 special soution이 2개 존재한다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?x_3"/>과 <img src="http://api.gmath.guru/cgi-bin/gmath?x_4"/>에 각각 <img src="http://api.gmath.guru/cgi-bin/gmath?%281%2C%200%29"/>과 <img src="http://api.gmath.guru/cgi-bin/gmath?%280%2C%201%29"/>을 대입한다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?N%28C%29"/>를 구성하는 <img src="http://api.gmath.guru/cgi-bin/gmath?%20%5C%20s_1%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D-2%20%5C%5C%0D0%20%5C%5C%0D1%20%5C%5C%0D0%0D%5Cend%7Bbmatrix%7D%0D"/>과 <img src="http://api.gmath.guru/cgi-bin/gmath?%20%5C%20s_2%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D0%20%5C%5C%0D-2%20%5C%5C%0D0%20%5C%5C%0D1%0D%5Cend%7Bbmatrix%7D%0D"/>를 구할 수 있다.

+ <img src="http://api.gmath.guru/cgi-bin/gmath?N%28C%29"/>는 <img src="http://api.gmath.guru/cgi-bin/gmath?s_1"/>과 <img src="http://api.gmath.guru/cgi-bin/gmath?s_2"/>의 linear combination이 된다.

### R.R.E.F (Reduced Row Echelon Form)

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%20%5C%20U%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%202%20%26%204%20%5C%5C%0D0%20%26%202%20%26%200%20%26%204%0D%5Cend%7Bbmatrix%7D%20%5C%20%5CRightarrow%20%5C%20R%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%20%26%202%20%26%200%20%5C%5C%0D0%20%26%201%20%26%200%20%26%202%0D%5Cend%7Bbmatrix%7D%0D"/></p>

+ RREF 형태에서는 단위행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>의 형태가 나온다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Rx%3D0"/>의 형태를 만들어 놓으면 special solution을 찾는 것이 훨씬 쉬워진다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?R"/>의 각 칼럼에 <img src="http://api.gmath.guru/cgi-bin/gmath?x_1%2C%20x_2%2C%20x_3%2C%20x_4"/>를 곱하고 각 행의 합이 0이 나오도록 만든다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?x_1%20+%202x_3%20%3D%200%2C%20%5C%20x_2%20+%202x_4%20%3D0"/>
+ <img src="http://api.gmath.guru/cgi-bin/gmath?N%28R%29"/>를 구성하는 <img src="http://api.gmath.guru/cgi-bin/gmath?%20%5C%20s_1%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D-2%20%5C%5C%0D0%20%5C%5C%0D1%20%5C%5C%0D0%0D%5Cend%7Bbmatrix%7D%0D"/>과 <img src="http://api.gmath.guru/cgi-bin/gmath?%20%5C%20s_2%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D0%20%5C%5C%0D-2%20%5C%5C%0D0%20%5C%5C%0D1%0D%5Cend%7Bbmatrix%7D%0D"/>를 구할 수 있다.

### N(A) = Z의 아주 중요한 의미

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 모든 칼럼들이 independent하다는 것을 뜻한다.
+ independent에 대한 아이디어는 추후 논의한다.

### Example :: Ax=0에 대한 Complete solution을 구하는 방법

<img src="http://api.gmath.guru/cgi-bin/gmath?%281%29%20%5C%20A%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%202%20%26%203%20%5C%5C%0D2%20%26%202%20%26%208%20%26%2010%20%5C%5C%0D3%20%26%203%20%26%2010%20%26%2013%0D%5Cend%7Bbmatrix%7D"/>

+ 1번째 pivot은 1번째 칼럼의 <img src="http://api.gmath.guru/cgi-bin/gmath?a_%7B11%7D"/>이다.
+ pivot 아래에 있는 값들을 모두 0으로 소거해준다.

<img src="http://api.gmath.guru/cgi-bin/gmath?%282%29%20%5C%20A%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%202%20%26%203%20%5C%5C%0D0%20%26%200%20%26%204%20%26%204%20%5C%5C%0D0%20%26%200%20%26%204%20%26%204%0D%5Cend%7Bbmatrix%7D"/>

+ 2번째 pivot은 3번째 칼럼의 <img src="http://api.gmath.guru/cgi-bin/gmath?a_%7B23%7D"/>이다.
+ pivot 아래에 있는 값을 0으로 소거해준다.

<img src="http://api.gmath.guru/cgi-bin/gmath?%283%29%20%5C%20U%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%202%20%26%203%20%5C%5C%0D0%20%26%200%20%26%204%20%26%204%20%5C%5C%0D0%20%26%200%20%26%200%20%26%200%0D%5Cend%7Bbmatrix%7D"/>

+ pivot 칼럼은 1번째와 3번째이다.
+ 칼럼은 4개인데 pivot 칼럼은 2개이므로 solution은 여러 개이다.
+ free 칼럼인 2번째와 4번째에 곱해질 free variable에 0과 1을 대입해서 special solution을 만들 수 있다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?x_2%2C%20x_4"/>에 <img src="http://api.gmath.guru/cgi-bin/gmath?%281%2C0%29"/>을 대입하면 <img src="http://api.gmath.guru/cgi-bin/gmath?x_3%3D0%2C%20x_1%3D-1"/>이 나온다. <img src="http://api.gmath.guru/cgi-bin/gmath?s_1%20%3D%20%28-1%2C1%2C0%2C0%29"/>
+ <img src="http://api.gmath.guru/cgi-bin/gmath?x_2%2C%20x_4"/>에 <img src="http://api.gmath.guru/cgi-bin/gmath?%280%2C1%29"/>을 대입하면 <img src="http://api.gmath.guru/cgi-bin/gmath?x_3%3D-1%2C%20x_1%3D-1"/>이 나온다. <img src="http://api.gmath.guru/cgi-bin/gmath?s_2%20%3D%20%28-1%2C0%2C-1%2C1%29"/>
+ free 칼럼인 <img src="http://api.gmath.guru/cgi-bin/gmath?x_2%2C%20x_4"/>에는 어떤 값을 넣어도 상관 없으므로 다음과 같다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ctherefore%20x%20%3D%20x_2%20%5Cbegin%7Bbmatrix%7D%0D-1%20%5C%5C%0D1%20%5C%5C%0D0%20%5C%5C%0D0%0D%5Cend%7Bbmatrix%7D%20+%20x_4%20%5Cbegin%7Bbmatrix%7D%0D-1%20%5C%5C%0D0%20%5C%5C%0D-1%20%5C%5C%0D1%0D%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%0D-x_2-x_4%20%5C%5C%0Dx_2%20%5C%5C%0D-x_4%5C%5C%0Dx_4%0D%5Cend%7Bbmatrix%7D"/>

### Reduced Row Echelon Matrix

<img src="http://api.gmath.guru/cgi-bin/gmath?%281%29%20%5C%20U%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%202%20%26%203%20%5C%5C%0D0%20%26%200%20%26%204%20%26%204%20%5C%5C%0D0%20%26%200%20%26%200%20%26%200%0D%5Cend%7Bbmatrix%7D%20%5CRightarrow%20E%20%3D%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%200%20%26%201%20%5C%5C%0D0%20%26%200%20%26%201%20%26%201%20%5C%5C%0D0%20%26%200%20%26%200%20%26%200%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>는 pviot 아래에만 0을 가지면 된다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?E"/>는 **pivot 위에도 0을 가져야 한다**.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?E"/>의 pivot 칼럼(<img src="http://api.gmath.guru/cgi-bin/gmath?%281%2C0%2C0%29%2C%20%5C%20%280%2C1%2C0%29"/>)을 붙여 놓으면 단위행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>가 된다.

### Example :: 널스페이스 묘사하기 :: R vs E

<img src="http://api.gmath.guru/cgi-bin/gmath?%281%29%20%5C%20U%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%205%20%26%207%5C%5C%0D0%20%26%200%20%26%209%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 2번째 칼럼이 free 칼럼이므로 <img src="http://api.gmath.guru/cgi-bin/gmath?x_2"/>가 free variable이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?x_2"/>에 1을 대입해본다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?s_1%20%3D%20%28-5%2C%201%2C%200%29"/>이 나온다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?N%28A%29"/>는 <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7B3%7D"/>의 line이 된다.

<img src="http://api.gmath.guru/cgi-bin/gmath?%282%29%20%5C%20U%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%205%20%26%207%5C%5C%0D0%20%26%200%20%26%209%0D%5Cend%7Bbmatrix%7D%20%5CRightarrow%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%205%20%26%207%5C%5C%0D0%20%26%200%20%26%207%0D%5Cend%7Bbmatrix%7D%20%5CRightarrow%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%205%20%26%200%5C%5C%0D0%20%26%200%20%26%207%0D%5Cend%7Bbmatrix%7D%20%5CRightarrow%20R%20%3D%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%205%20%26%200%5C%5C%0D0%20%26%200%20%26%201%0D%5Cend%7Bbmatrix%7D%20%3D%20rref%28U%29%0D"/>

+ 2번째 칼럼에서 pivot을 발견할 수 없으니 3번째 칼럼으로 간다.
+ 3번째 칼럼의 pivot 위치의 값 9를 1로 만든다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?x_2"/>에 1을 대입해본다.
+ 더 쉽게 <img src="http://api.gmath.guru/cgi-bin/gmath?s_1%20%3D%20%28-5%2C%201%2C%200%29"/>이 나온다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?N%28A%29"/>는 <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7B3%7D"/>의 line이 된다.

### Ax=0 (m<n)에 대한 통찰

+ 와이드 스크린처럼 가로가 세로보다 훨씬 긴 직사각형 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 상상해본다.
+ pivot의 개수는 행의 개수나 열의 개수를 초과할 수 없다. (대각선이므로)
+ pivot은 최대 <img src="http://api.gmath.guru/cgi-bin/gmath?m"/>개이고 free variable은 <img src="http://api.gmath.guru/cgi-bin/gmath?n-m"/>개이므로 special solution이 최소 1개 이상 존재한다.
+ 따라서 <img src="http://api.gmath.guru/cgi-bin/gmath?x%3D0"/>이 아닌 해가 반드시 존재한다.

### invertible matrix와 free variables

+ 역행렬이 존재한다면 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3D0"/>의 유일한 해는 <img src="http://api.gmath.guru/cgi-bin/gmath?x%3D0"/>이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?x%3D0"/>이면 <img src="http://api.gmath.guru/cgi-bin/gmath?N%28A%29%3DZ"/>이므로 free variables가 없다는 뜻이다.

**끝.**

---

## 09 Ax=b와 공간, 칼럼 스페이스

### 칼럼벡터와 공간의 의미

+ 공간 : **모든** 벡터(all column vectors)를 모아 놓은 집합
+ <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7Bn%7D"/> : (모든) <img src="http://api.gmath.guru/cgi-bin/gmath?n"/>차원 칼럼벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?v"/>로 구성되는 공간
+ <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7B2%7D"/> : (모든) 2차원 칼럼벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?v"/>로 구성되는 공간 = <img src="http://api.gmath.guru/cgi-bin/gmath?xy"/> plane
+ <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7B1%7D"/> : (모든) 1차원 칼럼벡터 <img src="http://api.gmath.guru/cgi-bin/gmath?v"/>로 구성되는 공간 = Linear

### 공간에 속하는 벡터

+ (4, <img src="http://api.gmath.guru/cgi-bin/gmath?%5Cpi"/>) is in <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7B2%7D"/>
+ (1, 1, 0, 1, 1) is in <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7B5%7D"/>

### 벡터의 연산과 벡터 공간 Vector space

+ 벡터를 원소로 가지는 집합을 벡터 공간이라 한다.
+ 벡터 공간 <img src="http://api.gmath.guru/cgi-bin/gmath?V"/>에 속하는 벡터들을 연산한 결과 벡터 또한 <img src="http://api.gmath.guru/cgi-bin/gmath?V"/>에 속한다.

### 벡터 공간 예시

+ <img src="http://api.gmath.guru/cgi-bin/gmath?M"/> : 2 by 2 행렬의 벡터 공간
  + <img src="http://api.gmath.guru/cgi-bin/gmath?M"/>에 속하는 요소를 연산하면 항상 <img src="http://api.gmath.guru/cgi-bin/gmath?M"/>에 속하게 된다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Z"/> : 영 벡터로 구성되는 벡터 공간

### 벡터 공간과 부분 공간 Subspaces

+ 벡터 공간에 속하는 임의의 벡터들로 만들어내는 공간을 부분 공간(subspace)이라고 한다.
+ 즉, 벡터들의 linear combination이 부분 공간(subspace)을 만들어낸다.
+ 다르게 말하면 임의의 벡터들이 <img src="http://api.gmath.guru/cgi-bin/gmath?span"/>한 것을 subspace라고 한다.
+ subspace에 속하는 벡터들을 linear combination한 결과 또한 당연히 subspace에 속한다.

### Subspace 구분법과 OX 퀴즈

#### 구분법

+ subspace에 속하는 벡터들을 linear combination한 결과가 subspace에 속하지 않으면 그것은 subspace가 아니다.

#### OX 퀴즈

+ A plane in <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7B3%7D"/> that misses the origin : (x)
  + plane에 속하는 <img src="http://api.gmath.guru/cgi-bin/gmath?v"/>에 0을 곱한 결과가 plane에 속하지 않기 때문이다.
+ The quarter-plane : (x)
  + (2, 3)에 -1을 곱한 결과가 1사분면에 속하지 않기 때문이다.

### 칼럼 스페이스 Column Space

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>에서 <img src="http://api.gmath.guru/cgi-bin/gmath?A%5E%7B-1%7D"/>이 존재하지 않을 때, 해가 있는지 없는지 어떻게 알 수 있을까.
+ 공간의 관점으로 접근하면 된다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax"/>는 하나의 벡터 공간인데 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 칼럼들이 <img src="http://api.gmath.guru/cgi-bin/gmath?span"/>하여 만드는 공간이므로 칼럼 스페이스 <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>라고 부른다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>에 <img src="http://api.gmath.guru/cgi-bin/gmath?b"/>가 속하면 해가 있는 것이고, 속하지 않으면 해가 없는 것이다.

> **Note:** <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>에는 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 칼럼뿐만 아니라 linear combination의 결과인 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax"/>까지 포함하고 있다.

### 칼럼 스페이스의 subspace

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>가 m by n 행렬일 때, 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 칼럼들은 <img src="http://api.gmath.guru/cgi-bin/gmath?m"/>차원 벡터이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?m"/>차원 벡터칼럼은 <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7Bm%7D"/>에 속한다.
+ 따라서 <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>는 <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7Bm%7D"/>의 subspace이다.

### Ax=b를 만족시키는 b 만들기

+ <img src="http://api.gmath.guru/cgi-bin/gmath?b_k"/>가 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 <img src="http://api.gmath.guru/cgi-bin/gmath?k"/>번째 칼럼 <img src="http://api.gmath.guru/cgi-bin/gmath?a_k"/>의 linear combination이 되도록 한다.
+ not yet

### C(A)가 full vector space가 되느냐 subspace가 되느냐

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 <img src="http://api.gmath.guru/cgi-bin/gmath?m"/>차원 칼럼벡터가 <img src="http://api.gmath.guru/cgi-bin/gmath?m"/>차원을 가득 채우면 full vector space (<img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7Bm%7D"/>)가 되고 그렇지 못하면 <img src="http://api.gmath.guru/cgi-bin/gmath?R%5E%7Bm%7D"/>의 subspace가 된다.

### Example :: 칼럼 스페이스 묘사하기

<img src="http://api.gmath.guru/cgi-bin/gmath?%281%29%20%5C%20I%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%200%5C%5C%0D0%20%26%201%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>의 칼럼벡터는 2차원이다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>의 칼럼벡터는 2개가 independent하다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?I"/>의 칼럼벡터로 모든 2차원 공간을 만들 수 있다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28I%29%20%5Crightarrow%20R%5E%7B2%7D"/>

<img src="http://api.gmath.guru/cgi-bin/gmath?%282%29%20%5C%20A%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%5C%5C%0D2%20%26%204%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 칼럼벡터는 2차원이다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 칼럼벡터들은 서로 dependent하다.
+ 2차원에서 칼럼벡터 1개는 line을 만들어낸다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29%20%5Csubset%20R%5E%7B2%7D"/>

<img src="http://api.gmath.guru/cgi-bin/gmath?%283%29%20%5C%20B%20%3D%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%200%20%5C%5C%0D0%20%26%200%20%26%204%0D%5Cend%7Bbmatrix%7D%0D"/>

+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?B"/>의 칼럼벡터는 2차원이다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?B"/>의 칼럼벡터는 2개가 서로 dependent하다.
+ 2차원에서 칼럼벡터 2개는 모든 2차원 공간을 만든다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28B%29%20%5Crightarrow%20R%5E%7B2%7D"/>

### Problem :: C(A)를 고려하여 Ax=b를 만족시키는 적절한 b 만들기

<img src="http://api.gmath.guru/cgi-bin/gmath?20.%28a%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%204%20%26%202%20%5C%5C%0D2%20%26%208%20%26%204%20%5C%5C%0D-1%20%26%20-4%20%26%20-2%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%20%5C%5C%0Dx_3%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0Db_1%20%5C%5C%0Db_2%20%5C%5C%0Db_3%0D%5Cend%7Bbmatrix%7D%0D"/>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>는 3차원 공간의 line이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?b"/>는 반드시 <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>에 속해야 하므로 <img src="http://api.gmath.guru/cgi-bin/gmath?%5B1%20%5C%202%20%5C%20%7B-%7D1%5D"/>과 같은 선상에 있으면 된다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ctherefore%20b%20%3D%20%5Bb_1%20%5C%202b_1%20%5C%20%7B-%7Db_1%5D"/>

<img src="http://api.gmath.guru/cgi-bin/gmath?20.%28b%29%20%5C%20%5Cbegin%7Bbmatrix%7D%0D1%20%26%204%20%5C%5C%0D2%20%26%209%20%5C%5C%0D-1%20%26%20-4%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_1%20%5C%5C%0Dx_2%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0Db_1%20%5C%5C%0Db_2%20%5C%5C%0Db_3%0D%5Cend%7Bbmatrix%7D%0D"/>

+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>는 3차원 공간에서 2차원 plane이다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 칼럼벡터를 <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ba_1%20%5C%20a_2%20%5C%20a_3%5D"/>라고 할 때, <img src="http://api.gmath.guru/cgi-bin/gmath?a_1"/>과 <img src="http://api.gmath.guru/cgi-bin/gmath?a_3"/>의 비율은 고정되고 <img src="http://api.gmath.guru/cgi-bin/gmath?a_2"/>만 움직인다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?b"/>는 반드시 <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>에 속해야 하므로 <img src="http://api.gmath.guru/cgi-bin/gmath?b_1"/>과 <img src="http://api.gmath.guru/cgi-bin/gmath?b_3"/>의 비율만 고정시키면 된다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?%5Ctherefore%20b_3%20%3D%20-b_1"/>

**끝.**

---

## 08 Ax=b를 푸는 방법 (3) 칼럼 스페이스

### 1) 가우스 소거법

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20Ux%3Db%27"/>
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>형태로 바꾼 후 back substituion을 적용하여 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 하나씩 구한다.

### 2) 가우스-조던 소거법

+ '**역행렬을 구하는 방법**'이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?AA%5E%7B-1%7D%3DI%20%5CRightarrow%20A%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%20%5C%20e_2%20%5C%20e_3%5D%20%5CRightarrow%20U%5Bx%20%5C%20y%5C%20z%5D%20%3D%20%5Be_1%27%20%5C%20e_2%27%20%5C%20e_3%27%5D%20%5CRightarrow%20I%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%27%27%20%5C%20e_2%27%27%20%5C%20e_3%27%27%5D"/>
+ 역행렬을 구했으니 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>의 양변에 역행렬을 곱하면 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 한꺼번에 구할 수 있다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20A%5E%7B-1%7DAx%3DA%5E%7B-1%7Db%20%5CRightarrow%20x%20%3D%20A%5E%7B-1%7Db"/>

### 3) 칼럼 스페이스

+ '**해가 존재하는지 존재하지 않는지 판별할 수 있는 방법**'이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>에서 <img src="http://api.gmath.guru/cgi-bin/gmath?A%5E%7B-1%7D"/>이 존재하지 않을 때, 해가 있는지 없는지 어떻게 알 수 있을까.
+ 공간의 관점으로 접근하면 된다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax"/>는 하나의 벡터 공간인데 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 칼럼들이 <img src="http://api.gmath.guru/cgi-bin/gmath?span"/>하여 만드는 공간이므로 칼럼 스페이스 <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>라고 부른다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?C%28A%29"/>에 <img src="http://api.gmath.guru/cgi-bin/gmath?b"/>가 속하면 해가 있는 것이고, 속하지 않으면 해가 없는 것이다.

**끝.**

---

## 07 A = LU Factorization

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

### A = LU (LU Factorization)

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

+ <img src="http://api.gmath.guru/cgi-bin/gmath?E_%7B21%7D"/>은 L(Lower triangular)이다.

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

## 06 가우스-조던 소거법으로 역행렬 구하기 Inverse Matrix Using Gauss-Jordan Elimination

### 역행렬을 어떻게 구할까 Inverse Matrix

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>에서 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 구하는 방법은 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 역행렬인 <img src="http://api.gmath.guru/cgi-bin/gmath?A%5E%7B-1%7D"/>을 각 항의 왼쪽에 곱하는 것이다.
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>의 역행렬을 구하는 방법은 가우스-조던 소거법을 적용하는 것이다.
+ 가우스 소거법은 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>를 <img src="http://api.gmath.guru/cgi-bin/gmath?Ux%3Db%27"/>의 형태로 만들지만
+ 가우스-조던 소거법은 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>를 <img src="http://api.gmath.guru/cgi-bin/gmath?Ix%3Db%27%27"/>의 형태로 만든다.
+ 여기서 <img src="http://api.gmath.guru/cgi-bin/gmath?b%27%27"/>은 <img src="http://api.gmath.guru/cgi-bin/gmath?A%5E%7B-1%7Db"/>를 뜻한다.


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

## 05 Ax=b를 푸는 방법 (2) 가우스-조던 소거법

### 1) 가우스 소거법

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20Ux%3Db%27"/>
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>형태로 바꾼 후 back substituion을 적용하여 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 하나씩 구한다.

### 2) 가우스-조던 소거법

+ 역행렬을 구하는 방법이다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?AA%5E%7B-1%7D%3DI%20%5CRightarrow%20A%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%20%5C%20e_2%20%5C%20e_3%5D%20%5CRightarrow%20U%5Bx%20%5C%20y%5C%20z%5D%20%3D%20%5Be_1%27%20%5C%20e_2%27%20%5C%20e_3%27%5D%20%5CRightarrow%20I%5Bx%20%5C%20y%20%5C%20z%5D%20%3D%20%5Be_1%27%27%20%5C%20e_2%27%27%20%5C%20e_3%27%27%5D"/>
+ 역행렬을 구했으니 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>의 양변에 역행렬을 곱하면 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 한꺼번에 구할 수 있다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20A%5E%7B-1%7DAx%3DA%5E%7B-1%7Db%20%5CRightarrow%20x%20%3D%20A%5E%7B-1%7Db"/>

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

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%203%20%5C%5C%0D2%20%26%202%20%26%204%20%5C%5C%0D3%20%26%207%20%26%209%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_%7B1%7D%20%5C%5C%0Dx_%7B2%7D%20%5C%5C%0Dx_%7B3%7D%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D5%20%5C%5C%0D7%20%5C%5C%0D10%0D%5Cend%7Bbmatrix%7D"/></p>

+ 위 행렬의 형태를 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>라고 할 때
+ 가우스 소거에서 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>는 아무런 관여를 하지 않는다.
+ 가우스 소거의 결과를 결정하는 것은 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>이다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%203%20%26%20%7C%20%26%205%20%5C%5C%0D2%20%26%202%20%26%204%20%26%20%7C%20%26%207%20%5C%5C%0D3%20%26%207%20%26%209%20%26%20%7C%20%26%2010%0D%5Cend%7Bbmatrix%7D%0D"/></p>

+ 따라서 가우스 소거에서 필요 없는 것을 제외하면 하나의 행렬로 나타낼 수 있다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%201%20%26%20%7C%20%26%205%20%5C%5C%0D0%20%26%200%20%26%202%20%26%20%7C%20%26%20-3%20%5C%5C%0D0%20%26%204%20%26%206%20%26%20%7C%20%26%20-5%0D%5Cend%7Bbmatrix%7D%0D"/></p>

+ 가우스 소거를 통해 위와 같은 형태가 만들어진다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%201%20%26%20%7C%20%26%205%20%5C%5C%0D0%20%26%204%20%26%206%20%26%20%7C%20%26%20-5%20%5C%5C%0D0%20%26%200%20%26%202%20%26%20%7C%20%26%20-3%0D%5Cend%7Bbmatrix%7D%0D"/></p>

+ 2번째 행과 3번째 행을 바꿔서 <img src="http://api.gmath.guru/cgi-bin/gmath?Ux%3Db%27"/> 형태로 만들어준다.

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

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%5Cbegin%7Barray%7D%7Blcl%7D%20x_%7B1%7D+2x_%7B2%7D%20%26%20%3D%20%26%205%20%5C%5C%202x_%7B1%7D+5x_%7B2%7D%20%26%20%3D%20%26%2012%20%5Cend%7Barray%7D"/></p>

+ 방정식을 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>로 표현한다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%5Cbegin%7Bbmatrix%7D%201%20%26%202%20%5C%5C%202%20%26%205%20%5Cend%7Bbmatrix%7D%20%5Cbegin%7Bbmatrix%7D%20x%20%5C%5C%20y%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%201%20%5C%5C%202%20%5Cend%7Bbmatrix%7D"/></p>

+ Gauss Elimination으로 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>(upper triangular)로 만들어준다.

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

**끝.**

---

## 02 Ax=b를 푸는 방법 (1) 가우스 소거법

### 1) 가우스 소거법

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db%20%5CRightarrow%20Ux%3Db%27"/>
+ 행렬 <img src="http://api.gmath.guru/cgi-bin/gmath?A"/>를 <img src="http://api.gmath.guru/cgi-bin/gmath?U"/>형태로 바꾼 후 back substituion을 적용하여 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 하나씩 구한다.

**끝.**

---

## 01 선형 방정식 Linear Equations

### 선형 방정식을 어떻게 풀까 Solving Linear Equations

+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>를 선형 방정식이라고 한다.
+ <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>를 만족시키는 <img src="http://api.gmath.guru/cgi-bin/gmath?x"/>를 찾는 것이 선형 방정식을 푸는 것이다.

**끝.**

---