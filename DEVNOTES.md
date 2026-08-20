# 開発メモ

AXMER 2026 Chapter 15（熱気球競技のタスク規定）を表示するビューアーアプリの開発メモです。

## リンク

- [競技名とルール（公開ページ）](https://ngr2000.github.io/AXMER2026Chp15JP/)
- [参考: 日本気球連盟 タスク解説](https://jballoon.jp/task)

## このアプリについて

- `index.html` 1ファイルで完結する静的サイト。GitHub Pages（上記リンク）でそのまま公開されている。
- Chapter 15 の各タスク（15.1〜15.21）を `AXMER_TASKS` という JSON データとして埋め込み、ボタンをタップすると該当タスクの条文（英語原文＋日本語訳）を開閉表示する。
- セクションに `image` / `image_alt` / `image_caption` / `image_original` / `image_original_label` を持たせると、そのセクションに参考図を表示できる（現状 APT = 15.21.2 のみ使用）。
  - `image`: 表示する画像（SVG/画像ファイルパス）。タップで別タブ表示。
  - `image_original` / `image_original_label`: 元の原本スキャンなど別画像へのリンクを追加したい場合に使用。

## APT（15.21）の参考図について

- `apt-sketch.svg`: 規定の Example sketch（高度プロファイルと内側帯/外側帯の空域）をSVGで再現したもの。
- `IMG_4819.jpeg`: 原本スキャン画像。参考図の下の「オリジナル画像（原本スキャン）を見る」リンクから確認できる。

## 今後の TODO（案）

- 他タスク（ELB / LRN など、スケッチが必要なタスク）にも同様の参考図を追加する
- 画像タップ時の拡大表示をモーダルにするなど、UXを改善する
