---
title: '방법: 단색으로 영역 그리기'
ms.date: 03/30/2017
helpviewer_keywords:
- solid colors [WPF], painting with
- brushes [WPF], painting with solid colors
- painting [WPF], with solid colors
ms.assetid: 5d27d8a7-4bd7-4063-bdf3-2c5c0f19f9d3
ms.openlocfilehash: 017c685139979ec3aa411be6e6b5fdf0e91657de
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43563143"
---
# <a name="how-to-paint-an-area-with-a-solid-color"></a>방법: 단색으로 영역 그리기
단색으로 영역을 그릴 사용할 수는 미리 정의 된 시스템 브러시와 같은 <xref:System.Windows.Media.Brushes.Red%2A> 또는 <xref:System.Windows.Media.Brushes.Blue%2A>, 하거나 새로 만들 수 있습니다 <xref:System.Windows.Media.SolidColorBrush> 설명 하 고 해당 <xref:System.Windows.Media.SolidColorBrush.Color%2A> 알파, 빨강, 녹색 및 파랑 값을 사용 하 여 합니다. XAML에서 16진수 표기법을 사용하여 단색으로 영역을 그릴 수도 있습니다.  
  
 다음 예제에서는 이러한 각 기법을를 그릴 때 사용 된 <xref:System.Windows.Shapes.Rectangle> 파란색입니다.  
  
## <a name="example"></a>예제  
 **미리 정의된 브러시 사용**  
  
 다음 예제에서는 미리 정의 된 브러시를 사용 하 여 <xref:System.Windows.Media.Brushes.Blue%2A> 에 파란색 사각형을 그립니다.  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_PredefinedBrush1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_predefinedbrush1)]  
  
 [!code-csharp[brushsamples_procedural_snip#_graphicsmm_PredefinedBrush1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/SolidColorBrushExample.cs#_graphicsmm_predefinedbrush1)]  
  
 **16진수 표기법 사용**  
  
 다음 예제에서는 8자리 16진수 표기법을 사용하여 파란색 사각형을 그립니다.  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_HexNotation8Digit1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_hexnotation8digit1)]  
  
 **ARGB 값 사용**  
  
 다음 예제에서는 만듭니다는 <xref:System.Windows.Media.SolidColorBrush> 에 대해 설명 하 고 해당 <xref:System.Windows.Media.SolidColorBrush.Color%2A> 파란색 값의 ARGB를 사용 하 여 합니다.  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_RgbNotation1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_rgbnotation1)]  
  
 [!code-csharp[brushsamples_procedural_snip#_graphicsmm_RgbNotation1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/SolidColorBrushExample.cs#_graphicsmm_rgbnotation1)]  
  
 색을 설명 하는 다른 방법에 대해서는 <xref:System.Windows.Media.Color> 구조입니다.  
  
 **관련 항목**  
  
 에 대 한 자세한 내용은 <xref:System.Windows.Media.SolidColorBrush> 및 추가 예제를 보려면 합니다 [단색 및 그라데이션 개요 그리기](../../../../docs/framework/wpf/graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md) 개요.  
  
 이 코드 예제는에 대해 제공 된 큰 예제의 일부는 <xref:System.Windows.Media.SolidColorBrush> 클래스입니다. 전체 샘플을 보려면 [브러시 샘플](https://go.microsoft.com/fwlink/?LinkID=159973)을 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.Windows.Media.Brushes>
