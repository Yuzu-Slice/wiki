# Modをゲーム内に読み込む

メタデータファイルが完成したら、ゲームを開始できます！
コマンドラインからゲームを実行すると、modがロードされたことを示すこれらのメッセージなど、役立つデバッグメッセージが多数表示されます。

```shell
source/funkin/modding/PolymodHandler.hx:316: Found 5 mods when scanning.
source/funkin/modding/PolymodHandler.hx:118: Attempting to load 5 mods...
...
source/funkin/modding/PolymodErrorHandler.hx:79: [INFO-] LOADING MOD - Preparing to load mod mods/introMod
source/funkin/modding/PolymodErrorHandler.hx:79: [INFO-] LOADING MOD - Done loading mod mods/introMod
...
source/funkin/modding/PolymodHandler.hx:169: Mod loading complete. We loaded 5 / 5 mods.
```

modが読み込まれました！(まだ何も起こりませんが)

----
#### [次のページへ](01-03-asset-replacement-and-additions.md)