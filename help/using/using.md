---
title: ' [!DNL Experience Manager] 데스크톱 앱 사용'
description: ' [!DNL Adobe Experience Manager] 데스크톱 앱을 사용하여 Win 또는 Mac 데스크톱에서  [!DNL Adobe Experience Manager] DAM 자산을 사용하여 작업하고 다른 응용 프로그램에서 사용합니다.'
mini-toc-levels: 1
feature: Desktop App,Asset Management
exl-id: fa19d819-231a-4a01-bfd2-6bba6fec2f18
source-git-commit: fb11b41020a4c2b2c40e8adcde822c65a7fe8985
workflow-type: tm+mt
source-wordcount: '4734'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager] 데스크톱 앱 사용 {#use-aem-desktop-app-v2}

[!DNL Adobe Experience Manager] 데스크톱 앱을 사용하여 로컬 데스크톱의 [!DNL Adobe Experience Manager] DAM 저장소에 저장된 디지털 자산에 액세스합니다. 그런 다음 모든 데스크탑 애플리케이션에서 이러한 자산을 사용할 수 있습니다. 데스크탑 애플리케이션에서 자산을 로컬로 열고 편집할 수 있습니다. 변경한 후 버전 제어로 [!DNL Experience Manager]에 업로드하여 다른 사용자와 업데이트를 공유하십시오. 새 파일과 폴더 계층을 [!DNL Experience Manager]에 업로드하고 폴더를 만들고 [!DNL Experience Manager] DAM에서 에셋 또는 폴더를 삭제할 수도 있습니다.

통합을 통해 조직의 다양한 역할이 [!DNL Experience Manager Assets]에서 자산을 중앙에서 관리하고 Windows 또는 macOS의 기본 응용 프로그램에서 로컬 데스크톱의 자산에 액세스할 수 있습니다.

로그아웃한 후 또는 처음으로 응용 프로그램을 열 때 [!DNL Experience Manager] 서버의 URL을 `https://[aem-server-url]:[port]/` 형식으로 제공하십시오. 그런 다음 [!UICONTROL Connect] 옵션을 선택합니다. 앱을 서버에 연결하기 위한 자격 증명을 제공합니다.

[!DNL Adobe Experience Manager] 데스크톱 앱을 사용하여 수행하는 주요 작업은 다음과 같습니다.

![데스크톱 앱 [!DNL Experience Manager]을(를) 사용하여 수행할 수 있는 워크플로 및 작업](assets/aem_desktop_app_usecases_v2.png "데스크톱 앱  [!DNL Adobe Experience Manager] 을(를) 사용하여 수행할 수 있는 워크플로 및 작업")

<!--Download [this](assets/aem_desktop_app_usecases_print.pdf) print-ready PDF file.-->

## 데스크탑 앱 작동 방식 {#how-app-works2}

응용 프로그램 사용을 시작하기 전에 [앱 작동 방식](release-notes.md#how-app-works)을 이해하세요. 또한 다음 용어를 숙지하십시오.

* **[!UICONTROL Desktop Actions]**: Assets 웹 인터페이스에서 브라우저의 내부 자산 위치를 탐색하거나 기본 데스크톱 응용 프로그램에서 편집할 자산을 체크아웃하고 열 수 있습니다. 이러한 작업은 웹 인터페이스에서 사용할 수 있으며, 데스크톱 앱 기능을 사용합니다. [데스크톱 작업을 사용하는 방법](using.md#desktopactions-v2)을 참조하세요.

* 파일 상태가 **[!UICONTROL Cloud Only]**&#x200B;입니다. 이러한 자산은 로컬 컴퓨터에서 다운로드되지 않았으며 [!DNL Experience Manager] 서버에서만 사용할 수 있습니다.

* 파일 상태가 **[!UICONTROL Available locally]**&#x200B;입니다. 자산이 다운로드되어 로컬 컴퓨터에서 그대로 사용할 수 있습니다. 자산은 변경되지 않습니다.

* 파일 상태가 **[!UICONTROL Edited locally]**&#x200B;입니다. 이러한 자산은 로컬에서 수정되고 변경 내용은 [!DNL Experience Manager] 서버에 업로드된 상태로 유지됩니다. 업로드한 후에는 상태가 [!UICONTROL Available locally]&#x200B;(으)로 변경됩니다. [자산 편집](using.md#edit-assets-upload-updated-assets)을 참조하세요.

* 파일 상태는 **[!UICONTROL Editing conflict]**&#x200B;입니다. 사용자와 다른 사용자가 동시에 자산을 편집하는 경우, 앱은 편집 충돌이 발생했음을 나타냅니다. 또한 앱은 변경 내용을 유지하거나 취소할 수 있는 옵션을 제공합니다. [편집 충돌을 피하는 방법](using.md#adv-workflow-collaborate-avoid-conflicts)을 참조하세요.

* 파일 상태는 **[!UICONTROL Modified remotely]**&#x200B;입니다. 앱은 다운로드한 에셋이 [!DNL Experience Manager] 서버에서 변경되었는지 여부를 나타냅니다. 이 앱은 최신 버전을 다운로드하고 로컬 복사본을 업데이트하는 옵션도 제공합니다. [편집 충돌을 피하는 방법](using.md#adv-workflow-collaborate-avoid-conflicts)을 참조하세요.

* **[!UICONTROL Check-out]**: 파일을 편집하고 있거나 편집하려는 경우 상태를 체크 아웃으로 전환합니다. 앱과 [!DNL Experience Manager] 웹 인터페이스의 에셋에 잠금 아이콘을 추가합니다. 잠금 아이콘은 동일한 에셋을 동시에 편집하면 편집 충돌이 발생하는 것을 방지하기 위해 다른 사용자에게 표시됩니다.

* **[!UICONTROL Check-in]**: 편집 충돌을 일으키지 않고 다른 사용자가 편집할 수 있는 안전한 자산으로 표시합니다. 변경 사항을 업로드할 때 잠금 아이콘이 자동으로 제거됩니다. 체크 인 상태를 전환하면 잠금 아이콘도 제거되지만 Adobe에서는 변경 사항을 업로드하지 않고 수동으로 체크 인하지 않는 것이 좋습니다. 변경 사항을 취소하는 경우 체크 인을 수동으로 전환합니다.

* **[!UICONTROL Open]** 작업: 에셋을 열어 기본 애플리케이션에서 미리 보십시오. Adobe에서는 이 작업을 사용하여 에셋을 편집하지 않는 것이 좋습니다. 그 이유는 자산을 체크아웃하지 않기 때문입니다. 한편 다른 사용자가 편집을 하면 편집 충돌이 발생할 수 있습니다.

* **[!UICONTROL Open with]** 작업: &quot;다음으로 열기&quot; 기능을 사용하면 기본 응용 프로그램이 아닌 특정 응용 프로그램으로 파일을 열 수 있습니다. 이 기능은 기본 프로그램을 선택하거나, 다른 형식으로 파일에 액세스하거나, 기본 앱의 문제를 해결하거나, 여러 프로그램을 사용하여 작업하는 데 유용합니다. 설정을 영구적으로 변경하지 않고 기본 응용 프로그램을 일시적으로 재정의할 수 있어 유연성을 제공합니다.

* **[!UICONTROL Open In Web]** 작업: [!DNL Experience Manager] 웹 인터페이스에서 자산을 보려면 웹에서 여십시오. [!DNL Experience Manager] 인터페이스에서 메타데이터 업데이트 또는 에셋 검색과 같은 더 많은 워크플로를 시작할 수 있습니다.

* **[!UICONTROL Edit]** 작업: 작업을 사용하여 이미지를 수정합니다. [!UICONTROL Edit]을(를) 클릭하면 에셋이 체크아웃되고 에셋에 잠금 아이콘이 추가됩니다. [편집]을 클릭한 후 자산을 편집하지 않으려면 [!UICONTROL Toggle check-in]을(를) 클릭합니다. [!DNL Experience Manager] DAM 폴더 계층 구조에서 자산을 삭제하거나 이름을 바꾸거나 이동하려면 편집 작업이 아닌 [!DNL Experience Manager] 웹 인터페이스 작업을 사용합니다.

* **[!UICONTROL Download]** 작업: 로컬 컴퓨터에 자산을 다운로드합니다. 지금 에셋을 다운로드하고 나중에 편집할 수 있습니다. 오프라인으로 작업하고 나중에 변경 사항을 업로드할 수 있습니다. Assets은 파일 시스템의 캐시 폴더에 다운로드됩니다.

* **[!UICONTROL Reveal File]** 또는 **[!UICONTROL Reveal Folder]** 작업: 에셋을 로컬 캐시 폴더로 다운로드하는 동안 앱은 로컬 네트워크 드라이브를 모방합니다. 각 에셋에 대한 로컬 경로를 제공합니다. 이 경로를 알려면 앱에서 적절한 표시 옵션을 사용합니다. Creative Cloud 애플리케이션에 에셋을 배치하려면 표시 작업이 필요합니다. [자산 배치](using.md#place-assets-in-native-documents)를 참조하십시오.

* **[!UICONTROL Delete]** 작업: [!DNL Experience Manager] DAM 저장소에서 자산을 삭제합니다. 이 작업은 Experience Manager 서버에서 에셋의 원본 복사본을 삭제합니다. 로컬 자산에 대한 수정 사항만 취소하려면 [변경 내용 취소](using.md#edit-assets-upload-updated-assets)를 참조하십시오.

* **[!UICONTROL Upload Changes]**: [!DNL Experience Manager] 서버에 명시적으로 업로드하는 경우에만 데스크톱 앱에서 업데이트된 에셋을 업로드합니다. 편집 내용을 저장하면 변경 내용이 로컬 컴퓨터에만 저장됩니다. 업로드할 때 에셋이 자동으로 체크 인되고 잠금 아이콘이 제거됩니다. [자산 편집](using.md#edit-assets-upload-updated-assets)을 참조하세요.

## [!DNL Experience Manager] 웹 인터페이스에서 데스크톱 작업 사용 {#desktopactions-v2}

브라우저의 [!DNL Assets] 사용자 인터페이스 내에서 자산 위치를 탐색하거나 데스크탑 애플리케이션에서 편집할 자산을 체크아웃하고 열 수 있습니다. 이러한 옵션은 [!UICONTROL Desktop Actions]이라고 하며 기본적으로 활성화되어 있지 않습니다. 활성화하려면 다음 단계를 수행합니다.

1. [!DNL Assets] 콘솔의 도구 모음에서 **[!UICONTROL User]** 아이콘을 클릭합니다.
1. **[!UICONTROL My Preferences]**&#x200B;을(를) 클릭하여 **[!UICONTROL Preferences]** 대화 상자를 표시합니다.

1. [!UICONTROL User Preferences] 대화 상자에서 **[!UICONTROL Show Desktop Actions For Assets]**&#x200B;을(를) 선택한 다음 **[!UICONTROL Accept]**&#x200B;을(를) 클릭합니다.

   ![데스크톱 작업을 사용하려면 Assets에 대한 데스크톱 작업 표시](assets/enable_desktop_actions.png)

   *그림: 데스크톱 작업을 사용하려면 [!UICONTROL Show Desktop Actions For Assets]을(를) 선택하십시오.*

## 자산 보기 {#view-assets}

AEM Desktop App을 사용하면 네 가지 서로 다른 보기에서 에셋을 볼 수 있습니다.

* **[!UICONTROL Show Assets]:** 모든 자산을 볼 수 있습니다.
* **[!UICONTROL Show Collections]:** 기본 AEM 애플리케이션에서 만든 모든 컬렉션을 볼 수 있습니다. [컬렉션](#collections-desktop-app)을 더 보세요.
* **[!UICONTROL Edited Locally]:** 로컬에서 수정된 모든 자산을 표시할 수 있습니다. 이 보기에서 여러 에셋을 추가하고 업로드할 수 있습니다.
* **[!UICONTROL Asset transfers]:** 기본 앱에서 로컬 또는 그 반대로 전송되는 모든 자산을 볼 수 있습니다.
* **[!UICONTROL Pinned items]:** 고정된 모든 항목을 볼 수 있습니다.

AEM Desktop App에 있는 다양한 자산 보기 중에서 선택하려면 다음 단계를 수행하십시오.

1. AEM 데스크탑 앱을 엽니다.

1. 오른쪽 상단의 보기 드롭다운으로 이동합니다. 사용 가능한 보기 중에서 하나를 선택합니다.

   ![폴더 고정 또는 고정 해제](assets/view-pinned-assets.png)

### 새로 추가된 폴더 및 파일 보기 {#view-newly-added-files-folders}

로컬 시스템에서 새로 만든 에셋을 중앙 저장소가 저장된 AEM에 업로드할 수 있습니다. 새로 만든 이러한 자산을 로컬에서 보려면 **[!UICONTROL View]** 드롭다운 메뉴로 이동하여 **[!UICONTROL Show Assets]**&#x200B;을(를) 선택하여 해당 타임라인 및 제목과 함께 모든 업데이트를 보거나 **[!UICONTROL Edited Locally]**&#x200B;을(를) 선택합니다. 두 옵션 모두 로컬에서 편집한 자산을 명시적으로 표시합니다.

## 에셋 검색 및 미리 보기 {#browse-search-preview-assets}

데스크톱 응용 프로그램 내에서 [!DNL Experience Manager] 저장소에서 사용 가능한 자산을 모두 찾아보고 검색하고 미리 볼 수 있습니다. 앱에서 다음을 시도해 보십시오.

1. 폴더를 탐색하여 모든 에셋의 작은 썸네일과 함께 폴더에서 사용할 수 있는 에셋에 대한 몇 가지 기본 정보를 확인합니다.

   ![DAM 파일 및 폴더 찾아보기](assets/browse_folder_da2.png "DAM 파일 및 폴더 찾아보기")

1. 개별 에셋에 대한 더 많은 정보와 더 큰 썸네일을 보려면 파일 이름을 클릭합니다.

   ![에셋 및 작업에 대한 더 큰 미리 보기](assets/large_preview_actions_da2.png "에셋 및 작업에 대한 더 큰 미리 보기")

1. 로컬로 파일을 다운로드하고 기본 응용 프로그램에서 보거나 편집하려면 **[!UICONTROL Open]** 또는 **[!UICONTROL Edit]**&#x200B;을(를) 각각 클릭하십시오.
1. 키워드를 사용하여 검색하여 [!DNL Experience Manager] 저장소에서 관련 자산을 찾습니다. `?` 및 `*`을(를) 와일드카드로 사용합니다. 이러한 와일드카드는 각각 단일 문자 또는 여러 문자를 대체합니다. 필요에 따라 결과를 필터링하고 정렬합니다.

   ![별표 와일드카드를 사용한 샘플 검색](assets/search_wildcard_da2.png "별표 와일드카드를 사용한 샘플 검색")

   ![별표 와일드카드를 사용한 다른 샘플 검색](assets/search_wildcard2_da2.png "다른 배치의 별표 와일드카드를 사용한 다른 샘플 검색")

>[!NOTE]
>
>이 앱은 에셋의 제목이나 파일 이름뿐만 아니라 여러 메타데이터 필드에서 검색 기준을 일치시켜 에셋을 표시합니다.

## 자산 관리 {#assets-management}

에셋 관리에는 워크플로를 간소화하기 위해 디지털 에셋을 구성, 유지 관리 및 최적화하는 작업이 포함됩니다. 여기에는 파일 복제 및 이름 변경, 빠른 액세스를 위해 폴더 고정 또는 고정 해제, 다양한 레이아웃에서 에셋 보기 등의 작업이 포함됩니다. 이를 통해 효율성을 향상시키고, 자산 추적을 단순화하고, 플랫폼 간에 디지털 자산을 쉽게 검색하고 구성할 수 있습니다.

### 중복 파일 {#duplicate-files}

원본 파일을 보존하고 유사한 파일을 변경하려는 경우 다른 위치(로컬 및 클라우드)에 파일을 동시에 복제할 수 있습니다. 에셋 간 중복 파일 작업을 통해 수행할 수 있습니다.

AEM Desktop App에서 파일을 복제하려면 아래 단계를 수행합니다.

1. 폴더를 찾아 복제할 자산을 선택합니다.

   ![중복 파일](assets/more-options.png)

1. **[!UICONTROL More actions]** ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png)을 클릭하고 ![중복 아이콘](assets/do-not-localize/duplicate.svg) **[!UICONTROL Duplicate File]** 작업을 선택합니다.

1. 중복 파일은 동일한 파일 이름과 콘텐츠로 만들어집니다.

### 에셋의 제목 변경 {#rename-asset-title}

에셋의 제목을 변경하려면 아래 단계를 수행하십시오.

1. 이름을 바꿀 자산을 찾습니다.

1. **[!UICONTROL More actions]** ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png)을 클릭하고 **[!UICONTROL Rename]**&#x200B;을(를) 선택하여 원하는 자산 제목을 추가합니다.

<!--1. Click **[!UICONTROL More actions]** ![More actions icon](assets/do-not-localize/more2_da2.png) and select **[!UICONTROL open in web]** to open the asset in its native application.

1. Go to asset details. Under [!UICONTROL Basic] tab, go to title and enter the text.-->

### 폴더 고정 또는 고정 해제 {#pin-unpin-folder}

빠른 액세스를 위해 아래 단계를 실행하여 폴더를 고정하거나 고정 해제할 수 있습니다.

1. 고정하거나 고정해제할 자산을 찾습니다.

1. **[!UICONTROL More actions]** ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png)을 클릭하고 [!UICONTROL pin]을(를) 선택하여 에셋 또는 폴더를 고정합니다. 또는 [!UICONTROL unpin]을(를) 클릭하여 고정 해제합니다.

   ![폴더 고정 또는 고정 해제](assets/pin-unpin.png)

### 자동 새로 고침 {#auto-refresh}

자동 새로 고침 기능은 콘텐츠를 실시간으로 자동으로 업데이트하므로 페이지를 수동으로 다시 로드하지 않고 항상 최신 정보를 확인할 수 있습니다. 업데이트된 자산 목록을 가져오려면 아래 단계를 실행하여 자산을 자동으로 새로 고칩니다.

1. AEM 데스크탑 앱을 엽니다.

1. 메뉴 표시줄에서 ![새로 고침 아이콘](assets/do-not-localize/refresh.png)을 클릭하여 업데이트를 가져옵니다.

## 자산 다운로드 {#download-assets}

로컬 파일 시스템에서 에셋을 다운로드할 수 있습니다. 앱은 [!DNL Experience Manager] 서버에서 자산을 가져와서 로컬 파일 시스템에 동일한 복사본을 저장합니다.

옵션을 보려면 **[!UICONTROL More actions]** ![추가 옵션 아이콘](assets/do-not-localize/more2_da2.png)을 클릭하고 다운로드하려면 ![다운로드 아이콘](assets/do-not-localize/download_cloud_da2.png)을 클릭하십시오.

![에셋에 대한 다운로드 옵션](assets/download_option_da2.png "에셋에 대한 다운로드 옵션")

>[!NOTE]
>
>큰 파일 또는 많은 파일을 다운로드하거나 업로드할 때 애플리케이션은 에셋 및 폴더에 대한 작업을 끕니다. 다운로드 또는 업로드가 완료되면 작업을 사용할 수 있습니다.

대기열 크기가 크거나 네트워크 문제가 있는 경우 여러 자산을 다운로드하면 성능이 저하될 수 있습니다. 또한 폴더를 다운로드할 때 모르는 사이에 많은 에셋을 다운로드용으로 대기열에 넣을 수 있습니다. 대기 시간이 길지 않도록 앱에서 한 번에 다운로드되는 에셋 수를 제한합니다. 구성 방법은 [환경 설정 지정](install-upgrade.md#set-preferences)을 참조하세요. 이 제한 미만이더라도 앱이 겉보기에 큰 폴더를 다운로드하기 전에 확인을 요청할 수 있습니다.

![앱에서 상대적으로 많은 에셋의 다운로드를 확인](assets/download_confirmation_da2.png "앱에서 상대적으로 많은 에셋의 다운로드를 확인")

폴더를 선택하고 다운로드하면 응용 프로그램은 [!DNL Experience Manager]의 폴더에 직접 저장된 자산만 다운로드합니다. 하위 폴더에서 에셋을 자동으로 다운로드하지는 않습니다.

## 데스크탑에서 자산 열기 {#openondesktop-v2}

기본 애플리케이션에서 볼 원격 자산을 열 수 있습니다. 자산이 로컬 폴더로 다운로드됩니다. 그런 다음 파일 형식과 연결된 기본 애플리케이션에서 실행됩니다. 기본 응용 프로그램을 변경하여 Mac 또는 Windows에서 특정 파일 형식(확장명)을 열 수 있습니다.

자산 메뉴에서 **[!UICONTROL Open]**&#x200B;을(를) 클릭합니다. 에셋이 로컬로 다운로드되고 기본 애플리케이션에서 열립니다. 상태 표시줄에서 대형 에셋의 다운로드 진행률 및 전송 속도를 확인합니다.

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>예상되는 변경 내용이 앱에 반영되지 않으면 새로 고침 아이콘 ![새로 고침 아이콘](assets/do-not-localize/refresh.png)을 클릭하거나 앱 인터페이스를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Refresh]**&#x200B;을(를) 클릭합니다. 더 큰 규모의 다운로드나 업로드가 진행되는 동안에는 작업을 사용할 수 없습니다.

에셋의 로컬 다운로드 폴더를 열려면 ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png)을 클릭하고 ![표시 아이콘](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** 작업을 클릭합니다.

## 컬렉션 {#collections-desktop-app}

AEM Desktop App을 사용하면 [보기](#view-collections-desktop-app), [다운로드](#download-collections-desktop-app) 및 [!DNL Adobe Experience Manager Assets] 응용 프로그램에서 만들어진 컬렉션을 검색할 수 있습니다.

### 컬렉션 보기 {#view-collections-desktop-app}

다음 단계를 실행하여 데스크탑 앱에서 컬렉션을 봅니다.

1. AEM 데스크톱 앱을 열고 [자산 보기](#view-assets)(으)로 이동합니다.

1. **[!UICONTROL Show Collections]**&#x200B;을(를) 선택합니다. 기본 애플리케이션에서 사용할 수 있는 컬렉션이 표시됩니다.

   ![컬렉션 데스크톱 앱](assets/collections-desktop-app.png)

### 컬렉션 다운로드 {#download-collections-desktop-app}

다음 단계를 실행하여 데스크탑 앱에서 컬렉션을 다운로드합니다.

1. [컬렉션 보기](#view-collections-desktop-app)와 같이 1단계와 2단계를 수행합니다.

1. 다운로드하려는 컬렉션에서 추가 작업 ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png)(으)로 이동합니다.

1. 특정 컬렉션을 다운로드하려면 **[!UICONTROL Download]**&#x200B;을(를) 클릭하십시오.

## 메타데이터 스키마로 폴더 만들기 {#create-folder-with-metadata-schema}

AEM 데스크탑 앱을 사용하면 새 폴더를 만드는 동안 메타데이터를 할당할 수 있습니다. 이렇게 하려면 다음 단계를 실행합니다.

1. 디렉터리 만들기 아이콘 ![폴더 추가 아이콘](assets/do-not-localize/add-folder.svg)(으)로 이동합니다. **[!UICONTROL Create Directory]** 화면이 나타납니다.

1. 다음 세부 정보를 추가합니다.
   * 폴더의 **[!UICONTROL Name]**&#x200B;입니다.
   * 폴더의 메타데이터 계층 구조를 선택하려면 **[!UICONTROL Folder Metadata Schema]**&#x200B;을(를) 선택하고, 폴더에 메타데이터를 연결하지 않으려면 **[!UICONTROL none]**&#x200B;을(를) 선택하십시오.

1. 계속 진행하려면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하십시오.

## 기본 문서에 에셋 사용 또는 배치 {#place-assets-in-native-documents}

경우에 따라 에셋을 기본 문서에 배치할 때 Windows 탐색기 또는 Mac Finder의 파일에 액세스합니다. 로컬로 다운로드한 파일의 파일 시스템 위치로 이동하려면 ![표시 아이콘](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** 옵션을 사용합니다.

![자산에 대한 파일 표시](assets/revealfile_action_da2.png "자산에 대한 파일 표시")

로컬 컴퓨터에서 파일 또는 폴더를 미리 선택한 상태로 Windows 탐색기 또는 Mac Finder를 열려면 **[!UICONTROL Reveal File]** 또는 **[!UICONTROL Reveal Folder]**&#x200B;을(를) 클릭합니다. 예를 들어 이 옵션은 로컬 파일 배치 또는 연결을 지원하는 기본 응용 프로그램에 [!DNL Experience Manager] 파일을 배치하는 데 유용합니다. Adobe InDesign에 파일을 배치하는 방법을 보려면 [그래픽 배치](https://helpx.adobe.com/indesign/using/placing-graphics.html)를 참조하십시오.

**[!UICONTROL Reveal File]** 작업은 로컬 네트워크 공유를 엽니다. 로컬에서 사용할 수 있는 에셋만 표시됩니다. 즉, 앱을 사용하여 공개, 다운로드 또는 열기/편집한 에셋을 표시합니다. 로컬 네트워크 공유가 [!DNL Experience Manager]에 변경 내용을 업로드하지 않습니다. 변경 내용을 업로드하려면 앱에서 **[!UICONTROL Upload Changes]** 또는 **[!UICONTROL Upload]** 작업을 명시적으로 사용하십시오.

>[!NOTE]
>
>[!DNL Experience Manager] 데스크톱 앱 v1.x와의 이전 버전과의 호환성을 위해, 로컬 네트워크 공유에서 표시된 파일을 제공하고 로컬에서 사용 가능한 파일만 노출합니다. 표시된 파일의 데스크탑 경로는 앱 v1.x에서 만든 경로와 동일합니다.

>[!CAUTION]
>
>기본 응용 프로그램에서 자산을 편집할 때 **[!UICONTROL Reveal File]** 옵션을 사용하지 마십시오. 대신 **[!UICONTROL Edit]** 작업을 사용하십시오. 자세한 내용은 [고급 워크플로: 동일한 파일에 대해 공동 작업 및 편집 충돌 방지](#adv-workflow-collaborate-avoid-conflicts)를 참조하십시오.

## 에셋을 편집하고 업데이트된 에셋을 [!DNL Experience Manager]에 업로드 {#edit-assets-upload-updated-assets}

변경한 후 업데이트된 자산을 [!DNL Experience Manager] 서버에 업로드하려면 편집할 자산을 여십시오. 다른 사용자의 편집과 충돌을 방지하려면 앱을 사용하여 편집 세션을 시작하십시오. 편집을 시작하기 전에 에셋에 다른 사용자가 에셋을 편집하고 있음을 나타내는 잠금 아이콘이 없는지 확인합니다.

에셋을 편집하려면 에셋을 검색하거나 에셋의 위치를 찾습니다. ![기타 아이콘](assets/do-not-localize/more2_da2.png)을 클릭하고 **[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.

다음 두 상황에서 다른 사용자의 편집과 충돌하지 않도록 자산을 잠그려면 **[!UICONTROL Toggle Check-out]**&#x200B;을(를) 사용하십시오.

* 자산을 먼저 체크아웃하지 않고 편집을 시작했습니다(자산을 열기만 하면 됨).
* 에셋 편집을 곧 시작하고 다른 사용자가 편집하지 않도록 하려는 경우

편집을 완료하면 변경된 에셋에 대한 **[!UICONTROL Edited Locally]** 상태가 앱에 표시됩니다. 변경 내용을 [!DNL Experience Manager]에 업로드할 때까지 자산에 저장된 모든 변경 내용이 로컬 전용입니다. 개별 또는 몇 개의 에셋을 하나씩 업로드하려면 에셋 옵션에서 **[!UICONTROL Upload Changes]**&#x200B;을(를) 클릭합니다. [!DNL Experience Manager]에 자산의 버전을 만듭니다. [!DNL Assets]의 웹 인터페이스를 사용하면 [타임라인 보기](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/using/activity-stream)에서 자산 내역을 볼 수 있습니다.

![앱의 변경 내용 업로드 옵션](assets/upload_changes_single1_da2.png "앱의 변경 내용 업로드 옵션")

![자산의 미리 보기를 크게 볼 때 변경 내용 업로드 옵션](assets/upload_changes_single2_da2.png "자산의 미리 보기를 크게 볼 때 변경 내용 업로드 옵션")

공동 편집에 대한 모범 사례는 [고급 워크플로우: 동일한 파일에 대해 공동 작업하고 편집 충돌을 피하십시오](#adv-workflow-collaborate-avoid-conflicts)를 참조하십시오.

다음과 같은 경우 로컬 자산에 대한 변경 사항 및 편집 내용을 취소할 수 있습니다. **[!UICONTROL Discard Changes]**&#x200B;를 클릭합니다.

* 변경 내용을 [!DNL Experience Manager]에 로컬로 저장하지 않으려는 경우
* 일부 변경 내용을 저장한 후 원래 에셋에서 변경 작업을 시작합니다.
* 더 이상 필요하지 않으므로 자산 편집을 중지합니다.

필요한 경우 체크 아웃을 전환합니다. 업데이트된 자산은 로컬 캐시 폴더에서 제거되고, 편집하거나 열 때 다시 다운로드됩니다.

## [!DNL Experience Manager]에 새 자산 업로드 및 추가 {#upload-and-add-new-assets-to-aem}

사용자는 DAM 저장소에 새 에셋을 추가할 수 있습니다. 예를 들어 사진 촬영에서 [!DNL Experience Manager] 리포지토리에 많은 사진을 추가하려는 에이전시 사진작가 또는 계약자일 수 있습니다. [!DNL Experience Manager]에 새 콘텐츠를 추가하려면 앱의 상단 표시줄에서 ![클라우드에 업로드 옵션](assets/do-not-localize/upload_to_cloud_da2.png)을 선택합니다. 로컬 파일 시스템에서 자산 파일을 찾은 다음 **[!UICONTROL Select]**&#x200B;을(를) 클릭합니다. 또는 에셋을 업로드하려면 애플리케이션 인터페이스에서 파일이나 폴더를 드래그합니다. Windows에서 앱 내의 폴더에 자산을 드래그하면 자산이 폴더에 업로드됩니다. 업로드하는 데 시간이 오래 걸리는 경우 앱에 진행률 표시줄이 표시됩니다.

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

로컬 파일 시스템에서 폴더 또는 개별 파일을 업로드할 수 있습니다. 업로드 시 폴더의 계층 구조가 유지됩니다. 자산을 일괄적으로 업로드하기 전에 [일괄 업로드](#bulk-upload-assets)를 참조하십시오.

특정 세션에서 전송된 자산 목록을 보려면 **[!UICONTROL View]** > **[!UICONTROL Assets transfers]**&#x200B;을(를) 클릭합니다. 목록을 사용하면 현재 세션의 파일 전송을 보고 신속하게 확인할 수 있습니다.

![특정 세션에서 전송된 에셋 목록](assets/assets_transfered_da2.png "특정 세션에서 전송된 에셋 목록")

**[!UICONTROL Preferences]** > **[!UICONTROL Upload acceleration]** 설정에서 업로드 동시성(가속)을 제어할 수 있습니다. 동시성이 높으면 일반적으로 업로드 속도가 빨라지지만 리소스가 많이 소모되고 로컬 컴퓨터의 처리 능력이 더 많이 소모될 수 있습니다. 시스템이 느려진 경우 더 낮은 동시성 값을 사용하여 업로드를 다시 시도합니다.

>[!NOTE]
>
>전송 목록이 지속적이지 않으며 앱을 종료한 후 다시 열면 사용할 수 없습니다.

<!--### Upload local file to AEM {#upload-local-file-to-aem}-->


### 자산 이름의 특수 문자 관리 {#special-characters-in-filename}

레거시 앱에서 리포지토리에서 만든 노드 이름은 사용자가 제공한 폴더 이름의 공백과 대/소문자를 유지합니다. 현재 응용 프로그램에서 v1.10 앱의 노드 이름 지정 규칙을 에뮬레이션하려면 [!UICONTROL Preferences]에서 [!UICONTROL Use legacy conventions when creating nodes for assets and folders]을(를) 사용하도록 설정하십시오. [앱 환경 설정](/help/using/install-upgrade.md#set-preferences)을 참조하세요. 이 레거시 환경 설정은 기본적으로 비활성화되어 있습니다.

>[!NOTE]
>
>이 앱은 다음 이름 지정 규칙을 사용하여 저장소의 노드 이름만 변경합니다. 앱에서 자산의 `Title`을(를) 그대로 유지합니다.

<!-- TBD: Do NOT use this table.

| Where do characters occur | Characters | Legacy preference | Renaming convention | Example |
|---|---|---|---|---|
| In file name extension | `.` | Enabled or disabled | Retained as is | NA |
| File or folder name | `. / : [ ] | *` | Enabled or disabled | Replaced with a `-` (hyphen) | `myimage.jpg` remains as is and `my.image.jpg` changes to `my-image.jpg`. |
| Folder name | `% ; # , + ? ^ { } "` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | `% # ? { } &` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Whitespaces | Enabled or disabled | Retained as is | NA |
| Folder name | Whitespaces | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Uppercase characters | Disabled | Retained as is | tbd |
| Folder name | Uppercase characters | Disabled | Replaced with a `-` (hyphen) | tbd |
-->

| 문자 ‡ | 앱의 이전 환경 설정 | 파일 이름에 발생할 때 | 폴더 이름에서 발생하는 경우 | 예 |
|---|---|---|---|---|
| `. / : [ ] \| *` | 활성화 또는 비활성화 | `-`(하이픈)으로 대체되었습니다. 파일 이름 확장명의 `.`(점)은 그대로 유지됩니다. | `-`(하이픈)으로 대체되었습니다. | `myimage.jpg`은(는) 그대로 유지되며 `my.image.jpg`이(가) `my-image.jpg`(으)로 변경됩니다. |
| `% ; # , + ? ^ { } "` 및 공백 | ![선택 취소 아이콘](assets/do-not-localize/deselect-icon.png) 비활성화됨 | 공백은 유지됩니다 | `-`(하이픈)으로 대체되었습니다. | `My Folder.`에서 `my-folder-`(으)로 변경되었습니다. |
| `# % { } ? & .` | ![선택 취소 아이콘](assets/do-not-localize/deselect-icon.png) 비활성화됨 | `-`(하이픈)으로 대체되었습니다. | 나. | `#My New File.`에서 `-My New File-`(으)로 변경되었습니다. |
| 대문자 | ![선택 취소 아이콘](assets/do-not-localize/deselect-icon.png) 비활성화됨 | 케이스는 그대로 유지됩니다. | 소문자로 변경되었습니다. | `My New Folder`에서 `my-new-folder`(으)로 변경되었습니다. |
| 대문자 | ![선택 확인 아이콘](assets/do-not-localize/selection-checked-icon.png) 활성화됨 | 케이스는 그대로 유지됩니다. | 케이스는 그대로 유지됩니다. | 나. |

‡ 문자 목록은 공백으로 구분된 목록입니다.

<!-- TBD: Check if the following is to be included in the footnote.

Do not use &#92;&#92; in the names of files and &#92;&#116; &#38; in the names of folders. 
-->


<!-- TBD: Securing the below presentation of the same content in a comment.

**File names**

| Characters | Replaced by |
|---|---|
| &#35; &#37; &#123; &#63; &#125; &#38; &#46; &#47; &#58; &#91; &#124; &#93; &#42; | hyphen (-) |
| whitespaces | whitespaces are retained |
| capital case | casing is retained |

>[!CAUTION]
>
>Avoid using &#92;&#92; in file names.

**Folder names**

| Characters | Replaced by |
|---|---|
| Characters | Replaced by |
| &#37; &#59; &#35; &#44; &#43; &#63; &#94; &#123; &#123; &#34; &#46; &#47; &#59; &#91; &#93; &#124; &#42; | hyphen (-) |
| whitespaces | hyphen (-) |
| capital case | lower case |

>[!CAUTION]
>
>Avoid using &#92;&#92; &#92;&#116; &#38; in folder names.

>[!NOTE]
>
>If you enable [!UICONTROL Use legacy conventions when creating nodes for assets and folders] in app [!UICONTROL Preferences], then the app emulates v1.10 app behavior when uploading folders. In v1.10, the node names created in the repository respect spaces and casing of the folder names provided by the user. For more information, see [app Preferences](/help/using/install-upgrade.md#set-preferences).

-->

## 여러 자산을 사용한 작업 {#work-with-multiple-assets}

사용자는 한 번에 모든 편집 내용을 업로드하거나 몇 번의 클릭으로 중첩된 폴더를 업로드하는 등의 작업을 사용하여 여러 에셋으로 쉽게 작업하고 관리할 수 있습니다.

### 큰 폴더 찾아보기 {#browse-large-folders}

많은 에셋이 포함된 폴더를 사용하여 작업할 때 스크롤하여 더 많은 에셋을 볼 수 있습니다. 키보드를 사용하여 스크롤하려면 탭을 몇 번 눌러 맨 위에 있는 에셋을 선택합니다. 강조 표시된 에셋이 언제 선택되었는지 확인합니다. 이제 아래쪽 화살표 키를 사용하여 에셋 목록을 이동합니다.

### 선택한 자산에 대한 빠른 작업 {#quick-actions-for-selected-assets}

몇 개의 에셋에 대한 축소판을 클릭하여 에셋을 선택합니다. 모든 에셋을 선택하려면 앱의 상단 표시줄에서 확인란을 클릭합니다. 선택한 모든 에셋에 일괄적으로 적용할 수 있는 작업 세트는 앱 하단의 도구 모음에 표시됩니다.

![맨 아래의 도구 모음에 선택한 자산과 관련된 작업이 표시됩니다](assets/actions_bottom_toolbar1_da2.png "맨 아래의 도구 모음에 선택한 자산에 대한 일반적인 작업이 표시됩니다")

![선택 항목에 대한 일반 작업이 없을 때 도구 모음에 작업이 없습니다](assets/actions_bottom_toolbar2_da2.png "선택 항목에 대해 일반 작업을 사용할 수 없을 때 도구 모음에 작업이 표시되지 않습니다.")

하단의 도구 모음에서 사용할 수 있는 작업은 선택한 파일의 상태에 따라 다릅니다. 예를 들어 **[!UICONTROL Edited Locally]**&#x200B;개의 파일만 선택하는 경우 **[!UICONTROL Upload Changes]** 아이콘이 표시됩니다. **[!UICONTROL Edited locally]**&#x200B;과(와) **[!UICONTROL Cloud only]**&#x200B;을(를) 혼합하여 선택하면 **[!UICONTROL Upload Changes]** 작업을 사용할 수 없습니다.

### 편집된 모든 이미지 찾기 {#find-all-edited-images}

이 응용 프로그램에서는 로컬에서 다운로드한 다음 수정한 모든 파일에 빠르게 액세스할 수 있도록 **[!UICONTROL Edited locally]**(이)라는 보기를 제공합니다([!UICONTROL Open] 또는 [!UICONTROL Edit] 작업 사용). 앱을 사용하면 몇 번의 클릭으로 로컬에서 편집한 모든 자산을 선택하고 변경 사항을 업로드할 수 있습니다. 이 보기는 편집 충돌이 있는 로컬로 편집된 에셋도 표시합니다.

![로컬에서 편집한 모든 자산을 보려면 필터링](assets/edited_locally_filter_da2.png "예를 들어 편집 일괄 업로드를 위해 로컬에서 편집한 모든 자산을 보려면 필터링")

### 자산 일괄 업로드 {#bulk-upload-assets}

사진작가나 광고 기획사와 같은 사용자 또는 조직은 사진 촬영, 리터치 또는 더 큰 세트에서 선택 등의 활동 중에 수많은 지역 자산을 만들 수 있습니다. 이러한 작업은 대개 [!DNL Experience Manager] 외부에서 수행됩니다. 이러한 대용량 로컬 폴더를 데스크톱 앱에서 바로 [!DNL Assets]에 업로드할 수 있습니다. 폴더 계층은 유지되고 중첩된 모든 하위 폴더와 포함된 에셋이 업로드됩니다. 업로드된 에셋은 동일한 서버의 다른 사용자도 즉시 사용할 수 있습니다. Assets은 백그라운드에서 업로드되므로 작업이 웹 브라우저 세션에 연결되어 있지 않습니다.

![데스크톱에서 여러 로컬 폴더를 [!DNL Experience Manager]](assets/upload_local_folders_da2.png "데스크톱에서 여러 로컬 폴더를 Experience Manager으로 일괄 업로드")

업로드한 후 예상되는 변경 내용이 앱에 반영되지 않으면 새로 고침 아이콘 ![새로 고침 아이콘](assets/do-not-localize/refresh.png)을 클릭합니다.

>[!NOTE]
>
>업로드 기능을 사용하여 두 개의 [!DNL Experience Manager] 배포 간에 자산을 마이그레이션하지 마십시오. 대신 [마이그레이션 안내서](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide)를 참조하세요.

### 양도된 자산 목록 {#list-of-transferred-assets}

특정 세션에서 전송된 에셋 목록을 보려면 [에셋 업로드 [!DNL Experience Manager]](#upload-and-add-new-assets-to-aem)를 참조하십시오.

## 고급 워크플로: [!DNL Assets] 웹 인터페이스에서 시작 {#adv-workflow-start-from-aem-ui}

필요한 경우 Assets 웹 인터페이스에서 워크플로우를 시작합니다. 데스크톱 앱은 데스크톱 작업을 사용하여 요청할 때 인계할 [!DNL Experience Manager]과(와) 통합됩니다.

웹 인터페이스에서 워크플로우를 시작하는 특별한 경우는 자산 검색입니다. Assets 사용자 인터페이스의 Omnisearch 표시줄은 풍부하고 고급 검색 환경을 제공합니다. 먼저 웹에서 원하는 자산을 찾은 다음 [!UICONTROL Desktop Actions]을(를) 사용하여 앱에서 워크플로를 시작할 수 있습니다. 일부 샘플 사례에는 패싯을 사용하여 검색 결과를 필터링하거나, Adobe Stock에서 라이선스가 부여된 특정 에셋을 찾거나, 웹 인터페이스에서 더 나은 검색을 수행할 수 있도록 조직에서 구현한 사용자 지정이 포함됩니다.

Assets 웹 인터페이스에서 다음 작업을 시도할 때 데스크탑 앱 기능이 사용됩니다.

* [!UICONTROL Open], [!UICONTROL Edit] 및 [!UICONTROL Reveal]을(를) 허용하는 [!UICONTROL Desktop Actions]
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

## 고급 워크플로우: 동일한 파일에 대해 공동 작업을 수행하고 편집 충돌 방지 {#adv-workflow-collaborate-avoid-conflicts}

공동 작업 환경에서는 여러 사용자가 동일한 에셋 세트에서 작업할 수 있으므로 버전 관리 충돌이 발생할 수 있습니다. 충돌을 방지하려면 다음 모범 사례를 따르십시오.

* [!UICONTROL Open]을(를) 클릭하여 자산을 편집하지 마십시오. 파일 시스템 폴더에서 을 열어 로컬로 다운로드한 에셋을 편집하지 마십시오. 다른 사용자는 자산이 편집되고 있다는 것을 알지 못합니다.
* 자산을 편집하려면 항상 [!UICONTROL Edit]을(를) 클릭하십시오. 기본 애플리케이션에서 에셋을 열고 에셋에 잠금 아이콘을 추가하여 다른 사용자가 에셋이 편집 중임을 알 수 있도록 합니다.
* [!UICONTROL Edit]을(를) 클릭하지 않고 실수로 편집을 시작하는 경우 [!UICONTROL Toggle Check-in]을(를) 클릭합니다. 이 기능은 에셋에 잠금 아이콘을 추가합니다. 나중에 자산을 편집할 계획이지만 다른 사용자가 자산을 편집하지 않도록 하려면 [!UICONTROL Toggle Check-in]을(를) 클릭하여 자산을 잠급니다.
* 에셋을 편집하기 전에 다른 사용자가 에셋을 편집하고 있지 않은지 확인하십시오. 에셋에서 잠금 아이콘을 찾습니다.
* 편집을 완료한 후 모든 변경 사항을 업로드한 다음 에셋을 체크 인합니다.

![편집 충돌 상태](assets/edits_conflicts_status_da2.png "편집 충돌 상태")

로컬로 다운로드한 자산이 [!DNL Experience Manager] 서버에서 업데이트된 경우 앱에 **[!UICONTROL Modified remotely]** 상태가 표시됩니다. 각각 [!UICONTROL Remove] 또는 [!UICONTROL Update]을(를) 클릭하여 로컬 복사본을 제거하거나 로컬 복사본을 새로 고칠 수 있습니다. 대화 상자의 링크를 통해 자산의 두 버전을 모두 볼 수 있습니다.

![자산을 원격으로 수정할 때 충돌을 해결하는 옵션](assets/modified_remotely_dialog_da2.png "자산을 원격으로 수정할 때 충돌을 해결하는 옵션")

로컬에서 편집하고 있는 자산이 서버에서 사용자 모르게 업데이트되는 경우 앱에 **[!UICONTROL Editing Conflict]** 상태가 표시됩니다. 변경 내용 중 하나를 유지할 수 있습니다. 업데이트 유지(**[!UICONTROL Keep Mine]** 클릭) 및 다른 사용자의 편집 내용을 삭제하거나 다른 사용자의 업데이트를 준수하여 자신의 업데이트(**[!UICONTROL Overwrite Mine]**)를 삭제합니다.

![편집 충돌 해결 옵션](assets/editing_conflict_dialog_da2.png "편집 충돌 해결 옵션")

## 고급 워크플로우: InDesign 파일에 자산 배치 및 연결 {#adv-workflow-place-assets-indesign}

[!DNL Experience Manager] 데스크톱 앱을 사용하여 연결된 자산이 있는 파일을 열면 자산이 미리 다운로드되어 기본 응용 프로그램에 배치된 것으로 나타납니다. 이 워크플로가 작동하려면 기본 응용 프로그램에서 로컬 자산에 대한 링크 배치를 지원해야 하며 [!DNL Experience Manager]에서 서버측 참조에 대한 이진 파일의 이러한 링크 해결을 지원해야 합니다.

[!DNL Experience Manager] 데스크톱 앱은 Adobe InDesign, Adobe Illustrator 및 Adobe Photoshop과 같은 몇 가지 Adobe Creative Cloud 데스크톱 응용 프로그램 및 파일 형식을 사용하여 이 워크플로를 지원합니다. 워크플로를 사용하면 지원되는 Creative Cloud 파일을 효율적으로 작업할 수 있습니다. 사용자 A가 InDesign 파일에 자산을 추가하고 [!DNL Experience Manager]&#x200B;(으)로 체크 인하면 사용자 B가 해당 파일에 속하지 않더라도 파일에 있는 자산을 볼 수 있습니다. 자산은 사용자 B의 컴퓨터에 로컬로 다운로드됩니다.

>[!NOTE]
>
>데스크탑 앱은 Windows의 모든 드라이브에 매핑할 수 있습니다. 그러나 원활한 작업을 위해 기본 드라이브 문자를 변경하지 마십시오. 동일한 조직의 사용자가 다른 드라이브 문자를 사용하는 경우 다른 사용자가 배치한 에셋을 볼 수 없습니다. 경로가 변경되므로 배치된 에셋을 가져오지 않습니다. 배치된 자산은 이진 파일(예: INDD)에 계속 배치된 상태로 유지되며 제거되지 않습니다.

이 워크플로우의 제한 사항을 알아보려면 [시스템 요구 사항 및 지원되는 버전](release-notes.md)을 참조하십시오.

이미지 에셋 및 InDesign으로 이 워크플로우를 시도하려면 다음 단계를 수행합니다.

1. [!DNL Experience Manager]에 배치된 자산이 있는 INDD 파일을 가까이 두십시오. 이러한 INDD 파일을 만드는 방법은 [그래픽 넣기](https://helpx.adobe.com/indesign/using/placing-graphics.html)를 참조하십시오.
1. 데스크톱 앱 내에서 [!DNL Experience Manager]에 배치된 자산이 있는 INDD 파일을 **[!UICONTROL Edit]**&#x200B;합니다.
1. 이 앱은 InDesign 파일과 연결된 자산을 다운로드합니다. InDesign이 문서를 열면 링크가 해석되고 에셋이 다운로드되고 에셋이 InDesign 문서에 표시됩니다.
1. InDesign 파일에 새 그래픽을 넣으려면 자산에 대해 **[!UICONTROL Reveal File]** 작업을 사용하십시오. 이 작업은 자산을 로컬로 다운로드하고 Windows 탐색기 또는 Mac Finder에서 로컬 네트워크 공유 위치를 엽니다.
1. 드러난 에셋을 InDesign 문서에 배치합니다. 이렇게 하면 문서에 링크가 만들어집니다.
1. InDesign 문서에서 편집을 완료하면 저장한 후 데스크톱 앱을 사용하여 [!DNL Experience Manager]에 업로드합니다.

## 고급 워크플로우: 로컬에서 에셋 다운로드 {#adv-workflow-download-assets-locally}

앱은 [!DNL Experience Manager] 서버에서 로컬 파일 시스템으로 자산을 자주 다운로드합니다. 다운로드에는 대역폭과 디스크 공간이 사용됩니다. 시나리오를 알면 다운로드가 완료될 때까지 기다리는 시간을 최적화하는 데 도움이 될 수 있습니다.

온디맨드 앱 내에서 자산을 다운로드할 수 있습니다. [자산 다운로드](#download-assets)를 참조하세요.

[!UICONTROL Open] 작업을 사용하여 기본 데스크톱 응용 프로그램에서 자산을 열 때 해당 자산은 로컬에서 아직 사용할 수 없는 경우 로컬로 다운로드됩니다. [자산 열기](#openondesktop-v2)를 참조하세요.

앱 내에서 에셋 또는 폴더의 위치를 표시하면 에셋 또는 폴더가 먼저 로컬로 다운로드된 다음 로컬 네트워크 공유의 시스템에서 열립니다. [자산 열기](#openondesktop-v2)를 참조하세요.

[!UICONTROL Edit] 작업을 사용하여 기본 데스크톱 응용 프로그램에서 자산을 편집할 때 해당 자산은 로컬에서 아직 사용할 수 없는 경우 로컬로 다운로드됩니다. [에셋 편집 및 업데이트된 에셋 업로드 [!DNL Experience Manager]](#edit-assets-upload-updated-assets)를 참조하십시오.

앱이 설치되고 허용되는 경우 [!DNL Experience Manager] 웹 인터페이스에서 [!UICONTROL Desktop Actions]을(를) 사용할 때 작업이 완료됩니다. 앱이 먼저 에셋을 다운로드한 다음 작업을 완료합니다.
