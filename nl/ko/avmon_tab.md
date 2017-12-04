---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Availability Monitoring에 액세스
{: #avmon_tab}

**모니터링** 탭에서 {{site.data.keyword.prf_hubshort}} 대시보드에 액세스할 수 있습니다. Cloud Foundry 애플리케이션의 **모니터링** 탭에는 테스트의 가용성 및 상태에 대한 요약 정보 및 서비스 구독 세부사항과 사용량이 표시됩니다.
{: shortdesc}

{{site.data.keyword.prf_hubshort}}에 액세스하려면 다음 단계를 완료하십시오. 

1.  **앱** 대시보드에서 Cloud Foundry 애플리케이션의 이름을 클릭하십시오.
2.  **모니터링** 탭을 클릭하십시오. 

**모니터링** 탭은 지난 24시간의 **평균 테스트 가용성**, 모든 테스트의 **현재 테스트 상태** 및 현재 플랜에 대한 할당의 **서비스 사용량**을 보여주는 3개의 게이지를 표시합니다. 

![Availability Monitoring 탭](images/avmon_tab.png)

가용성 계산에서 포함할 테스트를 선택하여 {{site.data.keyword.prf_hubshort}}에서 **평균 테스트 가용성**을 계산하는 방법을 구성할 수 있습니다. **평균 테스트 가용성** 게이지에서 **화살표** 아이콘 ![화살표 아이콘](images/arrow_dwn_icn_white.jpg)을 클릭하여 테스트 카드를 본 후에 **가용성 계산**을 클릭하십시오. 카드를 클릭하여 계산에 추가하거나 계산에서 제거하십시오. 제외된 테스트 카드는 희미하게 표시됩니다. 완료되면 **완료**를 클릭하십시오. **평균 테스트 가용성** 게이지가 새로 고쳐집니다. 

**현재 테스트 상태** 게이지에서 **화살표** 아이콘 ![화살표 아이콘](images/arrow_dwn_icn_white.jpg)을 클릭하여 모든 테스트의 상태를 볼 수 있습니다. 테스트를 위한 테스트 카드가 표시됩니다.

{{site.data.keyword.prf_hubshort}} 대시보드에 액세스하려면 **모니터링 세부사항 표시**를 클릭하십시오. {{site.data.keyword.prf_hubshort}} 대시보드에서 합성 테스트를 기반으로 애플리케이션의 가용성을 모니터할 수 있습니다. 또한 데이터 콜렉터에서 제공하는 사용자 트랜잭션 데이터를 기반으로 애플리케이션의 응답성과 처리량을 모니터할 수도 있습니다. 

합성 테스트 분할창에서 테스트를 보고 편집하려면 **모든 테스트 보기**를 클릭하십시오. 테스트를 작성하려면 **새 테스트 추가**를 클릭하십시오.

애플리케이션에 대한 월별, 주별, 일별 가용성 및 응답 시간 평균의 .csv 파일 보고서를 다운로드하려면 **다운로드** 아이콘 ![다운로드 아이콘](images/download_icn_white_smll.jpg)을 클릭하십시오. 
