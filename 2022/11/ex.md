# [W3] 보고서

생성일: 2022년 10월 1일 오전 10:10

### 🪜목차

## 1. 프로젝트의 배경과 목적

---

### 1.1. 배경

  데이터리안은 데이터 분석과 관련된 강의를 제작하고 판매하는 온라인 강의 플랫폼입니다. 

  **현재 데이터리안이 판매중인 핵심 강의 서비스는 아래와 같습니다:**

- 백문이불여일타 SQL 캠프 입문반
- 백문이불여일타 SQL 캠프 심화반

  2022년 2월, 첫 SQL 캠프를 성공적으로 진행한 데이터리안은 현재 고민에 빠졌습니다. 

  강의 홍보를 위해 여러 채널에 콘텐츠를 추가로 업로드하고 유료 광고에 더 큰 비용을 투자했지만, 2월 SQL 캠프 참여자 수가 목푯값에 도달하지 못했기 때문입니다. 또한, 늘어난 홍보 채널로 인해 관리에 어려움을 겪고 있습니다.

### 1.2. 분석 목적

- 참고 | 퍼널 분석이란?
    
    <aside>
    ✅ **퍼널 분석이란?**
       퍼널 분석은 고객들이 우리가 설계한 유저 경험 루트를 따라 잘 도착하고 있는지 확인해보기 위해 최초 유입부터 최종 목적지까지 단계를 나누어 살펴보는 분석 기법입니다. 얼마나 많은 사람들이 최종 단계까지 도착하는지, 또 어디에서 많이 이탈하는지 확인할 수 있습니다.
    
       퍼널 분석을 통해 사용자의 속성이나 동작에 따라 변환률이 어떻게 달라지는지를 파악할 수 있습니다. 따라서 **어떤 사용자 유형이 변환 가능성이 높은지**, **중도 이탈 원인이 무엇인지**, **중도 이탈 사용자들이 어떤 행동을 하는지** 파악하여 퍼널의 성능을 향상시킬 수 있을 뿐 아니라 중요한 퍼널과 사용자 이동의 잠재적 결함을 발견할 수 있게 됩니다.
    
    </aside>
    

<aside>
❓ 어떻게 하면 다음 달 SQL 캠프 참여자 수를 늘릴 수 있을까?
늘어난 홍보 채널을 어떻게 하면 효율적으로 관리할 수 있을까?

</aside>

  `**데이터리안 웹사이트 GA 로그 데이터**`를 **퍼널 분석(Funnel Analysis)** 방법을 통해 위 질문에 대한 답을 도출해보려고 합니다. 

## 2. 퍼널 정의와 가설 수립

---

### 2.1. 퍼널 정의

   데이터리안이 고객에게 유도하고 싶은 최종 액션은 ‘SQL 캠프 수강을 위한 결제’입니다. 하지만 데이터리안 웹사이트 내에서 결제 기능을 제공하고 있지 않기 때문에 ‘**신청하기 버튼 클릭’**을 **최종 퍼널로 정의**합니다. 

   따라서 최종적인 퍼널의 정의는 아래와 같습니다. 

![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled.png)

<aside>
🪜 **Funnel Step**:

- step 1 : 광고 혹은 특정 url을 통해 입문반 혹은 실전반 페이지로 유입
- step 2 : 정보 탐색을 위해 페이지 내 스크롤
- step 3 : 페이지 하단에 위치한 SQL 캠프 신청하기 버튼을 클릭
</aside>

### 1.3. 가설 수립

