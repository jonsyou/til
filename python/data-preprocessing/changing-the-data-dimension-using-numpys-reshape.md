# Numpy의 Reshape 함수를 활용한 데이터 차원 재배열
<b>Numpy</b>의 ```reshape``` 함수를 활용하여 기존 배열의 데이터를 그대로 유지한채 <b>배열의 차원을 지정</b>해 줄 수 있다.

아래의 코드와 같이 <b>1차원</b>의 데이터를 <b>2차원</b>으로 변환하는 것이 가능하다. 또한 <b>1차원</b>의 데이터를 <b>3차원</b>으로 변환하는 것 역시 가능하다.

```python
import numpy as np

# np.reshape(변경할 배열, 차원)
np.reshape([1,2,3,4,5,6,7,8],(2,4)) # 2차원
np.reshape([1,2,3,4,5,6,7,8],(2,2,2)) # 3차원
```

차원을 지정해주는 입력인수에 ```-1``` 값을 입력을 해주는 것도 가능하다. 
이는 해당 위치의 차원을 <b>"원래 배열의 길이와 남은 차원으로 부터 추정"</b> 하여 자동으로 입력하겠다는 뜻이다. 
```python
array_.reshape(-1,n)
```
위의 코드를 실행하면 n개의 열과 추정된 행의 개수를 가진 데이터 배열이 만들어진다. 즉 행의 위치에 ```-1``` 을 입력하면 행의 크기를 자동으로 추정해준다.

---
- <b>Flatten 함수를 활용하여 1차원 배열로 변환하기</b>

```array_.reshape(-1)``` 의 결과와 같이 1차원 배열을 반환해준다. 

```python
array_.flatten()
```
