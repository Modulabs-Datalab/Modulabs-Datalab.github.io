---
title: "선형대수-1.벡터"
categories:
  - Mathmatics
tags:
  - linear algebra
use_math: true
sidebar:
  nav: "docs"
---
# 선형 대수
## 1. 벡터(Vector)
벡터(Vector)는 스칼라(Scalar)와 다른 개념으로 양적인 Scalar와 함께 방향과 크기를 나타낼수 있다.

### 물리학에서의 벡터(Vector)
 - 물리학에서 백터는 크기과 방향을 가진 물리량으로 속도를 예로 들수 있으며 음의 값(-)는 방향이 반대임을 나타낸다
 예시> _동쪽으로 10km/h와 서쪽으로 10km/h는 서로 (-)의 관계를 가진다._

### 선형대수에서의 벡터(Vector)
 - 선형대수에서 벡터는 크기가 nX1(열 벡터/Column Vector)1xn(행벡터/Row Vector)인 행렬을 일컫는다.

 ~~~python
 a=[1,2] #1x2 열벡터(Row Vector)
 a_1=a[0]=1 #a1 성분
 a_2=a[1]=2 #a2 성분
 b=[[1,2],[4,5]] #2X2 행렬(2X2 Matrix)
 b_1_1=b[0][0]=1 #b11 성분
 b_1_2=b[0][1]=2 #b12 성분
 b_2_1=b[1][0]=4 #b21 성분
 b_2_2=b[1][1]=5 #b22 성분
 ~~~

### 벡터의 표기
![벡터의 표현](\assets\images\vector_expression.jpg)<br><br>
$$ | \vec a | $$ : $$ \vec a$$ 의 크기
$$ | \vec a |=5 $$
 - 선형 대수로 나타내면 $$ \left[\matrix{3 \cr 4} \right] $$ 가 된다.
 - 3차원 공간에서는 $$ \left[\matrix{3 \cr 4 \cr 8} \right] $$ 처럼 나타낼 수 있다.
 - 수식에서의 Notation은 다양하게 쓰이는데 _**a,x 처럼 소문자+bold+italic**_ 을 쓰자<br><br>
![평행인 두 벡터](\assets\images\paralle_vector.JPG)<br><br>
 - 두 벡터의 크기와 방향이 같다면 같은 벡터로 생각 할 수 있다. 평행 이동을 하면 겹치기 때문이다. 따라서, 똑같은 벡터는 무수히 많다.(선형 결합/Linear Combination 참조)

## 2.벡터의 연산
### 교환법칙
 - 벡터(Vertor)에 Scalar를 곱하면 교환법칙이 성립한다.
 $$ c \left[ \matrix{a \cr b} \right] = \left[ \matrix{a \cr b} \right] c $$
 ```python
 #벡터 스칼라 곱
 a=[1,2,3]
 b=4
 def vector_scalar_multi(v,s):#v는 vector, s는 scalar값
    for i in range(0,len(v)-1):
        v[i]=v[i]*s
    return v
 c=vector_scalar_multi(a,b)
 print(c)
 ```
 - 벡터(Vector)에 scalar를 더하거나 벡터끼리 더해도 교환법칙이 성립<br><br>
 $$ \left[ \matrix{a+c \cr b+c} \right] = \left[ \matrix{c+a \cr c
   +b} \right] $$<br><br>
 $$ \left[ \matrix{a \cr b} \right] + \left[ \matrix{c \cr d} \right] = \left[ \matrix{c \cr d} \right] + \left[ \matrix{a \cr b} \right] $$ <br><br>
```python
#두 벡터의 덧셈
a=[1,2,3]
b=[4,5,6]
def vector_add(a,b):
    c=[]
    if len(a)==len(b):
        for i in range(0,len(a)-1):
            c.append(a[i]+b[i])
    else:
        print("두 벡터의 길이가 같지 않습니다.")
    return c
c=vector_add(a,b)
print(c)
```

### 벡터 크기의 합
#### 도형으로 표현 하는 방법 <br>
[평행사변형법 이미지 삽입_그리거나 구할 것]
 - 평행사변형법
  $$ \vec a $$ 와 $$ \vec b $$<br>
 시작점 일치 시: 평행사변의 대각선이 두 백서의 합을 의미
 - $$| \vec a + \vec b |$$ : 두 벡터 합의 크기 $$ \rightarrow \overline{OC} $$ 대각선 길이를 의미<br>
 [삼각형법 이미지 삽입_그리거나 구할 것]
 - $$ \vec a $$ 와 $$ \vec b $$의 종점을 연결 시 : 시작점과 종점을 연결한 벡터가 두 벡터의 합을 의미<br>
 - $$ \vert \vec a + \vec b \vert $$ : 두 벡터의 합의 크기 $$ \rightarrow \overline{OB} $$ 길이를 의미<br>

#### 수식(?)으로 표현하는 방법
 - 2차원에서 두 벡터 합 계산<br>
![2차원 벡터 합](\assets\images\2d_vector_sum.jpg)<br>
 $$ \vec a=(a_1,a_2), \vec b=(b_1,b_2) $$<br><br>
 $$ \vec{a} +\vec{b}=(a_1+b_1,a_2+b_2) $$<br><br>
 $$ \vert \vec{a} + \vec{b} \vert = \sqrt{(a_1+b_1)^2 + (a_2+b_2)^2)} $$<br><br>
```python
# 평면벡터 크기
import math
a=[1,2]
def vector_abs(a):
   v_abs=0
   for i in a:
       v_abs+=i**2
       result=math.sqrt(v_abs)
   return result
b=vector_abs(a)
print(b)
```
<br>
 - 3차원에서 두 벡터 합 계산<br>
 ![3차원 벡터 합](\assets\images\3d_vector_sum.jpg)<br>
 $$ \vec a=(a_1,a_2,a_3), \vec{b}=(b_1,b_2,b_3) $$<br><br>
 $$ \vec a + \vec b=(a_1+b_1,a_2+b_2,a_3+b_3) $$<br><br>
 $$ \vert \vec a + \vec b \vert = \sqrt{(a_1+b_1)^2 + (a_2+b_2)^2 + (a_3+b_3)^2)} $$<br><br>
```python
 # 벡터 합의 크기
 import math
 a=[1,2]
 b=[3,4]
 v_sum=vector_add(a,b)
 v_abs=vector_abs(v_sum)
 print(v_sum)
 ```
<br>
## 2.벡터의 독립과 Span
### 선형독립(Linear Independence)
 - 벡터들의 유한 집합인 $$ S={V_1,V_2,\ldots,V_n}$$, $$  c_1V_1+c_2V_2+\ldots+c_nV_n=0$$일 때, 모든 $$c_j$$가 0이 아닌 경우가 존해하면 $$S$$는 선형 종속(Linear Dependence)라고 한다.<br>    
*회귀 분석과 연관*
 - $$c_1V_1+c_2V_2+\ldots+c_nV_n=0$$을 $$y=b_1x_1+b_2x_2$$ 식으로 고쳐보면 선형회귀식이 된다. 선형회귀에서는 $$x_i$$간의 연관성을 최소화 하여, $$x_i$$단위의 설명력을 잘 나타내고 $$y$$ 값을 잘 예측하는 $$b_i$$ 를(머신러닝에서 w)찾는것이 목적이다.<br>
