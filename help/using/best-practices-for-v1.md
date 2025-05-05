---
title: 데스크탑 앱 v1.10 우수 사례
description: ' [!DNL Adobe Experience Manager] 데스크톱 앱 버전 1.10의 주요 기능 및 권장 사용.'
exl-id: 5de06b33-c05c-47eb-b884-408b6f9afc94
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '1651'
ht-degree: 0%

---

# AEM desktop app v1.10 우수 사례 {#aem-desktop-app-best-practices}

## 개요 {#overview}

[!DNL Adobe Experience Manager] 데스크톱 앱은 DAM(디지털 자산 관리) 솔루션을 데스크톱과 연결하여 데스크톱에서 바로 AEM Web UI에서 사용할 수 있는 파일을 열 수 있도록 합니다. 데스크탑에서 자산을 저장한 경우 적절한 위치에서 AEM으로 업로드됩니다.

AEM 데스크탑 앱을 사용하면 AEM에서 잘못된 로컬 복사본을 업데이트하거나 잘못된 에셋을 업데이트할 필요가 없습니다. 데스크탑 앱의 사용하기 쉬운 워크플로는 데스크탑 운영 체제에서 제공하는 네트워크 공유 기술을 사용하여 활성화됩니다.

데스크탑 앱은 AEM Assets 저장소를 데스크탑에서 네트워크 공유로 마운트합니다. 따라서 폴더와 파일이 로컬인 것처럼 나타납니다. 그러나 Finder 또는 Explorer의 마운트된 네트워크 공유에 있는 데스크탑에서 직접 디지털 자산 관리 작업을 수행하는 것은 권장되지 않습니다. Adobe 대신 AEM Assets 웹 UI를 사용하여 많은 수의 에셋을 복사하거나 이동하는 등의 작업을 수행하는 것이 좋습니다.

>[!NOTE]
>
>이 문서를 읽기 전에 전체적인 [AEM 및 Creative Cloud 통합 모범 사례](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/assets/administer/aem-cc-integration-best-practices)를 검토하여 이 항목의 더 높은 수준의 개요를 확인할 수 있습니다.

## AEM 데스크탑 앱 아키텍처 {#aem-desktop-app-architecture}

AEM 데스크탑 앱은 WebDAV(Windows) 또는 SMB(Mac) 네트워크 공유를 사용하여 네트워크 공유를 마운트합니다. 마운트된 네트워크 공유는 로컬 전용입니다. AEM 데스크탑 앱은 호출(열기, 읽기, 쓰기)을 가로채고 추가 로컬 캐싱을 제공합니다. AEM Assets 서버에 대한 원격 호출을 최적화된 AEM HTTP 요청으로 변환합니다. 다음 다이어그램은 AEM 데스크탑 앱 아키텍처를 보여 줍니다.

![AEM 데스크톱 앱 아키텍처](assets/arch_v1.png)

*그림: 데스크톱 앱 아키텍처*

파일이 저장되면 쓰기 시 추가 캐싱이 먼저 로컬에 저장되므로 사용자가 네트워크 전송을 기다리지 않아도 됩니다. 미리 정의된 지연(30초) 후 백그라운드에서 파일이 AEM으로 업로드된 다음 에셋이 AEM으로 업로드됩니다. AEM 데스크탑 앱은 백그라운드 파일 업로드 상태를 모니터링하기 위한 UI를 제공합니다.

## AEM 데스크탑 앱의 권장 사용 {#recommended-use-of-aem-desktop-app}

AEM 데스크탑 앱의 주요 기능은 다음과 같습니다.

* **데스크톱에서 AEM Assets Web UI에서 파일을 여는 중**. 웹 UI에서 데스크탑의 에셋을 표시하거나(Finder, Explorer) 데스크탑 애플리케이션을 사용하여 에셋을 열 수 있습니다.

