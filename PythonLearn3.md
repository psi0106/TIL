# 3강 자료형 다루기
## 데이터 타입

- 변수 또는 객체의 유형을 정의
- 메모리 저장 및 연산 방식을 결정
예) 정수, 실수, 문자열, 리스트 등

## 데이터 타입의 중요성

1. **효율성**
    
    > 적절한 데이터 타입 선택으로 메모리 및 연산 최적화
    > 
2. **안정성**
    
    > 데이터 타입을 알면 예상치 못한 에러를 방지
    > 
3. **명확성**
    
    > 코드의 의도와 동작을 더 명확하게 파악
    > 

## 리스트

- 순서가 있는 컬렉션
- 다양한 타입의 요소 포함 가능
- 변경 가능 (Mutable)

### 리스트 생성

> 대괄호([ ]) 사용
> 

```python
fruits = ["apple", "banana", "cherry"]
print(fruits)
```

각 요소를 쉼표로(,) 구분

## 리스트의 연산

### 추가

append, insert, extand

```python
fruits.append("orange")
print(fruits)
```

### 삭제

remove, pop, del

```python
fruits.remove("banana")
print(fruits)
```

```python
popped = fruits.pop(1)
print(popped)
print(fruits)
```

### 수정

```python
fruits[0] = "grape"
print(fruits)
```

### 인덱싱

```python
print(fruits[1])
```

**index()** #첫 등장하는 위치만 확인 가능

```python
idx = fruits.index("cherry")
print(idx)
```

### 슬라이싱

```python
print(fruits[0:2])
```

### 정렬

**sort()** #오름차순으로 정리

```python
numbers = [3, 1, 4, 1, 5, 9]
numbers.sort()
print(numbers) #[1, 1, 3, 4, 5, 9]
```

## 튜플

- 변경 불가능한 순서가 있는 요소의 집합(시퀀스)
- 한번 생성하면 요소를 수정, 추가, 삭제 할 수 없음

### 튜플 생성

> 소괄호( )를 사용하여 튜플 생성
> 

```python
fruits = ("apple", "banana", "cherry")
print(fruits)
```

## 튜플과 리스트의 차이점

| 리스트 | 튜플 |
| --- | --- |
| 변경 가능 (요소 추가, 삭제, 수정) | 변경 불가능 |

> 데이터의 안정성이 필요할 때 튜플 사용
> 

## 튜플 사용 예시

### 여러 변수에 값을 동시에 할당

```python
x, y, z = ("apple", "banana", "cherry")
print(x)
print(y)
print(z)
```

### 함수에서 여러 값을 반환

```python
def get_info():
	return ("Alice", 25, "Engineer")
name, age, job = get_info()

print(name, age, job)
```

## 딕셔너리

- 키(Key)와 값(Value)의 쌍으로 데이터 저장
- 키 : 중복 불가 / 값 : 중복 가능

### 딕셔너리 생성

> 중괄호{ }를 사용하여 딕셔너리 생성
> 

```python
student = {"name": "Alice", "age": 20, "major": "Computer Sience"}
print(student)
```

데이터를 빠르게 검색하고 접근하는 데 매우 효율적

## 딕셔너리 연산

### 값 접근

> dict_name[key]
> 

```python
name = student["name"]
print(name)
```

### 값 수정

> dict_name[key] = new_value
> 

```python
student["age"] = 21
print(student)
```

### 키-값 쌍 추가

> dict_name[new_key] = value
> 

```python
student["plus"] = "plus"
print(student)
```

### 키-값 쌍 삭제

> del dict_name[key]
> 

```python
del student["plus"]
print(student)
```

### 모든 키 반환

> keys()
> 

```python
print(student.keys())
```

### 모든 값 반환

> values()
> 

```python
print(student.values())
```

### 모든 키-값 쌍 반환

> items()
> 

```python
print(student.items())
```

### 키에 해당하는 값을 반환
(키가 없으면 default(None) 반환)

> get(key, default)
> 

```python
print(student.get("name"))
print(student.get("None", "default")
```

### 키에 해당하는 값을 반환 및 삭제

> pop(key)
(key가 딕셔너리에 없으면 오류)
> 

```python
age = student.pop("age")
print(age)
print(student)
```

### 다른 딕셔너리의 키-값 쌍을 현재 딕셔너리에 추가/갱신

> update(dict_name)
> 

```python
extra_info = {"job": "Engineer", "city": "San Francisco"}
student.update(extra_info)
```

## 인공지능과 데이터 과학의 자료

### 배열(Arrays) 및 행렬(Matrices)

- 대부분의 수치 계산 라이브러리는 배열 및 행렬 연산에 최적화된 데이터 구조 제공
예) Numpy, TensorFlow, PyTorch
- 행렬은 다차원 데이터, 이미지, 신경망의 가중치 등을 표현하는 데 중요

### 시리즈(Series) 및 데이터프레임(DataFrames)

- 판다스(Pandas)와 같은 라이브러리에서 사용되며, 통계 및 데이터 분석 작업에 매우 유용
- 데이터프레임은 표 형식의 데이터를 표현하며, 각 열은 다른 데이터 타입을 가질 수 있음

### 텐서(Tensors)

- 딥러닝 프레임워크에서 널리 사용
예) TensorFlow, PyTorch
- 다차원 배열을 일반화한 것으로, 스칼라, 벡터, 행렬, 그 이상의 차원을 가질 수 있음

복잡한 데이터 구조와 연산을 효과적으로 처리

### 범주형 데이터(Categorical Data)

- 머신러닝에서 범주형 변수는 종종 원-핫 인코딩 등의 방법으로 숫자로 변환
- 변환을 통해 머신러닝 알고리즘에 적합한 형식으로 데이터 준비 가능

### 시간-시퀀스 데이터(Time-Sequence Data)

- 시간에 따른 연속적인 데이터 포인트로 구성
- 주식 가격, 기후 데이터, 심박수 등의 시계열 분석에 사용

패턴 분석을 통해 미래 예측이나 이상치 탐지

### 텍스트(Text)

- 텍스트 분석 및 자연어 처리(NLP)에서 중요
- 워드 임베딩, TF-IDF, BERT 등의 방법을 통해 텍스트를 숫자 벡터로 변환 가능

유용한 정보의 추출과 그 패턴의 파악

### 이미지 및 비디오

- 이미지는 대체로 픽셀 값의 3차원 배열로 표현
- 이미지 및 비디오 데이터는 컴퓨터 비전 및 딥러닝 응용 프로그램에서 중요

RGB의 3차원 배열로 표현