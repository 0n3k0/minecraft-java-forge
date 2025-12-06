How to deploy Minecraft forge server on OCI
Oracle Cloud Infrastracture(OCI)のFree Tierにマイクラ鯖をたてる手順


Requirements
OCIのFree tierのアカウント(https://www.oracle.com/jp/cloud/free/)


Deployment & Configuration
1.OCIインスタンスのデプロイ
コンピュート > インスタンス > インスタンスの作成

基本情報
名前: 任意 (minecraft-forge-1.20.1)
コンパートメント: デフォルト
配置: AD1 (OENr:AP-OSAKA-1-AD-1)
拡張オプション: 変更なし
シェイプ: Ampere (ARM), VM.Standard.A1.Flex
イメージ: 任意 (OracleLinux or Ubuntu or CentOS)
OCPU: 任意, 4
メモリ: 任意, 24GB




セキュリティ
デフォルト




ネットワークの設定

ネットワーキング
vnic: 任意 (vnic01)
新規仮想クラウドネットワーク
名前: 任意 (vcn-network01)

サブネット
名前: 任意 (subnet-network01)
CIDR: 10.0.0.0/24

SSHキーの追加
キー・ペアを自動で生成
秘密鍵と公開鍵をダウンロードしておく



ストレージ
ブートボリューム: デフォルト
ブロックボリューム: ひとまずなし






2. 
3. 
