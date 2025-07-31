---
title: ' [!DNL Experience Manager] 데스크톱 앱 사용'
description: ' [!DNL Adobe Experience Manager] 데스크톱 앱을 사용하고 있습니다.'
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---


# 데스크탑에서 자산 열기 {#openondesktop-v2}

기본 애플리케이션에서 볼 원격 자산을 열 수 있습니다. 자산이 로컬 폴더로 다운로드됩니다. 그런 다음 파일 형식과 연결된 기본 애플리케이션에서 실행됩니다. 기본 응용 프로그램을 변경하여 Mac 또는 Windows에서 특정 파일 형식(확장명)을 열 수 있습니다.

자산 메뉴에서 **[!UICONTROL Open]**&#x200B;을(를) 클릭합니다. 에셋이 로컬로 다운로드되고 기본 애플리케이션에서 열립니다. 상태 표시줄에서 대형 에셋의 다운로드 진행률 및 전송 속도를 확인합니다.

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>예상되는 변경 내용이 앱에 반영되지 않으면 새로 고침 아이콘 ![새로 고침 아이콘](assets/do-not-localize/refresh.png)을 클릭하거나 앱 인터페이스를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Refresh]**&#x200B;을(를) 클릭합니다. 더 큰 규모의 다운로드나 업로드가 진행되는 동안에는 작업을 사용할 수 없습니다.

에셋의 로컬 다운로드 폴더를 열려면 ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png)을 클릭하고 ![표시 아이콘](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** 작업을 클릭합니다.

## 기본 문서에 에셋 사용 또는 배치 {#place-assets-in-native-documents}

경우에 따라 에셋을 기본 문서에 배치할 때 Windows 탐색기 또는 Mac Finder의 파일에 액세스합니다. 로컬로 다운로드한 파일의 파일 시스템 위치로 이동하려면 ![표시 아이콘](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** 옵션을 사용합니다.

![자산에 대한 파일 표시](assets/revealfile_action_da2.png "자산에 대한 파일 표시")

로컬 컴퓨터에서 파일 또는 폴더를 미리 선택한 상태로 Windows 탐색기 또는 Mac Finder를 열려면 **[!UICONTROL Reveal File]** 또는 **[!UICONTROL Reveal Folder]**&#x200B;을(를) 클릭합니다. 예를 들어 이 옵션은 로컬 파일 배치 또는 연결을 지원하는 기본 응용 프로그램에 [!DNL Experience Manager] 파일을 배치하는 데 유용합니다. Adobe InDesign에 파일을 배치하는 방법을 보려면 [그래픽 배치](https://helpx.adobe.com/kr/indesign/using/placing-graphics.html)를 참조하십시오.

**[!UICONTROL Reveal File]** 작업은 로컬 네트워크 공유를 엽니다. 로컬에서 사용할 수 있는 에셋만 표시됩니다. 즉, 앱을 사용하여 공개, 다운로드 또는 열기/편집한 에셋을 표시합니다. 로컬 네트워크 공유가 [!DNL Experience Manager]에 변경 내용을 업로드하지 않습니다. 변경 내용을 업로드하려면 앱에서 **[!UICONTROL Upload Changes]** 또는 **[!UICONTROL Upload]** 작업을 명시적으로 사용하십시오.

>[!NOTE]
>
>[!DNL Experience Manager] 데스크톱 앱 v1.x와의 이전 버전과의 호환성을 위해, 로컬 네트워크 공유에서 표시된 파일을 제공하고 로컬에서 사용 가능한 파일만 노출합니다. 표시된 파일의 데스크탑 경로는 앱 v1.x에서 만든 경로와 동일합니다.

>[!CAUTION]
>
>기본 응용 프로그램에서 자산을 편집할 때 **[!UICONTROL Reveal File]** 옵션을 사용하지 마십시오. 대신 **[!UICONTROL Edit]** 작업을 사용하십시오. 자세한 내용은 [고급 워크플로: 동일한 파일에 대해 공동 작업 및 편집 충돌 방지](#adv-workflow-collaborate-avoid-conflicts)를 참조하십시오.

## 다음 단계 {#next-steps}

* [비디오로 Adobe Experience Manager 데스크톱 앱 시작](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 오른쪽 사이드바에서 사용 가능한 [!UICONTROL Edit this page] ![페이지 편집](assets/do-not-localize/edit-page.png) 또는 [!UICONTROL Log an issue] ![GitHub 문제 만들기](assets/do-not-localize/github-issue.png)를 사용하여 문서 피드백을 제공하십시오

* [고객 지원 센터](https://experienceleague.adobe.com/ko?support-solution=General#support) 문의

>[!MORELIKETHIS]
>
>* [사용자 인터페이스 이해](/help/using/user-interface.md)
>* [데스크톱 앱에서 Assets 관리](/help/using/assets-management-tasks.md)
>* [검색](/help/using/search.md)
