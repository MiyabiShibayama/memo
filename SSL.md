# SSL/TLSについて
- SSLの新しいバージョンがTLS
- 大切な情報(ex. クレカの番号など)をやりとりする際に使われる
- SSL/TLSの上にHTTPをのせる(プロトコルを二重にする)ことによって暗号化
- http://ではなく、http*s*://になる

# HTTPS
- DjangoでそのままHTTPSを受け取るのはちょっと...
- Apatcheを使う
[APACHE]:https://httpd.apache.org/docs/2.4/'Apache公式'
