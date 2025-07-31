---
title: 시작하기 [!DNL Experience Manager] 데스크톱 앱
description: ' [!DNL Experience Manager] 데스크탑 앱에서 간소화된 워크플로우와 생산성 기능을 통해 콘텐츠 제작 및 게시를 개선하는 방법을 알아봅니다.'
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 0%

---


# [!DNL Adobe Experience Manager] 데스크톱 앱 사용 시작 {#getting-started-desktop-app}

[!DNL Adobe Experience Manager] 데스크톱 앱을 사용하여 로컬 데스크톱의 [!DNL Adobe Experience Manager] DAM 저장소에 저장된 디지털 자산에 액세스합니다. 그런 다음 모든 데스크탑 애플리케이션에서 이러한 자산을 사용할 수 있습니다. 데스크탑 애플리케이션에서 자산을 로컬로 열고 편집할 수 있습니다. 변경한 후 버전 제어로 [!DNL Experience Manager]에 업로드하여 다른 사용자와 업데이트를 공유하십시오. 새 파일과 폴더 계층을 [!DNL Experience Manager]에 업로드하고 폴더를 만들고 [!DNL Experience Manager] DAM에서 에셋 또는 폴더를 삭제할 수도 있습니다.

통합을 통해 조직의 다양한 역할이 [!DNL Experience Manager Assets]에서 자산을 중앙에서 관리하고 Windows 또는 macOS의 기본 응용 프로그램에서 로컬 데스크톱의 자산에 액세스할 수 있습니다.

로그아웃한 후 또는 처음으로 응용 프로그램을 열 때 [!DNL Experience Manager] 서버의 URL을 `https://[aem-server-url]:[port]/` 형식으로 제공하십시오. 그런 다음 [!UICONTROL Connect] 옵션을 선택합니다. 앱을 서버에 연결하기 위한 자격 증명을 제공합니다.

[!DNL Adobe Experience Manager] 데스크톱 앱을 사용하여 수행하는 주요 작업은 다음과 같습니다.

![ 데스크톱 앱을 사용하여 수행할 수 있는 [!DNL Experience Manager]워크플로 및 작업](assets/aem_desktop_app_usecases_v2.png)

## 데스크탑 앱 작동 방식 {#how-app-works2}

