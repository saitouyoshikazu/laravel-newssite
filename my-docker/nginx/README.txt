1.  hostsファイルに以下の設定を追加して下さい。
        127.0.0.1 laravelnewwssite.com
        127.0.0.1 www.laravelnewwssite.com
        127.0.0.1 admin.laravelnewwssite.com

2.  ブラウザでhttps://www.laravelnewssite.comにアクセスして下さい。
    その際、SSL証明書関連で警告が発生すると思われます。
    警告を無視してアクセスしても構いませんが、気になる方は
        my-docker/nginx/ssl/server.crt
    が発行機関の証明書(ルート証明書)になりますので、
    my-docker/nginx/ssl/server.crtを信頼されたルート証明として登録して下さい。
