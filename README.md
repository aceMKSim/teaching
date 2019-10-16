# 참고자료

## R for Data Science (by Hadley Wickam)

+ 웹북 <https://r4ds.had.co.nz/> (크롬에서 우클릭 -> 번역기능 사용)
+ 영문판 <https://www.amazon.com/Data-Science-Transform-Visualize-Model/dp/1491910399/ref=sr_1_3?keywords=r+for+data+science&qid=1553390913&s=gateway&sr=8-3>
+ 번역서 <http://book.interpark.com/product/BookDisplay.do?_method=detail&sc.shopNo=0000400000&sc.prdNo=298756807>

## RStudio 단축키 

+ Ctrl + Alt + I: Insert a r chunk in rmd
+ Ctrl + Shift + 1: Editor를 전체화면으로
+ Ctrl + Shift + 2: Console을 전체화면으로
+ Ctrl + Shift + C: 선택된 코드 부분을 주석으로
+ Ctrl + Shift + K: Knit the document

# 9월 27일

## Purpose

1. 그동안 진행한 데이터 보내드립니다. 혹시 개선할 부분이 있으면 의견 주시면 좋겠습니다.
2. 향후 두달간 진행할 내용에 대한 가이드를 받고 싶습니다. 
    + 그동안 데이터 전처리와 기본 그래프 작업을 했으나, 막상 주제를 정해서 진행하려니 막막하네요. --; 
    + 기존에 진행했던 데이터와 형식은 거의 같은데요, 전처리 이후에 어디서부터 해야할지 감이 오지 않습니다.
    + 우선은 기본이 되는 주문데이타/최소한의 회원데이타만 가지고 진행하고자 하나,
    + 깊이있는 내부 데이터도 많이 있으니, 혹시 필요한 항목이 있으면 말씀주세요.
    + 이 과제를 수행하기 위한 분석시나리오와 필요한 함수에 대한 가이드를 받고 싶습니다. 
    + (샘플 데이터 첨부합니다.vip_order_sample.csv)

## <주제> 우수구매고객의 구매패턴을 분석한다.

+ 공통 : 1년간 구매데이타 기준 / vip,vvip고객에 한함

1. 자주 구매하는 카테고리가 무엇인가?
    + 예시. 재구매주기 분석 (2D/3D의 재구매횟수를 통해, 어떤 카테고리가 재구매 경쟁력이 있는가?)

2. 교차구매(1D, 2D)는 어떤 상품이 있는가?

3. 왜 인터파크를 이용할까?
    + 예시. 쿠폰이나 포인트가 많은가? (아이포인트, 카드 행사, 쿠폰 등등)

