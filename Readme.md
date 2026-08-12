Today I learned 
 
# 기초수학
**1장 1강: 벡터의 수학적 정의와 기하학적 해석**
---
### 벡터의 수학적 정의와 기하학적 해석
- 스칼라(Scalar): 크기만 가지는 하나의 숫자 <==> 숫자 하나 
  - Ex. 25kg, 60km/hr

- 벡터(Vector): 여러개의 숫자를 순서대로 나열한 묶음, 벡터의 성분(component)라고 부른다 <==> 숫자들을 방향과 함께 표현하는것

- 행렬(Matrix): 숫자는 행과 열의 2차원 격자 형태고 배열한 것이다. <==> 숫자들을 행과 열로 배열한 것

==> 스칼라는 0차원, 벡터는 1차원, 행렬은 2차원 형태로 숫자를 담는 그릇이다. 

---

import numpy as np  
// Python에서 숫자, 벡터, 행렬 같은 수학 계산을 쉽게 하기 위해 NumPy 라이브러리를 블러오고 앞으로 np라고 짧은 이름을 사용하겠다는 뜻  

scalar = 3.5  
// 크기만 가지고 있는 하나의 값

vector = np.array([2, 3])  
// 원점 (0, 0)에서 (2,3)까지 뻗어나가는 화살표  

matrix = np.array([[1, 2], [3, 4]])  
// 왼쪽 좌표가 행렬에서 첫 번째 행이고 두 번째 좌표가 두 번째 행이다. 

Norm(벡터의 크기, 길이): ||v|| = sqrt((v_1)^2 + (v_2)^2)  
// 이 공식을 통해 우리는 벡터의 크기, 즉 길이의 값을 알 수 있다.  
// 2차원 벡터 v=(v_1, v_2)의 노름은 피타고라스 정리를 이용해 구한다. 

벡터의 덧셈: 같은 위치에 있는 성분끼리 더하는 연산이라고 할 수 있음. 좌표로 생각해보면 x 위치에 있는 좌표 값들끼리 더하고 y 위치에 있는 좌표 값들끼리 더하는것이다.  

Ex.  
&nbsp; a = (a_1 + a_2)  
&nbsp; b = (b_1 + b_2)  

&nbsp; a + b = (a_1 + b_1, a_2 + b_2)  

스칼라 곱:  벡터의 모든 성분에 같은 숫자(스칼라)를 곱하는 연산  

Ex.   
&nbsp; c = 스칼라  
&nbsp; v = (v_1, v_2)  
&nbsp; cv = (cv_1, cv_2)  
==> 스칼라 곱은 벡터의 길이를 늘리거나 줄이는 역할을 한다.   
==> C 가 음수면 방향이 반대로 뒤집힌다.  

---

### 단위벡터와 정규화

단위벡터: 노름, 즉 벡터의 크기가 1인 벡터  
정규화: 어떤 벡터든 자기 자신의 노름으로 나누면 방향은 그대로 유지한채 크기만 1롤 만들 수 있다.  
- unit_v = v/||v||  

v = np.array([3, 4])   
norm_v = np.linalg.norm(v)  
unit_v = v/norm_v  

==> 이 코드는 벡터(vector) [3, 4]의 길이(Norm)를 구한 뒤, 길이가 1인 단위벡터(unit vector)로 변환하는 코드  

&nbsp;&nbsp; 1. v = np.array([3, 4])&nbsp;&nbsp;// numpy를 이용해서 벡터를 만드는것이다.  
&nbsp;&nbsp; ==> v = (3, 4) &nbsp;// 원점(0,0)에서 (3,4)를 향하는 화살표라고 생각하면 된다.  

&nbsp;&nbsp; 2. np.linalg.norm(v) &nbsp;&nbsp;// 벡터의 Norm은 쉽게 말하면 벡터의 길이이다.  
&nbsp;&nbsp; ==> ||V|| = sqrt((V_1)^2 + (V_2)^2)  
&nbsp;&nbsp; ==> ||V|| = sqrt(3^2 + 4^2)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = sqrt(25)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = 5.0   
&nbsp;&nbsp; ==> norm_v = np.linalg.norm(v) = 5.0 &nbsp;&nbsp;&nbsp;// NumPy의 np.linalg.norm()은 일반적으로 실수형 값을 반환한다. 그래서 5가 아닌 5.0

