* **체크아웃 및 체크인**. Assets은 편집을 위해 체크 아웃할 수 있으며, AEM Assets에서 사용자에 대해 잠겨 있는 것으로 표시됩니다. 편집한 후 자산을 체크인하여 잠금을 해제할 수 있습니다.

* **변경 내용을 파일에 저장**&#x200B;합니다. 네트워크 공유의 파일에 저장하는 모든 변경 사항은 AEM에 자동으로 업로드되고 새 버전이 만들어집니다.

* **연결된 자산을 다른 문서에 배치**. Creative Cloud([!DNL Adobe Photoshop], [!DNL Adobe InDesign] 및 [!DNL Adobe Illustrator])과 같은 응용 프로그램에서 외부 파일을 링크로 배치할 수 있습니다. 예를 들어 이미지를 InDesign 문서에 배치할 수 있습니다. 이 경우 네트워크 공유 마운트를 사용하여 AEM에서 에셋을 찾아 배치할 수 있습니다. 링크된 파일 배치는 MS® Office와 같은 일부 Adobe 이외의 앱에서도 작동합니다.

* **AEM의 참조 확인**. 배치된 파일과 링크가 있는 기본 파일이 모두 AEM에 저장된 경우 에셋 참조에 대한 서버측 정보를 자동으로 제공할 수 있습니다.

* **데스크톱에서 자산에 액세스**. 탑재된 네트워크 공유에서 상황에 맞는 메뉴가 [!UICONTROL More Info] 대화 상자(더 큰 미리 보기, 키 메타데이터)와 AEM UI에서 자산을 여는 기능을 제공합니다.

* **대규모 계층 구조 폴더를 일괄적으로 업로드**. AEM UI의 **만들기** > **폴더 업로드** 옵션을 사용하여 자산을 업로드하는 경우 AEM 데스크톱 앱에서 선택한 폴더 계층 구조를 백그라운드의 AEM에 업로드합니다. 업로드 진행률은 데스크탑 앱의 전용 UI를 통해 모니터링됩니다.

## AEM 데스크탑 앱의 부적절한 사용 {#inappropriate-use-of-aem-desktop-app}

* AEM 데스크탑 앱을 사용하여 데스크탑에서 자산을 관리하지 마십시오. AEM 데스크탑 앱은 네트워크 드라이브를 대체하지 않습니다. 대신 다음 기능을 사용하십시오.

   * 디지털 자산 관리(자산, 메타데이터 및 복사 또는 이동 찾기 또는 공유)를 위한 AEM Assets 웹 UI.

   * 대형 계층 폴더를 업로드할 AEM 데스크톱 앱 [!UICONTROL Folder Upload]입니다.

* AEM 데스크톱 앱을 AEM Assets용 &quot;데스크톱 동기화&quot; 클라이언트로 취급하지 마십시오. AEM 데스크톱 앱의 주요 이점은 전체 저장소에 대한 &quot;가상&quot; 액세스를 제공하며 데스크톱 동기화 애플리케이션은 일반적으로 한 명의 사용자에 속한 자산만 동기화한다는 것입니다. AEM 데스크탑 앱은 일정 수준의 캐싱 및 백그라운드 업로드를 제공하지만, Adobe Creative Cloud 데스크탑 앱 또는 Microsoft OneDrive와 같은 일반적인 &quot;동기화&quot; 응용 프로그램과는 매우 다르게 작동합니다.

* 자산을 자주 저장하는 데 AEM 데스크탑 앱 네트워크 드라이브를 사용하지 마십시오. 모든 저장 작업은 AEM Assets으로 전송됩니다. 따라서 마운트된 AEM Assets 저장소에서 직접 집중 편집 작업을 수행하는 것은 어렵습니다. 탑재된 저장소에서 직접 에셋을 편집하면 관련 없는 버전으로 에셋의 타임라인이 조정되고 서버에 추가 오버헤드가 부과됩니다.

