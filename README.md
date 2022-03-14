# Netflix-EDA with Three Other Ott Services
- Basic EDA for Netflix, Disney+, Amazon Prime, HULU
- EDA and correlation analysis using Netflix Data

### 참고자료
1. [🔴Netflix Visualizations, Recommendation, EDA🍿](https://www.kaggle.com/niharika41298/netflix-visualizations-recommendation-eda)
2. [Netflix Data Visualization - Target Ages](https://www.kaggle.com/joshuaswords/netflix-data-visualization)
3. [IMDb Top 1000 dataset](https://www.kaggle.com/hrishabhtiwari/imdb-top-1000-movies-dataset)

### Dataset
1. [Amazon Prime Video Movies and TV Shows](https://www.kaggle.com/shivamb/amazon-prime-movies-and-tv-shows)
2. [Disney+ Movies and TV Shows](https://www.kaggle.com/shivamb/disney-movies-and-tv-shows)
3. [Netflix Prime Video Movies and TV Shows](https://www.kaggle.com/shivamb/netflix-shows)
4. [Hulu Movies and TV Shows](https://www.kaggle.com/shivamb/hulu-movies-and-tv-shows)
5. [Netflix Revenue from 2018 to 2020](https://www.kaggle.com/pariaagharabi/netflix2020)
6. [IMDB Top 10](https://www.kaggle.com/omarhanyy/imdb-top-1000)
7. [Latest Netflix data with 26+ joined attributes](https://www.kaggle.com/ashishgup/netflix-rotten-tomatoes-metacritic-imdb)

### 1. 넷플릭스, 디즈니+, 아마존 프라임, HULU 데이터 비교

각 장르가 타겟으로 삼는 시청 연령의 분포 분석

- 넷플릭스

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2015.png)

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2016.png)

- 디즈니 +

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2017.png)

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2018.png)

- 아마존 프라임

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2019.png)

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2020.png)

- HULU

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2021.png)

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2022.png)

- 4개의 ott 서비스를 분석한 결과, 주된 장르와 시청 대상 연령에서 차이를 보였다. 특히 가족을 중심으로 한 컨텐츠를 제공하는 디즈니의 경우 성인 연령을 대상으로 한 컨텐츠는 아예 존재하지 않았다.

### 2. 지역과 분기별 수익성의 상관관계

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2023.png)

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2024.png)

지역과 분기별 수익, 컨텐츠 사이 상관관계를 살펴봤을 때 분기별 공개된 컨텐츠와 지역별 수익 사이의 상관관계는 비교적 약한 것으로 드러났다. 

### 3. 넷플릭스의 분기별 수익성과 장르, 시청 대상 연령 사이의 상관관계

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2025.png)

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2026.png)

- 넷플릭스에서 분기별로 공개된 장르의 수와 분기 별 수익성에 관해 살펴본 결과는 다음과 같았다.

```
약한 상관성:
['Reality TV', 'Cult Movies', "Kids' TV", 'Classic Movies', 'Teen TV Shows', 'Sports Movies', 'Spanish-Language TV Shows', 'Thrillers', 'Science & Nature TV', 'TV Thrillers', 'Romantic TV Shows']

상관성:
['Children & Family Movies', 'TV Horror', 'Crime TV Shows', 'Korean TV Shows', 'Anime Features', 'TV Dramas', 'Anime Series', 'TV Sci-Fi & Fantasy', 'Romantic Movies', 'Comedies', 'International TV Shows']

강한 상관성:
['TV Action & Adventure']
```

- 특히 Kid’s TV의 경우 시청 연령과 수익성 간의 관계를 살펴보았을 때도 어느 정도 상관관계를 보였다. 즉, 두 상관관계에서 모두 의미 있는 결과를 보였기 때문에 공략할 만한 시장이라고 생각된다.
- 다만 단순한 컨텐츠의 수와 수익성의 상관관계이기 때문에, 특정 장르가 업로드 되어 수익성이 증가했다는 인과관계를 설명하기 위해선 다른 근거를 보충할 필요성이 있다.

### 4. 넷플릭스의 분기별 수익성과 장르의 평균 별점 사이 상관관계

- 넷플릭스의 수익성과 높은 상관관계를 보이는 경우, 해당 장르를 좋은 컨텐츠라고 판단해 많은 사람이 시청했고, 그런 경과가 수익성에 영향을 미치지 않았을까 생각했다. 따라서 수익성에 영향력이 있는 컨텐츠일 경우 IMDB에서의 평점이 높을 것이라고 생각했고, 그렇다면 평점과 수익성 사이의 관계도 파악할 수 있을 것이라고 생각했다. 이러한 전제를 바탕으로 분기별 공개된 장르의 평균 별점을 구한 후, 분기별 수익성과의 상관관계를 파악했다.

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2027.png)

- 하지만 분기별 공개된 장르의 평균 별점을 구해본 결과, 위와 같이 전반적으로 평점이 크게 높지 않은 것으로 드러났다. 다만 해당 데이터는 IMDB Top 1000 데이터셋과 대회에서 주어진 데이터 사이의 교집합을 이용한 것으로, 2000개라는 적은 수이기 때문에 이를 고려해야할 것이다.

![Untitled](https://github.com/Yeyeong99/Aiffel_Datathon/blob/main/README%20images/Untitled%2028.png)

- 넷플릭스의 분기별 수익성과의 상관관계가 높게 측정된 장르를 선별해, 각 장르의 평균 별점과 분기별 수익성의 상관관계를 파악했다. 그 결과, 장르별 별점과 수익성 사이의 관계는 높지 않다는 사실을 확인할 수 있었다.
