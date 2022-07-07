# API를 이용한 네이버 기사 크롤링

## 간단한 과정
1. 네이버 개발자센터에서 API를 이용할 수 있도록 애플리케이션을 등록한다. 
2. 크롤링을 이용해서 csv파일 형태로 기사들을 불러온다. 

## 환경
Jupyter Notebook환경에서 진행

## 주의사항 
국문은 기본적으로 제공해주는 불용어 리스트가 없으므로 직접 제작
```
stopWords = ['의한', '과', '와', '관한', '에서의', '을', '위한', '와', '의', '통한', '따른', '이', '있', '하', '것', '들', '그', '되', '수', '이', '보', '않', '없', '나', '사람', '주', '아니', '등', '같','과', '간의', '를', '의' '우리', '때', '년', '가', '한', '지', '오', '말', '일', '그렇', '위하', '및', '에', '뒤진', '대한']
lemma = WordNetLemmatizer()
```

또는 Okt라이브러리 이용
```
nlp = Okt()
words_N = nlp.nouns(str(words2)) # 리스트에서는 명사 추출이 불가능하기 떄문에 str로 바꿔줌
words_N
```

## 결과물 
![image](https://user-images.githubusercontent.com/48540791/177828334-2bc17fbb-1dbe-4c87-9d41-f607803cef90.png)

