뉴스 헤드라인 분류
===
# Overview
* 뉴스 헤드라인을 입력받아 7가지 Topic 중 하나로 분류합니다. (정치,사회,생활문화,IT과학,스포츠,경제,세계)
* 사용한 모델 : klue의 [Klue-tc (a.k.a. ynat)](https://github.com/KLUE-benchmark/KLUE) data set으로 [bert-base-multilingual-cased](https://huggingface.co/bert-base-multilingual-cased) 모델을 fine-tuning하였습니다.

## How to use
----
News Headline Textbox에 분류하고 싶은 Headline을 입력합니다.

## How to make
----
1. [Klue-tc (a.k.a. ynat)](https://github.com/KLUE-benchmark/KLUE) data set을 준비했습니다.

2. data set을 [bert-base-multilingual-cased](https://huggingface.co/bert-base-multilingual-cased) 모델에 fine-tuning 하였습니다.

## Post Parameter
----
```
headline="뉴스 헤드라인"

```

## output format
----
```
{
    "0": [
        {
            "label": "IT과학",
            "score": 점수
        },
        {
            "label": "경제",
            "score": 점수
        },
        {
            "label": "사회",
            "score": 점수
        },
        {
            "label": "생활문화",
            "score": 점수
        },
        {
            "label": "세계",
            "score": 점수
        },
        {
            "label": "스포츠",
            "score": 점수
        },
        {
            "label": "정치",
            "score": 점수
        }
    ]
}
```

## API Predict Test
----
```
curl -L -X POST 'https://main-klue-tc-bert-base-multilingual-cased-rjdm1324.endpoint.ainize.ai/generate' -F 'headline="손흥민 첼시전 시즌 5호골.. 득점 2위 도약"'

{
    "0": [
        {
            "label": "IT과학",
            "score": 0.00038005816168151796
        },
        {
            "label": "경제",
            "score": 0.00018529930093791336
        },
        {
            "label": "사회",
            "score": 0.00023768933897372335
        },
        {
            "label": "생활문화",
            "score": 0.00036717255716212094
        },
        {
            "label": "세계",
            "score": 0.0004559744265861809
        },
        {
            "label": "스포츠",
            "score": 0.9982724189758301
        },
        {
            "label": "정치",
            "score": 0.00010135045886272565
        }
    ]
}

```


## Healthy Check
----
Using curl in the terminal:

```

$ curl --request GET https://main-klue-tc-bert-base-multilingual-cased-rjdm1324.endpoint.ainize.ai/healthz  
{
    Health
}

```
