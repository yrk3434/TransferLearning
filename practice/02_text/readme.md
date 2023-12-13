# 텍스트 데이터 전이학습

- 텍스트 데이터는 다음 두 가지 사전학습 결과가 필요
    1. 사전학습된 단어 임베딩
    2. 사전학습된 task(ex. 분류) 수행 모델

- 실습파일 설명(practice_02_01_text.ipynb)
    - IMDB 영화리뷰 감성분류(부정, 긍정)
    - 사전학습 출처
        1. 단어 임베딩: GloVe(외부 임베딩 완료 파일)
        2. 분류 모델
            - amazon 리뷰 기반 분류 모델 구축(HandsOn-03_Movie_Review.ipynb) <br/>
            (a) model>cnn_document_model.py 기반 딥러닝 레이어 구조 구축 <br/>
            (b) base model - CNN 1D 텍스트 분류기 <br/> 참고. [11-02 자연어 처리를 위한 1D CNN(1D Convolutional Neural Networks)](https://wikidocs.net/80437) <br/>
            단, amazon 리뷰 전처리 시 사전학습된 임베딩(GloVe) 사용 
    - 전이학습 순서:
        -  영화리뷰 Raw Data 전처리(nltk 모듈로 시퀀스화) -> (1) GloVe 기반 워드 임베딩 -> (2) amazon 분류 모델