
### Таблица: Неявно импортированные пространства имен по SDK

| SDK            | Неявно импортированные пространства имен                   |
| -------------- | ---------------------------------------------------------- |
| .NET Framework | `System`; `System.Collections`; `System.Linq`; `System.IO` |
| .NET Core      | `System`; `System.Collections.Generic`; `System.Linq`      |
| ASP.NET        | `System.Web`; `System.Web.Mvc`; `System.Web.Mvc.Html`      |
| Xamarin        | `Xamarin.Forms`; `System.Collections.ObjectModel`          |
| Unity          | `UnityEngine`; `System.Collections`                        |
| Android SDK    | `Android.Widget`; `Android.Views`; `Android.Content`       |
| iOS SDK        | `UIKit`; `Foundation`; `CoreGraphics`                      |

Традиционно каждый файл .cs, которому необходимо импортировать пространства имен, должен начинаться с операторов using для импорта этих пространств. Пространства имен, такие как System и System.Linq, необходимы почти во всех файлах .cs, поэтому первые несколько строк каждого файла .cs, как правило, содержат несколько операторов using:

using System;

using System.Linq;

using System.Collections.Generic;

При создании сайтов и сервисов с помощью ASP.NET Core возникает необходимость импортировать в каждом файле десятки пространств имен.

В C# 10 представлены некоторые новые функции, упрощающие импорт пространств имен.

Во-первых, оператор global using позволяет импортировать пространство имен только в одном файле .cs, и оно будет доступно во всех файлах .cs. Вы можете поместить операторы global using в файл Program.cs, но я рекомендую создать для них отдельный файл, например, GlobalUsings.cs или GlobalNamespaces.cs.

global using System;

global using System.Linq;

global using System.Collections.Generic;


_______
[[Версии .Net]]




123123
123123