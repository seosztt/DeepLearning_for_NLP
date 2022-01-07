# 다양한 단어의 표현 방법

단어의 표현 방법은 크게 국소 표현(Local Representation) 방법과 분산 표현(Distributed Representation) 방법으로 나뉩니다. 국소 표현 방법은 해당 단어 그 자체만 보고, 특정값을 맵핑하여 단어를 표현하는 방법이며, **분산 표현 방법은 그 단어를 표현하고자 주변을 참고하여 단어를 표현하는 방법**입니다.

두 방법의 차이는 국소 표현 방법은 단어의 의미, 뉘앙스를 표현할 수 없지만, 분산 표현 방법은 단어의 뉘앙스를 표현할 수 있게 됩니다.

국소 표현 방법(Local Representation)을 이산 표현(Discrete Representation)이라고도 하며, 분산 표현(Distributed Representation)을 연속 표현(Continuous Represnetation)이라고도 합니다.

구글의 연구원 토마스 미코로브(Tomas Mikolov)는 2016년에 한 발표에서 잠재 의미 분석(LSA)이나 잠재 디리클레 할당(LDA)과 같은 방법들은 단어의 의미를 표현할 수 있다는 점에서 연속 표현(Continuous Represnetation)이지만, 엄밀히 말해서 다른 접근의 방법론을 사용하고 있는 워드투벡터(Word2vec)와 같은 분산 표현(Distributed Representation)은 아닌 것으로 분류하여 연속 표현을 분산 표현을 포괄하고 있는 더 큰 개념으로 설명하기도 했습니다.



![](https://wikidocs.net/images/page/31767/wordrepresentation.PNG)



BoW의 확장인 DTM(또는 TDM)

빈도수 기반 단어 표현에 단어의 중요도에 따른 가중치를 줄 수 있는 TF-IDF

워드 임베딩 챕터에서는 연속 표현(Continuous Representation)에 속하면서, 예측(prediction)을 기반으로 단어의 뉘앙스를 표현하는 워드투벡터(Word2Vec)와 그의 확장인 패스트텍스트(FastText)를 학습하고, 예측과 카운트라는 두 가지 방법이 모두 사용된 글로브(GloVe)에 대해서 학습합니다.



# Bag of Words(BoW)

Bag of Words는 국소 표현에(Local Representation)에 속하며, 단어의 빈도수를 카운트(Count)하여 단어를 수치화하는 단어 표현 방법입니다. Bag of Words란 단어들의 순서는 전혀 고려하지 않고, 단어들의 출현 빈도(frequency)에만 집중하는 텍스트 데이터의 수치화 표현 방법입니다.

BoW는 각 단어가 등장한 횟수를 수치화하는 텍스트 표현 방법이므로 주로 어떤 단어가 얼마나 등장했는지를 기준으로 문서가 어떤 성격의 문서인지를 판단하는 작업에 쓰입니다. 즉, 분류 문제나 여러 문서 간의 유사도를 구하는 문제에 주로 쓰입니다.