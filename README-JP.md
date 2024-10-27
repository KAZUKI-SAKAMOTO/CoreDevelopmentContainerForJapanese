# Core Development Container for Japanese

これはCoreと呼ばれるベース開発コンテナで、Ubuntuを使用して構築されています。zsh、oh-my-zsh、git、およびHomebrewなどの基本的な開発ツールが含まれています。このコンテナは、さまざまなプログラミング言語や開発ツールを追加するための基盤として設計されています。

## Features

- ベースコンテナ: Ubuntu
- シェル: `zsh` with `oh-my-zsh`
- 最低限必要なツール: `git`, `gh`, `vim`, `build-essential`, etc.
- 簡単なパッケージ管理のためにHomebrewをインストール
- ロケールを日本語（ja_JP.UTF-8）に設定
- タイムゾーンをAsia/Tokyo（UTC+9）に設定

## How to Use

### コンテナをベースとして使用する

このコンテナを開発環境のBaseコンテナとして使用できます。このベースコンテナを拡張することで、プロジェクトに必要な特定のツールと依存関係を追加できます。以下は、このコンテナを拡張して Python を含める方法の例です。

```Dockerfile
FROM <your-dockerhub-username>/core-dev-container:latest

# Example of adding Python
RUN apt-get update && \
    apt-get install -y python3 python3-pip
```

# ライセンス

このプロジェクトはMITライセンスの下で提供されています。
