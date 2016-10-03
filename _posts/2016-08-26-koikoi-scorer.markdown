---
layout: post
title: 코이코이 점수 계산기
category: Game making made easy
license: GPLv3
---
[koikoi-scorer @ GitHub][github]

코이코이는 일본 고스톱입니다. 
일본에선 국민 게임 마작도 있고, 고스톱보다 규칙도 단순하고 해서 많이 하진 않는답니다.

언젠가 고스톱 한번 만들어볼까 싶었는데, 더욱 쉬운 코이코이부터 만들어 봤습니다. 
점수 계산기뿐이지만요.

[github]: https://github.com/sidsryu/koikoi-scorer


## 기본 점수 규칙

일단 만들려면 기준이 되는 규칙이 있어야 하는데. 
다행히도 닌텐도가 오랫동안 화투를 만들어오고 있어서 [공식 설명서][nintendo]도 있더군요.
그 규칙을 사용했습니다.

[nintendo]: https://www.nintendo.co.jp/n09/hana-kabu_games/

### 점수 계산 

- 7점이상은 2배

### 시작패 즉시 승리

- 총통 - 손패에 같은월 4장 있을때 6점
- 들러붙기 - 손패에 같은월 2장씩 4쌍 있을때 6점

### 특수규칙

- 국화열끗(술잔)은 열끗과 껍데기 동시인정

### 족보

1. 오광 10점

    ![Pine Bright][11]![Cherry Bright][31]![Pampas Bright][81]![Paulownia Bright][121]![Willow Bright][111]

2. 사광 8점

    ![Pine Bright][11]![Cherry Bright][31]![Pampas Bright][81]![Paulownia Bright][121]

3. 삼광 5점

    ![Pine Bright][11]![Cherry Bright][31]![Pampas Bright][81]

4. 화견주 5점

    ![Cherry Bright][31]![Mums Kind][91]

5. 월견주 5점

    ![Pampas Bright][81]![Mums Kind][91]

6. 맹록접 5점

    ![Clover Kind][71]![Maple Kind][101]![Peony Kind][61]

7. 홍단 5점, 추가 띠마다 1점

    ![Pine Ribbon][12]![Plum Ribbon][22]![Cherry Ribbon][32]

8. 청단 5점, 추가 띠마다 1점

    ![Mums Ribbon][92]![Peony Ribbon][62]![Maple Ribbon][102]

9. 열끗 5장 1점, 추가 열끗마다 1점

    ![Iris Kind][51]![Wisteria Kind][41]![Plum Kind][21]![Peony Kind][61]![Mums Kind][91]

10. 띠 5장 1점, 추가 띠마다 1점

    ![Clover Ribbon][72]![Wisteria Ribbon][42]![Peony Ribbon][62]![Mums Ribbon][92]![Willow Ribbon][113]

11. 껍데기 10장 1점, 추가 껍데기마다 1점

    ![Wisteria Plain][43]![Plum Plain][24]![Pampas Plain][83]![Clover Plain][74]![Plum Plain][23]  
    ![Maple Plain][103]![Mums Plain][94]![Paulownia Plain][122]![Peony Plain][63]![Pine Plain][13]

12. 홍단/청단 중복 10점, 추가 띠마다 1점

    ![Pine Ribbon][12]![Plum Ribbon][22]![Cherry Ribbon][32]![Mums Ribbon][92]![Peony Ribbon][62]![Maple Ribbon][102]

