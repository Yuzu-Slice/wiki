# メタデータファイル

はじめに、`mods`フォルダの中に新しいフォルダを作りましょう。このフォルダがあなたのModの素材やスクリプトが入る場所になります。 次に、新しい新しいテキストファイルを作り、名前を`_polymod_meta.json`に変更しましょう。`_polymod_meta.json.txt`のように間違えないように注意！

このファイルには、ゲームがModを認識するために必要な情報を入力します。[Visual Studio Code](https://code.visualstudio.com/)などのプログラムを使うことをお勧めします。カンマなどを間違えても修正してくれます。

```json
{
  "title": "Mod名",
  "description": "説明用のMod",
  "contributors": [
    {
      "name": "作者名",
      "role": "リーダー"
    }
  ],
  "dependencies": {
    "modA": "1.0.0"
  },
  "optionalDependencies": {
    "modB": "1.3.2"
  },
  "api_version": "0.7.0",
  "mod_version": "1.0.0",
  "license": "Apache-2.0"
}
```

`_polymod_meta.json` には以下の設定できる項目があります。

- `title`:Modのわかりやすい名前。
- `description`:Modのわかりやすい説明。
- `contributors`: 作者の役職と名前のリスト。
- `homepage`: ユーザーがMODの詳細を確認できる URL。
- `dependencies`: 必須の依存関係であるModID とそのバージョン番号のマップ。
  - これらのModは、このModをロードするために同時にロードする必要があります。
  - このModが含まれていない場合、ロードは失敗します。
- `optionalDependencies`: 完全に必要でないオプションの依存関係であるModのIdとそのバージョン番号のマップ。
  - これらのModは、このModをロードするために必ずしもインストールする必要はありませんが、依存関係がこのModよりも先にロードされるように、MOD リストが並べ替えられます。
- `api_version`: MODがFunkin'と互換性があるかどうかを判断するために使用されるバージョン番号です。サポートしたいFriday Night Funkin'のバージョン番号に変更してください。最新バージョン（執筆時点では`0.7.0`）が望ましいです。
- `mod_version`: MOD固有のバージョン番号です。任意のバージョンを選択するか、`1.0.0`のままにしてください。
- `license`: MODの配布ライセンスです。[こちらから選択](https://opensource.org/licenses)するか、FNF本家に倣って`Apache-2.0`のままにしてください。

contributorsの中身には以下のフィールドを挿入できます。

- `name`: 貢献者の名前。
- `role`: *(任意)* 貢献者が担った役割（例:「アーティスト」または「プログラマー」など）
- `email`: *(任意)* 連絡先メールアドレス
- `url`: *(任意)* ホームページURL
----
これらの項目の多くは、ユーザーがModを整理できるようになる、今後実装されるModメニューによって使用されることを目的としています。

#### [次のページへ](01-02-loading-the-mod-in-game.md)