---
title: ' [!DNL Experience Manager] 데스크톱 앱 사용'
description: ' [!DNL Adobe Experience Manager] 데스크톱 앱을 사용하여 Win 또는 Mac 데스크톱에서  [!DNL Adobe Experience Manager] DAM 자산을 사용하여 작업하고 다른 응용 프로그램에서 사용합니다.'
feature: Desktop App,Asset Management
source-git-commit: c5aeee9ab636ba7bedff4225172140d59cfe627d
workflow-type: tm+mt
source-wordcount: '1416'
ht-degree: 0%

---


# [!DNL AEM Desktop App]의 Assets 관리 작업 {#assets-management-tasks}

에셋 관리에는 워크플로를 간소화하기 위해 디지털 에셋을 구성, 유지 관리 및 최적화하는 작업이 포함됩니다. 여기에는 파일 복제 및 이름 변경, 빠른 액세스를 위해 폴더 고정 또는 고정 해제, 다양한 레이아웃에서 에셋 보기 등의 작업이 포함됩니다. 이를 통해 효율성을 향상시키고, 자산 추적을 단순화하고, 플랫폼 간에 디지털 자산을 쉽게 검색하고 구성할 수 있습니다.

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

## 새로 추가된 폴더 및 파일 보기 {#view-newly-added-files-folders}

로컬 시스템에서 새로 만든 에셋을 중앙 저장소가 저장된 AEM에 업로드할 수 있습니다. 새로 만든 이러한 자산을 로컬에서 보려면 **[!UICONTROL View]** 드롭다운 메뉴로 이동하여 **[!UICONTROL Show Assets]**&#x200B;을(를) 선택하여 해당 타임라인 및 제목과 함께 모든 업데이트를 보거나 **[!UICONTROL Edited Locally]**&#x200B;을(를) 선택합니다. 두 옵션 모두 로컬에서 편집한 자산을 명시적으로 표시합니다.

## 중복 파일 {#duplicate-files}

원본 파일을 보존하고 유사한 파일을 변경하려는 경우 다른 위치(로컬 및 클라우드)에 파일을 동시에 복제할 수 있습니다. 에셋 간 중복 파일 작업을 통해 수행할 수 있습니다.

AEM Desktop App에서 파일을 복제하려면 아래 단계를 수행합니다.

1. 폴더를 찾아 복제할 자산을 선택합니다.

   ![추가 옵션](assets/more-options1.png)

1. **[!UICONTROL More actions]** ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png)을 클릭하고 ![중복 아이콘](assets/do-not-localize/duplicate.svg) **[!UICONTROL Duplicate File]** 작업을 선택합니다.

1. 중복 파일은 동일한 파일 이름과 콘텐츠로 만들어집니다.

## 에셋 또는 폴더의 제목 변경 {#rename-asset-title}

에셋 또는 폴더의 제목 이름을 변경하려면 아래 단계를 수행하십시오.

1. 이름을 바꿀 자산을 찾습니다. 폴더 이름을 지정할 때 `\ / : * ?  | < > [ ] %`; 같은 특수 문자는 허용되지 않습니다. 포함된 경우 자동으로 하이픈 `-`(으)로 바뀝니다.

1. **[!UICONTROL More actions]** ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png)을 클릭하고 **[!UICONTROL Rename]**&#x200B;을(를) 선택하여 원하는 자산 제목을 추가합니다.


## 폴더 고정 또는 고정 해제 {#pin-unpin-folder}

고정 폴더는 앱 내에서 기본적으로 변경된 사항을 반영하도록 자동으로 동기화됩니다. 빠른 액세스를 위해 아래 단계를 실행하여 폴더를 고정하거나 고정 해제할 수 있습니다.

1. 고정하거나 고정해제할 자산을 찾습니다.

1. **[!UICONTROL More actions]** ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png)을 클릭하고 [!UICONTROL pin]을(를) 선택하여 에셋 또는 폴더를 고정합니다. 또는 [!UICONTROL unpin]을(를) 클릭하여 고정 해제합니다.

   ![폴더 고정 또는 고정 해제](assets/pin-unpin.png)

## 자동 새로 고침 {#auto-refresh}

