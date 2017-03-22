---
title: "때문에이 &quot; Sub n e &quot;의 첫째 문은 &quot;MyBase.New&quot; 또는 &quot;MyClass.New&quot;를 명시적으로 호출 해야는 &quot;&lt;constructorname&gt;&quot;에서 기본 클래스&quot;&lt;baseclassname&gt;&quot;의&quot;&lt;derivedclassname&gt;&quot; 것으로 표시 됩니다: &quot;&lt;errormessage&gt;&quot; | Microsoft 문서"
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc30920
- bc30920
dev_langs:
- VB
helpviewer_keywords:
- BC30920
ms.assetid: e47dc755-4294-4368-b813-2177b7677957
caps.latest.revision: 10
author: stevehoag
ms.author: shoag
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: feb04d426b7e050b7ad05cdfd4d481172dda3a49
ms.lasthandoff: 03/13/2017

---
# <a name="first-statement-of-this-39sub-new39-must-be-an-explicit-call-to-39mybasenew39-or-39myclassnew39-because-the-39ltconstructornamegt39-in-the-base-class-39ltbaseclassnamegt39-of-39ltderivedclassnamegt39-is-marked-obsolete-39lterrormessagegt39"></a>때문에이 ' Sub n e '의 첫째 문은 'MyBase.New' 또는 'MyClass.New'를 명시적으로 호출 해야는 '&lt;constructorname&gt;'에서 기본 클래스'&lt;baseclassname&gt;'의'&lt;derivedclassname&gt;' 것으로 표시 됩니다: '&lt;errormessage&gt;'
클래스 생성자는 기본 클래스 생성자를 명시적으로 호출 하지 않는 한 암시적 기본 클래스 생성자로 표시 된 <xref:System.ObsoleteAttribute>특성과 오류로 처리 하는 지시문.</xref:System.ObsoleteAttribute>  
  
 파생 클래스 생성자가 기본 클래스 생성자를 호출하지 않는 경우 [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]이 매개 변수가 없는 암시적 기본 클래스 생성자에 대한 암시적 호출을 생성하려고 합니다. 인수 없이 호출될 수 있는 기본 클래스에 액세스할 수 있는 생성자가 없는 경우 [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]은 암시적 호출을 생성할 수 없습니다. 이 경우 필요한 생성자는 기본적으로 <xref:System.ObsoleteAttribute>특성 [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] 합니다.를 호출할 수 없습니다</xref:System.ObsoleteAttribute>  
  
 모든 프로그래밍 요소에 <xref:System.ObsoleteAttribute>합니다.</xref:System.ObsoleteAttribute> 적용 하 여 더 이상 사용 중인 것으로 표시할 수 없습니다. 이 작업을 수행 하는 경우에 특성을 설정할 수 있습니다 <xref:System.ObsoleteAttribute.IsError%2A>속성을 `True` 또는 `False`.</xref:System.ObsoleteAttribute.IsError%2A> `True`로 설정하면 컴파일러가 요소를 사용하려는 시도를 오류로 처리합니다. `False`로 설정하거나 기본값인 `False`로 두면 컴파일러가 요소를 사용하려는 시도가 있을 경우 경고를 발생시킵니다.  
  
 **오류 ID:** BC30920  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  따옴표 붙은 오류 메시지를 검사하고 적절한 조치를 수행합니다.  
  
2.  `MyBase.New()` 또는 `MyClass.New()` 에 대한 호출을 파생 클래스에 `Sub New` 의 첫 번째 문으로 포함합니다.  
  
## <a name="see-also"></a>참고 항목  
 [특성 개요](../../../visual-basic/programming-guide/concepts/attributes/index.md)
 