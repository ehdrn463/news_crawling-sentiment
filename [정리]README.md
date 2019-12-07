## 네이버 뉴스 댓글정책 변화 [순공감순] -> [최신순] <br> 이에 따른 침묵의 나선 이론 효과 변화 분석
> 연구방법: 네이버 뉴스 댓글 크롤링, 감성분석

<br>

#### 연구 과정1 [Python을 이용한 감성분석]

![](images/news_crawling1.jfif)
![](images/news_crawling2.jfif)
![](images/news_crawling3.jfif)
![](images/news_crawling4.jfif)


#### 연구 과정2 [코더 간 신뢰도를 이용한 감성분석] 및 결과
```sh
   댓글 배열 방식에 따라 침묵의 나선 효과와 여론왜곡현상이 변화하는지 알아보기 위해 한국갤럽의 여론조사를 활용했다. 2018년 한국갤럽의 최저임금에 대한 여론조사 결과는 긍정 41%, 중립 13%, 부정 41%였고, 2019년은 긍정 24%, 중립 15%, 부정 52%였다. 최저임금 인상에 대해서 2018년보다 2019년이 다소 부정적인 것으로 드러났다. 2018년(공감순) 뉴스 댓글은 총 951개로 ‘긍정 16.2%(155개), 중립 10.7%(102개), 부정 72.9%(694개)’으로 분류되었다. 2019년(최신순)은 총 835개이며 ‘긍정 9.2%(77개), 중립 15%(47개), 부정 52%(717개)’이란 결과가 나왔다.      

    연도별 여론조사와 댓글의미 분포 차이를 ‘적합도검정(범주형 자료) - 카이제곱’로 분석했다. 2018년 여론조사 결과를 기댓값으로 두고, 2018년(공감순) 댓글의미 분포를 관찰도수로 설정했다. 2019년도 같은 방식으로 진행했다. 그 결과 각각 검정통계량이 383.25, 309가 나왔다. 유의확률 0.05에 대한 카이제곱 (df=2)의 임계값은 7.81로 18년과 19년 모두 댓글의미 분포는 여론조사 분포를 따르지 않는 것으로 드러났다.

   2018년의 검정통계량이 383.25, 2019년의 검정통계량은 309이 나왔다. 2019년 검정통계량값이 더 낮다는 것은 관찰도수인 여론조사와 관찰도수인 댓글의미 분포가 2018년보다 더 비슷하게 나왔다는 것이다. 즉 2018년 10월의 네이버 기사 댓글 노출 정책이 변화하면서, 침묵의 나선이론 효과가 약해졌고 여론왜곡현상이 약해졌다는 것을 의미한다.
```

#### 핵심 모듈
```sh
#크롤링 관련-
from bs4 import BeautifulSoup
from selenium import webdriver
from selenium.common import exceptions
from collections import defaultdict

#감성분석 
from konlpy.tag import Kkma
from konlpy.tag import Hannanum
from konlpy.utils import pprint
import nltk
from nltk.sentiment.vader import SentimentIntensityAnalyzer as Vade
```
