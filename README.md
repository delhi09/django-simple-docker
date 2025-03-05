# django-simple-docker

## 前提

- Djangoの公式チュートリアルの1まで完了した状態
  - https://docs.djangoproject.com/ja/5.1/intro/tutorial01/#id1
- `settings.py`にプロダクション想定で以下を設定
  - `DEBUG = False`
  -  `ALLOWED_HOSTS = ["*"]`

## 動作確認

```sh
docker build -t djangotutorial .
docker run -p 8000:8000 djangotutorial
```

http://localhost:8000/polls/ にアクセスすると「Hello, world. You're at the polls index.」と表示される

## フォーマット

```sh
ruff check . --fix && ruff format .
```
