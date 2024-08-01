---
title: "[!DNL Adobe Experience Manager] 데스크톱 앱 릴리스 노트"
description: ' [!DNL Adobe Experience Manager] 데스크톱 앱에 대한 릴리스 정보, 개선 사항, 새로운 기능, 호환성 및 다운로드 링크.'
mini-toc-levels: 1
feature: Desktop App,Release Information
exl-id: e058e7a2-fcc8-4ad1-899e-20695db6bc72
source-git-commit: 19f059875a7519cf28628fd801662da7243b077b
workflow-type: tm+mt
source-wordcount: '1955'
ht-degree: 11%

---

# [!DNL Adobe Experience Manager] 데스크톱 앱 릴리스 노트 {#release-notes-v2}

최신 데스크탑 앱 버전 2.3.1의 릴리스 정보는 다음과 같습니다. 릴리스 날짜는 2024년 7월 25일입니다.

최신 버전의 데스크탑 앱에는 다음과 같은 버그 수정 및 개선 사항이 포함되어 있습니다.

* 새 Enterprise Windows Installer는 프로그램 파일 아래에 응용 프로그램을 설치합니다.
* AEM 및 SSO 로그인 중 **기본 인증**&#x200B;을 지원합니다.
* 업로드 작업 중 허용된 구성 가능한 에셋 수.

**지원되는 [!DNL Experience Manager] 버전**&#x200B;은(는) 다음과 같습니다.

* [!DNL Experience Manager]을(를) [!DNL Cloud Service](으)로 설정합니다. [릴리스 정보](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/home)를 참조하세요.
* [!DNL Experience Manager] 6.5.0 이상, Adobe Managed Services(AMS) 또는 온-프레미스. [서비스 팩 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/release-notes/release-notes)를 참조하세요.

[!DNL Adobe Experience Manager] 데스크톱 앱은 다음 **운영 체제**&#x200B;에서 사용할 수 있습니다.

* macOS X 10.14 이상(최신 버그 수정 포함)
* 최신 서비스 팩 및 버그 수정 사항이 포함된 Windows 10.

AEM Desktop App 버전 2.3.1 이상 버전에서는 두 버전의 Windows Installer를 사용할 수 있습니다. 기본 설치 관리자는 사용자의 로컬 앱 데이터 디렉터리 아래에 AEM Desktop App을 설치합니다. Adobe은 대부분의 사용자에게 이 설치 프로세스를 권장합니다. 공유 프로그램 파일 디렉터리 아래에 AEM 데스크톱 앱을 설치하는 Enterprise Windows 설치 프로그램도 사용할 수 있습니다. 이 두 설치 관리자는 기능에 차이점 없이 동일한 버전의 AEM Desktop App을 설치합니다.

지원되는 OS의 **다운로드 URL**&#x200B;은(는) 다음과 같습니다.

