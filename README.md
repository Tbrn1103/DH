# DH
For the class "Collaboration across STEM and Liberal Arts:AI design concept and technology that supports digital humanities[2]"

# Keithley 2450 SourceMeter RAGシステム

このプロジェクトは、**Keithley 2450 SourceMeter**に関するユーザーマニュアルをもとに、RAG（Retrieval-Augmented Generation）システムを構築したものです。Google Colabで.ipynbファイルとして作成され、**マニュアルに基づいて質問に対する回答や解説を提供**します。

## リポジトリ概要
このリポジトリには、Google Colab上で作成された.ipynbファイルが含まれており、Colab環境でRAGモデルを実行するためのコードが記述されています。

リンク：[Model 2450 SourceMeter Instrument User's Manual](https://www.tek.com/ja/keithley-source-measure-units/keithley-smu-2400-graphical-series-sourcemeter-manual-17)

## 目次
- [DH](#dh)
- [Keithley 2450 SourceMeter RAGシステム](#keithley-2450-sourcemeter-ragシステム)
  - [リポジトリ概要](#リポジトリ概要)
  - [目次](#目次)
  - [プロジェクトの概要](#プロジェクトの概要)
  - [インストールとセットアップ](#インストールとセットアップ)
    - [前提条件](#前提条件)
    - [ライブラリのインストール](#ライブラリのインストール)
  - [使い方](#使い方)
  - [PDFファイルの読み込みについて](#pdfファイルの読み込みについて)
  - [使用する言語モデルについて](#使用する言語モデルについて)
  - [機能](#機能)

## プロジェクトの概要
このRAGシステムは、Keithley 2450 SourceMeterに関する使い方や設定の質問に対して、ユーザーマニュアルの内容に基づいて回答します。Colabノートブック上で実行可能であり、特に次のような用途に役立ちます：
- 機器の操作方法に関する迅速な解答
- 各種設定の手順や実行方法
- よくあるトラブルの対処法

## インストールとセットアップ

### 前提条件
- Google Colabアカウント
- GitHubリポジトリのクローン、またはColab上でGitHubに接続する設定

### ライブラリのインストール
1. リポジトリをクローンするか、GitHubからColabに.ipynbファイルを直接インポートします。
   ```python
   # Colab上でGitHubからリポジトリをクローン
   !git clone https://github.com/Tbrn1103/DH.git
   %cd DH
   ```

2. Colabノートブックの最初のセルで、以下のように必要なライブラリをインストールしてください。
   ```python
   !pip install transformers torch faiss flask
   ```

## 使い方

1. **ノートブックの実行**:
   - Colabノートブック内でセルを順番に実行し、必要なデータベースとモデルを読み込みます。

2. **質問を入力**:
   - プロジェクトが起動すると、Keithley 2450 SourceMeterの操作や設定に関する質問を入力することができます。
   - 例: 「電圧を設定するにはどうすれば良いか？」、「エラーコードの解決方法は？」

## PDFファイルの読み込みについて
- **PDFファイルの読み込み**: ダウンロードしたPDFファイルをそのまま読み込ませることができます。
- **DOCXファイルの推奨**: PDFをWordで開いてdocx形式で保存してから読み込ませると、情報抽出の精度が向上する場合があります。精度が重要な場合は、この手順をおすすめします。

## 使用する言語モデルについて
- **デフォルトモデル**: `rinna/japanese-gpt2-medium`をデフォルトで使用します。
- **精度向上のためのオプション**: デフォルトモデルで精度が低いと感じた場合は、有料モデル`gpt-4o-mini-2024-07-18`を使用することを推奨します。

## 機能
- **Q&A対応**: マニュアルに基づき、特定の機器設定や操作方法に関する質問に答えます。
- **情報検索**: マニュアルのデータベースを活用し、使い方や調整方法などを詳しく説明します。
- **トラブルシューティング**: よくあるエラーや問題に関する解決策を提供します。