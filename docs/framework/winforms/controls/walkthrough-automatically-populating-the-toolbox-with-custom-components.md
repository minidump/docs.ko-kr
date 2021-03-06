---
title: '연습: 도구 상자에 자동으로 사용자 지정 구성 요소 채우기'
ms.date: 03/30/2017
helpviewer_keywords:
- IToolboxService interface
- Toolbox [Windows Forms], populating
- custom components [Windows Forms], adding to Toolbox
ms.assetid: 2fa1e3e8-6b9f-42b2-97c0-2be57444dba4
ms.openlocfilehash: 488d51e748ea17b09e61b982db7abadc34f8e311
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43671893"
---
# <a name="walkthrough-automatically-populating-the-toolbox-with-custom-components"></a>연습: 도구 상자에 자동으로 사용자 지정 구성 요소 채우기
구성 요소는 현재 열려 있는 솔루션의 프로젝트에서 정의 된 경우는 자동으로 나타나는 합니다 **도구 상자**, 작업이 사용자가 필요 하지 않습니다. 채울 수도 있습니다는 **도구 상자** 사용 하 여 사용자 지정 구성 요소를 사용 하 여 합니다 [선택 도구 상자 항목 대화 상자 (Visual Studio)](https://msdn.microsoft.com/library/bd07835f-18a8-433e-bccc-7141f65263bb), 하지만 **도구 상자** 고려 솔루션에 있는 항목의 다음 특성을 모두 사용 하 여 출력을 빌드하십시오.  
  
-   구현 <xref:System.ComponentModel.IComponent>;  
  
-   없는 <xref:System.ComponentModel.ToolboxItemAttribute> 로 `false`;  
  
-   없는 <xref:System.ComponentModel.DesignTimeVisibleAttribute> 로 `false`합니다.  
  
> [!NOTE]
>  합니다 **도구 상자** 때문 솔루션의 프로젝트에 의해 빌드되지 않는 항목을 표시 하지 것입니다 참조 체인을 따르지 않습니다.  
  
 이 연습에서는 사용자 지정 구성 요소에 자동으로 표시 하는 방법을 보여 줍니다.는 **도구 상자** 빌드될 때 구성 요소입니다. 이 연습에서 설명하는 작업은 다음과 같습니다.  
  
-   Windows Forms 프로젝트를 만드는 중입니다.  
  
-   사용자 지정 구성 요소를 만드는 중입니다.  
  
-   사용자 지정 구성 요소의 인스턴스를 만드는 중입니다.  
  
-   언로드 및 사용자 지정 구성 요소를 다시 로드 합니다.  
  
 완료 했으면 확인 하 게 합니다 **도구 상자** 사용자가 만든 구성 요소를 사용 하 여 채워집니다.  
  
> [!NOTE]
>  표시되는 대화 상자와 메뉴 명령은 활성 설정이나 버전에 따라 도움말에서 설명하는 것과 다를 수 있습니다. 설정을 변경하려면 **도구** 메뉴에서 **설정 가져오기 및 내보내기** 를 선택합니다. 자세한 내용은 [Visual Studio IDE 개인 설정](/visualstudio/ide/personalizing-the-visual-studio-ide)을 참조하세요.  
  
## <a name="creating-the-project"></a>프로젝트 만들기  
 첫 번째 단계는 프로젝트를 만들고 폼을 설정하는 것입니다.  
  
#### <a name="to-create-the-project"></a>프로젝트를 만들려면  
  
1.  라는 Windows 기반 응용 프로그램 프로젝트를 만듭니다 `ToolboxExample` (**파일** > **New** > **프로젝트**  >  **Visual C#** 나 **Visual Basic** > **클래식 데스크톱** > **Windows Forms 응용 프로그램**).  
  
2.  프로젝트에 새 구성 요소를 추가 합니다. 호출 `DemoComponent`합니다.  
  
     자세한 내용은 [NIB: 방법: 새 프로젝트 항목 추가](https://msdn.microsoft.com/library/63d3e16b-de6e-4bb5-a0e3-ecec762201ce)합니다.  
  
3.  프로젝트를 빌드합니다.  
  
4.  **도구** 메뉴를 클릭 합니다 **옵션** 항목. 클릭 **일반** 아래에서 **Windows Forms 디자이너** 항목을 확인 합니다 **AutoToolboxPopulate** 옵션을 설정 **True**합니다.  
  
## <a name="creating-an-instance-of-a-custom-component"></a>사용자 지정 구성 요소 인스턴스 만들기  
 다음 단계는 양식의 사용자 지정 구성 요소의 인스턴스를 만드는 것입니다. 때문에 합니다 **도구 상자** 자동으로 새 구성 요소에 대 한 계정,이 다른 구성 요소나 컨트롤을 만드는 것 만큼 쉽습니다.  
  
#### <a name="to-create-an-instance-of-a-custom-component"></a>사용자 지정 구성 요소의 인스턴스를 만들려면  
  
1.  프로젝트의 폼을 엽니다는 **Forms 디자이너**합니다.  
  
2.  에 **도구 상자**, 이라는 새 탭을 클릭 **ToolboxExample 구성 요소**합니다.  
  
     탭을 클릭 하면 표시 됩니다 **DemoComponent**합니다.  
  
    > [!NOTE]
    >  성능상의 이유로, 자동으로 채워진 영역의 구성 요소를 **도구 상자** 사용자 지정 비트맵을 표시 하지 않습니다 및 <xref:System.Drawing.ToolboxBitmapAttribute> 지원 되지 않습니다. 사용자 지정 구성 요소에 대 한 아이콘을 표시 하는 **도구 상자**를 사용 하 여를 **도구 상자 항목 선택** 대화 상자 요소를 로드 합니다.  
  
3.  구성 요소를 양식에 끌어다 놓습니다.  
  
     구성 요소 인스턴스의 생성 되어에 추가 합니다 **구성 요소 트레이에**합니다.  
  
## <a name="unloading-and-reloading-a-custom-component"></a>사용자 지정 구성 요소를 다시 로드 및 언로드  
 합니다 **도구 상자** 의 각 구성 요소는 계정 프로젝트를 로드 하 고 프로젝트를 로드할 프로젝트의 구성 요소에 대 한 참조를 제거 합니다.  
  
#### <a name="to-experiment-with-the-effect-on-the-toolbox-of-unloading-and-reloading-components"></a>구성 요소를 다시 로드 및 언로드의 도구 상자에 대 한 효과 사용 하 여 실험  
  
1.  솔루션에서 프로젝트를 언로드하십시오.  
  
     언로드 프로젝트에 대 한 자세한 내용은 참조 하세요. [NIB: 방법: 프로젝트 다시 로드 및 언로드](https://msdn.microsoft.com/library/abc0155b-8fcb-4ffc-95b6-698518a7100b)합니다. 저장 하 라는 메시지가 나타나면 선택할 **예**합니다.  
  
2.  새 **Windows 응용 프로그램** 프로젝트를 솔루션입니다. 폼을 엽니다는 **디자이너**합니다.  
  
     합니다 **ToolboxExample 구성 요소** 탭에서 이전 프로젝트는 이제 사라집니다.  
  
3.  다시 로드를 `ToolboxExample` 프로젝트입니다.  
  
     합니다 **ToolboxExample 구성 요소** 탭 이제 다시 나타납니다.  
  
## <a name="next-steps"></a>다음 단계  
 이 연습을 보여 줍니다 합니다 **도구 상자** 프로젝트의 구성 요소를 고려 되지만 **도구 상자** 컨트롤 고려 합니다. 추가 하 고 솔루션에서 제어 프로젝트를 제거 하 여 사용자 고유의 사용자 지정 컨트롤을 사용 하 여 실험 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [일반적으로 Windows Forms 디자이너, 옵션 대화 상자](https://msdn.microsoft.com/library/8dd170af-72f0-4212-b04b-034ceee92834)  
 [방법: 도구 상자 탭 조작](https://msdn.microsoft.com/library/21285050-cadd-455a-b1f5-a2289a89c4db)  
 [도구 상자 항목 선택 대화 상자(Visual Studio)](https://msdn.microsoft.com/library/bd07835f-18a8-433e-bccc-7141f65263bb)  
 [Windows Forms에 컨트롤 넣기](../../../../docs/framework/winforms/controls/putting-controls-on-windows-forms.md)
