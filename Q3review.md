
# PRT(PeerReviewTemplate)

각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.

- [x] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [x] 주석을 보고 작성자의 코드가 이해되었나요?
- [x] 코드가 에러를 유발할 가능성이 있나요?
- [x] 코드 작성자가 코드를 제대로 이해하고 작성했나요? (직접 인터뷰해보기)
- [x] 코드가 간결한가요?

---

import string

file_line = []
with open('/content/sample_data/06TheAvengers.txt', 'r') as file:
  for line in file:
    temp = line.strip('\n').casefold()
    temp = temp.translate(str.maketrans('', '', string.punctuation))
    temp = ''.join(filter(lambda x: x not in string.punctuation, temp))
    
    file_line.append(temp)
file_line
### 파일 출력이 잘 되었습니다.

string.punctuation
'!"#$%&\'()*+,-./:;<=>?@[\\]^_`{|}~'
###문자이외에 기호제거.

baglist = []
for line in file_line:
  words = line.split()
  for i in range(len(words) - 1):
    gram_temp = (words[i], words[i + 1])
    baglist.append(gram_temp)
baglist
### 2-gram으로 리스트 작성.

from collections import Counter
countdict = Counter(baglist)
sorted(countdict.items(), key=lambda x: x[1], reverse=True) 
### 텍스트와 대조하여 빈도수 측정. 
   
   - Code 에 대한 리뷰어의 Comment 를 남겨주세요

1. Quest를 잘 해결한 모범답안 같습니다.
2. 코딩도 간결하고 이해하기 좋게 잘 짜여졌습니다.
---

# 참고 링크 및 코드 개선 여부
