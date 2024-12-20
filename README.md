# iOS TLS Configuration Profile

## 概要

このプロファイルは、iOS 18以降で制限されているTLS 1.0/1.1の通信を、特定のドメイン（*.secure.ne.jp）に対してのみ許可するための設定プロファイルです。

### インストール方法

1. [こちらのリンク](https://mc-nekoneko.github.io/cpi-mail/cpi-mail-profile.mobileconfig)をiOSデバイスで開く
2. プロファイルのダウンロードを許可
3. 設定アプリを開く
4. 「プロファイルがダウンロードされました」という通知をタップ
5. インストールボタンをタップ
6. デバイスのパスコードを入力
7. 警告を確認してインストールを完了

### インストール用QR
![qrcode_mc-nekoneko github io](https://github.com/user-attachments/assets/0266d0ee-eda9-4246-8f6c-7b613dc21ef4)

### アンインストール方法

1. 設定アプリを開く
2. 「一般」→「VPNとデバイス管理」を選択
3. [TLS Exception Settings] を選択し、プロファイルを削除

### 注意事項
- このプロファイルは`*.secure.ne.jp`ドメインのみに影響します
- 必要がなくなった場合は設定からプロファイルを削除してください。

## メールアプリの設定方法

### 事前準備
1. プロファイルのインストールを完了してください
2. メールアプリを一度完全に終了してください

### 新規アカウント設定手順
1. 「設定」アプリを開く
2. 「メール」→「アカウント」→「アカウントを追加」を選択
3. 「その他」→「メールアカウントを追加」を選択
4. 基本情報を入力
   - 名前
   - メールアドレス
   - パスワード

### 受信メールサーバー（IMAP）の設定
1. 「受信メールサーバー」セクションで以下を設定：
   - ホスト名: `xxxx.secure.ne.jp`（お使いのサーバーに応じて変更）
   - ユーザー名: メールアドレス
   - パスワード: メールアカウントのパスワード
   - 「詳細設定」をタップ
   - **重要**: 「SSL」をオフにする

### 送信メールサーバー（SMTP）の設定
1. 「送信メールサーバー」セクションで以下を設定：
   - ホスト名: `xxxx.secure.ne.jp`（お使いのサーバーに応じて変更）
   - ユーザー名: メールアドレス
   - パスワード: メールアカウントのパスワード
   - 「詳細設定」をタップ
   - **重要**: 「SSL」をオフにする

### 既存アカウントの設定変更
1. 「設定」→「メール」→「アカウント」
2. 対象のアカウントを選択
3. 「アカウント」→「詳細設定」
4. 「受信設定」セクション
   - **重要**: 「SSL」をオフにする

## Gmailアプリでの設定方法

純正メールアプリでの設定が正常に機能しないことがあります。その場合は、以下の手順でGmailアプリから設定を行ってください。
> **注意**: ページ上部の専用プロファイルのインストールを完了してください。

### Gmailアプリのインストール
[App Store](https://apps.apple.com/jp/app/gmail-google-のメール/id422689480)からGmailアプリをインストール
   
#### インストール用QR
![image](https://github.com/user-attachments/assets/a820b099-0696-4c83-a6b5-8210f6830a85)

### Gmailアプリでのメール設定手順
1. Gmailアプリを開き、ログインボタンを押下
2. メールの設定画面で「その他（IMAP）」を選択
3. メールアドレスを入力し、「次へ」を押下

### 受信サーバー（IMAP）の設定
- ユーザー名: 設定するメールアドレス
- パスワード: メールアカウントのパスワード
- IMAPサーバー: `xxxx.secure.ne.jp`（お使いのサーバーに応じて変更）
- ポート: 993
- セキュリティの種類: SSL/TLS

### 送信サーバー（SMTP）の設定
- ユーザー名: 設定するメールアドレス
- パスワード: メールアカウントのパスワード
- SMTPサーバー: `xxxx.secure.ne.jp`（お使いのサーバーに応じて変更）
- ポート: 465
- セキュリティの種類: SSL/TLS

## Outlookアプリでの設定方法

純正メールアプリでの設定が正常に機能しないことがあります。その場合は、以下の手順でOutlookアプリから設定を行ってください。
> **注意**: ページ上部の専用プロファイルのインストールを完了してください。

### Outlookアプリのインストール
[App Store](https://apps.apple.com/jp/app/microsoft-outlook/id951937596)からOutlookアプリをインストール

#### インストール用QR
![qrcode_apps apple com](https://github.com/user-attachments/assets/7669aa2f-2998-4ead-a544-9abc5d4941ef)

### Outlookアプリでのメール設定手順
1. Outlookアプリを開く
2. 「アカウントの追加」を押下
3. メールアドレスの欄に設定するメールアドレスを入力し、「アカウントの追加」を押下
4. メールアドレスに設定するメールアドレスを入力

### 受信サーバー（IMAP）の設定
- IMAPサーバー: `xxxx.secure.ne.jp`（お使いのサーバーに応じて変更）
- ポート: 993
- セキュリティの種類: SSL
- ユーザー名: 設定するメールアドレス
- パスワード: メールアカウントのパスワード

### 送信サーバー（SMTP）の設定
- SMTPサーバー: `xxxx.secure.ne.jp`（お使いのサーバーに応じて変更）
- ポート: 465
- セキュリティの種類: SSL
- ユーザー名: 設定するメールアドレス
- パスワード: メールアカウントのパスワード