| 운영 체제 | [!DNL Experience Manager] as a [!DNL Cloud Service] | [!DNL Experience Manager] 6.x |
|---|---|---|
| macOS (v2.3.1) | [다운로드 링크](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081954149%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=mwSX5ilZL0he2raIx8t5ecQ%2FWuizky4MpcCXX3mEN38%3D&amp;reserved=0) | [다운로드 링크](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081981239%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=LJH3OCFq7yRykN4wU8HN9%2FBXC%2BjfXLJH4QizeFZfRHE%3D&amp;reserved=0) |
| macOS Apple 실리콘(M1)(v2.3.1) | [다운로드 링크](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081965822%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=2YENn0tDduiucogClt6aBZHDOE6dbzBdigq8VQawIO0%3D&amp;reserved=0) | [다운로드 링크](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081986151%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=jCepldg4dMej0%2BrK2mUonXwqsWL8ksE8%2BLMSgsH9qTA%3D&amp;reserved=0) |
| Windows 64비트(v2.3.1) | [다운로드 링크](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081970892%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=sRn2UWW%2Bi7SMEvSO74ZGGvJ40vHh1KhLc7zAfKc37Es%3D&amp;reserved=0) | [다운로드 링크](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081991004%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=aQWZtEK%2F3cWX8n8Au%2FwZ5Zd9xPVo5phvk%2FuF%2Be0HRrE%3D&amp;reserved=0) |
| Windows 64비트 Enterprise(v2.3.1) | [다운로드 링크](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081976350%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=v9C0sLDSkuL%2FMIyae2WkbitJPVgSlAw2BqcaH5Im0uw%3D&amp;reserved=0) | [다운로드 링크](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081995827%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=2btCh0aIrUBiyeG37K9YorvzTeIJOggbq%2FRauUMn4LY%3D&amp;reserved=0) |
| macOS (v2.3.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) |
| macOS Apple 실리콘(M1)(v2.3.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) |
| Windows 64비트(v2.3.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) |
| macOS (v2.2.2) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) |
| macOS Apple 실리콘(M1)(v2.2.2) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) |
| Windows 64비트(v2.2.2) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) |
| macOS (v2.2.1) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) |
| macOS Apple 실리콘(M1)(v2.2.1) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) |
| Windows 64비트(v2.2.1) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) |
| macOS (v2.2.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) |
| macOS Apple 실리콘(M1)(v2.2.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) |
| Windows 64비트(v2.2.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) |
| macOS (v2.1.5.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) |
| Windows 64비트(v2.1.5.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) |
| Windows 32비트(v2.1.5.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) |
| macOS (v2.1.4.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) |
| Windows 64비트(v2.1.4.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) |
| Windows 32비트(v2.1.4.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) |
| macOS (v2.1.3.4) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) |
| Windows 64비트(v2.1.3.4) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) |
| Windows 32비트(v2.1.3.1) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) |

## 다양한 에셋 및 파일 유형 지원 {#support-for-file-types}

응용 프로그램이 기본 작업을 위해 이진 파일을 나타내는 [!DNL Experience Manager]에 저장된 자산을 지원합니다. 기본 데스크탑 애플리케이션에서 열리는 파일은 운영 체제에서 특정 애플리케이션(예: Mac Preview 또는 Adobe Photoshop)에 연결된 특정 파일 유형(예: PNG 또는 JPG)에 따라 다릅니다.

몇 가지 파일 유형은 연결된 자산을 바이너리에 배치하는 것을 지원합니다. 데스크톱 앱을 사용하여 이진 파일을 열 때 자산이 [!DNL Experience Manager] 저장소에 있는 경우 연결된 자산을 미리 다운로드합니다. 현재 지원되는 파일 유형은 다음과 같습니다.

* [!DNL Adobe InDesign]개 파일(INDD 형식)
* [!DNL Adobe Illustrator]개 파일(AI 형식)
* [!DNL Adobe Photoshop]개 파일(PS 형식)

위의 응용 프로그램의 [!DNL Adobe Creative Cloud] 2018 및 [!DNL Adobe Creative Cloud] 2019 버전에서 이 기능이 지원됩니다. 앱에서는 가장 일치하는 방식을 추론하여 연결된 자산의 로컬 데스크톱 경로를 [!DNL Experience Manager] 서버의 URL에 매핑합니다. 몇 가지 가정을 이용합니다.

* 기본 응용 프로그램에 배치된 파일에 대한 경로에는 글로벌 데스크톱 경로([!UICONTROL Reveal] 옵션과 함께 표시된 로컬 네트워크 공유에서 배치됨)가 사용됩니다.

* 경로는 기본 앱에서 파일의 XMP 레코드에 저장합니다.

* [!DNL Experience Manager]이(가) 자산의 메타데이터 레코드 경로가 포함된 XMP 레코드를 추출했습니다.

* 경로가 [!DNL Experience Manager]의 자산에 일치할 수 있습니다. 즉, 배치된 파일이 일치하는 경로 아래의 [!DNL Experience Manager]에도 있습니다.

## 새로운 기능, 개선 사항 및 버그 수정 {#what-is-new}

