# Problem Name

* [문제 출처](https://app.codesignal.com/challenge/J785w3Xu4BFzqnREg)
* 푼 날짜 : 2020-01-16
* 언어 : Python

## 문제 설명

* 설명

  ```markdown
  1~10000의 수는 1그룹 10001~20000의 수는 2그룹 ...  99001~1000000의 수는 100그룹입니다. 주어진 정수 배열 `a`를 그룹화 하였을 때 그룹의 개수와 정수의 총 개수를 더하여 반환해 주세요. 
  ```

* 예시

  ```markdown
  `a` : [20000, 239, 10001, 999999, 10000, 20566, 29999]
  
  return : 11
  ```
## 문제 풀이

* 내 코드

  ```python
  #
  ```

* 팀원1 코드

  ```python
  def numbersGrouping(a):
      len_a = len(a)
      man = 10000
      dict_l = {}
      for i in(a):
          if i/man > i//man:
              temp_num = (i//man)+1
          else:
              temp_num = (i//man)
          dict_l[temp_num] = 1
      
      
      return len_a + len(dict_l)
  ```

* 팀원2 코드

  ```python
  def numbersGrouping(a):
      empty_set = set()
      for i in a:
          empty_set.add((i+9999)//10000)
      return len(empty_set)+len(a)
  ```

## 주관적인 Best 코드

* 작성자 : 본인 (팀원2 코드 리팩토링)

```python
from math import ceil

def numbersGrouping(a):
    groups = {ceil(n/10000) for n in a}
    
    return len(groups) + len(a)
```

