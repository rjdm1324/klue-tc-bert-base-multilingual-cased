## News Headline classification
----
뉴스 헤드라인을 입력받아 7가지 Topic 중 하나로 분류합니다.
(정치,사회,생활문화,IT과학,스포츠,경제,세계)

## How to use
----
News Headline Textbox에 분류하고 싶은 Headline을 입력합니다.

## How to make
----
1. [Klue-tc (a.k.a. ynat)](https://github.com/KLUE-benchmark/KLUE) data set을 준비했습니다.

2. data set을 bert-base-multilingual-cased 모델에 fine-tuning 하였습니다.

## Healthy Check
----
Using curl in the terminal:

'''
$ curl --request GET https://main-klue-tc-bert-base-multilingual-cased-rjdm1324.endpoint.ainize.ai/healthz  

'''
