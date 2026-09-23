# Maraxsis Classic 日本語翻訳パッチ

Factorio 2.1 用の独立 Mod です。[Maraxsis Classic](https://github.com/kryzeth/maraxsis-classic) 本体には変更を加えず、日本語 locale を上書きします。本体 Mod が必要です。

日本語訳は upstream の `locale/ja/locale.cfg` を基に修正し、`1.33.10`（コミット `c077483abc0a1caabeff155969338cb462ec1ced`）の `locale/en/locale.cfg` を基準にしています。

## インストール

このディレクトリの `info.json`、`LICENSE`、`locale/ja/locale.cfg` を、`maraxsis-classic-ja_0.1.0` という名前のフォルダに入れて ZIP 化し、Factorio の `mods` フォルダに置きます。リポジトリのルートで作る場合:

```sh
python3 - <<'PY'
import json
from pathlib import Path
from zipfile import ZipFile

info = json.loads(Path('info.json').read_text())
name = f"{info['name']}_{info['version']}"
with ZipFile(f'{name}.zip', 'w') as archive:
    for path in ('info.json', 'LICENSE', 'locale/ja/locale.cfg'):
        archive.write(path, f'{name}/{path}')
PY
```

作成した `maraxsis-classic-ja_0.1.0.zip` を友人に共有できます。全員が同じバージョンの Maraxsis Classic と翻訳パッチを使用してください。
