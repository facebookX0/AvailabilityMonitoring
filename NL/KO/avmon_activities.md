---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}


# 활동
{: #avmon_activities}

활동 분할창에서 활동에 대한 정보를 봅니다. _활동_은 사용자 정의 이벤트의 외부에서 발생하는 조치입니다.
{: shortdesc}

활동 분할창에는 지난 24시간 동안 애플리케이션에 대한 모든 활동(예: 시작, 중지 및 배치)에 대한 정보가 표시됩니다. 

![Availability Monitoring 대시보드의 활동 분할창.](images/avmon_activity_pane.png)

{{site.data.keyword.Bluemix_notm}} 활동은 {{site.data.keyword.Bluemix_notm}}에서 발생하는 애플리케이션 이벤트입니다(예: 애플리케이션 중지, 시작 또는 다시 스테이징). 파이프라인 활동은 DevOps 파이프라인에서 발생하는 이벤트입니다(예: 빌드, 배치 및 테스트). 테이블 헤더는 {{site.data.keyword.Bluemix_notm}} 활동 및 파이프라인 활동에 대한 개별 총계를 표시합니다. 활동 분할창 헤더에서 {{site.data.keyword.Bluemix_notm}} 또는 파이프라인 아이콘을 클릭하여 {{site.data.keyword.Bluemix_notm}} 활동 또는 파이프라인 활동을 표시하도록 활동 소스별로 필터링할 수 있습니다. 

{{site.data.keyword.prf_hubshort}} 대시보드에서 파이프라인 활동을 보려면 먼저 애플리케이션에 대해 {{site.data.keyword.contdelivery_short}}를 사용 설정하고 파이프라인 및 {{site.data.keyword.DRA_short}} 서비스를 포함하는 도구 체인을 구성해야 합니다. **파이프라인 설정**을 클릭하여 애플리케이션에 대한 도구 체인을 작성하십시오. 자세한 정보는 [Continuous Delivery 시작하기](../ContinuousDelivery/index.html "(새 탭이나 창에서 열림)"){:new_window} 및 [DevOps Insights 시작하기](../DevOpsInsights/index.html#gettingstarted "(새 탭이나 창에서 열림)")를 참조하십시오.
{: tip}

애플리케이션에 대해 {{site.data.keyword.contdelivery_short}} 및 {{site.data.keyword.DRA_short}}가 구성되어 있는 경우에는 이벤트 열에서 **Insights 보기**를 클릭하여 {{site.data.keyword.DRA_short}} 대시보드에 액세스하고 파이프라인 활동에 대한 추가 세부사항을 볼 수 있습니다. 

{{site.data.keyword.Bluemix_notm}} 및 파이프라인 활동은 응답 시간 및 가용성 분할창의 그래프 및 **메트릭 피드**에서도 표시됩니다. 
