# VRMA Sequence Player

[日本語](#日本語) | [English](#english)

## 日本語

VRMモデルに複数のVRMAモーションを順番に続けて再生し、1本の動画として録画するブラウザツールです。インストールは不要で、`index.html` を開くだけで動きます。

読み込んだVRMとVRMAは、ブラウザの中だけで処理します。サーバーには送信しません。

### できること

- VRM(0.x / 1.0)と、複数のVRMAの読み込み
- VRMAを並べた順に、続けて再生
- つなぎ目を0.2秒かけてなめらかにする
- 前のモーションが終わった位置から次を始める(中央に引き戻されるのを防ぐ)
- 表情(笑顔など)とまばたきを重ねる
- 画面サイズ(縦 / 横)、背景色、カメラの距離と高さの調整
- 動画として録画して保存(対応ブラウザではMP4、それ以外はWebM)

### 使い方

1. `index.html` をブラウザで開きます(Chrome または Edge を推奨)。
2. 「VRMファイルを選ぶ」でモデルを読み込みます。
3. 「VRMAファイルを選ぶ」でモーションをまとめて選びます。ファイル名の順に並び、↑↓で入れ替えできます。
4. 再生して、全身が画面に収まっているかを確認します。
5. 「最初から録画する」を押し、終わったら「動画を保存する」を押します。

### 注意

- 録画は実時間で行います。録画中はタブを表示したままにしてください。
- 向き(回転)は次のモーションに引き継ぎません。ターンで終わるモーションは最後に置いてください。
- 表示部品(three.js、three-vrm)はCDNから読み込むため、インターネット接続が必要です。

### 使用ライブラリ

- [three.js](https://github.com/mrdoob/three.js)(MIT)
- [@pixiv/three-vrm](https://github.com/pixiv/three-vrm) / three-vrm-animation(MIT)

## English

A browser tool that plays multiple VRMA motions back-to-back on a VRM model and records them as a single video. No install needed: just open `index.html`.

The VRM and VRMA files you load are processed inside your browser only. Nothing is uploaded.

### Features

- Load a VRM (0.x / 1.0) and multiple VRMA files
- Play the VRMA files in list order, one after another
- Smooth each join with a 0.2-second blend
- Start each motion where the previous one ended (no snapping back to the center)
- Overlay a facial expression (such as a smile) and blinking
- Adjust frame size (portrait / landscape), background color, camera distance and height
- Record and save as a video (MP4 where the browser supports it, otherwise WebM)

### Usage

1. Open `index.html` in a browser (Chrome or Edge recommended).
2. Load a model with "VRMファイルを選ぶ".
3. Select your motions with "VRMAファイルを選ぶ". They are sorted by file name; reorder with ↑↓.
4. Play it back and check that the whole body stays in frame.
5. Press "最初から録画する", then "動画を保存する" when it finishes.

The interface is currently in Japanese only.

### Notes

- Recording runs in real time. Keep the tab visible while recording.
- Facing direction is not carried over to the next motion. Put motions that end in a turn last.
- three.js and three-vrm are loaded from a CDN, so an internet connection is required.

### Libraries

- [three.js](https://github.com/mrdoob/three.js) (MIT)
- [@pixiv/three-vrm](https://github.com/pixiv/three-vrm) / three-vrm-animation (MIT)
