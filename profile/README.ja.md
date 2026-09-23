<!-- Language Selector -->
<div align="center">

[English](README.md) | [日本語](README.ja.md)

</div>

![image](https://github.com/user-attachments/assets/dee7188a-9a10-4599-b5b3-8a8aa3968e5e)

![image](https://github.com/user-attachments/assets/0599ebde-4d33-4766-9593-4531b958ad7f)

---

# 株式会社 Aid-On

Aid-On は宮崎の小さな会社です。**人が AI に渡す権限の境界**に絞って製品を作っています。

土台は WebAssembly と [WASI](https://wasi.dev/) の capability ベースの設計です。
実行は [Wasmtime](https://wasmtime.dev/) と OS のカーネル機能に任せ、
実装には LLM が最も正確に書ける自社開発の言語 [Almide](https://github.com/almide/almide) を使っています。

> **渡していない権限は、行使できない。**

必要な情報と操作だけを渡す。範囲を超える操作は止める。必要なら権限を取り戻せる。
これを人と AI のあいだに置くのが Aid-On の仕事です。

---

- ウェブサイト - <https://aid-on.org/>
- 解説記事 - <https://aid-on.org/module>
- お問い合わせ - <info@aid-on.org>

## 商用製品

準備中です。ご相談は [info@aid-on.org](mailto:info@aid-on.org) までお願いします。

## オープンソース

### Almide

LLM が最も正確に書ける静的型付け言語です。Rust と WebAssembly にコンパイルします。
Aid-On が開発しています。

- [almide](https://github.com/almide/almide) - コンパイラ本体
- [als](https://github.com/almide/als) - 言語仕様、適合性コーパスと、それを任意の almide バイナリに対して走らせる判定器
- [playground](https://github.com/almide/playground) - ブラウザで `.almd` を書いて動かす
- [vscode-almide](https://github.com/almide/vscode-almide) / [tree-sitter-almide](https://github.com/almide/tree-sitter-almide) - エディタ対応
- [almide-grammar](https://github.com/almide/almide-grammar) - 文法の単一の出どころ
- [parsegen](https://github.com/almide/parsegen) - grammar.json を読む tree-sitter 互換のパーサジェネレータ。C を使わず WASM で動く
  - パーサまわりは、そのうち Almide 製の gramide へ交代させる予定です
- [almide-agents](https://github.com/almide/almide-agents) - コーディングエージェントに Almide を正しく書かせるための AGENTS.md
- 組織 - <https://github.com/almide>

### Porta

渡した権限の分だけエージェントを動かすサンドボックスです。
止めるのはラッパーやプロンプトではなく OS のカーネルで、macOS は Seatbelt、Linux は Landlock + seccomp を使います。
カーネルが表現できない制限は、緩めるのではなく実行を拒否します。

- [porta](https://github.com/almide/porta)

### ライブラリ

- Almide 向け - [toml](https://github.com/Aid-On/toml) / [yaml](https://github.com/Aid-On/yaml) / [sha1](https://github.com/Aid-On/sha1)
- TypeScript・エッジ向け - [unillm](https://github.com/Aid-On/unillm) / [nagare](https://github.com/Aid-On/nagare) / [auth](https://github.com/Aid-On/auth) / [whenm](https://github.com/Aid-On/whenm)

その他は [Repositories](https://github.com/orgs/Aid-On/repositories) を参照してください。
ライセンスは各リポジトリの LICENSE に従います。

## 私たちについて

| | |
| --- | --- |
| **Mission** | 人と AI が、安心して力を預け合える世界を |
| **Vision** | AI とともに挑戦することを、あたりまえに |
| **Value** | 信頼が、可能性をひらく |

詳しくは <https://aid-on.org/> をご覧ください。

## 会社概要

|                |                            |
| -------------- | -------------------------- |
| **会社名**     | 株式会社 Aid-On / Aid-On Inc. |
| **所在地**     | 宮崎県宮崎市               |
| **事業内容**   | 人工知能および応用技術に係るソフトウェア、システム等の企画・開発・コンサルティング・保守 |
| **連絡先**     | [info@aid-on.org](mailto:info@aid-on.org) |

---

© 2026 Aid-On Inc.
