---
title: Transacted Operations In Doubt Per Second
ms.date: 03/30/2017
ms.assetid: 7e6b0716-c107-42e5-a21d-31d988e7a691
ms.openlocfilehash: f7365c4e5f03711129916c8c6964f7e25e9b553e
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43734722"
---
# <a name="transacted-operations-in-doubt-per-second"></a>Transacted Operations In Doubt Per Second
카운터 이름: Transacted Operations In Doubt Per Second  
  
## <a name="description"></a>설명  
 초당 이 서비스에서 확실하지 않은 결과가 있는 트랜잭션 작업의 수입니다.  
  
 이 카운터는 성능 카운터 형식 [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), 값은 다음 수식을 사용 하 여 계산 됩니다.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
