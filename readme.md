ⓒ JMC 2017

**COURSE**  
\- 서울대학교 4차산업혁명 아카데미  
\- 인공지능 에이전트 과정  
\- 기계학습 기초수학, 김종권 교수님

**SOURCE**  
\- Introduction to Linear Algebra, Strang  
\- [MIT 선형대수학 Strang 교수 강의 OCW](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8 )  
\- [KOCW 건국대 이향원 교수 강의](http://www.kocw.net/home/search/kemView.do?kemId=1039395 )  
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

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%5Cbegin%7Barray%7D%7Blcl%7D%20x_%7B1%7D+2x_%7B2%7D%20%26%20%3D%20%26%205%20%5C%5C%202x_%7B1%7D+5x_%7B2%7D%20%26%20%3D%20%26%2012%20%5Cend%7Barray%7D"/></p>

+ 방정식을 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>로 표현한다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%5Cbegin%7Bbmatrix%7D%201%20%26%202%20%5C%5C%202%20%26%205%20%5Cend%7Bbmatrix%7D%20%5Cbegin%7Bbmatrix%7D%20x%20%5C%5C%20y%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%201%20%5C%5C%202%20%5Cend%7Bbmatrix%7D"/></p>

+ Gauss Elimination으로 행렬 A를 U(upper triangluar)로 만들어준다.

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
Ax = b => [A | b] => [u | b]

행렬 A에 칼럼 벡터 b를 붙여서 하나의 행렬로 나타낸 것을 첨가행렬이라 한다.
```

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%203%20%5C%5C%0D2%20%26%202%20%26%204%20%5C%5C%0D3%20%26%207%20%26%209%0D%5Cend%7Bbmatrix%7D%0D%5Cbegin%7Bbmatrix%7D%0Dx_%7B1%7D%20%5C%5C%0Dx_%7B2%7D%20%5C%5C%0Dx_%7B3%7D%0D%5Cend%7Bbmatrix%7D%0D%3D%0D%5Cbegin%7Bbmatrix%7D%0D5%20%5C%5C%0D7%20%5C%5C%0D10%0D%5Cend%7Bbmatrix%7D"/></p>

+ 위 행렬의 형태를 <img src="http://api.gmath.guru/cgi-bin/gmath?Ax%3Db"/>라고 할 때
+ 가우스 소거에서 x는 아무런 관여를 하지 않는다.
+ 가우스 소거의 결과를 결정하는 것은 행렬 A이다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%202%20%26%203%20%26%20%7C%20%26%205%20%5C%5C%0D2%20%26%202%20%26%204%20%26%20%7C%20%26%207%20%5C%5C%0D3%20%26%207%20%26%209%20%26%20%7C%20%26%2010%0D%5Cend%7Bbmatrix%7D%0D"/></p>

+ 따라서 가우스 소거에서 필요 없는 것을 제외하면 하나의 행렬로 나타낼 수 있다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%201%20%26%20%7C%20%26%205%20%5C%5C%0D0%20%26%200%20%26%202%20%26%20%7C%20%26%20-3%20%5C%5C%0D0%20%26%204%20%26%206%20%26%20%7C%20%26%20-5%0D%5Cend%7Bbmatrix%7D%0D"/></p>

+ 가우스 소거를 통해 위와 같은 형태가 만들어진다.

<p align="center"><img src="http://api.gmath.guru/cgi-bin/gmath?%0D%5Cbegin%7Bbmatrix%7D%0D1%20%26%201%20%26%201%20%26%20%7C%20%26%205%20%5C%5C%0D0%20%26%204%20%26%206%20%26%20%7C%20%26%20-5%20%5C%5C%0D0%20%26%200%20%26%202%20%26%20%7C%20%26%20-3%0D%5Cend%7Bbmatrix%7D%0D"/></p>

+ 2번째 행과 3번째 행을 바꿔서 <img src="http://api.gmath.guru/cgi-bin/gmath?ux%3Db"/> 형태로 만들어준다.

---