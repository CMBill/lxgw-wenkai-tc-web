# LXGW WenKai TC / 霞鶩文楷 TC 網絡字體倉庫

> 其他版本霞鶩文楷字體的網絡字體倉庫：
>   - [霞鶩文楷 / LXGW WenKai](https://github.com/CMBill/lxgw-wenkai-web)：原版。
>   - [霞鶩文楷屏幕閱讀版 / LXGW WenKai Screen](https://github.com/CMBill/lxgw-wenkai-screen-web)：適用於 PC 和 Android 手機屏幕顯示且無需特別切換到粗體。
>   - [霞鶩文楷 GB / LXGW WenKai GB](https://github.com/CMBill/lxgw-wenkai-gb-web)：調整字形和筆形，符合 G 源字形規範。包含《通用規範漢字表》8105 個漢字。


## 簡介
[LXGW WenKai TC / 霞鶩文楷 TC](https://github.com/lxgw/LxgwWenkaiTC) 是 [霞鶩文楷](https://github.com/lxgw/LxgwWenKai) 的繁體中文版。字體詳情請參閱原字體倉庫。

為使原字體更適合進行網絡分發，本倉庫使用 Github Action，利用[中文網字計劃](https://chinese-font.netlify.app/)開髮的[字體分包工具](https://github.com/KonghaYao/cn-font-split)對原字體分包，網頁加載時隻需獲取所使用的文字所在的分包，大幅降低所需加載的大小，提昇網頁加載速度。

為方便使用，本倉庫的版本號將與字體原倉庫版本號一致。目前隻提供了 `v1.011` 及之後的版本。

## 使用
直接將文後提供的鏈接以 `<link>` 的形式添加到網頁的 `<head>` 內即可

```html
<html>
<head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/lxgw-wenkai-tc-web@latest/style.css" />
  <style>
    body {
      font-family: "LXGW WenKai TC";
      font-weight: normal;
    }
  </style>
</head>
<body>
  
</body>
</html>
```

這樣引入的 `style.css` 可以調用倉庫包含的所有字體，使用字體時以以表格中所示 `font-family` 與 `font-weight` 在 CSS 中調用即可。

| 字體                      | `font-family`               | `font-weight` |
| ------------------------- | --------------------------- | ------------- |
| LXGW Wenkai TC            | `LXGW Wenkai TC`            | `normal`      |
| LXGW Wenkai TC Bold       | `LXGW Wenkai TC`            | `bold`        |
| LXGW Wenkai TC Light      | `LXGW Wenkai TC Light`      | `normal`      |
| LXGW WenKai Mono TC       | `LXGW WenKai Mono TC`       | `normal`      |
| LXGW WenKai Mono TC Bold  | `LXGW WenKai Mono TC`       | `bold`        |
| LXGW WenKai Mono TC Light | `LXGW WenKai Mono TC Light` | `normal`      |

如果只需某一特定的字體，也可只引用其對應分包的 CSS 文件，將如下表格中 `repositoryURL` 替換為倉庫的鏈接即可。

| 字體                      | 鏈接                                                              |
| ------------------------- | ----------------------------------------------------------------- |
| LXGW Wenkai TC            | `https://repositoryURL/lxgwwenkaitc-regular/result.css`     |
| LXGW Wenkai TC Bold       | `https://repositoryURL/lxgwwenkaitc-bold/result.css`        |
| LXGW Wenkai TC Light      | `https://repositoryURL/lxgwwenkaitc-light/result.css`       |
| LXGW WenKai Mono TC       | `https://repositoryURL/lxgwwenkaimonotc-regular/result.css` |
| LXGW WenKai Mono TC Bold  | `https://repositoryURL/lxgwwenkaimonotc-bold/result.css`    | 
| LXGW WenKai Mono TC Light | `https://repositoryURL/lxgwwenkaimonotc-light/result.css`   |

例如若只需調用 LXGW Wenkai Mono TC，則只需引入：
```
https://cdn.jsdelivr.net/npm/lxgw-wenkai-tc-web@latest/lxgwwenkaimonotc-regular/result.css
``` 

### 自行部署
如果下方提供的連結連接效果不甚理想，建議自行部署並配合自己的 CDN 使用。可以直接 Fork 本倉庫並啟用 Github Pages，使用時將下方連結修改為自己的倉庫地址即可，亦可直接克隆本倉庫到服務端、對象存儲等。

### 使用 CDN
#### 作為 npm 包（推荐）
目前已作為 npm 包上傳到 npmjs，可以使用 npm 包的鏡像引用，如 JSDeliver 的 npm 鏡像：
```
https://cdn.jsdelivr.net/npm/lxgw-wenkai-tc-web@latest/style.css
```

也可指定版本號，將連結中的 `$VERSION` 替換為目標版本號（但 npm 的語義化版本號回省略版本號數字開頭的 0，具體版本號建議先查詢 npmjs），如 `1.011` 或 `v1.011` 均可。目前僅提供 `v1.011` 及之後的版本。
```
https://cdn.jsdelivr.net/npm/lxgw-wenkai-tc-web@VERSION/style.css
```

### 直接使用本倉庫連結
隻提供最新版本
```
https://cmbill.github.io/lxgw-wenkai-tc-web/style.css
```
