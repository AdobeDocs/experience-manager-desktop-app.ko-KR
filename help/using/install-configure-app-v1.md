---
title: 데스크탑 앱 v1.10 설치 및 구성
description: ' [!DNL Assets] 서버에서 작동하도록  [!DNL Experience Manager] 데스크톱 앱 버전 1.10을 설치 및 구성하고 자산을 데스크톱에 드라이브로 탑재하도록 매핑합니다.'
exl-id: 7f3bdfb1-d345-4e48-b020-6e06531f46f2
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# [!DNL Experience Manager] 데스크톱 앱 v1.10 설치 및 구성 {#install-and-configure-aem-desktop-app}

[!DNL Experience Manager] 데스크톱 앱을 사용하면 로컬 데스크톱에서 [!DNL Experience Manager] 내의 자산에 쉽게 액세스할 수 있으며 모든 데스크톱 응용 프로그램에서 사용할 수 있습니다. Assets은 Mac Finder 또는 Windows 탐색기에서 볼 수 있으며 데스크톱 앱에서 편집되고 변경 사항이 [!DNL Experience Manager]에 다시 저장되며 업로드 시 새 버전이 만들어집니다.

이 통합을 통해 다양한 역할이 Assets의 조직 내에서 자산을 중앙에서 관리하고 Creative Cloud 및 기타 애플리케이션에서 액세스하며 브랜딩을 비롯한 다양한 표준을 쉽게 준수할 수 있습니다.

[!DNL Experience Manager] 데스크톱 앱을 사용하려면,

