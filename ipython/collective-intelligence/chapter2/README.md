
#협업 필터링

협업 필터링 알고리즘은 큰 무리의 사람들을 검색해서 여러분과 유사한 취향을 가진 작은 집합을 발견하는 방식으로 동작한다. <br>
그것은 사람들이 좋아할 만한 여러 것들을 보고 결합하여 추천 목록을 생성한다. <br>
어떤 사람들이 유사한지 결정하거나 그들의 선택을 결합하여 목록을 만드는 여러가지 방법이 있는데 이 장에서는 몇몇 가지 방법만 소개 

선호 정보를 수집 위와 같이 자료형에 데이터를 추가 한다. 


    critics={'Lisa Rose': {'Lady in the Water': 2.5, 'Snakes on a Plane': 3.5,
     'Just My Luck': 3.0, 'Superman Returns': 3.5, 'You, Me and Dupree': 2.5, 
     'The Night Listener': 3.0},
    'Gene Seymour': {'Lady in the Water': 3.0, 'Snakes on a Plane': 3.5, 
     'Just My Luck': 1.5, 'Superman Returns': 5.0, 'The Night Listener': 3.0, 
     'You, Me and Dupree': 3.5}, 
    'Michael Phillips': {'Lady in the Water': 2.5, 'Snakes on a Plane': 3.0,
     'Superman Returns': 3.5, 'The Night Listener': 4.0},
    'Claudia Puig': {'Snakes on a Plane': 3.5, 'Just My Luck': 3.0,
     'The Night Listener': 4.5, 'Superman Returns': 4.0, 
     'You, Me and Dupree': 2.5},
    'Mick LaSalle': {'Lady in the Water': 3.0, 'Snakes on a Plane': 4.0, 
     'Just My Luck': 2.0, 'Superman Returns': 3.0, 'The Night Listener': 3.0,
     'You, Me and Dupree': 2.0}, 
    'Jack Matthews': {'Lady in the Water': 3.0, 'Snakes on a Plane': 4.0,
     'The Night Listener': 3.0, 'Superman Returns': 5.0, 'You, Me and Dupree': 3.5},
    'Toby': {'Snakes on a Plane':4.5,'You, Me and Dupree':1.0,'Superman Returns':4.0}}

critics라는 딕션어리형 자료형에 영화에 대한 정보를 입력한다.<br>
이와 같은 정보는 목적에 따라 다른 선호도 값을 가진다. <br>
공연 티켓의 경우 <br>
구매 : 1, 비 구매 : 0 <br><br>
온라인 쇼핑몰의 경우 <br>
구매 : 2 , 찾음 : 1 , 비구매 <br><br>
사이트 추천의 경우 <br>
좋음 : 1 , 모름 : 0 , 싫음 -1<br> <br>
과 같은 기준으로 선호도를 표시 한다. 

<img src=./img/prefer_table.png>

critics 딕션어리에 값이 제대로 있는지 확인


    critics['Lisa Rose']['Lady in the Water']




    2.5




    critics['Toby']['Snakes on a Plane']=4.5
    critics['Toby']




    {'Snakes on a Plane': 4.5, 'Superman Returns': 4.0, 'You, Me and Dupree': 1.0}



#유사 사용자 찾기

사람들이 선호하는 정보를 수집 했다면<br>
다음 단계는 유사한 사용자를 찾는것이다.<br>
유사한 사용자를 찾는 방법은 <br>
유클리디안 거리 점수와 피어슨 상관 점수가 있다. 

<img src=./img/eucdlian-distance.png>


    