- 참고 | 자세한 가설 설정 과정 흐름
    
    [1.3. 가설 설정 ](https://www.notion.so/1-3-2743f35919ff4201bca6c1f683daada9)
    

<aside>
🧮 **현재 데이터리안의 문제 상황을 정리하자면 아래와 같습니다:**

![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%201.png)

</aside>

  2022년 1월 기준, 데이터리안의 홍보 채널(source)은 총 13개이며, 그중 SQL 캠프 페이지로 유입되는 채널은 9개입니다. 적은 자원으로 효율적인 운영이 이루어져야 하는 사업 초기 단계에서 많은 채널을 한꺼번에 관리하는 것은 리소스의 낭비로 이어집니다. 이에 데이터리안의 현 문제 상황의 주된 원인을 홍보 채널 증가로 인해 흩어진 리소스라 정의합니다. 

  각 퍼널 단계별 전환율이 높은 유저들이 어떤 홍보 채널을 통해 SQL 캠프 페이지로 유입되었는지 파악하면, 해당 채널에 더 많은 리소스를 집중하여 최종적으로 SQL 캠프 참여자 수를 증가시킬 수 있을 것입니다. 

<aside>
📄 **가설 : 전환율 성과가 좋은 홍보 채널에 리소스를 집중 시키면 SQL 캠프 참여자 수가 증가할 것이다. 

검증 방법 : UTM 파라미터를 기준으로 유입 유저의 특징을 세분화 하여 분석을 진행합니다.**

- 각 홍보 채널(`**source**`)로 유입 된 유저들의 양상이 다를 것이다.
- 각 홍보 매체(`**campaign**`)으로 유입 된 유저들의 양상이 다를 것이다.
</aside>

## 3. 결과

---

### 3.1. 입문반 퍼널 분석

- *query*
    
    ```sql
    -- 입문반 퍼널 
    WITH pv AS (SELECT ga_session_id, user_pseudo_id 
                        ,event_timestamp_kst AS pv_at
                  FROM ga 
                  WHERE event_name='page_view'
                  AND page_title='백문이불여일타 SQL 캠프 입문반') , 
        scroll AS (SELECT ga_session_id, user_pseudo_id,
                          event_timestamp_kst AS scroll_at
                   FROM ga 
                   WHERE event_name='scroll'
                   AND page_title='백문이불여일타 SQL 캠프 입문반'),
        click AS (SELECT ga_session_id, user_pseudo_id,
                          event_timestamp_kst AS click_at
                   FROM ga 
                   WHERE event_name IN ('SQL_basic_form_click','SQL_package_form_click','SQL_basic_1day_form_click')
                   AND page_title='백문이불여일타 SQL 캠프 입문반')
                   
    SELECT COUNT(DISTINCT pv.ga_session_id, pv.user_pseudo_id) AS pv 
          ,COUNT(DISTINCT scroll.ga_session_id, scroll.user_pseudo_id) AS scroll 
          ,COUNT(DISTINCT click.ga_session_id, click.user_pseudo_id) AS click 
          ,COUNT(DISTINCT scroll.ga_session_id, scroll.user_pseudo_id)/COUNT(DISTINCT pv.ga_session_id, pv.user_pseudo_id) AS scroll_pv_rate 
          ,COUNT(DISTINCT click.ga_session_id, click.user_pseudo_id)/COUNT(DISTINCT scroll.ga_session_id, scroll.user_pseudo_id) AS click_scroll_rate 
          ,COUNT(DISTINCT click.ga_session_id, click.user_pseudo_id)/COUNT(DISTINCT pv.ga_session_id, pv.user_pseudo_id) AS click_pv_rate 
    FROM pv 
    LEFT JOIN scroll ON pv.user_pseudo_id = scroll.user_pseudo_id 
                    AND pv.ga_session_id  = scroll.ga_session_id
                    AND pv.pv_at <= scroll.scroll_at
    LEFT JOIN click ON scroll.user_pseudo_id = click.user_pseudo_id
                   AND scroll.ga_session_id  = click.ga_session_id 
                   AND scroll.scroll_at <= click.click_
    ```
    

![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%202.png)

<aside>
✅ **입문반은 페이지뷰는 높지만, 각 퍼널 단계에서 이탈되는 유저가 매우 많습니다. 이로 인해 최종 전환율이 3.35%로 매우 낮은 문제가 발생했습니다.**

</aside>

### 1) 입문반 유입 채널별 퍼널 분석

- *query*
    
    ```sql
    WITH pv AS (
                SELECT user_pseudo_id
                     , ga_session_id
                     , event_timestamp_kst pv_at
                     , source
                     , medium
                FROM ga
                WHERE event_name = 'page_view'
                AND page_title = '백문이불여일타 SQL 캠프 입문반'
               )
       , scroll AS (
                    SELECT user_pseudo_id
                         , ga_session_id
                         , event_timestamp_kst scroll_at
                    FROM ga
                    WHERE event_name = 'scroll'
                    AND page_title = '백문이불여일타 SQL 캠프 입문반'
                   )
      , click AS (
                  SELECT user_pseudo_id
                       , ga_session_id
                       , event_timestamp_kst AS click_at
                  FROM ga 
                  WHERE event_name IN ('SQL_basic_form_click', 'SQL_basic_1day_form_click', 'SQL_package_form_click')
    							AND page_title = '백문이불여일타 SQL 캠프 입문반'
                  )
    
    SELECT source
         , medium
         , COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) pv
         , COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) scroll_after_pv
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) click_after_scroll
         , COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) / COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) pv_scroll_rate
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) / COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) scroll_click_rate
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) / COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) pv_click_rate
    FROM pv
         LEFT JOIN scroll ON pv.user_pseudo_id = scroll.user_pseudo_id
                          AND pv.ga_session_id = scroll.ga_session_id
                          AND pv.pv_at <= scroll.scroll_at
         LEFT JOIN click ON scroll.user_pseudo_id = click.user_pseudo_id
                         AND scroll.ga_session_id = click.ga_session_id
                         AND scroll.scroll_at <= click.click_at
    GROUP BY source, medium
    ORDER BY pv DESC
    ```
    

![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%203.png)

<aside>
💡 **유료 채널보다 무료 채널에서의 최종 전환율이 높습니다.**

- 유료 채널은 광고로 인해 페이지 뷰는 높지만, 최종 전환율이 각 1.03%와 4.85%으로 낮았습니다.
- 무료 채널은 페이지 뷰 자체는 높지 않지만, 두 자리 수의 높은 최종 전환율을 나타냈습니다.
    - `**brunch**` 는 페이지 뷰(54)도 높으면서, 최종 전환율(14.81%) 또한 높았습니다.
    - `**open_katalk**`과 `**youtube**`는 페이지 뷰(17,11)는 낮지만, 최종 전환율(17.65%, 18.18%)이 높았습니다.
</aside>

### ❓무료 채널로 유입 된 유저들의 전환율이 높은 이유는 무엇일까

![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%204.png)

<aside>
❓ **무료 채널로 유입된 유저들의 전환율이 높은 이유는 무엇일까?**

- 무료 채널로 유입된 유저는 **적극적 유저**로 볼 수 있습니다.
- 유저가 **직접 구글, 유튜브 등에서 데이터 분석과 관련된 키워드 검색을 통해 유입** 되었을 가능성이 높습니다. 이에 니즈에 부합되는 강의를 발견했을 때 강의를 수강할 의지 강할 것이라 추측할 수 있습니다.

**유료 채널로 유입된 유저들의 전환율이 낮은 이유는 무엇일까?**

- 유료 채널로 유입된 유저는 **소극적 유저**로 볼 수 있습니다.
- 스스로 정보를 찾아서 유입되는 유저가 아닌 **광고로부터 정보를 제공 받은 유저**이므로 적극적 유저에 비해 강의를 수강 할 의지가 낮다고 추측할 수 있습니다.
</aside>

### 2) 입문반 무료 채널의 캠페인/콘텐츠 분석

  앞서 유입 채널별 전환율 분석에서 무료 채널로 유입된 유저들은 **적극적 유저의 특징**(⇒ 스스로 데이터 분석과 관련된 정보를 검색한다)을 가지고 있을 것이라 가정했습니다. 이에 무료 채널에서 페이지 뷰가 많이 발생된 컨텐츠의 특징을 분석 후, 관련 컨텐츠를 추가로 발행하여 적극적 유저들의 유입을 늘린다면 최종적으로 캠프 참여자 수 또한 늘릴 수 있을 것입니다. 

![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%205.png)

- 참고 | 유료 채널의 캠페인/콘텐츠를 분석하지 않은 이유와 데이터 전처리 과정
    
    **1) 유료 채널의 `campaign`/`content`를 분석하지 않은 이유**  
    
    - 페이스북과 인스타그램의 유입 매채(**`campaign`**)는 각각`**sql_basic**`과 `**linktree**`로 고정되어 있습니다.
    - 페이스북의 총 `**content**` 개수는 45개로, 아래와 같이 식별하기 어려운 경우가 많았기 때문에 해당 분석에서는 제외 되었습니다.
    
    ![페이스북의 content 예시 ](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%206.png)
    
    페이스북의 content 예시 
    
     ****
    
    **2) 데이터 수집과 전처리 과정** 
    
    - 데이터리안이 제공하는 SQL 실습 사이트인 solvesql에서 ga 데이터를 추출.
    - PYTHON 환경에서 page_location내에 있는 `**campaign**`과 `**content**`를 특정하여 분리한 후 pandas 라이브러리를 이용하여 새로이 정의된 GA 데이터 생성.
        - *Python Code*
            
            ```python
            # 사용 할 라이브러리 불러오기 
            import pandas as pd 
            import re 
            
            # solvesql내에서는 5000행 이상의 데이터는 출력해주지 않기 때문에 source 기준으로 분리해서 csv 파일 저장
            x = pd.read_csv("경로/direct_youtube.csv") 
            y = pd.read_csv("경로/etc.csv")
            a = pd.read_csv("경로/fb_linktree_brunch.csv")
            
            # 하나의 데이터 프레임으로 합쳐주기
            ga = pd.concat([x,y,a],ignore_index=True)
            ga.info() # 값 체크 
            
            # 원본 보존하기 
            ga_new = ga.copy()
            
            # split 
            ga_new['page_location']  = ga_new['page_location'].astype('str') # 데이터 타입 변경 
            ga_new['page_location'].dtypes # 타입 변경 되었는지 확인
            
            # &을 기준으로 문자열 분리하기 
            ga_new['page_location'] = ga_new['page_location'].str.split("&")
            ga_new['page_location']
            
            # page_location에서 campaign과 content가 포함된 문자열을 각 컬럼(campaign,content)에 분배하기 
            ga_new['campaign']=ga_new['page_location'].str.findall("(utm_campaign=\w+&?)")
            ga_new['content']=ga_new['page_location'].str.findall("(utm_content=\w+&?)")
            
            ga_new[['campaign','content']] # 값이 잘 들어왔는지 체크하기 
            
            # 데이터 전처리 
            ## campaign
            ga_new['campaign'] =ga_new['campaign'].astype('str') # 데이터 타입 변경
            ga_new['campaign'] = ga_new['campaign'].replace("utm_campaign=","",regex=True) # 'utm_campaign'을 공백으로 치환하기
            ga_new['campaign'] = ga_new['campaign'].replace("&","",regex=True) # '&'을 공백으로 치환하기
            ga_new['campaign'] = ga_new['campaign'].replace("\]","",regex=True)
            ga_new['campaign'] = ga_new['campaign'].replace("[","",regex=True)
            
            ## content
            ga_new['content'] =ga_new['content'].astype('str')
            ga_new['content'] = ga_new['content'].replace("utm_content=","",regex=True)
            ga_new['content'] = ga_new['content'].replace("&","",regex=True)
            ga_new['content'] = ga_new['content'].replace("\[","",regex=True)
            ga_new['content'] = ga_new['content'].replace("]","",regex=True)
            
            # MySQL로 연동을 위해 csv 파일로 원본 저장하기 
            ga_ansi.to_csv("경로/ga_new.csv",index=False, encoding='ANSI')
            
            # 엑셀 활용시 사용할 수 있도록 excel로 저장하기 
            ga_excel.to_excel('경로/ga_1.xlsx',index=False) 
            ```
            
    - 새로이 정의된 GA 데이터를 MySQL 환경에 불러온 후 분석을 진행.
    
