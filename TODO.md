# TODO

NUR テンプレートからの移行に伴う残タスク。

## 完了済み
- [x] パッケージ追加：`pkgs/ghq-fzf/` を作成し `default.nix` に `ghq-fzf` を登録
- [x] CI 選択：GitHub Actions（`.github/workflows/build.yml`）を採用

## 残タスク

### 1. `.github/workflows/build.yml` のプレースホルダ置換
- [ ] `<YOUR_REPO_NAME>`（24, 74行目）→ NUR リポジトリ名（例 `nur-packages`）に変更
  - ※ 57・75行目の `if:` 内はテンプレの動作判定用なので**置換しない**
- [ ] `<YOUR_CACHIX_NAME>`（36, 56行目）→ cachix を使うなら設定、使わないなら該当箇所を削除
- [ ] cron タイマー（12行目 `'51 2 * * *'`）→ ランダムな値に変更

### 2. README の整備（`README.md` / `README_ja.md` 両方）
- [ ] 冒頭の template 説明＋ Setup セクションを削除
- [ ] `<YOUR-GITHUB-USER>` → `myuron`
- [ ] `<YOUR_CACHIX_CACHE_NAME>` → cachix 名（未使用ならバッジ削除）
- [ ] タイトルを `nur-packages-template` → `nur-packages` に変更

### 3. NUR へ自分を登録
- [ ] [NUR リポジトリ](https://github.com/nix-community/NUR#how-to-add-your-own-repository) の `repos.json` に PR を出す

### 4. コミット
- [ ] `default.nix`（変更）、`README_ja.md`・`pkgs/ghq-fzf/`（未追跡）をコミット
