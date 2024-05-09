# 변수

## 변수 선언

```dart
//자료형 자료이름 = 자료의 값;
var name = '코드팩토리';
```

## 변수 내용 변경

```dart
var name = '코드팩토리';
print(name);
//var name = '코드팩토리2'; 는 불가능 똑같은 이름의 변수 선언 불가
name = '레드벨벳';
print(name);
```
코드팩토리   
레드벨벳
## 변수 타입

- **var**  //타입 미지정 및 타입 변경 불가 *되도록 쓰지 말아야 함*
- **int**  //정수형
- **double** //실수형
- **bool** //true or false
- **String** //문자열
문자열 **연결**
    
    ```dart
     String name = 'Hello';
     String name2 = 'world'; 
     print(name + name2);
     
     print(name + ' ' + name2);
    
     print('${name} ${name2}');
    
     print('$name $name2');
    
     print('$name.runtimeType $name2'); //변수 하나 쓸때만 가능
    ```
    Helloworld   
Hello world   
Hello world   
Hello world   
Hello.runtimeType world
- **dynamic** //타입 미지정 및 타입 변경 가능
- **List** //하나의 변수로 여러 값을 저장함
List 선언 방법
    
    ```dart
    //List<자료형> 변수이름 = [변수값0, 변수값1, 변수값2, 변수값3];
    List<String> blackPink = ['제니', '지수', '로제', '리사'];
    ```
    
    List 순서는 0부터 시작
    
    ```dart
    print(blackPink[0]);
    ```
    제니
    
    ### **List의 함수들**
    
    - .length (길이 측정)
    - .add (List에 값 넣기)
    - .remove (List에 값 지우기)
    - .indexOf (함수 안 값의 인덱스 값 알 수 있음)
- **Map //**Key & Value
Key 값으로 Value 값을 찾음
    
    ```dart
    Map<String, String> dictionary = {
    	'Herry Potter' : '해리포터',
    	'Ron Weasley' : '론 위즐리',
    	'Hermione Granger' : '헤르미온느 그레인저',
    };
    
    print(dictionary);
    
    Map<String, bool> isHerryPotter = {
    	'Herry Potter' : true,
    	'Ron Weasley' : true,
    	'Iron man' : false,
    };
    
    print(isHerryPotter);
    
    isHerryPotter.addAll({    //Map에 Key와 Value 추가
    	'Spiderman' = false,
    });
    isHerryPotter['spiderman'] = false;
    
    print(isHerryPotter);
    
    print(isHerryPotter['Iron man']);
    
    isHerryPotter.remove('HerryPotter');    //Map에 HerryPotter라는 Key 제거
    
    print(isHerryPotter);
    
    print(isHerryPotter.keys);
    print(isHerryPotter.values);
    ```
    {Herry Potter: 해리포터, Ron Weasley: 론 위즐리, Hermione Granger: 헤르미온느 그레인저}   
{Herry Potter: true, Ron Weasley: true, Iron man: false}   
{Herry Potter: true, Ron Weasley: true, Iron man: false, Spiderman: false}   
false   
{Ron Weasley: true, Iron man: false, Spiderman: false}   
(Ron Weasley, Iron man, Spiderman)   
(true, false, false)   
- Set //중복 값이 들어가지 않는 리스트
    
    ```dart
    Set<String> names = {"Code Factory", "Flutter", "Black Pink"};
    ```
    

## nullable / non-nullable

> nullable이 되는 방법
> 

```dart
//자료형? 변수이름 = 변수값;
String name = null; //오류발생

String? name = '코드팩토리';
String? name2 = null;

print(name2);

print(name!);    // !는 현재 이 값은 null이 아니라는 것을 알려줌
```
null   
코드팩토리
## DateTime

코드가 실행될 때의 시간을 저장함

```dart
DateTime now = DateTime.now();

print(now);
```
실행된 날짜 시간 분 초   
2024-05-02 21:02:55.142
## final / const

```dart
final String name = '코드팩토리'; // 변경 못하게 만듦
final name = '코드팩토리'; //타입 생략 가능 var로 만들어짐

name = '블랙핑크'; // 오류발생

print(name);

const String name2 = '블랙핑크'; // 변경 못하게 만듦
const name2 = '블랙핑크'; //타입 생략 가능 var로 만들어짐

name2 = '코드팩토리'; // 오류발생

print(name2);
```  
코드팩토리   
블랙핑크
## final과 const의 차이

> filnal은 빌드 타임에 상관없이 돌아가고
const는 빌드 타이밍 절대적으로 빌드타임의 값을 알아야한다.
> 

# 연산

## 산수 연산자