자세한 내용은 [v2.0의 새로운 기능](introduction.md#whats-new-v2)을 참조하세요.

**앱 v2.3.0의 업데이트**

* IMS 로그인에 대한 지원이 추가되었습니다. IMS 통합을 통해 데스크탑 앱에서 액세스 토큰 새로 고침을 자동으로 수행하여 사용자가 최대 14일 동안 로그인 상태를 유지할 수 있습니다.

* 기업 프록시 및 웹 필터링에 대한 지원이 개선되었습니다.

**앱 v2.2.2의 업데이트**

* (Windows 전용) 데스크탑 앱은 2.2.0 및 2.2.1 릴리스 버전을 설치한 후 빈 화면을 표시합니다.

**앱 v2.2.1의 업데이트**

* **[!UICONTROL Sign In]**&#x200B;을(를) 클릭하면 데스크톱 앱에 세션 시간 초과 오류 메시지가 표시됩니다.

* macOS에서 데스크탑 앱 v2.2.0에 액세스하는 동안 문제가 발생합니다.

* **[!UICONTROL Edited Locally]**&#x200B;을(를) 클릭하여 자산을 정렬할 때 데스크톱 앱에 오류 메시지가 표시됩니다.

**앱 v2.2.0의 업데이트**

* Apple Silicon(M1) 지원

* 데스크탑 앱에 로그온하는 동안 연결 문자열을 기억하는 기능.

**앱 v2.1.5.0의 업데이트**

* 중국어 문자가 포함된 폴더에 있는 파일을 업로드할 때 데스크탑 앱이 응답하지 않습니다(ASSETS-9237).

* 데스크탑 앱은 파일 이름의 점을 대시로 바꿉니다(ASSETS-10955).

**앱 v2.1.4.0의 업데이트**

애플리케이션의 새 버전은 버그 수정을 제공합니다.

**앱 v2.1.3.4의 업데이트**

애플리케이션의 새 버전은 버그 수정을 제공합니다.

**앱 v2.1.3.3의 업데이트**

애플리케이션의 새 버전은 버그 수정을 제공합니다.

**앱 v2.1.3.2의 업데이트**

이 버전의 애플리케이션은 버그 수정을 제공합니다.

**앱 v2.1.3.1의 업데이트**

이 버전에서 수정된 버그는 다음과 같습니다.

* 큰 에셋의 경우에도 에셋 업로드 및 다운로드 속도가 개선되었습니다. 이 릴리스에서는 대용량 파일을 업로드할 때 종종 [!DNL desktop app]에 자산을 업로드하지 못하는 문제를 해결했습니다.

**앱 v2.1.2.0에서 업데이트**

* [!UICONTROL Clear Cookies]에 대한 새 옵션이 응용 프로그램의 기본 메뉴에 추가되었습니다. 서버에서 다른 서버로 연결을 변경하는 등의 잠재적 로그온 문제를 해결하는 데 도움이 됩니다. [연결하기 전에 쿠키 지우기](/help/using/troubleshoot.md#cannot-login-cookies-issue)를 참조하십시오.

* 선택하면 앱에서 로컬 파일 및 폴더 이름과 일치하는 [!DNL Adobe Experience Manager]의 노드 이름을 가진 폴더 및 파일을 업로드할 수 있는 새 옵션이 추가되었습니다. 이 프로세스는 로컬 이름과 업로드된 이름 간의 일관성을 보장합니다.

  이 동작은 데스크탑 앱 버전 1의 기본 동작과 유사합니다. 반면 현재 버전에서는 옵션이 활성화되어 있지 않으면 폴더 이름에서 공백과 `% ; # , + ? ^ { } "` 문자가 폴더 경로의 대시로 바뀝니다. 또한 폴더 경로에서 대문자 문자는 소문자로 변환됩니다. 그러나 파일 이름에서 `# % { } ? &` 문자는 대시로 바뀌지만 공백과 대/소문자는 그대로 유지됩니다. 자세한 내용은 [앱 환경 설정](/help/using/install-upgrade.md#set-preferences) 및 [새 에셋 업로드 및 추가](/help/using/using.md#upload-and-add-new-assets-to-aem)를 참조하십시오.

**앱 v2.1.1.0에서 업데이트**

* 고급 설정을 사용하면 폴더를 업로드할 때 앱에서 v1.10 앱 동작을 에뮬레이션할 수 있습니다. v1.10에서 저장소에서 생성된 노드 이름은 사용자가 제공한 폴더 이름의 공백 및 대소문자를 따릅니다. 버전 2.1에서는 기본 동작이 변경되지 않습니다. 폴더 이름의 여러 공백은 저장소 노드 이름에서 하이픈으로 대체되고 노드 이름은 소문자로 변환됩니다. [앱 환경 설정](/help/using/install-upgrade.md#set-preferences)을 참조하세요.

**앱 v2.1.0.0에서 업데이트**

* 이제 에셋을 업로드하기 위해 Windows 탐색기 또는 Mac Finder에서 직접 애플리케이션 인터페이스의 파일 또는 폴더를 드래그할 수 있습니다. 이 프로세스는 애플리케이션에서 사용할 수 있는 업로드 옵션과 함께 작동합니다. [자산 업로드](/help/using/using.md#upload-and-add-new-assets-to-aem) <!-- CQ-4309527 --> 참조

**앱 v2.0.3에서 업데이트**

이 버전에서 수정된 버그는 다음과 같습니다.

* [!DNL Adobe Experience Manager] 6.5.5.0의 DAM 저장소에 액세스하려는 Windows의 앱 사용자에 대한 로그인 문제를 해결했습니다.

**앱 v2.0.2의 업데이트**

버그 수정 및 업데이트:

* 업로드 가속화 설정을 사용하여 업로드 성능을 높일 수 있습니다. 이 설정을 켜면 앱이 더 많은 로컬 CPU 스레드를 사용하여 더 빠르게 업로드되고 더 많은 리소스를 사용합니다.

* 파일 이름 또는 특정 GB18030 문자가 포함된 경로가 수정되면 에셋이 업로드됩니다. <!-- CQ-4283494 -->

* 관련성을 기준으로 정렬 옵션은 검색 결과에서 다른 정렬 유형으로 전환한 후 사용할 수 있습니다. <!-- CQ-4286874 -->

* 이제 데스크탑 앱은 명시적으로 새로 고치지 않아도 하위 폴더를 나열합니다. <!-- CQ-4285711 -->

* (Windows) 일부 Windows 컴퓨터에서 앱 인터페이스를 사용할 수 없는 드문 문제를 해결했습니다. 인터페이스 요소가 &#39;이동됨&#39; 옆으로 클릭 영역이 왜곡되어 표시되므로 앱 인터페이스를 클릭할 수 없습니다. <!-- CQ-4280785 -->

**앱 v2.0.1의 업데이트**

버그 수정 및 업데이트:

* `%APPDATA%` 경로와 일치하도록 `%Temp%` 디렉터리를 구성하는 옵션을 허용합니다. <!-- CQ-4282665 -->

* 사용자가 Okta SAML 인증을 통해 [!DNL Experience Manager] 작성자에 로그인할 수 있도록 허용합니다. <!-- CQ-4278134 -->

## 설치 지침 {#installation-instructions-v2}

앱을 설치하고 구성하는 방법은 [설치 [!DNL Experience Manager] 데스크톱 앱](install-upgrade.md)을 참조하세요.

이전 [!DNL Experience Manager] 데스크톱 앱에서 업그레이드하는 경우 [이전 버전에서 업그레이드](install-upgrade.md#upgrade-from-previous-version)에 나열된 전환 우수 사례를 따라야 합니다.

## 앱 작동 방식에 대한 중요한 참고 사항 {#how-app-works}

애플리케이션 및 애플리케이션 작동 방식에 대한 다음 내용을 알고 있어야 합니다.

* [!DNL Experience Manager](으)로 에셋 바이너리를 완전히 전송해야 하는 작업에 대한 모든 권한을 응용 프로그램에서 제공합니다(**열기**, **편집**, **변경 내용 업로드** 및 **Assets 업로드**).

   * 데스크탑에서 자산으로 작업하려면 개별적으로, 폴더로 또는 다중 선택을 통해 열기, 편집 또는 데스크탑으로 다운로드를 명시적으로 수행해야 합니다.

   * [!DNL Experience Manager]에 업로드된 자산에 로컬 변경 내용을 가져오려면 개별적으로 또는 다중 선택을 통해 [!UICONTROL Upload Changes]을(를) 선택해야 합니다.

   * 응용 프로그램이 데스크톱과 [!DNL Experience Manager]에서 자산을 동기화하는 &#39;동기화 클라이언트&#39;가 아닙니다.

   * 응용 프로그램에서 [!DNL Experience Manager] 리포지토리를 가상 폴더 구조로 매핑하는 네트워크 공유를 제공하지 않습니다.

* 애플리케이션에서 표시하는 에셋 목록은 Assets 저장소의 상태를 기반으로 합니다. 로컬로 다운로드한 후 로컬 파일 또는 캐시 폴더에서 이름을 변경한 파일은 애플리케이션에서 표시하거나 관리하지 않습니다.

* 예상한 결과가 앱에 표시되지 않으면 상단 표시줄의 새로 고침 아이콘을 클릭합니다.

* [!UICONTROL Reveal File] 작업을 사용할 때 표시되는 로컬 네트워크 공유에는 로컬에서 사용할 수 있는 파일(및 폴더)만 표시됩니다. 로컬 네트워크 공유에 표시되는 적합한 자산을 가져올 수 있도록 [!UICONTROL Reveal File] 및 [!UICONTROL Reveal Folder]에서 자산을 미리 다운로드합니다.

* SMB(Mac)/WebDAV(Win) 로컬 네트워크 공유는 Adobe Creative Cloud 앱이 Creative Cloud 앱의 기본 파일에 연결/배치된 에셋 파일을 읽을 때 사용됩니다.

다음 다이어그램은 사용자 작업에서 시작된 자산과 파일의 클라우드와 로컬 파일 시스템 간 흐름을 보여줍니다.

![데스크톱 앱을 통해 [!DNL Experience Manager] 서버에서 기본 데스크톱 앱으로 자산 흐름](assets/da20_flow_diagram.png)

## 알려진 문제 {#known-issues-v2}

**사용자 인터페이스 문제:**

* 데스크탑 앱의 인터페이스가 비어 있는 경우가 가끔 있습니다. 마우스 오른쪽 단추를 클릭하고 [!UICONTROL Refresh]을(를) 클릭하여 응용 프로그램을 다시 로드합니다. 새로 고친 후에는 DAM 저장소의 루트에서 시작합니다. 에셋의 또는 상태에 대한 업데이트가 유지됩니다. <!-- CQ-4270267 -->

* 트랙 패드나 마우스 포인터가 없으면 폴더/검색 결과를 탐색하기 어렵습니다. 휠 없는 마우스 장치에는 스크롤 막대가 표시되지 않습니다. <!-- CQ-4269947 -->

* 자산 업로드가 변경될 때 진행률 표시줄이 제대로 표시되지 않는 경우가 가끔 있습니다.

* 필터를 적용하고 제거하여 로컬에서 편집한 모든 자산을 찾으면 사용자가 시작한 검색 결과 또는 폴더 보기로 앱에서 이동하지 않습니다. DAM 저장소의 루트 폴더를 앱에서 표시합니다.

* 실행 중인 [!DNL Experience Manager] 서버가 없는 URL에 연결하면 연결 화면이 응답하지 않는 경우가 가끔 있습니다. 애플리케이션을 종료하고 다시 시작합니다.

**CRUD(만들기, 읽기, 업데이트 및 삭제) 문제:**

* 변경 내용을 주석과 함께 자산에 업로드할 때 주석이 자산과 함께 [!DNL Experience Manager]에 저장되지만 버전 관리 주석으로 표시되지 않습니다. 이 문제는 [!DNL Experience Manager] 6.4.5 및 [!DNL Experience Manager] 6.5.1에서 해결되었습니다. Adobe은 최신 서비스 팩을 설치할 것을 권장합니다. <!-- CQ-4268990 -->

* 사용자가 자산 전송을 취소할 수 없습니다. 의도하지 않은 대용량 전송을 트리거한 경우 애플리케이션을 종료하고 다시 시작합니다. <!-- CQ-4278940 -->

**플랫폼 문제:**

* 자산을 열면 해당 자산을 편집하지 않았더라도 [!UICONTROL Edited Locally] 상태로 즉시 변경되는 경우가 가끔 있습니다. [!UICONTROL Refresh] 아이콘을 클릭하여 업데이트합니다.

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] documentation](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service)
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] [!DNL Assets] documentation](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/overview)
>* [사용 방법 [!DNL Experience Manager] 데스크톱 앱](using.md)
>* [데스크탑 앱 설치 및 업그레이드](install-upgrade.md)
>* [우수 사례 및 문제 해결 팁](troubleshoot.md)
