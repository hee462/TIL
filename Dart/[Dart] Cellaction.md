>- 데이터 구조에 따른 대표적인 컬렉션(자료구조)
1) List : 순서 대로 쌓여있는 구조 (아이템의 중복 허용)
2) Map : 키(key)와 값(value)의 쌍으로 저장 (키의 중복 불가)
3) Set : 순서가 없는 집합 (중복 불가)



> ##  1. List < == 기반동작 ,동등성check >
List는 데이터를 `여러 개` 담을 수 있는 자료구조이다. 데이터를 List에 담을 때 순서를 가지기 때문에 배열을 대체할 수 있고 데이터에 `순차적`으로 접근하기 쉽다. 기본 형태는 다음과 같다.

```
List<데이터 타입> 변수명 = 
[데이터1, 데이터2, 데이터3, ..];
또는
List<데이터 타입> 변수명 = List();
colors.add(데이터1);
colors.add (E|0/E/2);
colors.add 5|0|E3);
ex)
List<String> colors = ['Red', 'Orange', 'Yellow'];
List<String> colors = List();
colors.add ('Red');
colors.add ('Orange');
colors.add ('Yellow');
```



  
> ##    2. Set <hashcode기반>
Set은 데이터를 `여러 개` 담을 수 있는 자료구조인 것은 List와 동일하다. 하지만 데이터의 `순서가 없고 중복된 요소를 허용`하지 않는다. 기본 형태는 다음과 같다.

```
Set:데이터 타입> 변수명 = 
{데이터1, 데이터2, 데이터3,..};
또는
Set<데이터 타입> 변수명= Set();
colors.add(데이터1);
colors .add(데이터2);
colors.add (50 E13);
ex)
Set<String> colors = {'RED', 'Orange', 'Yellow'};
또는
Set<String> colors = Set);
colors.add ('Red');
colors.add('Orange');
colors .add('Yellow');
```
  

  
> ##  3. Мар <hashcode기반>
Map은 `키와 값`으로 이뤄진 것이 가장 큰 특징이다. 키와 값은 한 쌍으로 이뤄진다. 키에 대한 값이 매칭 되어 있어서 `빠른 탐색`이 가능하다.
맵은 순서를 가지지 않지만 키를 정수로 설정하면 순서를 가진 것처럼 사용할 수도 있다. `키는 중복이 불가하 고 값은 중복 가능`하다.

 ```
 Maps키 타입, 값 타입> 변수명= [ 
  키1:값1,
  키2:값2,
  키3:키3
  ];
또는
Map<키 타입, 값 타입> 변수명 = Map();
변수명[1] = 값1;
변수명[2] = 값2 변수명 3」 = 값3;
ex)
Map<int, String> testMap = {
1:'Red',
2:'Orange',
3:'Yellow'
  };
또는
Map<int, String> testMap = Map();
testMap[1]= 'Red'; 
testMap[2]= 'Orange';
testMap[3] = 'Yellow'; 
``` 
  
  
  > ![](https://velog.velcdn.com/images/hee462/post/7ebe3375-facb-4b06-ad2a-65946a1100d5/image.png)