- **+** (덧셈) : 3+4=7
- **-** (뺄셈) : 5-2=3
- ***** (곱셈) : 4*2=8
- **/** (나눗셈) : 4/2=2
- **%** (나머지) : 6%4=2
- **~/** (몫) : 6//4=1
- **++** (변수에 1을 더함) : 5++ = 6
- **--** (변수에 1을 뺌) : 5-- = 4

## 할당 연산자

- **=** (변수에 값을 할당함) : a=1
- **+=** (변수에 연산자 뒤의 값을 더하고 할당함) : a=1 , a+=2 >> a=3
- **-=** (변수에 연산자 뒤의 값을 빼고 할당함) : a=1, a-=1 >> a=0
- ****=*** (변수에 연산자 뒤의 값을 곱하고 할당함) : a=1, a*=9 >> a=9
- **/=** (변수에 연산자 뒤의 값을 나누고 할당함) : a=10, a/=3 >> a=3.3333…
- **~/=** (변수에 연산자 뒤의 값을 나누고 몫을 할당함) : a=10, a~/=3 >> a=3
- ??= (변수가 만약 null라면 연산자 뒤의 값으로 할당) : a?=null, a??=3 >> a=3

## 관계 연산자

- **==** (같음) : 5==5 >> True
- **!=** (다름) : 5!=3 >> True
- **<** (작음) : 3<5 >> True
- **>** (큼) : 5>3 >> True
- **<=** (작거나 같음) : 3<=5 >> True
- **>=** (크거나 같음) : 5>=3 >> True
- **is** (자료형의 종류가 같은지 확인) :  int a = 1, a is int >> True
- **is!** (자료형의 종류가 다른지 확인) :  int a = 1, a is String >> True

## 논리연산

- **&&** : 둘 다 True일 때 True
- **||** : 둘 중 하나가 True일 때 True
- **!**  : True를 False로 False를 True로

# if문

## if : if 뒤 ()괄호 안에 있는 조건식이 true라면 코드를 실행한다.

## else if : if 조건이 틀렸을 때 else if로 가고 else if 뒤 조건식이 true라면 코드를 실행한다

## else : 모든 조건에 false일 때 실행한다

```dart
int number = 3;
if(number % 3 == 0){
	print("3으로 나누어 떨어집니다.");
}
else if(number % 3 == 2){
	print("3으로 나누었을 때 나머지가 2입니다.");
}
else{
	print("3으로 나누었을 때 나머지가 1입니다.");
}
```
3으로 나누어 떨어집니다.
# switch 문

## switch문 사용 방법 = c언어와 같음

```dart
switch(number % 3){
	case 0:
		print("3으로 나누어 떨어집니다.");
		break;
		
	case 2:
		print("3으로 나누었을 때 나머지가 2입니다.");
		break;
		
	default:
		print("3으로 나누었을 때 나머지가 1입니다.");
		break;
	}
```

# loop문

## for문

```dart
for(int i = 0; i<5; i++){
	print(i);
}
```
0   
1   
2   
3   
4
```dart
total = 0;
List<int> numbers = [1, 2, 3, 4, 5, 6];

for(int i = 0; i<numbers.length; i++){
	total += numbers[i];
}

print(total);
```
21
```dart
List<int> numbers = [1, 2, 3, 4, 5, 6];
for(int number in numbers){
	print(number);
}
```
1   
2   
3   
4   
5   
6
```dart
int total;
for(int i = 0; i<10; i++){
	total += 1;
	if(total == 5){
		break;
	}
}
print(total);
```
5
```dart
for(int i = 0; i<10; i++){
	if(i == 5){
		continue;
	}
	print(i);
}
```
0   
1   
2   
3   
4   
6   
7   
8   
9    
## while문

```dart
int total = 0;
while(total < 10){
	total += 1;
}
print(total);
```
10
```dart
int total = 0;

do {
	total += 1;
}while(total<10)
print(total);
```
10
```dart
int total = 0;
while(total < 10){
	total += 1;
	
	if(total == 5){
		break;
	}
}
print(total);
```
5
# enum

## main함수 밖에 선언 하여 값의 집합을 이루는 자료형

```dart
enum Status{
	pending,
	approved,
	rejected
}

void main() {
	Status status = Status.pending;
	
	if(status == Status.approved){
		print("승인입니다.");
	}
	else if(status == Status.pending){
		print("대기입니다.");
	}
	else{
		print("거절입니다.");
	}
```
대기입니다.   
> 타입을 강제할 수 있어 알아보기 편하며 코드 짤 때도 편하다.
> 

# 함수

> 반복되는 기능을 한번만 작성하고 바로 사용할 수 있게 해준다.
> 

```dart
void main() {
	addNumbers(10, 20, 30);
	addNumbers(20, 25, 30);
}

// optional parameter - 있어도 되고 없어도 되는 파라미터(대괄호로 선언)
// positional parameter - 순서가 중요한 파라미터
// 세개의 숫자 (x, y, z)를 더하고 짝수인지 홀수인지 알려주는 함수
addNumbers(int x, [int y, int z]){
	int sun = x + y + z;
	
	print("x : $x");
	print("y : $y");
	print("z : $z");
	
	if(sum % 2 == 0){
		print("짝수입니다");
	}
	else{
		printf("홀수입니다");
	}
}
```
x : 10   
y : 20   
z : 30   
짝수입니다   
x : 20   
y : 25   
z : 30   
홀수입니다