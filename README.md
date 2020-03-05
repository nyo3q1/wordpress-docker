# nginx + php7.2-fpm + MySQL5.6 + phpMyAdminの環境

## なんでnginxとphpにプロジェクトフォルダを置いてるの？
URLでアクセスした場合、nginxにファイルがなければ404、phpにファイルがなければ実行ができないから

## phpの9000ポートは何？
nginxにはphp-fpmがないから、nginxの設定には
fastcgi_pass php:9000;
な感じにかいて処理代替するため、もしかするとデフォルトで空いてるからいらないかも

## phpMyAdminにはDBの接続先がないけど？
よく若rないけどこれでできる、公式のDockerfileみればわかるかも