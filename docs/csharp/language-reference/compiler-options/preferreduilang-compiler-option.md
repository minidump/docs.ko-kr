---
title: -preferreduilang(C# 컴파일러 옵션)
ms.date: 07/20/2015
f1_keywords:
- /preferreduilang
helpviewer_keywords:
- preferreduilang compiler option [C#]
- /preferreduilang compiler option [C#]
- -preferreduilang compiler option [C#]
ms.assetid: 68b2462f-6778-48d7-8052-62805fe8e02c
ms.openlocfilehash: a1fbbb8415e5e3405f039489aa071b0624065a9d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43405893"
---
# <a name="-preferreduilang-c-compiler-options"></a>-preferreduilang(C# 컴파일러 옵션)
`-preferreduilang` 컴파일러 옵션을 사용하여 C# 컴파일러에서 오류 메시지 등의 출력을 표시하는 언어를 지정할 수 있습니다.  
  
## <a name="syntax"></a>구문  
  
```console  
-preferreduilang: language  
```  
  
## <a name="arguments"></a>인수  
 `language`  
 컴파일러 출력에 사용할 언어의 [언어 이름](/windows/desktop/Intl/language-names)입니다.  
  
## <a name="remarks"></a>설명  
 `-preferreduilang` 컴파일러 옵션을 사용하여 C# 컴파일러에서 오류 메시지와 기타 명령줄 출력에 사용할 언어를 지정할 수 있습니다. 해당 언어의 언어 팩이 설치되지 않은 경우 운영 체제의 언어 설정이 대신 사용되고 오류가 보고되지 않습니다.  
  
```csharp  
csc.exe -preferreduilang:ja-JP  
```  
  
## <a name="requirements"></a>요구 사항  
  
## <a name="see-also"></a>참고 항목

- [C# 컴파일러 옵션](../../../csharp/language-reference/compiler-options/index.md)
