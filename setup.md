# セットアップ方法

## 認証鍵受け取り
dth-smbc.ovpn : vpnアクセス鍵。取扱は厳重にお願いします。絶対に外部に置かないようにしてください。  
memo.txt : VPNパスワードとVNCパスワード  
access.xlsx : VNCにアクセスするために個人に振り分けられたIPアドレスとポート番号  

## ソフトウェアインストール
### Windows
* OpenVPN
* VNCクライアントビューワー (UltraVNC等)

### Mac
* OpenVPN
* VNCクライアントビューワー(RealVNC等)

### Linux
* OpenVPN
* VNCクライアントビューワー(TigerVNC等)

## VPN接続
作業PCのあるネットワークに接続します。  
送付されたVPN公開鍵を自分のPCへ保存してください。


>**公開鍵の取り扱いには十分注意してください**  
クラウドやチャットツールにアップロードすることの無いよう注意してください。
PCのローカルストレージへコピーしなくてもCD-R等から直接VPNソフトへインポートできると思います（後述）。  
インポート後、鍵自体はできる限りオフライン環境で保管して下さい。  
ローカルのストレージへ保存する場合、Windowsだと`ドキュメント`などへ保存するとOneDriveへアップロードされてしまう可能性があるため、`¥C:/Download/vpn`など、¥C：下へ保存するようにしてください。

1. OpenVPNに公開鍵をインポートします

![import](images/import_file.png)
![select](images/ovpn_file_select.png)

2. VPNへ接続します

![connect](images/conect.png)

VPNネットワークのパスワードを入力してください。

![vpnpass](images/vpn_connect.png)

3. それっぽいダイアログが出てきたら接続完了です。ipアドレスは`10.8.0.xx`になっているはずです。

## VNC接続
作業環境PCへアクセスします。  

1. VNCクライアントアプリを起動してください

2. VNCの接続設定をします

![vnc_config](images/vnc_config.png)

* Server:port  
各グループに割り振られたPCのIPアドレスと、ご自身のポート番号を入力してください。  
`IPアドレス:ポート番号`
* 接続オプション  
エンコードは`ZRLE`, `32(64)Colors`, `Jpeg Quality=5~8` がおすすめです。

3. VNCパスワードを入力してください。

![vnc_password](images/vnc_login.png)

4. 画面が出てくれば接続成功です。少しデスクトップの表示に時間がかかるかもしれません。30秒程何も表示されなかったら、問い合わせてください。作業環境詳細については[hands_on](https://github.com/kuriatsu/rwdc-remotework-manual/blob/main/hands_on.md)参照。

![vnc_window](images/connected.png)

## データアクセス
提供データは暗号化されたHDDに格納されています。
デスクトップのリンク`workspace`からアクセスすることができます。
パスは`/home/自分の名前/Desktop/workspace/data`
です。

作業に関する詳細は[hands_on](https://github.com/kuriatsu/rwdc-remotework-manual/blob/main/hands_on.md)参照。

## 作業終了
1. VNCの切断ボタン (`Close Connection`)
2. VPN切断  

![vpn_disconnect](images/disconnect.png)

作業環境内でログオフすると、再度ログインできなくなってしまうので、注意して下さい。
手が滑った場合は管理者に連絡して下さい。
VPNへ接続すると、全てのトラフィックは作業環境ルータを経由します。  
VPN接続したままYouTube等を閲覧すると、帯域が圧迫されて、他の作業者に影響が出る可能性があるので、作業が終わったらVPNを必ず切断して下さい。
