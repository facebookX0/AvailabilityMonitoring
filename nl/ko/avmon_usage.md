---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 서비스 사용량
{: #avmon_usage}

앱의 **모니터링** 탭과 {{site.data.keyword.prf_hubshort}} 기본 대시보드에서 {{site.data.keyword.prf_hubshort}} 사용량에 대한 세부사항을 볼 수 있습니다. 

**모든 애플리케이션** 테이블에서 {{site.data.keyword.prf_hubshort}} 사용량에 대한 개요를 보려면 앱 이름을 클릭하고 앱 분할창에서 **모니터링** 탭을 클릭하십시오. 사용 중인 플랜과 함께 **사용량** 백분율이 게이지 그래프에 표시됩니다.  

{{site.data.keyword.prf_hubshort}} 기본 대시보드에서 사용량의 개요를 보려면 **구성** 아이콘 ![구성 아이콘](images/config_icn_white_smll.jpg)을 클릭하십시오. {{site.data.keyword.prf_hubshort}} 라이트 플랜 사용자인 경우 사용 중인 테스트 수와 함께 사용량이 막대 그래프와 백분율로 표시됩니다. 유료 사용제 사용자인 경우 사용량이 데이터 점으로 표시됩니다. 합성 테스트 분할창에서 각 개별 테스트에 대한 사용량 세부사항을 볼 수 있습니다. 

사용량은 데이터 점으로 측정됩니다. 데이터 점의 예상 수는 다음 공식으로 계산됩니다.

데이터 점의 예상 수 = 매월 T \* L \* (60/M \* 24 \* 30) 

여기서 T = 실행된 합성 테스트의 수, L = 위치 수 및 M = 테스트 간 간격(분).

웹 페이지 및 REST API 테스트와 같은 단순 테스트는 테스트마다 하나의 데이터 점을 사용합니다. Selenium 스크립트 및 REST API 스크립트와 같은 고급 테스트는 테스트마다 100개의 데이터 점을 사용합니다.

{{site.data.keyword.Bluemix_notm}} 계정 페이지의 사용량 대시보드에서 실제 사용량을 볼 수 있습니다. **계정**을 클릭한 후에 **사용량 대시보드**를 선택하고 **서비스 이용료** 섹션으로 스크롤 다운하십시오. {{site.data.keyword.prf_hubshort}} 서비스에 대한 **화살표** 아이콘을 클릭하여 사용한 데이터 점의 수를 확인하십시오. {{site.data.keyword.prf_hubshort}} 가격 책정 및 사용량 플랜에 대한 자세한 정보는 [Availability Monitoring](https://console.{DomainName}/catalog/services/availability-monitoring/ "(새 탭이나 창에서 열림)"){: new_window} 카탈로그 페이지에서 가격 책정 플랜을 참조하십시오. 
