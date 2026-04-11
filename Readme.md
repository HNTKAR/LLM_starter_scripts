# LLM Start

このリポジトリは、Open WebUIを使用してローカルでLLM（大規模言語モデル）を実行するためのセットアップガイドを提供しています。以下の手順に従って、環境を構築してください。

まず、UVをインストールして、Open WebUIをセットアップします。以下のコマンドを実行してください。

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
cp open-webui.service ~/.config/systemd/user/
systemctl --user enable --now open-webui.service
systemctl --user start open-webui.service
```

次に、Ollamaをインストールして、必要なモデルをダウンロードします。以下のコマンドを実行してください。

```bash
curl -fsSL https://ollama.com/install.sh | sh

# https://ollama.com/library からモデルを選択して、以下のコマンドを実行してください。
ollama pull genm
ollama serve
```
