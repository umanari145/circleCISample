# circleCISample

## インストール
```
curl https://raw.githubusercontent.com/CircleCI-Public/circleci-cli/master/install.sh --fail --show-error | zsh
```
curlが新しければ↓
```
 curl -fLSs https://circle.ci/cli | bash

```
https://circleci.com/docs/ja/2.0/local-cli/

## チュートリアル
```
mkdir .circleci
touch .circleci/config.yml
```

config.ymlにタスクのファイルを記述

```
#　設定ファイルのエラーチェック
circleci config validate

# 正しいとき
Config file at .circleci/config.yml is valid.

# 誤っている時
Error: Unable to parse YAML
詳細なエラー内容
```

タスクのビルド
```
circleci local execute

Downloading latest CircleCI build agent...
Docker image digest: sha256:a5b42b7078a01dc90449e50b10887d5ae2c3263cbce3db9aae800e63cf1d2f3b
====>> Spin up environment

Dockerのイメージのダウンロード(初回は時間がかかる)

The redacted variables listed above will be masked in run step output.====>> echo "Hello World"
  #!/bin/bash -eo pipefail
echo "Hello World"
Hello World
Success!

#Successが出ていたらOK
```