- *query*
    
    ```sql
    WITH pv AS (
            SELECT user_pseudo_id,
                  ga_session_id,
                  event_timestamp_kst AS pv_at,
                  source,
                  medium
            FROM ga 
            WHERE event_name = 'page_view'
            AND page_title = '백문이불여일타 SQL 캠프 입문반'
            AND source IN ('brunch','youtube','publy','velog','careely')
            ),
        scroll AS(
            SELECT user_pseudo_id,
                  ga_session_id,
                  event_timestamp_kst as scroll_at
            FROM ga
            WHERE event_name = 'scroll'
            AND page_title = '백문이불여일타 SQL 캠프 입문반'
            AND source IN ('brunch','youtube','publy','velog','careely')
            ),
        click AS(
            SELECT
                    user_pseudo_id,
                    ga_session_id,
                    event_timestamp_kst AS click_at
            FROM ga
            WHERE event_name IN ('SQL_basic_form_click', 'SQL_basic_1day_form_click', 'SQL_package_form_click')
            AND page_title = '백문이불여일타 SQL 캠프 입문반'
            AND source IN ('brunch','youtube','publy','velog','careely'))
    
    SELECT source
         , medium
         , COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) AS pv
         , COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) AS scroll_after_pv
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) AS click_after_scroll
         , COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) / COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) AS pv_scroll_rate
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) / COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) AS scroll_click_rate
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) / COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) AS pv_click_rate
    FROM pv
         LEFT JOIN scroll ON pv.user_pseudo_id = scroll.user_pseudo_id
                          AND pv.ga_session_id = scroll.ga_session_id
                          AND pv.pv_at <= scroll.scroll_at
         LEFT JOIN click ON scroll.user_pseudo_id = click.user_pseudo_id
                         AND scroll.ga_session_id = click.ga_session_id
                         AND scroll.scroll_at <= click.click_at
    GROUP BY source, medium
    ORDER BY pv DESC
    ```
    

