# Compatible-AZIK

ローマ字入力拡張系の **AZIK** から破壊的な変更点を取り除き、従来のローマ字入力との互換性を高めたローマ字テーブル設定（Google日本語入力用）

AZIKを手軽に利用するための環境としてGoogle日本語入力が使われるため、本リポジトリでもGoogle日本語入力のローマ字テーブル設定ファイルを提供します。

## AZIKとは

AZIKは、「ローマ字入力の経験をそのまま活かして入力効率を上げる」ことに着目した、ローマ字入力の拡張定義です。そのコンセプトから、ローマ字入力に慣れた方が少ない習熟コストで習得できるというのが特徴です。

AZIKでは基本のローマ字入力方式をそのままに、日本語での頻出パターンの入力を短縮化するように独自のアルファベットの組み合わせが拡充されています。

※AZIKの基本的な入力方法についてはAZIK開発者による [AZIK総合解説書](http://hp.vector.co.jp/authors/VA002116/azik/azikinfo.htm) を参照してください。

## Compatible-AZIKが目指すもの

AZIKはローマ字入力の拡張系でありながらも、元のローマ字入力方式から一部の互換性が失われています。

特に気になるのは、`kk = きん` のように一部の子音を重ねる表現が追加されるにあたり、従来のローマ字入力にあった `kka = っか` のような「子音を重ねることで促音を入力」が使えなくなってしまっている点です。

Compatible-AZIKでは、入力効率よりも従来のローマ字入力との互換性を重視することを目的に、AZIKに改変を加えました。

## インストール

[Compatible-AZIK.txt](./Compatible-AZIK.txt) をダウンロードして、 `Google日本語入力 プロパティ -> ローマ字テーブル [編集]ボタン -> 編集 -> インポート` を実行し、当該ファイルを読み込む。

## AZIKからの変更点

| 概要 | 変更内容 |
| :--- | :--- |
| `tta = った` のような「子音を重ねることで促音を入力」に対応 | 「子音を重ねることで促音を入力」の定義追加。これに伴い `dd = でん` `hh = ふう` `jj = じゅん` `kk = きん` `ll = ぉん` `pp = ぽう` `rr = られ` `ss = せい` `tt = たち` `ww = うぇい` `zz = ざん` などの2文字の表現を3文字に変更 (例: `dd -> ddd`) |
| `ltu = っ` を新たに割り当て | 左記割り当て追加 |
| `tha = てゃ` `thi = てぃ` `thu = てゅ` `the = てぇ` `tho = てょ` を追加 | 左記割り当て追加。これに伴い `th = つう` を `thh = つう` に変更 |
