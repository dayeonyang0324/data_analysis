### 오픈데이터를 활용한 데이터 분석

<hr>
### 1. matplotlib 활용한 그래프

<hr>

##### 	1. 데이터 불러오기

```python
import csv
f = open('파일명.csv')
data = csv.reader(f)
next(data)  # 첫줄 제거
```

​	

##### 2. plot : 꺾은선 그래프

```python
import matplotlib.pyplot as plt

plt.plot(x축 리스트 형태 or range형태, y축 리스트 형태, label='범례에 표시할 이름', color='선 색상', ls='라인 스타일')
plt.legend()  # 범례표시
plt.title()  # 제목넣기
plt.style.use('ggplot')  # 격자 스타일
plt.show()  # 그래프 그리기
```



##### 3. hist : 히스토 그램

```python
import matplotlib.pyplot as plt

plt.hist(x축 리스트 형태, bins=x축의 갯수)  # 히스토그램에서 y축은 갯수(횟수)로 나타남
```



##### 	4. boxplot : 상자 수염 그림

```python
import matplotlib.pyplot as plt

plt.boxplot(리스트, (showfliers=False : 이상값 생략))  # 이중 리스트의 경우 [[], []] x축이 내부 리스트 갯수만큼 나뉨
plt.figure(dpi=숫자)  # 그래프 크기 수정
```



##### 	5. bar : 막대그래프

```python
import matplotlib.pyplot as plt

# pyplot과 유사
plt.bar(가로축 리스트 or range형태, 세로축 리스트, label='범레에 표시할 이름')

plt.barh(가로축 리스트 or range형태, 세로축 리스트)  # 수평 막대그래프
```



##### 6. pie : 파이 차트

```python
import matplotlib.pyplot as plt

plt.pie(리스트, labels=리스트 or '', color=리스트 or '', autopct='%.1f%%' : 백분율 1자리까지 나타냄, startangle = 90 : 시작 각도를 90도 부터, explode=(0, 0, 0.1) : 3번째 요소를 0.1만큼 부각시킴)
plt.axis('equal')  # 파이 차트 동그랗게 표현
```



##### 	7. scatter : 산점도

```python
import matplotlib.pyplot as plt

plt.scatter(가로축 리스트, 세로축 리스트, s=[] : 점 사이즈, c=[] : 색상, cmap='jet' : 컬러바 색상 빨~보, alpha=숫자 : 투명도)
plt.colorbar()  # 컬러바 표현
plt.xlabel('')  # x축 이름
plt.ylabel('')  # y축 이름
```



