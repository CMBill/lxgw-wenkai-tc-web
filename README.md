# LXGW WenKai TC / 霞鶩文楷 TC 網絡字體倉庫

## 倉庫仍在完善，但可以初步使用
## 簡介
[LXGW WenKai TC / 霞鶩文楷 TC](https://github.com/lxgw/LxgwWenkaiTC) 是 [霞鶩文楷](https://github.com/lxgw/LxgwWenKai) 的繁體中文版。字體詳情請參閱原字體倉庫。

為使原字體更適合進行網絡分發，本倉庫使用 Github Action，利用[中文網字計劃](https://chinese-font.netlify.app/)開髮的[字體分包工具](https://github.com/KonghaYao/cn-font-split)對原字體分包，網頁加載時隻需獲取所使用的文字所在的分包，大幅降低所需加載的大小，提昇網頁加載速度。

為方便使用，本倉庫的版本號將與字體原倉庫版本號一致。目前隻提供了 `v1.011` 及之後的版本。

## 使用
### 自行部署
如果下方提供的連結連接效果不甚理想，建議自行部署並配合自己的 CDN 使用。可以直接 Fork 本倉庫並啟用 Github Pages，使用時將下方連結修改為自己的倉庫地址即可，亦可直接克隆本倉庫到服務端、對象存儲等。

### 使用 JsDelivr 的 CDN
#### 最新版本
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-tc-web/style.css
```

#### 特定版本
將連結中的 `$VERSION` 替換為目標版本號，如 `1.011` 或 `v1.011` 均可。目前僅提供 `v1.011` 及之後的版本。
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-tc-web@VERSION/style.css
```
例如請求 `v1.011` 版本的字體：
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-tc-web@1.011/style.css
```

### 直接使用本倉庫連結
隻提供最新版本
```
https://cmbill.github.io/lxgw-wenkai-tc-web/style.css
```
