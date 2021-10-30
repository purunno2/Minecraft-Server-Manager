# Minecraft Bedrock Server Manager 日本語化版
Original:[Benjerman](https://github.com/Benjerman)  
Original Project:[Github](https://github.com/Benjerman/Minecraft-Server-Manager)  
![Imgur](https://imgur.com/4SG0mSH.png) 
<br>
<br>

## 日本語化（まだ完全ではない）
[Benjerman](https://github.com/Benjerman)氏が開発したMinecraft Bedrock Edition（以下、統合版）の公式サーバーソフトをGUIで操作できる機能を実装したアプリケーション、
[Minecraft Bedrock Server Manager](https://github.com/Benjerman/Minecraft-Server-Manager)を日本語化しました。ただし、まだ完全ではありません。  
<br>
<br>

## フォークした理由
Java Edition（以下、Java版）マインクラフトでは、公式サーバー自体簡易的なGUIを持っており、またサーバー管理ソフトとしてサードパーティ製のものが充実しているのに対して、統合版用のサーバーソフトは2021年10月現在、アルファ版とまだ開発中ということもありJava版であったようなGUIもまだ実装されておらず、CUIベースで動作するものになっています。また、海外の方が開発されていたという事もあり、テキストなど全て英語で実装されているので、日本人にも多少使いやすくしたかったため、フォークし日本語化をしました。  
<br>
<br>

## オリジナルからの変更点
- UIを日本語化しました。
- ゲームルール欄のテキストがテキストボックスから見切れていたため、オンラインプレイヤー(Players Online)欄とゲームルール(Current Game Rules)欄を入れ替え、サーバープロパティ欄を拡張しました。
- 各ボタンの大きさ、位置を変更しました。  
<br>
<br>

## ビルド方法
ビルドに開発ソフト「[Microsoft Visual Studio 2019](https://visualstudio.microsoft.com/ja/downloads/)」以降で行う事を推奨します。  
エディションは無料のCommunityでビルド可能です。  
Microsoft Visual Studio 2019（以下、VS2019）と、C#アドオンをインストールしていることを前提での手順となります。
1. このページの<span style="background-color:rgb(35,134,54)"><span style="color:rgb(255,255,255)"> **Code** </span></span>ボタンから「Download ZIP」を押し、ダウンロードします。  
<img src="https://imgur.com/AzObz16.png" width="320">

2. 任意の場所に解凍し、`Minecraft Server Manager.sln`をクリックすると、VS2019が起動します。  

https://user-images.githubusercontent.com/69942251/139399350-ec1eea99-020b-4047-a663-4cbfc50d91f1.mp4

3. ここで、対象となるフレームワークがインストールされていないと、メッセージが出てきます。その場合は中央の「".NETFramework,Version=v4.6.1"のターゲットパックをダウンロードする(D)。プロジェクトは変更されません。」を選択します。  
※何もメッセージウィンドウが出ずに開けた場合は、「6.」へスキップしてください。  
<img src="https://imgur.com/30r9VHe.png" width="320">

4. ブラウザが起動しますので、Webサイトを下へスクロールし、.NET Framework欄の.NET Framework 4.6.1のDeveloper Packをダウンロードし、インストールします。  
<img src="https://imgur.com/J0Me4kS.png" width="320">

5. VS2019を一度閉じ、再度`Minecraft Server Manager.sln`をクリックし起動します。何も表示されなければ、ソリューション（ソースファイル群）の読み込みに成功しています。  
<br>

6. （必須ではない）最近のパソコンは64bitが主流ですので、64bitアプリとしてビルドします。VS2019上部の「Any CPU」と書いてあるプルダウンメニューを開き「構成マネージャー」を開きます。   
※32bitアプリケーションとして使用する場合は「8.」へスキップしてください。  
<img src="https://imgur.com/zvOKmW1.png" width="320">

7. 「アクティブソリューション構成(C)」を”Release”に、「アクティブソリューションプラットフォーム(P)」を”x64”にして、構成マネージャーを閉じます。  
<img src="https://imgur.com/4qd8d8H.png" width="320">

8. ビルドを行います。VS2019上部メニュー「ビルド(B)」の”ソリューションのビルド(B)”を選択するとビルドが始まります。  
<img src="https://imgur.com/hze6rfi.png" width="320">

9. `Minecraft-Server-Manager-master\Minecraft Server Manager\bin\x64\Release`の中に`Minecraft Server Manager.exe`と`Minecraft Server Manager.exe.Config`ができていればビルド成功です。  
※32bitアプリとしてビルドされた方は、`Minecraft-Server-Manager-master\Minecraft Server Manager\bin\Release`の中を参照してください。  
<img src="https://imgur.com/8PGWrAX.png" width="320">  
<br>
<br>

## 使用方法
1. [Minecraft公式ダウンロードページ](https://www.minecraft.net/ja-jp/download/server/bedrock)から統合版サーバーをダウンロードします。  
1. 任意の場所にZIPフォルダーを解凍します。  
1. `bedrock_server.exe`と同じディレクトリにビルドで出てきた2つのファイルをコピーします。  
1. Minecraft Server Manager.exeを実行し、左上の開始ボタンを押すとサーバーが稼働します。  
以上。  
<br>
止める際は停止ボタンを押すとサーバーを閉じる事が出来ます。  
<br>
<br>

## 免責
このアプリケーションのビルド、または使用によって、如何なる場合も私[purunno2](https://github.com/purunno2)、[Benjerman](https://github.com/Benjerman)氏は責任を負いかねます。  
自己責任でご利用ください。  
<br>
<br>

### 参考
- [Benjerman氏のGithubページ](https://github.com/Benjerman)
- [Benjerman/Minecraft-Server-Manager](https://github.com/Benjerman/Minecraft-Server-Manager)
- [Visual Studio Tools のダウンロード](https://visualstudio.microsoft.com/ja/downloads/)（日本語 - Japanese）
- [Bedrockサーバーダウンロード | Minecraft](https://www.minecraft.net/ja-jp/download/server/bedrock)（日本語 - Japanese）
- [Bedrock Server Download | Minecraft](https://www.minecraft.net/en-us/download/server/bedrock)（英語 - English）
- [purunno2のGithubページ](https://github.com/purunno2)
