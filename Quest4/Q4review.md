# Code Peer Review Templete

- 코더 : 박동원님
- 리뷰어 : 백기웅

---

# PRT(PeerReviewTemplate)

각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.

- [x] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [x] 주석을 보고 작성자의 코드가 이해되었나요?
- [x] 코드가 에러를 유발할 가능성이 있나요?
- [x] 코드 작성자가 코드를 제대로 이해하고 작성했나요? (직접 인터뷰해보기)
- [x] 코드가 간결한가요?

---

```python
# Fish 클래스
class Fish:
  def __init__(self, name, speed):
    self.name = name
    self.speed = speed
  
  def movement(self):
    print(f"{self.name} is swimming at {self.speed} m/s")
  
# 컴프리헨션 사용해서 출력하는 함수
def show_fish_movement_comprehension(fish_list):
  [i.movement() for i in fish_list]

# 이터레이터 사용해서 출력하는 함수
def show_fish_movement_iterator(fish_list):
  fish_iter = iter(fish_list)
  for i in range(len(fish_list)):
    fish_iter.__next__().movement()  # next함수를 이용해 출력. 이런 방법도 있네요. 잘 배웠습니다.

# 제너레이터 사용해서 출력하는 함수
def show_fish_movement_generator(fish_list):
  def fish_generator(obj):
    yield obj.movement()
  for i in fish_list:
    print(i)
    # print(fish_generator(i))

show_fish_movement_generator(fish_list)
  
# 물고기 리스트
fish_list = [
    Fish("Nemo", 3),
    Fish("Dory", 5),
    Fish("Marlin", 7),
    Fish("Bubbles", 2),
    Fish("Gill", 4)
]

# 물고기들의 움직임 출력
print("Using Comprehension:")
show_fish_movement_comprehension(fish_list)

print("\nUsing Iterator:")
show_fish_movement_iterator(fish_list)

# 출력결과
Using Comprehension:
Nemo is swimming at 3 m/s
Dory is swimming at 5 m/s
Marlin is swimming at 7 m/s
Bubbles is swimming at 2 m/s
Gill is swimming at 4 m/s

Using Iterator:
Nemo is swimming at 3 m/s
Dory is swimming at 5 m/s
Marlin is swimming at 7 m/s
Bubbles is swimming at 2 m/s
Gill is swimming at 4 m/s
```
---

1. Fish class 생성으로 fish_list 값들을 접근할 수 있도록 잘 만들어 주셧습니다.
2. 이후, 컴프리헨션/이터레이터/제너레이터로 출력하는 함수를 정의.
3. 컴프리헨션/이터레이터 출력결과 성공적입니다.
4. 다만 제너레이터는 좀 더 보안이 필요해 보입니다. 고생하셨습니다.

# 참고 링크 및 코드 개선 여부

```python
#
#
#
#
```
