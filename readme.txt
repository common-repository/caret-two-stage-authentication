=== Plugin Name ===
Contributors: Caret Inc.
Tags: Caret, Login, Authentication, admin
Requires at least: 3.0.0
Tested up to: 6.4.3
Stable tag: 1.0.3
License: GPLv2
License URI: http://www.gnu.org/licenses/gpl-2.0.html

二段階認証プラグイン - Caret Two Stage Authentication

== Description ==

### 管理画面の認証にベーシック認証を追加し、簡易二段階認証を実現します。
紹介ページ
http://www.ca-ret.co.jp/?p=822

WordPressを狙った大規模な攻撃が多発しておりますが、対策として、通常ログインにもう一つベーシック認証を追加するプラグインを開発してみました。
簡易的な二段階認証ではございますが、よろしければお試しくださいませ。

== Installation ==

### ■注意事項
* 初めてエントリを追加した場合は、設定直後に認証が必要となります。
* 認証済みのエントリを変更した場合は、設定直後に再認証が必要となります。
* 大文字小文字は区別しますので、ご注意ください。
* IDまたはパスワードを忘れてしまいログインできなくなった場合は、FTPでプラグインを削除するか、「wp_caret2sa」テーブルのエントリを全て削除してください。
* エントリが0件の場合(何も設定されていない場合)、ベーシック認証は行われません。

### ■プラグインの有効化
管理ページ＞プラグイン＞Caret Two Stage Authentication を有効にしてください。

### ■設定
管理ページ＞設定＞ベーシック認証設定 にて、認証ID・認証パスワードを設定してください。

* ID・パスワードは、複数設定可で、上限はございません。
* 1アカウント追加毎に新規設定欄が追加されます。
* 削除をしたい場合は、対象となるID・パスワードを削除し、更新してください。

### ■正しい認証ID/パスワードを入力しても認証が通らない場合
.htaccessに下記を追加してみてください。

> RewriteEngine On
>
> RewriteCond %{HTTP:Authorization} ^(.*)
>
> RewriteRule ^(.*) - [E=HTTP_AUTHORIZATION:%1]

== Screenshots ==

1. 設定画面

== Changelog ==
= 1.0.3 =
* 設定画面のセキュリティを強化

= 1.0.2 =
* readme.txt修正

= 1.0.1 =
* PHP7に対応

= 1.0.0 =
* 正式版リリース

== Upgrade Notice ==
####none


== Arbitrary section ==

> 免責事項
> 
> 本プラグインは無料でご利用いただけますが、ご自身の責任においてご利用ください。
> 利用の結果生じた損害について、一切責任を負いません。予めご了承ください。
> 
> お問い合わせ、ご意見、ご要望、不具合等は、以下お問い合わせフォームよりご連絡ください。
> http://www.ca-ret.co.jp/contact
