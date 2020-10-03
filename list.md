# List

## Example

Listは以下のようなものを指します(olでも同様です）。

```html
<ul>
  <li>List element 1</li>
  <li>List element 2</li>
</ul>
```

## Checklist

- [ ] [Listの中身が長くなっても，markerがきちんと独立して表示される（markerの下にテキストが回り込まない）](#marker-isolation)

## Details

<a name="marker-isolation"></a>

```css
ul {
  list-style-type: none;
  padding-left: 0;
}

li::before {
  content: "-";
}
```

のような形で，listのmarkerのデザインをカスタマイズすると思いますが，忘れがちなのが疑似属性にmargin-rightだけ設定して，テキストが長くなった際にmarkerの下にテキストが回り込んでしまうことを考慮できていないパターンです。