* [!DNL Experience Manager] 서버 버전이 [!DNL Experience Manager] 데스크톱 앱과 호환되는지 확인하십시오. [호환성 매트릭스](release-notes-of-v1.md#compatibilitymatrix)를 참조하십시오.

* 애플리케이션을 다운로드하여 설치합니다.

* 몇 가지 자산을 사용하여 연결을 테스트합니다. [데스크톱에서 자산 액세스 및 열기](use-app-v1.md#openondesktop)를 참조하세요.

## 시스템 요구 사항, 사전 요구 사항 및 다운로드 링크 {#system-requirements-prerequisites-and-download-links}

자세한 내용은 [[!DNL Experience Manager] 데스크톱 앱 릴리스 정보](release-notes-of-v1.md)를 참조하세요.

## 앱을 설치하고 [!DNL Experience Manager] 서버에 연결 {#install-and-connect-aem-desktop-app-to-aem-server}

자세한 내용은 [데스크톱 앱 설치 및 연결 [!DNL Experience Manager] 서버 [!DNL Experience Manager] 연결](use-app-v1.md#installandconnect)을 참조하세요.

>[!NOTE]
>
>[!DNL Experience Manager] 데스크톱 앱의 인스턴스는 한 번에 하나만 설치하고 활성화할 수 있습니다.

## 파일 처리 {#file-handling}

데스크탑 앱에서 마운트한 네트워크 공유 위치에서 파일을 변경하면 파일이 두 단계로 해당 위치에 저장됩니다. 첫 번째 단계에서는 파일이 로컬에 저장됩니다. 사용자는 전송이 완료될 때까지 기다리지 않고 파일을 저장하고 파일 작업을 계속할 수 있습니다.

두 번째 단계에서는 미리 정의된 지연(예: 30초) 후 업데이트된 파일을 [!DNL Experience Manager] 서버에 업로드합니다. 이 작업은 백그라운드에서 수행됩니다. 업로드 작업의 상태를 보려면 에셋 상태 보기 옵션을 사용하십시오.

1. Assets에 에셋을 업로드합니다.

1. 도구 모음에서 [!DNL Experience Manager] 데스크톱 앱 아이콘을 클릭합니다.

1. 메뉴에서 에셋 상태 보기 옵션을 선택합니다.

1. 대화 상자에서 업로드 작업 상태를 검토합니다.

>[!NOTE]
>
>[!DNL Experience Manager] 데스크톱 앱에서 최대 40GB의 자산을 처리할 수 있습니다.

## Dispatcher의 [!DNL Experience Manager] 인스턴스에 연결 {#connect-to-an-aem-instance-behind-a-dispatcher}

Assets API의 복사 및 이동 메서드를 사용하려면 다음 추가 헤더를 [!DNL Experience Manager]에 전달해야 합니다.

* X-대상
* X-깊이
* X-덮어쓰기

[!DNL Experience Manager] 데스크톱이 기본 포트가 포함된 URL을 사용하여 [!DNL Experience Manager]에 연결합니다. 따라서 Dispatcher 구성의 `virtualhosts` 설정에는 기본 포트 번호가 포함되어야 합니다. `virtualhosts` 구성에 대한 자세한 내용은 [가상 호스트 식별](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#identifying-virtual-hosts-virtualhosts)을 참조하십시오.

이러한 추가 헤더를 전달하도록 Dispatcher을 구성하는 방법에 대한 자세한 내용은 [HTTP 헤더 지정](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#specifying-the-http-headers-to-pass-through-clientheaders)을 참조하십시오.

### 프록시 지원 {#proxy-support}

[!DNL Experience Manager] 데스크톱 앱은 시스템의 사전 정의된 프록시를 사용하여 HTTPS를 통해 인터넷에 연결합니다. 앱은 추가 인증이 필요하지 않은 네트워크 프록시만 사용하여 연결할 수 있습니다.

Windows용 프록시 서버 설정(인터넷 옵션 > LAN 설정)을 구성하거나 수정하는 경우 [!DNL Experience Manager] 데스크톱 앱을 다시 시작하여 변경 내용을 적용하십시오.

>[!NOTE]
>
>프록시 구성은 데스크탑 앱을 시작할 때만 적용됩니다. 변경 사항을 적용하려면 앱을 닫았다가 다시 실행하십시오.

프록시에 인증이 필요한 경우 IT 팀은 프록시 서버 설정의 Experience Manager Assets URL을 사용하여 응용 프로그램 트래픽을 전달할 수 있습니다.

## 에셋 정보 대화 상자 맞춤화 {#customize-the-asset-info-dialog}

다음 구성 요소 중 하나 또는 둘 다를 오버레이하여 자산 정보 대화 상자를 사용자 정의할 수 있습니다.

* `/libs/dam/gui/content/assets/moreinfo`의 Granite 사용자 인터페이스 페이지입니다.

* `/libs/dam/gui/components/admin/moreinfo`의 HTL `/css/javascript` 구성 요소입니다.

오버레이되는 구성 요소는 맞춤화의 특성에 따라 다릅니다. 에셋 정보 대화 상자의 일부로 표시되는 구성 요소를 변경하려면 Granite 사용자 인터페이스 페이지를 오버레이합니다. 대화 상자의 HTML, CSS 또는 JavaScript 콘텐츠를 변경하려면 HTL 구성 요소를 오버레이합니다.

## 캐시 관리 {#manage-cache}

Windows에서 캐시는 `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`에 있습니다. 여기서 은(는) 데스크톱 앱에 구성된 [!DNL Experience Manager] 호스트의 인코딩된 버전입니다. 예를 들어 `http://localhost:4502`은(는) `http%3A%2F%2Flocalhost%3A4502%2F`(으)로 나타납니다.

macOS X에서 유사한 디렉터리는 `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`에 있습니다.

### 캐시 관리를 위한 인앱 옵션 {#in-app-option-to-manage-cache}

로컬 캐싱에 사용할 수 있는 디스크 공간의 크기를 제어할 수 있습니다. Assets 서버의 아티팩트는 보다 원활한 경험을 위해 로컬에 캐시됩니다. 요구 사항에 맞게 기본값을 변경할 수 있습니다. 또한 캐시를 지우면 모든 에셋을 새로 가져올 수 있습니다. 원하는 옵션을 설정하려면 응용 프로그램의 아이콘을 클릭하고 **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**&#x200B;을(를) 클릭합니다. ****

>[!NOTE]
>
>캐시를 지우면 저장되지 않은 변경 사항이 유지됩니다. [!DNL Experience Manager] 서버에 체크 인되지 않은 자산은 유지되며 삭제되지 않습니다.

### Windows에서 캐시 위치 변경 {#change-location-of-cache-on-windows}

[!DNL Experience Manager] 데스크톱 앱에 대한 캐시의 기본 위치는 다음과 같습니다.

* Windows에서는 `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`입니다.

* Mac에서 `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`.

`EncodedAEMEndpoint`은(는) 앱에서 구성한 [!DNL Experience Manager] 끝점 URL입니다. 값이 [!DNL Experience Manager] 서버의 대상 URL의 인코딩된 버전입니다. 예를 들어 응용 프로그램에서 `http://localhost:4502`을(를) 대상으로 하는 경우 디렉터리 이름은 `http%3A%2F%2Flocalhost%3A4502`입니다. 이 예제의 캐시 디렉터리에 대한 Windows 경로는 `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`입니다.

응용 프로그램을 다른 폴더 또는 다른 드라이브로 지정하려면 응용 프로그램의 구성 파일을 편집합니다.

1. 앱의 설치 디렉토리로 이동합니다. Windows의 기본 위치는 `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`입니다.

1. 텍스트 편집기로 `Adobe Experience Manager Desktop.exe.config` 파일을 편집합니다.

   이 파일에 변경 사항을 저장하려면 관리자 권한이 필요합니다.

1. 문자열 &quot;ProxyCacheRoot&quot;를 검색합니다. 해당 값이 캐시 위치 `%LocalAppData%\Adobe\AssetsCompanion\Cache`(으)로 설정되어 있습니다. 이 값을 유효한 경로로 변경하기만 하면 됩니다.

   >[!NOTE]
   >
   >앱에서 *&lt;인코딩된 AEM 끝점>* 하위 디렉터리를 자동으로 만듭니다. 이 동작은 구성할 수 없습니다.

>[!MORELIKETHIS]
>
* [데스크톱 앱 소개 [!DNL Experience Manager] 2}를 시청하십시오(5분 43초).](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)
* [사용 [!DNL Experience Manager] 데스크톱 앱](use-app-v1.md).
* [문제 해결 [!DNL Experience Manager] 데스크톱 앱](troubleshoot-app-v1.md).