* 한 AEM 인스턴스에서 다른 AEM 인스턴스로 대량의 데이터를 마이그레이션하는 데 데스크탑 앱을 사용하지 마십시오. 자산 마이그레이션을 계획하고 실행하려면 [마이그레이션 안내서](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/assets/administer/assets-migration-guide)를 참조하세요. 반면 데스크톱 앱 [은(는) [!DNL Adobe Experience Manager]에서 처음으로 많은 수의 에셋을 일괄 업로드](use-app-v1.md#bulkupload)할 수 있도록 지원합니다.

## 선택한 사용 사례에 대한 Recommendations {#recommendations-for-selected-use-cases}

### 크리에이티브 사용자를 위한 에셋에 액세스 {#access-to-assets-for-creative-users}

AEM 데스크탑 앱에서는 전체 DAM 저장소에 대한 가상 액세스를 제공합니다. 데스크탑의 크리에이티브 사용자가 데스크탑에서 올바른 자산을 찾아 액세스하는 것은 복잡할 수 있습니다. 이러한 모범 사례를 사용하여 이를 단순화합니다.

* AEM Assets Web UI의 공동 작업 기능을 사용하여 크리에이티브 사용자에게 적합한 에셋에 보다 직접 액세스할 수 있습니다. 폴더 또는 컬렉션을 공유하거나, 스마트 컬렉션(저장된 검색)을 제공하거나, 올바른 자산에 대한 포인터를 사용하여 알림을 전송하는 것도 그중 일부입니다. 그런 다음 Creative 사용자는 웹 UI에서 데스크탑 작업을 사용하여 데스크탑에서 이러한 에셋에 빠르게 액세스할 수 있습니다.

* 자산에 대한 올바른 권한(액세스 제어)을 고려하여 크리에이티브 사용자의 DAM 저장소에 대한 보기를 단순화하고, 기본적으로 필요한 자산 또는 관심 자산에 대한 액세스만 제한하십시오.

   * 크리에이티브 사용자와 관련이 없는 특정 영역은 사용자 그룹의 보기나 데스크탑에서 제거하기 위해 거부될 수 있습니다.

   * DAM의 에셋 대부분은 최종적이며 변경하기 위한 것이 아닙니다. 이러한 에셋은 크리에이티브 사용자를 위해 읽기 전용이어야 합니다.

   * 크리에이티브 사용자에 대해 변경 또는 수정이 필요한 자산만 쓰기 가능해야 합니다. 일부 조직에서는 AEM Projects와 이들이 생성하는 폴더를 사용하여 여전히 변경의 대상인 자산을 호스팅합니다.

### 자산 검색 중 {#searching-assets}

데스크탑에서 열 파일을 검색하려면 다음을 수행합니다.

* AEM Assets 웹 UI를 사용하여 에셋을 찾습니다. AEM Assets의 검색 기능(검색 패싯, 저장된 검색)은 물론, 적절한 자산을 찾을 수 있는 추가 기능도 제공합니다. 여기에는 상태(승인, 만료), 컬렉션, 작업, 알림 및 다른 사용자/그룹과 폴더/컬렉션을 공유하는 기능과 같은 추가 필터가 포함됩니다.

* 에셋을 찾으면 AEM UI의 데스크탑 작업을 사용하여 데스크탑의 에셋에 액세스합니다.

### AEM 데스크탑 앱을 사용하여 연 자산 업데이트 {#updating-assets-opened-using-aem-desktop-app}

AEM Assets에서 로컬 네트워크 공유로 매핑된 위치에서 자산을 직접 편집하는 경우 데스크탑에 저장할 때마다 자산이 AEM에 업로드됩니다. 또한 AEM은 버전을 만들고 렌디션을 생성합니다.

AEM에 저장된 에셋에 업데이트가 필요한 경우:

* 승인 프로세스에서 사소한 수정 요청과 같은 **작은 업데이트**&#x200B;의 경우:

   * 파일을 체크 아웃하고 데스크탑에서 엽니다.

   * 파일을 업데이트합니다.

   * 업데이트된 버전을 저장합니다. 에셋이 업데이트되고, 비교할 원본 버전이 타임라인에 표시됩니다.

* 작은 창의적 WIP 주기가 필요한 변경 요청과 같은 **주요 업데이트**&#x200B;의 경우:

   * 표시 옵션을 사용하여 데스크탑에서 적절한 폴더를 엽니다.

   * 매핑된 AEM Assets 공유 외부의 WIP 폴더에 파일을 복사합니다(예: Adobe Creative Cloud 데스크탑 앱과 동기화된 폴더에 파일 복사).

   * 파일을 작업하고 간헐적으로 저장합니다. 변경 사항이 AEM Assets에 저장되지 않습니다.

   * 편집이 완료되면 AEM에서 매핑된 파일을 이동, 복사 또는 저장하여 새 버전으로 업로드합니다.

## 네트워크 성능 {#network-performance}

AEM 데스크탑 앱에 대한 훌륭한 사용자 경험은 안정적인 네트워크 연결과 잘 조정된 서버, 특히 에셋 업로드 및 업데이트에 의존합니다. 이러한 권장 사항은 조직의 네트워크/IT 팀을 위한 것입니다.

### 네트워크 고려 사항 {#network-considerations}

AEM Assets 네트워크 구성에 대한 모범 사례를 이해하려면 [자산을 대량 마이그레이션하는 방법](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/assets/administer/assets-migration-guide) 문서로 이동하십시오. 사용자를 위한 AEM 데스크탑 앱 환경을 최적화하는 데 도움이 되는 몇 가지 중요한 측면은 다음과 같습니다.

* **올바르게 구성된 Dispatcher 사용**. 추가 보안을 위해 AEM Dispatcher을 사용하고, Dispatcher 뒤의 AEM에 대한 [AEM 데스크톱 앱 연결에 대해 구성되어 있는지 확인하십시오](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher)

* **대역폭 저장**. Finder를 사용하여 마운트된 저장소를 탐색할 때 Mac에서 Finder의 아이콘 미리 보기를 끄는 것이 좋습니다. Finder는 미리 보기를 생성하도록 각 파일을 요청하고 데스크탑 앱에서 자산을 로컬로 다운로드하고 캐시하도록 합니다. 대역폭을 저장하는 동안 데스크탑의 사용자에 대한 사용자 경험도 감소하므로 큰 에셋이나 제한된 대역폭이 있는 리포지토리에서 작업할 때 수행해야 합니다.

>[!NOTE]
>
>아이콘 미리 보기를 해제하려면 Finder에서 [!UICONTROL View] (으)로 이동하여 [!UICONTROL View Options]을(를) 선택한 다음 [!UICONTROL Show icon preview] 옵션을 선택 취소하십시오. 이 옵션은 현재 폴더에만 적용됩니다. 기본값으로 설정하려면 같은 대화 상자에서 [!UICONTROL Use as default] 옵션을 클릭하십시오.

### 서버 성능 최적화 {#optimizing-server-performance}

AEM Assets 서버를 성능에 맞게 최적화하는 방법을 이해하려면 [AEM Assets 성능 조정 가이드](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/assets/administer/performance-tuning-guidelines)로 이동하십시오. AEM 데스크탑 앱의 서버 성능에 대한 몇 가지 중요한 측면은 자산 업로드에 잘 수행되도록 워크플로 구성을 최적화하는 것입니다.

* **추가 성능 자산 업로드**. [AEM Asset Update 워크플로 모델을 임시 ](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/assets/administer/performance-tuning-guidelines)(으)로 구성하십시오.

* **업로드에 대한 서버 CPU 제한**. 업로드가 모든 CPU를 소모하지 않도록 최대 병렬 워크플로우 작업 매개 변수가 올바르게 설정되었는지 확인합니다.
