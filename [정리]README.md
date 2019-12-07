## 네이버 뉴스 댓글정책 변화 [순공감순] -> [최신순] <br> 이에 따른 침묵의 나선 이론 효과 변화 분석
> 연구방법: 네이버 뉴스 댓글 크롤링, 감성분석

<br>
#### 연구 과정 및 결과
![](images/news_crawling1.jfif)
![](images/news_crawling2.jfif)
![](images/news_crawling3.jfif)
![](images/news_crawling4.jfif)


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
