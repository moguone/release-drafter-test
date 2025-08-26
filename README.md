# Release Drafter Test Repository

このリポジトリは [release-drafter](https://github.com/release-drafter/release-drafter) の動作検証用です。

## 機能

- PRをマージするたびにドラフトリリースが自動更新
- セマンティックバージョニングに基づく自動バージョン管理
- PRラベルによる変更履歴の自動カテゴリ分類
- リリース公開時の自動デプロイ

## ワークフロー

1. **Pull Request作成** → ラベルを付与
2. **mainブランチへマージ** → ドラフトリリース自動更新
3. **リリース公開** → タグ付与＆デプロイ実行

## 利用可能なラベル

### バージョン管理
- `major` - メジャーバージョンアップ (1.0.0 → 2.0.0)
- `minor`, `feature`, `enhancement` - マイナーバージョンアップ (1.0.0 → 1.1.0)
- `patch`, `fix`, `bug` - パッチバージョンアップ (1.0.0 → 1.0.1)

### カテゴリ分類
- 🚀 Features: `feature`, `enhancement`
- 🐛 Bug Fixes: `fix`, `bugfix`, `bug`
- 🧰 Maintenance: `chore`, `maintenance`
- 📚 Documentation: `documentation`, `docs`
- ⬆️ Dependencies: `dependencies`, `deps`

## セットアップ

このリポジトリの設定を参考にする場合：

1. `.github/release-drafter.yml` - release-drafterの設定
2. `.github/workflows/release-drafter.yml` - ドラフトリリース更新
3. `.github/workflows/deploy.yml` - リリース時のデプロイ