# Modal

## Example

Modalは以下のようなものを指します。

```html
<dialog open>
  <p>Hoge hoge</p>
</dialog>
```

## Checklist

- [ ] [dialogを閉じる際にpositionのアニメーションを使っている場合，backdropのshadowを一緒に動かさない](#backdrop-animation)

## Details

### <a name="backdrop-animation">dialogを閉じる際にpositionのアニメーションを使っている場合，backdropのshadowを一緒に動かさない</a>

TODO: sampleのcssを追加

ときどき見かけるのが，Modalを開く/閉じるでtopやleftの数値をtransitionする，みたいなのがある。  
Modalは後ろにあるものより前面にあることを強調するため，backdropを使うことがあったり，疑似要素などでw 100vw h 100vhで透過の黒などなどを使って表現することがあるが，この背景も一緒にtransitionしている例を見る。

これはなんだか気持ちが悪いので，ぜひbackdropは位置固定でmodalだけtop/leftをtransitionし，backdropはopacityだけをanimationさせてほしい。
