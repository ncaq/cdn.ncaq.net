# What

<https://cdn.ncaq.net/>のソースです。

HTTPで配布したいものを置きます。

# デプロイ

masterにpushされると、
GitHub Actionsのセルフホストランナーが自宅サーバseminarの配信ディレクトリへrsyncします。

配信はseminarのCaddyからCloudflare Tunnel経由で行われます。
サーバ側の設定は[dotfiles](https://github.com/ncaq/dotfiles)の`nixos/host/seminar/cdn.nix`、
DNSなどは[infra.ncaq.net](https://github.com/ncaq/infra.ncaq.net)にあります。
