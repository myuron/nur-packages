# nur-packages-template

**[NUR](https://github.com/nix-community/NUR) リポジトリ用のテンプレート**

## セットアップ

2. パッケージを [pkgs](./pkgs) ディレクトリと [default.nix](./default.nix) に追加します。
   * ビルドできないパッケージには `meta` 属性で `broken = true;` を設定するのを忘れないでください。さもないと travis（ひいてはキャッシュ）が失敗します！
   * ライブラリ関数、モジュール、オーバーレイはそれぞれ対応するディレクトリに配置します
3. CI を選択します。好みに応じて github actions（推奨）または [Travis ci](https://travis-ci.com) を使用できます。
   - Github actions: [.github/workflows/build.yml](./.github/workflows/build.yml) で NUR リポジトリ名を変更し、必要に応じて cachix 名を追加します。また、ファイル内の説明に従って cron タイマーをランダムな値に変更します
   - Travis ci: [.travis.yml](./.travis.yml) で NUR リポジトリ名を変更し、必要に応じて cachix リポジトリ名を変更します。その後、リポジトリで travis を有効にします。travis のリポジトリ設定で cron ジョブを追加すると、cachix キャッシュを新鮮に保つことができます
5. README のテンプレートセクションで travis と cachix の名前を変更し、残りを削除します
6. [NUR に自分を追加する](https://github.com/nix-community/NUR#how-to-add-your-own-repository)

## README テンプレート

# nur-packages

**私の個人用 [NUR](https://github.com/nix-community/NUR) リポジトリ**

<!-- github actions を使用しない場合はこれを削除してください -->
![Build and populate cache](https://github.com/<YOUR-GITHUB-USER>/nur-packages/workflows/Build%20and%20populate%20cache/badge.svg)

<!--
travis を使用する場合はこのコメントを解除してください:

[![Build Status](https://travis-ci.com/<YOUR_TRAVIS_USERNAME>/nur-packages.svg?branch=master)](https://travis-ci.com/<YOUR_TRAVIS_USERNAME>/nur-packages)
-->
[![Cachix Cache](https://img.shields.io/badge/cachix-<YOUR_CACHIX_CACHE_NAME>-blue.svg)](https://<YOUR_CACHIX_CACHE_NAME>.cachix.org)
