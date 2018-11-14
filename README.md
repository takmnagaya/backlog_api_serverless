# 認可

- 先に`make deploy`でサーバレスをデプロイしておく。
  - ここでデプロイされたAPI Gatewayのエンドポイント(https://xxxxx.execute-api.region.amazonaws.com/dev/hello)をコピーしておく。
- [Application](https://backlog.com/developer/applications/)からBacklogアプリケーションを作成する。
  - リダイレクトURLにメモしたAPI Gatewayのエンドポイントを指定する。
  - アプリケーションを作成したら、「Client Id」と「Client Secret」をメモ。
- メモした「Client Id」をパラメータにつけて、下記のURLにアクセス

```sh
export CLIENT_ID=xxxxxxxx
curl https://xxx.backlog.com/OAuth2AccessRequest.action?client_id=${CLIENT_ID}&response_type=code
```