[11]: {{ site.url }}/images/hanafuda/11.png "Pine Bright"
[12]: {{ site.url }}/images/hanafuda/12.png "Pine Ribbon"
[13]: {{ site.url }}/images/hanafuda/13.png "Pine Plain"
[14]: {{ site.url }}/images/hanafuda/14.png "Pine Plain"
[21]: {{ site.url }}/images/hanafuda/21.png "Plum Kind"
[22]: {{ site.url }}/images/hanafuda/22.png "Plum Ribbon"
[23]: {{ site.url }}/images/hanafuda/23.png "Plum Plain"
[24]: {{ site.url }}/images/hanafuda/24.png "Plum Plain"
[31]: {{ site.url }}/images/hanafuda/31.png "Cherry Bright" 
[32]: {{ site.url }}/images/hanafuda/32.png "Cherry Ribbon"
[33]: {{ site.url }}/images/hanafuda/33.png "Cherry Plain"
[34]: {{ site.url }}/images/hanafuda/34.png "Cherry Plain"
[41]: {{ site.url }}/images/hanafuda/41.png "Wisteria Kind"
[42]: {{ site.url }}/images/hanafuda/42.png "Wisteria Ribbon"
[43]: {{ site.url }}/images/hanafuda/43.png "Wisteria Plain"
[44]: {{ site.url }}/images/hanafuda/44.png "Wisteria Plain"
[51]: {{ site.url }}/images/hanafuda/51.png "Iris Kind"
[52]: {{ site.url }}/images/hanafuda/52.png "Iris Ribbon"
[53]: {{ site.url }}/images/hanafuda/53.png "Iris Plain"
[54]: {{ site.url }}/images/hanafuda/54.png "Iris Plain"
[61]: {{ site.url }}/images/hanafuda/61.png "Peony Kind"
[62]: {{ site.url }}/images/hanafuda/62.png "Peony Ribbon"
[63]: {{ site.url }}/images/hanafuda/63.png "Peony Plain"
[64]: {{ site.url }}/images/hanafuda/64.png "Peony Plain"
[71]: {{ site.url }}/images/hanafuda/71.png "Clover Kind"
[72]: {{ site.url }}/images/hanafuda/72.png "Clover Ribbon"
[73]: {{ site.url }}/images/hanafuda/73.png "Clover Plain"
[74]: {{ site.url }}/images/hanafuda/74.png "Clover Plain"
[81]: {{ site.url }}/images/hanafuda/81.png "Pampas Bright"
[82]: {{ site.url }}/images/hanafuda/82.png "Pampas Kind"
[83]: {{ site.url }}/images/hanafuda/83.png "Pampas Plain"
[84]: {{ site.url }}/images/hanafuda/84.png "Pampas Plain"
[91]: {{ site.url }}/images/hanafuda/91.png "Mums Kind"  
[92]: {{ site.url }}/images/hanafuda/92.png "Mums Ribbon" 
[93]: {{ site.url }}/images/hanafuda/93.png "Mums Plain"
[94]: {{ site.url }}/images/hanafuda/94.png "Mums Plain"
[101]: {{ site.url }}/images/hanafuda/101.png "Maple Kind"
[102]: {{ site.url }}/images/hanafuda/102.png "Maple Ribbon"
[103]: {{ site.url }}/images/hanafuda/103.png "Maple Plain"
[104]: {{ site.url }}/images/hanafuda/104.png "Maple Plan"
[111]: {{ site.url }}/images/hanafuda/111.png "Willow Bright"
[112]: {{ site.url }}/images/hanafuda/112.png "Willow Kind"
[113]: {{ site.url }}/images/hanafuda/113.png "Willow Bribbon"
[114]: {{ site.url }}/images/hanafuda/114.png "Willow Plain"
[121]: {{ site.url }}/images/hanafuda/121.png "Paulownia Bright"
[122]: {{ site.url }}/images/hanafuda/122.png "Paulownia Plain"
[123]: {{ site.url }}/images/hanafuda/123.png "Paulownia Plain"
[124]: {{ site.url }}/images/hanafuda/124.png "Paulownia Plain"


## 선택규칙

사실 닌텐도 규칙에는 다른 곳에서 잘 사용되지 않는 규칙이 있습니다. 
홍단이나 청단, 맹록접을 먹게 되면, 열끗이나 띠의 추가로 인한 점수 규칙이 달라지는데요.
다른 규칙에선 홍단/청단을 먹든 말든 띠는 5장부터 1점, 맹록접도 열끗 5장부터 1점씩 올라갑니다.

이런 자잘한 부분들은 선택 가능하도록 별도로 분리했습니다.
이후 추가될 닌텐도 이외의 규칙들은 모두 선택 규칙으로 포함될 겁니다.


## 주의

삽입된 화투 이미지는 GPLv3 라이센스입니다.
따라서 이 글도 동일 라이센스를 따릅니다.


<br>끝.
