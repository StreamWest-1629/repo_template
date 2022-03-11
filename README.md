# repo_template
面倒だと思うその前にtemplateを作りました．

## ブランチ運用ルール（`Git-flow`ベースな感じ）
- Issueに紐づいたブランチを作るときはIssueのDevelopmentからブランチを切る
    - Issueとブランチを紐づけて管理しやすくするため
- コミット時には必ず先頭に `#[Issue番号]:` を付ける
    - Issueから追跡できるようにするため
- ブランチ名に関しては下に示すものに加え，プロダクトに応じて `release`, `staging`, `nightly` などのブランチを用意しておく．

### ブランチ命名規則とその運用
| ブランチ名 | 運用方法 | チェックアウト/マージ先 |
| :-: | :-- | :-: |
| `main` | 開発用ブランチ．<br/>ここで直接作業を行わないでください． | （最上位格） |
| `[Issue番号]-improve/[Issue説明]` | 機能実装系のIssueを裁く際のブランチ．<br/>IssueのDevelopmentから作ると左記のようなブランチ名になるはず． | `main` |
| `[Issue番号]-bugfix/[Issue説明]` | バグ修正系のIssueを裁く際のブランチ．<br/>IssueのDevelopmentから作ると左記のようなブランチ名になるはず． | `main` |
| `[Issueベース系ブランチ名]/hotfix` | `main` ブランチ以外で修正を行う必要があるときに使用するブランチ．<br/>`123-bugfix/緊急の修正/hotfix` みたいな使い方をする． | 任意のブランチ |
