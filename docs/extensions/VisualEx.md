---
title: Composition Visual Attached Properties
author: nmetulev
ms.date: 08/20/2017
description: The Composition Visual Attached Properties allow Composition Visual Properties to be modified directly in XAML (outdated docs).
keywords: windows 10, uwp, uwp community toolkit, uwp toolkit, Visual, composition, xaml, attached property
---

# Composition Visual Attached Properties

> [!WARNING]
> This docs page is outdated and the `VisualEx` type has been removed from the Windows Community Toolkit, please refer to the docs for the [`VisualExtensions`](VisualExtensions.md) type.

The Composition Visual Attached Properties allow developers to modify common properties of the [object visual](/uwp/api/Windows.UI.Composition.Visual) of an element directly in XAML.

## Example

```xaml
<Page
    ...
    xmlns:extensions="using:Microsoft.Toolkit.Uwp.UI.Extensions">

<Border Height="100"
    Width="100"
    Background="Purple"
    extensions:VisualEx.CenterPoint="50,50,0"
    extensions:VisualEx.Opacity="0.5"
    extensions:VisualEx.RotationAngleInDegrees="80"
    extensions:VisualEx.Scale="2, 0.5, 1"
    extensions:VisualEx.NormalizedCenterPoint="0.5, 0.5, 0" />
```

## Properties

> Note. Properties of type Vector2, Vector3 or Vector4 on the Visual are represented as strings here. To specify the Vector2, Vector3, or Vector4 value, use the following string format:
>
> * Vector2 - "0" or "0, 0"
> * Vector3 - "0" or "0, 0, 0"
> * Vector4 - "0" or "0, 0, 0, 0"

### AnchorPoint (Vector2)

The point on the visual to be positioned at the visual's offset. Value is normalized with respect to the size of the visual.

### CenterPoint (Vector3)

The point about which rotation or scaling occurs.

### Offset (Vector3)

The offset of the visual relative to its parent or for a root visual the offset relative to the upper-left corner of the windows that hosts the visual.

### Opacity (double)

The opacity of the visual.

### RotationAngle (double)

The rotation angle in radians of the visual.

### RotationAngleInDegrees (double)

The rotation angle of the visual in degrees.

### RotationAxis (Vector3)

The axis to rotate the visual around.

### Scale (Vector3)

The scale to apply to the visual.

### Size (Vector2)

The width and height of the visual.

### NormalizedCenterPoint (Vector3)

The point about which rotation or scaling occurs, normalized between the values 0.0 and 1.0

## Requirements (Windows 10 Device Family)

| [Device family](https://go.microsoft.com/fwlink/p/?LinkID=526370) | Universal, 10.0.16299.0 or higher |
| --- | --- |
| Namespace | Microsoft.Toolkit.Uwp.UI.Extensions |
| NuGet package | [Microsoft.Toolkit.Uwp.UI](https://www.nuget.org/packages/Microsoft.Toolkit.Uwp.UI/) |

## API

* [Visual extensions source code](https://github.com/Microsoft/UWPCommunityToolkit/blob/rel/7.0.0/Microsoft.Toolkit.Uwp.UI/Extensions/Visual/VisualEx.cs)
