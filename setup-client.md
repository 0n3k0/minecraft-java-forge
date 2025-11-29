# How to setup your PC for minecraft forge

## Requirements
- minecraft java edition 
- java 1.17
- minecraft-forge 1.20.1
 
## Deployment & Configuration

### 1. Javaのインストール (Javaをインストールしていない人)
- AdoptiumのサイトへGo  
- **JDK17-LTS**のWindowsをダウンロード   
[https://adoptium.net/temurin/releases?version=21&os=any&arch=any](https://adoptium.net/temurin/releases?version=17&os=any&arch=any)  
- DLしたインストーラー(OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10)をクリックしウィザードに従いインストール  
- コマンドプロンプトを開き以下のコマンドを実行、openjdk version "17.0.17"と出れば成功 (注:コマンド苦手な人はやらなくてもいい)    
```$ java -version```
 
### 2. Minecraft Forgeのインストール
- Forgeのサイトにgo  
  https://files.minecraftforge.net/net/minecraftforge/forge/
- 左ペインで**1.20.1**を選択 (マルチサーバのバージョンとあわせる)
- Download RecommendedのInstallerをクリック
- 5秒ぐらい待つと画面右上に赤いSKIPというボタンがでるのでSKIPをクリック
- PCにforge-1.20.1-47.4.10-installer.jarがDLされたことを確認
- DLしたインストーラーをクリック (forge-1.20.1-47.4.10-installer.jaｒ)
- Install Clientを選択し、OK
- Successfully Installedを確認
  
### 3. Minecraft Launcherを起動
  - Launcherに1.20.1-forge-47.4.10が表示されていること
  表示されていない人はなにかがおかしいのでトラシューしましょう
  

### 4. Forgeの起動構成の変更
  - Launcherの起動構成をクリックして編集  
名前: 適当に入れる (例 forge-1.21.10)  
バージョン: release 1.20.1-forge-47.4.10  
ディレクトリ: 任意（事前にディレクトリを作っておくといいかも）  
例: C:\Users\[名前]\AppData\Roaming\.minecraft\forge\1.20.1-forge-47.4.10  


### 5. 起動確認
  - 1.20.1-forge-47.4.10を選択して起動
  - Language: 日本語選択
  - 起動した画面にModが表示されていればOK


## References
 このあたりを参考にするとよいかもしれない  
https://games.xserver.ne.jp/minecraft-media/minecraft-forge/