자동 새로 고침 기능은 콘텐츠를 실시간으로 자동으로 업데이트하므로 페이지를 수동으로 다시 로드하지 않고 항상 최신 정보를 확인할 수 있습니다. 업데이트된 자산 목록을 가져오려면 아래 단계를 실행하여 자산을 자동으로 새로 고칩니다.

1. AEM 데스크탑 앱을 엽니다.

1. 메뉴 표시줄에서 ![새로 고침 아이콘](assets/do-not-localize/refresh.png)을 클릭하여 업데이트를 가져옵니다.

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

## 양도된 자산 목록 {#list-of-transferred-assets}

특정 세션에서 전송된 에셋 목록을 보려면 [에셋 업로드 [!DNL Experience Manager]](#upload-and-add-new-assets-to-aem)를 참조하십시오.

## 고급 워크플로우: 동일한 파일에 대해 공동 작업을 수행하고 편집 충돌 방지 {#adv-workflow-collaborate-avoid-conflicts}

공동 작업 환경에서는 여러 사용자가 동일한 에셋 세트에서 작업할 수 있으므로 버전 관리 충돌이 발생할 수 있습니다. 충돌을 방지하려면 다음 모범 사례를 따르십시오.

* [!UICONTROL Open]을(를) 클릭하여 자산을 편집하지 마십시오. 파일 시스템 폴더에서 을 열어 로컬로 다운로드한 에셋을 편집하지 마십시오. 다른 사용자는 자산이 편집되고 있다는 것을 알지 못합니다.
* 자산을 편집하려면 항상 [!UICONTROL Edit]을(를) 클릭하십시오. 기본 애플리케이션에서 에셋을 열고 에셋에 잠금 아이콘을 추가하여 다른 사용자가 에셋이 편집 중임을 알 수 있도록 합니다.
* [!UICONTROL Toggle Check-in]을(를) 클릭하지 않고 실수로 편집을 시작하는 경우 [!UICONTROL Edit]을(를) 클릭합니다. 이 기능은 에셋에 잠금 아이콘을 추가합니다. 나중에 자산을 편집할 계획이지만 다른 사용자가 자산을 편집하지 않도록 하려면 [!UICONTROL Toggle Check-in]을(를) 클릭하여 자산을 잠급니다.
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

1. [!DNL Experience Manager]에 배치된 자산이 있는 INDD 파일을 가까이 두십시오. 이러한 INDD 파일을 만드는 방법은 [그래픽 넣기](https://helpx.adobe.com/kr/indesign/using/placing-graphics.html)를 참조하십시오.
1. 데스크톱 앱 내에서 **[!UICONTROL Edit]**&#x200B;에 배치된 자산이 있는 INDD 파일을 [!DNL Experience Manager]합니다.
1. 이 앱은 InDesign 파일과 연결된 자산을 다운로드합니다. InDesign이 문서를 열면 링크가 해석되고 에셋이 다운로드되고 에셋이 InDesign 문서에 표시됩니다.
1. InDesign 파일에 새 그래픽을 넣으려면 자산에 대해 **[!UICONTROL Reveal File]** 작업을 사용하십시오. 이 작업은 자산을 로컬로 다운로드하고 Windows 탐색기 또는 Mac Finder에서 로컬 네트워크 공유 위치를 엽니다.
1. 드러난 에셋을 InDesign 문서에 배치합니다. 이렇게 하면 문서에 링크가 만들어집니다.
1. InDesign 문서에서 편집을 완료하면 저장한 후 데스크톱 앱을 사용하여 [!DNL Experience Manager]에 업로드합니다.

## 다음 단계 {#next-steps}

* [비디오로 Adobe Experience Manager 데스크톱 앱 시작](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 오른쪽 사이드바에서 사용 가능한 [!UICONTROL Edit this page] ![페이지 편집](assets/do-not-localize/edit-page.png) 또는 [!UICONTROL Log an issue] ![GitHub 문제 만들기](assets/do-not-localize/github-issue.png)를 사용하여 문서 피드백을 제공하십시오

* [고객 지원 센터](https://experienceleague.adobe.com/ko?support-solution=General#support) 문의

<!--* Provide product feedback using the [!UICONTROL Feedback] option available on the AEM Desktop App user interface>-->

>[!MORELIKETHIS]
>
>* [사용자 인터페이스 이해](/help/using/user-interface.md)
>* [시작 안내서](/help/using/get-started.md).
