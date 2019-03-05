# REST API について
## REST API
- RESSTful APIのこと。Webシステムを外部から利用するためのプログラムの呼び出し規約(API)の種類の一つで、RESTと呼ばれる設計原則に従って策定されたもの

## REST
- REpresentational State Transfer
  WebサービスのURIにHTTPメソッドでアクセスすることでデータの送受信を行う

## API
- Application Programming Interfaceのこと。プログラムからソフトウェアを操作するためのインターフェイス
*インターフェイス*
- 何かと何かをつなぐもの ex.)USBなど

### 原則
1. アドレス指定可能なURIで公開されていること
2. インターフェース(HTTPメソッドの利用)の統一がされていること
3. ステートレスであること
4. 処理結果がHTTPステータスコードで通知されること

## REST APIとAPIの違い
REST APIでは...
- URLがユーザー情報に対応している(処理によってURLを変えたりしない)
　ユーザーID等はURLに含んでシステム側に渡す
- HTTPの一般的なリクエストメソッド(GET POST PUT DELETEなど)を利用して処理を決定する
