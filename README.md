# Shopping Site
Djangoを使用して開発したショッピングサイトです。

## 1. 開発環境
- Python 3.12
- Django 4.2系
- SQLite
- HTML / CSS
- JavaScript
- Bootstrap
- Pillow（画像処理用）

## 2. 環境準備
プロジェクトのフォルダでターミナルを開き、仮想環境を作成します。
```powershell
py -3.12 -m venv .venv
```

仮想環境を有効化します。
```powershell
.\.venv\Scripts\Activate.ps1
```

必要なライブラリをインストールします。
```powershell
pip install "Django>=4.2,<5.0" Pillow
```
※ すでに環境を構築している場合は、仮想環境の作成とインストールは不要です。

## 3. プログラムの実行方法
### ① データベースの準備
```powershell
python manage.py migrate
```
※ 既存のデータベースを使用する場合も、必要に応じて実行してください。

### ② 開発サーバーの起動
```powershell
python manage.py runserver
```

ブラウザで以下のURLにアクセスします。
http://127.0.0.1:8000/

### ③ 管理者画面
管理者アカウントがない場合は、以下のコマンドで作成します。

```powershell
python manage.py createsuperuser
```

管理者画面：
http://127.0.0.1:8000/admin/
管理者画面から商品を登録できます。

Username：user
Password：admin000

## 4. 主な機能
- 商品一覧表示
- ショッピングカートへの商品追加
- 商品数量の変更
- カート内商品の削除
- 合計金額の計算
- 管理者画面での商品管理

## 5. 補足
開発サーバーは `Ctrl + C` で停止できます。

2回目以降は、仮想環境を有効化し、以下のコマンドで起動できます。

```powershell
python manage.py runserver
```

※ 決済機能は検証・改善が必要なため、実際の決済には使用しないでください。