<aside>
💡 **SQL_CAMP 실전반 소개와 XXIT_QNA에서 가장 많은 페이지 뷰가 발생했습니다. 
하지만 최종 전환율은 CAMP_PREVIEW와 책 추천이 가장 높았습니다.**

각 캠페인이 가지는 세부 정보는 아래와 같습니다 : 

![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%207.png)

  입문반의 타겟 고객은 **데이터 분석가로 취업을 희망**하는 혹은 **현업에서 데이터 분석 기술을 활용**하고 싶은 사람 입니다. 그렇기에 캠프 소개와 관련된 **sql_camp**와 **camp_preview** 캠페인에서 많은 페이지뷰가 발생 되었습니다. 

**고객을 세분화하여 결과를 살펴본다면 아래와 같이 추측해 볼 수 있습니다.** 

- 공통
    - sql_camp, camp_preview을 통해 입문반 페이지로 유입됨.
- 데이터 분석가로 취업을 희망하는 취업 준비생
    - 데이터 분석가 직무 정보와 관련된 xxit_QnA와 interview을 통해 유입됨.
- 현업에서 데이터 분석 기술을 활용하고 싶은 직장인
    - 책_추천을 통해 유입되었을 가능성이 높다.
</aside>

[SEO(검색엔진최적화)로 무료 유입 고객 수 늘리기 (2/2) | 뷰저블](https://www.beusable.net/blog/?p=4266)

### 3.2. 실전반 퍼널 분석

![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%208.png)

- *query*
    
    ```sql
    -- 실전반 퍼널 
    WITH pv AS (
                SELECT user_pseudo_id
                     , ga_session_id
                     , event_timestamp_kst AS pv_at
                FROM ga
                WHERE event_name = 'page_view'
                AND page_title = '백문이불여일타 SQL 캠프 실전반'
               ) 
       , scroll AS (
                    SELECT user_pseudo_id
                         , ga_session_id
                         , event_timestamp_kst AS scroll_at
                    FROM ga
                    WHERE event_name = 'scroll'
                    AND page_title = '백문이불여일타 SQL 캠프 실전반'
                   )
       , click AS (
                   SELECT user_pseudo_id
                        , ga_session_id
                        , event_timestamp_kst AS click_at
                   FROM ga 
                   WHERE event_name IN ('SQL_advanced_form_click', 'SQL_package_form_click')
    							 AND page_title = '백문이불여일타 SQL 캠프 실전반'
                  )
    SELECT COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) pv
         , COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) scroll
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) click
         , COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) / COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) pv_scroll_rate
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) / COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) scroll_click_rate
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) / COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) pv_click_rate
    FROM pv
         LEFT JOIN scroll ON pv.user_pseudo_id = scroll.user_pseudo_id
                          AND pv.ga_session_id = scroll.ga_session_id
                          AND pv.pv_at <= scroll.scroll_at
         LEFT JOIN click ON scroll.user_pseudo_id = click.user_pseudo_id
                         AND scroll.ga_session_id = click.ga_session_id
                         AND scroll.scroll_at <= click.click_at
    ```
    

<aside>
✅ 실전반**은 유료 광고로 인해 페이지뷰는 높지만, 각 단계에서 이탈되는 유저가 많습니다. 이로 인해 최종 전환율이 3.35%로 매우 낮은 문제가 발생했습니다.**

</aside>

### 1) 실전반 유입 채널별 퍼널 분석

![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%209.png)

- *query*
    
    ```sql
    
    ```
    

### 2) 실전반 무료 채널별 캠페인, 콘텐츠 분석

- *query*
    
    ```sql
    with pv as (
            select user_pseudo_id,
                  ga_session_id,
                  event_timestamp_kst as pv_at,
                  source,
                  medium
            from ga 
            where event_name = 'page_view'
            and page_title = '백문이불여일타 SQL 캠프 실전반'
            and source in ('brunch','youtube','publy','velog','careely')
            ),
        scroll as(
            select user_pseudo_id,
                  ga_session_id,
                  event_timestamp_kst as scroll_at
            from ga
            where event_name = 'scroll'
            and page_title = '백문이불여일타 SQL 캠프 실전반'
            and source in ('brunch','youtube','publy','velog','careely')
            ),
        click as(
            select
                    user_pseudo_id,
                    ga_session_id,
                    event_timestamp_kst as click_at
            from ga
            where event_name in ('SQL_advanced_form_click', 'SQL_package_form_click')
            and page_title = '백문이불여일타 SQL 캠프 실전반'
            and source in ('brunch','youtube','publy','velog','careely'))
    
    SELECT source
         , medium
         , COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) pv
         , COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) scroll_after_pv
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) click_after_scroll
         , COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) / COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) pv_scroll_rate
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) / COUNT(DISTINCT scroll.user_pseudo_id, scroll.ga_session_id) scroll_click_rate
         , COUNT(DISTINCT click.user_pseudo_id, click.ga_session_id) / COUNT(DISTINCT pv.user_pseudo_id, pv.ga_session_id) pv_click_rate
    FROM pv
         LEFT JOIN scroll ON pv.user_pseudo_id = scroll.user_pseudo_id
                          AND pv.ga_session_id = scroll.ga_session_id
                          AND pv.pv_at <= scroll.scroll_at
         LEFT JOIN click ON scroll.user_pseudo_id = click.user_pseudo_id
                         AND scroll.ga_session_id = click.ga_session_id
                         AND scroll.scroll_at <= click.click_at
    GROUP BY source, medium
    ORDER BY pv DESC
    ```
    

## 4. 추가 분석

효과가 좋은 채널이 무엇인지 알았다, 그렇다면 Acquisition을 높이기 전 Product에 대한 문제점은 없는지 추가로 살펴보자. 

     AARRR을 근거로 했을 때, 프로덕트에 대한 개선이 없이 무작정 acquisition 채널을 열어버리면 소중한 고객을 안티로 만드는 가장 쉬운 방법임. 또한, CAC를 고려해 봤을 때에도 고객 획득비용에 추가 코스트를 투입하는 것 보다는 리텐션을 올리는 것이 좋음.

     여기서 Funnel 분석을 왜 해당 프로젝트의 분석기법으로 사용하게 되었는지 설명하기

     그 다음 신규 고객을 추가 모집하기 위해서는 고객에 대한 파악이 중요하다. 고객의 페인포인트가 무엇인지 알아보기 위해서 추가로 acquisition funnel을 단계별로 짜보며 이러한 가설을 내려 해당 분석을 진행해보려 한다고 설명하기 

## 5. 제안

## 6. 데이터 설명과 EDA

### 5.1. `GA` 테이블 파악하기

- `**GA**` 테이블은 데이터리안 웹사이트에 접속한 사용자의 행동 데이터가 저장되어 있습니다.
- 데이터가 수집된 기간은 **총 9일**로, 2022-01-20부터 2022-01-28까지 입니다.
- `**user_pseudo_id**`와 `**ga_session_id**`는 서로 **N:M 관계**를 가집니다. 한 명의 사용자가 여러 개의 `**ga_session_id**`값을 가질 수 있습니다.
    - 이에 **개별 세션을 특정하기 위해서는 `user_pseudo_id`와 `ga_session_id`를 함께 고려**해야 합니다.

### 5.2. 각 컬럼 데이터의 상세 정보 파악하기

- 전체 컬럼 파악하기:
    
    ![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%2010.png)
    

- **event_name**
    
    ![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%2011.png)
    

- **Source(트래픽 채널)와 Medium(트래픽 매채)**
    
    ![Untitled](%5BW3%5D%20%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%20aadc1c266f4d49f98684e7463db3aac2/Untitled%2012.png)
    

### 5.3. EDA

[사용자 1명을 특정하여 세션 파악하기 ](https://www.notion.so/1-6de298cf1633453999b5913c18f48cef)

## 7. 프로젝트 회고

### KPT 회고

KEEP (이번에 잘했고, 앞으로도 이렇게 하자)

Problem (문제가 있었거나, 개선이 필요한 부분)

Try (다음에는 이런 걸 시도해보면 어떨까) 

[What Does Direct/None Mean in Google Analytics? - Data Driven U](https://www.datadrivenu.com/direct-none-traffic-source-google-analytics/)

### 7. 참고

- 참고 | 퍼널 분석이란?
    
    <aside>
    ✅ **퍼널 분석이란?**
       퍼널 분석은 고객들이 우리가 설계한 유저 경험 루트를 따라 잘 도착하고 있는지 확인해보기 위해 최초 유입부터 최종 목적지까지 단계를 나누어 살펴보는 분석 기법입니다. 얼마나 많은 사람들이 최종 단계까지 도착하는지, 또 어디에서 많이 이탈하는지 확인할 수 있습니다.
    
       퍼널 분석을 통해 사용자의 속성이나 동작에 따라 변환률이 어떻게 달라지는지를 파악할 수 있습니다. 따라서 어떤 사용자 유형이 변환 가능성이 높은지, 중도 이탈 원인이 무엇인지, 중도 이탈 사용자들이 어떤 행동을 하는지 파악하여 퍼널의 성능을 향상시킬 수 있을 뿐 아니라 중요한 퍼널과 사용자 이동의 잠재적 결함을 발견할 수 있게 됩니다.
    
    </aside>
