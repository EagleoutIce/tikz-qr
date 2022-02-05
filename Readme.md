# tikz-qr

[![compile qr](https://github.com/EagleoutIce/tikz-qr/actions/workflows/compile.yaml/badge.svg)](https://github.com/EagleoutIce/tikz-qr/actions/workflows/compile.yaml)

Simple package to create fancy qr codes with the help of the [`qrcode`](https://www.ctan.org/pkg/qrcode)-package.
You may use `\fancyqr` just like the normal `\qrcode` (`\fancyqr[<qr-options>]{<url>}`).
You can change the gradient by changing the designated colors:

```latex
\colorlet{qr@fancy@gradient@tl}{teal}
\colorlet{qr@fancy@gradient@br}{purple}
```

If you do want to hide a center square (e.g, because you want to embed an image) you can use `\FancyQrDoNotPrintSquare{<x>}{<y>}` to hide a rectangle with radius x and y set from the center. If you choose this option, the default `\FancyQrRoundCut` that rounds cut corners can be changed with `\FancyQrHardCut`.
At the moment, there are two other styles `flat` and `frame` that you can load (locally) by using `\FancyQrLoad{<name>}`.

Using `\fancyqrimage[<qr-options>]{<url>}{<image>}` the package will automatically calculate the required `\FancyQrDoNotPrintSquare` (you have to make sure the, the qr code still has enough information to readable).

Example from [qr.tex](qr.tex):

[<img src="https://github.com/EagleoutIce/tikz-qr/blob/gh-pages/preview-1.png?raw=true" width="600"/>](https://media.githubusercontent.com/media/EagleoutIce/tikz-qr/gh-pages/qr.pdf)
