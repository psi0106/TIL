# 1강 자료구조
## 조건문 / 선택문 : 
프로그램의 흐름에 따라 분기시키는 구조 /
여러 가능한 경로 중 하나를 선택하여 실행하는 구조

<aside>
💡 *조건식 뒤에 콜론(:) 붙히기*

</aside>

### if문

> 예시)
> 

```python
a=1
if a==1:
	print("a는 1입니다.")
```

### 중첩if문

> 예시)
> 

```python
a=1, b=1
if a==1:
	print("a는 1입니다.")
	if b==1:
		print("b도 1입니다.")
```

### elif문

> 예시)
> 

```python
a=15
if a>=18:
	print("성인입니다.")
elif a>=13:
	print("청소년입니다")
```

### else문

> 예시)
> 

```python
a=12
if a>=18:
	print("성인입니다.")
elif a>=13:
	print("청소년입니다")
else
	print("어린이입니다")
```

## 비교연산자

- **==** (같음) : 5==5 >> True
- **!=** (다름) : 5!=3 >> True
- **<** (작음) : 3<5 >> True
- **>** (큼) : 5>3 >> True
- **<=** (작거나 같음) : 3<=5 >> True
- **>=** (크거나 같음) : 5>=3 >> True

## 논리연산자

- **and** : 둘 다 True일 때 True
- **or** : 둘 중 하나가 True일 때 True
- **not**  : True를 False로 False를 True로

## 연산자들의 활용

```python
age=29
if age>=20 and age<30:
	print("20대입니다.")
```

```python
score=90, extra_credit=80
if (score >= 90) or (extra_credit and score>=85):
	print("A 학점입니다.")
```

## 반복문 : 특정 코드를 조건에 따라 여러 번 실행시키는 구조

### for

> 시퀀스의 각 요소를 순차적으로 탐색하기 (**기본구조**)
> 

```python
for i in [1, 2, 3, 4, 5]:
	print(i)
```

> 현재 반복문을 완전히 종료하기 (**break**)
> 

```python
for num in [1, 3, 5, 2, 4]:
	if num % 2 == 0:    #숫자 리스트에서 짝수 찾기
		print(num)
		break             #반복문 종료하기
```

> 현재 반복의 나머지 부분을 건너 뛰고 다음 반복으로 진행하기 (**continue**)
> 

```python
for num in [1, 2, 3, 4, 5] or range[1, 6, 1]:
	if num % 2 == 0:    #숫자 리스트에서 짝수 찾기
		continue          #이번 반복 건너 뛰고 다음 반복 진행
	print(num)
```

### while

> 조건이 ‘참’인 동안 반복 실행하기 (**기본구조**)
> 

```python
count = 1
while count <= 5:
	print(count)
	count += 1
```