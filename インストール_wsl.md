Windows Subsystem for Linux（WSL）は、Windows 10上でLinuxを実行できる機能です。以下は、WSLをインストールする手順です。

**注意:**  WSLのバージョンは1と2があり、WSL 2が最新であり、推奨されています。WSL 2はHyper-Vテクノロジーを使用してLinuxカーネルをエミュレートするため、性能が向上し、機能が追加されています。以下は、WSL 2を使用してインストールする手順です。 
1. **Windowsのバージョンを確認する** :
WSL 2はWindows 10 バージョン 1903 以降で利用可能です。バージョンがそれより古い場合、Windowsのアップデートを検討してください。 
2. **WSLの有効化** :
WSLを有効化するには、コマンドプロンプトを管理者権限で実行し、次のコマンドを実行します。

```bash
#versionの確認
wsl --version

#コマンドのアップデート
wsl --update

#デフォルトではubuntuがインストールされる
wsl --install

#エラーが出たら下記を実施してみる
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

#それでもだめならBIOSの設定を変更する
``` 
3. **初回起動と設定** :
インストールが完了したら、Linuxディストリビューションを起動します。初回起動時にユーザー名とパスワードを設定します。その後、パッケージのアップデートや必要なソフトウェアのインストールが可能です。

これで、WSLがWindows 10に正常にインストールされ、Linuxを実行できるようになります。WSLはWindowsとLinux間でシームレスな統合を提供し、開発やシステム管理などのさまざまなタスクに役立ちます。
