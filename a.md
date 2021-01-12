전체계획을 6월까지 잡고, 4월까지 초판이 나오며 홍보팀은 6월 기준으로 미리 홍보.
- [[라이선스가격정책]]

## 2021/01

- 사용자메뉴얼 개선
    - [[사용자메뉴얼 현행화]]
    - [[tutorial문서작성]]
    - [[사용자메뉴얼을 화면요소들과 연결]]
- [[AWS생태계와 연동하기]]
    - [[S3 파일을 주고 받을 수 있는 형태로 개선]]
- [[AccuTuning Client 만들기]]
- [[실험별 파일시스템 크기 계산]]
- [[다국어 키워드 추출을 위한 전처리 및 KeyBERT 추가]]
    - Language Identifier
    - 언어별 Tokenizer
    - KeyBert 키워드 추출 알고리즘 추가
- [[fewshot 수행 후 모델 생성]]
- [[AutoDL과 통합과제]]
- [[AUTO관점에서 WORKFLOW재정비]] - accu workflow에 들어가는 내용에서 정리해야 함.ㅋ

## 2021/02

- [[AWS생태계와 연동하기]]
    - [[EKS 환경에서 구동할 수 있는 형태로 개선]]
- [[Domain specific preprocessor]] - 화학식관련
- [[Bulk Prediction을 편하게 할 수 있도록 정비]]
- [[AutoSampler개발]]
    - Sampling for Large-scale AutoML
    - Probability Sampling : Simple random, Systematic, Stratified, Cluster, Reservoir
    - Non-Probability Sampling : Convenience, Quota, Judgement, Snowball
    - Aspects to consider : Sample Goal, Population, Selection Criteria, Sample Size
    - 필요하다면 반지도, 지도학습 방식의 sampling 방법도 려


## 2021/03

- [[사용성개선]]
    - [[CONTAINER수행을 QUEUE방식으로 전환]] - 사용성 측면에서.
    - 현재 labeler가 수행중인 경우 동작여부가 잘 드러나지 않는다.
    - 컨테이너 사용개수, 누가 어떻게 쓰고 있는지에 대한 표시
    - GPU 사용 여부 및 메모리 모니터링
- [[Azure생태계에 들어가기]]
- [[AutoCluster 재정비]]
    - Clustering algorithm 추가
    - autoCluster 목적함수 재정의
    - AutoCluster dimension reduction 디버깅


## 2021/04

- [[Few-shot labeler재정비]]
    - Add Active-learning methods
    - Model 추가 및 hpo grid search - searching space 확장
    - Transfer-Learning
- ensemble(voting) 로직 개선필요. 상위권에 동일한 estimator를 섞지 말고 가급적 다양한 알고리즘을 섞어서 수행할 수 있도록. -> 어떻게 하는게 좋을까부터 고민 필요. 일단 상위에 20개가 모두 같은 알고리즘이더라도 voting을 만들기 때문에 이 경우는 별로 효력이 없다.
- 시계열데이터 지원
    - 시계열 전처리 기능 보강 (window, walk-forward/blocking walk-forward cross validation, noise reduction - moving average, wavelet transform...)
    - 시계열 모델링 기능 추가 (Regression - prophet, ARIMA ...)

## 2021/05

- [[TextAugmenter개발]]
    - Round-trip-translation 방법 추가 (Transformer기반)
    - MixText Bert Layer 활용한 데이터 보완
- [[Label Embedding 개발]]
    - text tag이후 tag 를 어떻게 automl 에 전달할지에 대한 고민
    - WCEs
    - LEAM

## 2021/06

- [[Labeler Benchmark]]
- [[Labeler 통합테스트]]


## Bugs

- #BUG celery monitoring (구동중인지 확인해봐야 함.) 가끔 안 뜨는 경우가 있는데 왜 그런지 확인도 해봤으면 좋겠음.
- #BUG [[JWT 사용자토큰 연장하는 부분]]
- #BUG [[Django admin과 연계시에 JWT가 충돌나는 부분]]
- #BUG labeler가 영문에 대해서는 현재 잘 동작하지 않고 있음
- #BUG 수행이 종료된 컨테이너들이 일부는 삭제되고 일부는 삭제되지 않음
- #BUG fewshot수행후에는 metric, plot이 생성되지 않음.
- #BUG stop버튼의 경우 modeler 수행만 중지할 수 있도록.

