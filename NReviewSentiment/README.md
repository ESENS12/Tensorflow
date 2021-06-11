# NBlog Sentiment
 - NBlog 리뷰 감정분류

# 데이터 수집 및 전처리 계획
-> 네이버 영수증 리뷰 데이터 무작위 수집 (10만건)
-> 분류 (별점 + tokenizer 된 리뷰 문구 분류 해서 label화 한다 e.g) label =  0: 부정, 1:긍정 ,  document = 가격 대비 양은 별로.. 
-> 분류 방식은 고민해봐야함, 해당 리뷰어의 평균 리뷰 점수 보다 높거나, 가게 평균 점수보다 높거나, 단순히 수치화해서 3점 이상이던가 (5점만점) ..  여러가지 방식을 고민해봐야함

# 모델링
-> 모델은 GRU, BiLSTM 으로 먼저 테스트 해볼 계획

# 프로젝트 구조
-> Crawler,  Leaner, Classifier 구조로 분류 해서 세분화한다. 


# EX
기존에 SearchNBlogWithoutAds 크롤링을 너무 난잡하게 처리했기때문에 최대한 간결하게..
다만 문제는 키워드 인데... 데이터 평준화를 위해서 특정 키워드, 가게의 최대 수집 데이터값을 정해놓고 해야겠다

크롤링 전략
1. 구버전 네이버 지도로 restaurant id 를 리스팅 후
2. place 방문자 리뷰 요청 후 데이터 수집 


# References
 - BiLSTM (https://wikidocs.net/94748)
 - BiLSTM (https://paperswithcode.com/method/bilstm)
