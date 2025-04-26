# ToDoリストアプリ

シンプルなToDoリストアプリケーションです。React（フロントエンド）とFastAPI（バックエンド）を使用しています。

## 機能

- ToDoの追加
- ToDoの一覧表示
- ToDoの完了/未完了の切り替え
- ToDoの削除
- ToDoの編集

## プロジェクト構成

```
todo-app/
├── backend/         # FastAPIバックエンド
│   ├── app/
│   │   ├── main.py
│   │   ├── models.py
│   │   ├── schemas.py
│   │   ├── database.py
│   │   └── routers/
│   │       └── todos.py
│   ├── requirements.txt
│   └── pyproject.toml
└── frontend/        # Reactフロントエンド
    ├── src/
    │   ├── components/
    │   │   ├── TodoList.jsx
    │   │   ├── TodoItem.jsx
    │   │   └── AddTodo.jsx
    │   ├── App.jsx
    │   └── main.jsx
    ├── package.json
    └── vite.config.js
```

## セットアップ方法

### バックエンド

1. Pythonの仮想環境を作成し、有効化します：

```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windowsの場合: venv\Scripts\activate
```

2. 依存関係をインストールします：

```bash
pip install -r requirements.txt
```

または、Poetryを使用する場合：

```bash
poetry install
```

3. バックエンドサーバーを起動します：

```bash
uvicorn app.main:app --reload
```

バックエンドは http://localhost:8000 で実行されます。
APIドキュメントは http://localhost:8000/docs で確認できます。

### フロントエンド

1. 依存関係をインストールします：

```bash
cd frontend
npm install
```

2. 開発サーバーを起動します：

```bash
npm run dev
```

フロントエンドは http://localhost:5173 で実行されます。

## 使用技術

- **バックエンド**: FastAPI, SQLAlchemy, SQLite
- **フロントエンド**: React, Vite, Tailwind CSS

## 注意事項

このアプリケーションはデモンストレーション目的で作成されており、SQLiteデータベースを使用しています。本番環境では、より堅牢なデータベース（PostgreSQLなど）の使用を検討してください。
