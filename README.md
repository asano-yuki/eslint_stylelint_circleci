# 目的
ESLint、StyleLintをCircleCIで実行
# ポイント
## config.yml
`.circleci`配下に`config.yml`を作成。<br/>
複数のjobを実行する場合はを`workflows`の指定が必要。
```
jobs:
  eslint:
    ...
  stylelint:
    ...
workflows:
  build-deploy:
    jobs:
      - eslint
      - stylelint
```
