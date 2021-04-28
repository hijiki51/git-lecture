# traP スライドテーマ for Marp

[traP スライドテーマ](https://wiki.trap.jp/resources/traP_slide-template) のMarp用派生テーマです。

Marp for VSCode で使えるようになっているはずです。

WSLでは拡張機能での書き出しが行えないっぽいので、marp-cli を利用してください。


以下のような `showcase.yaml` を置くことでshowcaseでの静的配信ができます。

```yaml
type: static

startup: |
  npm i -g @marp-team/marp-cli
  npx @marp-team/marp-cli {{スライド名}} -o index.html --theme theme.css
```