응용 프로그램 사용을 시작하기 전에 [앱 작동 방식](release-notes.md#how-app-works)을 이해하세요. 또한 다음 용어를 숙지하십시오.

* **[!UICONTROL Desktop Actions]**: Assets 웹 인터페이스에서 브라우저의 내부 자산 위치를 탐색하거나 기본 데스크톱 응용 프로그램에서 편집할 자산을 체크아웃하고 열 수 있습니다. 이러한 작업은 웹 인터페이스에서 사용할 수 있으며, 데스크톱 앱 기능을 사용합니다.

* 파일 상태가 **[!UICONTROL Cloud Only]**&#x200B;입니다. 이러한 자산은 로컬 컴퓨터에서 다운로드되지 않았으며 [!DNL Experience Manager] 서버에서만 사용할 수 있습니다.

* 파일 상태가 **[!UICONTROL Available locally]**&#x200B;입니다. 자산이 다운로드되어 로컬 컴퓨터에서 그대로 사용할 수 있습니다. 자산은 변경되지 않습니다.

* 파일 상태가 **[!UICONTROL Edited locally]**&#x200B;입니다. 이러한 자산은 로컬에서 수정되고 변경 내용은 [!DNL Experience Manager] 서버에 업로드된 상태로 유지됩니다. 업로드한 후에는 상태가 [!UICONTROL Available locally]&#x200B;(으)로 변경됩니다. [자산 편집](upload-assets.md#edit-assets-upload-updated-assets)을 참조하세요.

* 파일 상태는 **[!UICONTROL Editing conflict]**&#x200B;입니다. 사용자와 다른 사용자가 동시에 자산을 편집하는 경우, 앱은 편집 충돌이 발생했음을 나타냅니다. 또한 앱은 변경 내용을 유지하거나 취소할 수 있는 옵션을 제공합니다. [편집 충돌을 피하는 방법](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts)을 참조하세요.

* 파일 상태는 **[!UICONTROL Modified remotely]**&#x200B;입니다. 앱은 다운로드한 에셋이 [!DNL Experience Manager] 서버에서 변경되었는지 여부를 나타냅니다. 이 앱은 최신 버전을 다운로드하고 로컬 복사본을 업데이트하는 옵션도 제공합니다. [편집 충돌을 피하는 방법](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts)을 참조하세요.

* **[!UICONTROL Check-out]**: 파일을 편집하고 있거나 편집하려는 경우 상태를 체크 아웃으로 전환합니다. 앱과 [!DNL Experience Manager] 웹 인터페이스의 에셋에 잠금 아이콘을 추가합니다. 잠금 아이콘은 동일한 에셋을 동시에 편집하면 편집 충돌이 발생하는 것을 방지하기 위해 다른 사용자에게 표시됩니다.

* **[!UICONTROL Check-in]**: 편집 충돌을 일으키지 않고 다른 사용자가 편집할 수 있는 안전한 자산으로 표시합니다. 변경 사항을 업로드할 때 잠금 아이콘이 자동으로 제거됩니다. 체크 인 상태를 전환하면 잠금 아이콘도 제거되지만 Adobe에서는 변경 사항을 업로드하지 않고 수동으로 체크 인하지 않는 것이 좋습니다. 변경 사항을 취소하는 경우 체크 인을 수동으로 전환합니다.

* **[!UICONTROL Open]** 작업: 에셋을 열어 기본 애플리케이션에서 미리 보십시오. Adobe에서는 이 작업을 사용하여 에셋을 편집하지 않는 것이 좋습니다. 그 이유는 자산을 체크아웃하지 않기 때문입니다. 한편 다른 사용자가 편집을 하면 편집 충돌이 발생할 수 있습니다.

* **[!UICONTROL Edit]** 작업: 작업을 사용하여 이미지를 수정합니다. [!UICONTROL Edit]을(를) 클릭하면 에셋이 체크아웃되고 에셋에 잠금 아이콘이 추가됩니다. [편집]을 클릭한 후 자산을 편집하지 않으려면 [!UICONTROL Toggle check-in]을(를) 클릭합니다. [!DNL Experience Manager] DAM 폴더 계층 구조에서 자산을 삭제하거나 이름을 바꾸거나 이동하려면 편집 작업이 아닌 [!DNL Experience Manager] 웹 인터페이스 작업을 사용합니다.

* **[!UICONTROL Download]** 작업: 로컬 컴퓨터에 자산을 다운로드합니다. 지금 에셋을 다운로드하고 나중에 편집할 수 있습니다. 오프라인으로 작업하고 나중에 변경 사항을 업로드할 수 있습니다. Assets은 파일 시스템의 캐시 폴더에 다운로드됩니다.

* **[!UICONTROL Reveal File]** 또는 **[!UICONTROL Reveal Folder]** 작업: 에셋을 로컬 캐시 폴더로 다운로드하는 동안 앱은 로컬 네트워크 드라이브를 모방합니다. 각 에셋에 대한 로컬 경로를 제공합니다. 이 경로를 알려면 앱에서 적절한 표시 옵션을 사용합니다. Creative Cloud 애플리케이션에 에셋을 배치하려면 표시 작업이 필요합니다. [자산 배치](search.md#place-assets-in-native-documents)를 참조하십시오.

* **[!UICONTROL Open In Web]** 작업: [!DNL Experience Manager] 웹 인터페이스에서 자산을 보려면 웹에서 여십시오. [!DNL Experience Manager] 인터페이스에서 메타데이터 업데이트 또는 에셋 검색과 같은 더 많은 워크플로를 시작할 수 있습니다.

* **[!UICONTROL Delete]** 작업: [!DNL Experience Manager] DAM 저장소에서 자산을 삭제합니다. 이 작업은 Experience Manager 서버에서 에셋의 원본 복사본을 삭제합니다. 로컬 자산에 대한 수정 사항만 취소하려면 [변경 내용 취소](upload-assets.md#edit-assets-upload-updated-assets)를 참조하십시오.

* **[!UICONTROL Upload Changes]**: [!DNL Experience Manager] 서버에 명시적으로 업로드하는 경우에만 데스크톱 앱에서 업데이트된 에셋을 업로드합니다. 편집 내용을 저장하면 변경 내용이 로컬 컴퓨터에만 저장됩니다. 업로드할 때 에셋이 자동으로 체크 인되고 잠금 아이콘이 제거됩니다. [자산 편집](upload-assets.md#edit-assets-upload-updated-assets)을 참조하세요.

## [!DNL Experience Manager] 웹 인터페이스에서 데스크톱 작업 사용 {#desktopactions-v2}

브라우저의 [!DNL Assets] 사용자 인터페이스 내에서 자산 위치를 탐색하거나 데스크탑 애플리케이션에서 편집할 자산을 체크아웃하고 열 수 있습니다. 이러한 옵션은 [!UICONTROL Desktop Actions]이라고 하며 기본적으로 활성화되어 있지 않습니다. 활성화하려면 다음 단계를 수행합니다.

1. [!DNL Assets] 콘솔의 도구 모음에서 **[!UICONTROL User]** 아이콘을 클릭합니다.
1. **[!UICONTROL My Preferences]**&#x200B;을(를) 클릭하여 **[!UICONTROL Preferences]** 대화 상자를 표시합니다.

1. [!UICONTROL User Preferences] 대화 상자에서 **[!UICONTROL Show Desktop Actions For Assets]**&#x200B;을(를) 선택한 다음 **[!UICONTROL Accept]**&#x200B;을(를) 클릭합니다.

   ![데스크톱 작업을 사용하려면 Assets에 대한 데스크톱 작업 표시](assets/enable_desktop_actions1.png)

## [!DNL Assets] 웹 인터페이스에서 시작 {#adv-workflow-start-from-aem-ui}

필요한 경우 Assets 웹 인터페이스에서 워크플로우를 시작합니다. 데스크톱 앱은 데스크톱 작업을 사용하여 요청할 때 인계할 [!DNL Experience Manager]과(와) 통합됩니다.

웹 인터페이스에서 워크플로우를 시작하는 특별한 경우는 자산 검색입니다. Assets 사용자 인터페이스의 Omnisearch 표시줄은 풍부하고 고급 검색 환경을 제공합니다. 먼저 웹에서 원하는 자산을 찾은 다음 [!UICONTROL Desktop Actions]을(를) 사용하여 앱에서 워크플로를 시작할 수 있습니다. 일부 샘플 사례에는 패싯을 사용하여 검색 결과를 필터링하거나, Adobe Stock에서 라이선스가 부여된 특정 에셋을 찾거나, 웹 인터페이스에서 더 나은 검색을 수행할 수 있도록 조직에서 구현한 사용자 지정이 포함됩니다.

Assets 웹 인터페이스에서 다음 작업을 시도할 때 데스크탑 앱 기능이 사용됩니다.

* [!UICONTROL Desktop Actions], [!UICONTROL Open] 및 [!UICONTROL Edit]을(를) 허용하는 [!UICONTROL Reveal]
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] 또는 [!UICONTROL check-in]

예를 들어 앱에서 체크 아웃된 에셋에 사용할 수 있는 웹 인터페이스의 작업은 [!UICONTROL Open], [!UICONTROL Reveal] 및 [!UICONTROL Check in]입니다.

![[!DNL Experience Manager] 웹 인터페이스의 데스크톱 작업](assets/assets_web_actions_da2.png "Experience Manager 웹 인터페이스의 데스크톱 작업")

>[!NOTE]
>
>브라우저에서 [!DNL Adobe Experience Manager] 데스크톱의 시작을 허용하라는 메시지를 표시할 수 있습니다. 매번 중단되지 않고 브라우저에서 앱으로 전송하려면 적절한 확인란을 선택하여 앱을 상속할 수 있도록 합니다.

웹 인터페이스를 사용하여 다음 정보나 워크플로를 찾을 수 없습니다. 웹 인터페이스가 로컬 변경 사항을 추적하지 않고 다음을 인식하지 못하므로 데스크탑 앱을 사용하십시오.

* 파일은 로컬에서 편집됩니다.
* 편집 충돌이 있는 파일과 이를 해결하는 방법.
* 로컬 변경 내용을 [!DNL Experience Manager]에 업로드합니다.
* 로컬에서 사용할 수 있는 파일의 다양한 상태.

반대로 **[!UICONTROL Open In Web]** 작업을 사용하여 데스크톱 앱부터 웹 인터페이스에서 자산을 열 수 있습니다.

## 다음 단계 {#next-steps}

* [비디오로 Adobe Experience Manager 데스크톱 앱 시작](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 오른쪽 사이드바에서 사용 가능한 [!UICONTROL Edit this page] ![페이지 편집](assets/do-not-localize/edit-page.png) 또는 [!UICONTROL Log an issue] ![GitHub 문제 만들기](assets/do-not-localize/github-issue.png)를 사용하여 문서 피드백을 제공하십시오

* [고객 지원 센터](https://experienceleague.adobe.com/?support-solution=General#support) 문의

>[!MORELIKETHIS]
>
>* [사용자 인터페이스 이해](/help/using/user-interface.md)
>* [릴리스 정보 및 알려진 문제](/help/using/release-notes.md)
>* [데스크톱 앱 설치 또는 업그레이드](/help/using/install-upgrade.md)
