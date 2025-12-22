# How to deploy Minecraft forge server on OCI 
Oracle Cloud Infrastracture(OCI)のFree Tier(ARM)にマイクラ鯖をたてる手順


## Requirements
- OCIのFree tierのアカウント(https://www.oracle.com/jp/cloud/free/)
  * 有料サブスクリプションにアップグレードした方がいいかも、無料枠のリソース不足で確保できない
- ssh ツール (powershellとかなんでも)
- 
  


## Deployment & Configuration
### 1.Deploy OCI instance

基本情報 
- 名前: 任意 (minecraft-forge-1.20.1) 
- コンパートメント: デフォルト 
- 配置: AD1 (OENr:AP-OSAKA-1-AD-1) 
- 拡張オプション: 変更なし 
- シェイプ: Ampere (ARM), VM.Standard.A1.Flex 
- イメージ: 任意 (OracleLinux or Ubuntu or CentOS) 
- OCPU: 任意, 4 
- メモリ: 任意, 24GB  

![Screenshot_22-12-2025_225715_cloud oracle com](https://github.com/user-attachments/assets/39329e6a-d400-43d5-84f1-964f28e04584)


ネットワーク

ネットワーキング
- vnic: 任意 (vnic01) 
- 新規仮想クラウドネットワーク 
- 名前: 任意 (vcn-network01)  

サブネット
- 名前: 任意 (subnet-network01)
- CIDR: 10.0.0.0/24  

SSHキーの追加
- キー・ペアを自動で生成
- 秘密鍵と公開鍵をダウンロードしておく  

![Screenshot_22-12-2025_23140_cloud oracle com](https://github.com/user-attachments/assets/d73794ba-b57a-45b0-96e0-8f8ada0e6d11)
![Screenshot_22-12-2025_23230_cloud oracle com](https://github.com/user-attachments/assets/0e2a5621-9259-48df-8eca-c7837575c7eb)

  
ストレージ
- ブートボリューム: デフォルト 
- ブロックボリューム: ひとまずなし  

![Screenshot_22-12-2025_23746_cloud oracle com](https://github.com/user-attachments/assets/127e2a12-a974-470c-8d53-2b06ed6d13d1)
![Screenshot_22-12-2025_23918_cloud oracle com](https://github.com/user-attachments/assets/c3bd8eb8-f961-4aa2-8ef2-a84cb831e8b3)



### 2. Create Network

![Screenshot_22-12-2025_231321_cloud oracle com](https://github.com/user-attachments/assets/f9d0071b-2644-4b38-b63e-e769521bf6b2) 
![Screenshot_22-12-2025_231356_cloud oracle com](https://github.com/user-attachments/assets/90f010fa-0498-4992-bd9a-d18f2e7da5bd) 
![Screenshot_22-12-2025_231356_cloud oracle com](https://github.com/user-attachments/assets/b0871a30-b50f-4c47-ab39-82e79eed0de3) 
![Screenshot_22-12-2025_231415_cloud oracle com](https://github.com/user-attachments/assets/56f2bd71-b86d-458f-a90b-a9eeaf1459ac) 
![Screenshot_22-12-2025_23150_cloud oracle com](https://github.com/user-attachments/assets/f3d9142c-f9b3-4030-b46a-97f4c5f21286)
![Screenshot_22-12-2025_231436_cloud oracle com](https://github.com/user-attachments/assets/75b5b9f2-a115-4601-8746-a3729b259ae9)  
![Screenshot_22-12-2025_232231_cloud oracle com](https://github.com/user-attachments/assets/f5da4fa2-dfe9-4140-b7c3-bb53252701db) 
![Screenshot_22-12-2025_232249_cloud oracle com](https://github.com/user-attachments/assets/2a7e6964-49ac-4513-887e-e2aeddb284e6) 
![Screenshot_22-12-2025_23232_cloud oracle com](https://github.com/user-attachments/assets/8a25925e-49b5-4c3a-a35e-90469509a6cd) 
![Screenshot_22-12-2025_232340_cloud oracle com](https://github.com/user-attachments/assets/9f4193f3-fda4-4a38-9813-4b1a2457cbcf) 
![Screenshot_22-12-2025_232359_cloud oracle com](https://github.com/user-attachments/assets/78a17ce5-334a-4ae8-a683-b6b348f07da5) 


### 3. Check to access ssh

- 開発者シェル > Cloud Shellを開く
- 歯車マークからプライベートキーをアップロード、パーミッション変更 
 ```$ chmod 600 [ssh-key file]```
- sshで接続  
 ```ssh -i ~/[sssh key] opc@xx.xxx.xxx.xxx```












3. 
4. 
