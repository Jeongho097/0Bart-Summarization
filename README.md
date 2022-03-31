# Bart-Summarization

개인프로젝트
1. 투자에 있어서 뉴스 기사를 읽는 시간을 줄이고자 뉴스 기사에 대한 요약문을 생성
2. 투자에 대한 간단한 판단을 위해 뉴스 기사 요약문을 감성 분석을 통해 긍정/부정 분류


# 1. 기업 뉴스 기사 크롤링
- 다음 증권의 뉴스를 이용함
- 원하는 기업의 최신 뉴스 기사를 크롤링 하기 위해 크롤링 시점의 날짜부터 원하는 날짜까지 설정해 크롤링 함

# 2. Bart를 이용한 기업 뉴스 기사 요약
- Bart 사전 학습 모델 'gogamza/kobart-base-v1'을 사용
- 데이터는 AI Hub의 문서요약 텍스트 데이터 셋 사용 
    - https://aihub.or.kr/aidata/8054 
    - 데이터 중 'media_sub_type'이 '경제지인 데이터 65,865개의 데이터를 train data로 사용

# 3. 'klue/bert-base'와 "snunlp/KR-FinBert" 성능 비교
- 뉴스 기사 요약문을 BERT 사전학습모델 'klue/bert-base'또는 "snunlp/KR-FinBert"을 이용해 긍정/부정 분류
    - "snunlp/KR-FinBert"는  KR-BERT_MEDIUM에서 72개의 언론사의 기업 관련 경제 뉴스 기사, 16개의 증권사 애널리스트 보고서가 확장됨([KR-Finbert Github](https://github.com/snunlp/KR-FinBert))
