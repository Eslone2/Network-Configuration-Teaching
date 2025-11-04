**ネットワーク構築_講習会(第一回)**
<br>
*Network_installation/Building_Workshop(1st_session)*
<BR><br>
**今回の最終目標**
<br>
*The topics for the time*
<br>
・IPアドレスやサブネットマスク、ネットワークアドレスの仕組みとは？<br>
*(Understand how to works of IP addersses, subnet masks and Network addresses.)*
<br>
・ネットワーク内で、ルータやL2スイッチはどのような役割を果たしている？<br>
*(In the Network systems, what to do for network routing, and L2 switching?)*
<br>＞次回以降かも？<br>
**メインの話に入る前に…**
<br>But first...
<br>
皆さんのPC(特にWindows)に"**Teraterm**"が入っているか確認します！
<br>
Have you installed the "**Teraterm**?"
<br>
無ければ[**こちら**](https://github.com/TeraTermProject/teraterm/releases)からダウンロードとインストールを行って下さい！
<br>
If you have not installed it, prease click [**here**](https://github.com/TeraTermProject/teraterm/releases) to download and install !!
<br>
<br>
※第２回以降で使用する予定です！！消さないでね！！
<br>To be used from the second session onwards. Please keep this!!
<br>
<br>
**IPアドレスやサブネットマスク、ネットワークアドレスの仕組み**
<br>
*How to works of IP addersses, subnet masks and Network addresses*
<br>
<br>
**IPアドレスの仕組み**
<br>(What's the "IP address?")
<br>
IPアドレスとは、(ざっくり言うと)**インターネット上の住所**のようなものです！
<br>また、通信が出来なくなるので**IPアドレスは絶対に重複させてはいけない**です！
<br>
例えば…
<br>手紙を送った人 青森県青森市XX町x丁目x-x 
<br>手紙を受け取る人 青森県八戸市xx町x丁目x-x
<br>だったとして、この住所をIPアドレスに置き換えると…
<br>データを送る機器 172.155.10.1
<br>データを受け取る機器 153.128.11.1
<br>という感じです(細かな違いはありますが)
<br>※ここでの説明は基本**IPv4**で説明していきます。**IPv6**はそのうち説明します！
<br>(**IPv4**は32bitで動作します)
<br>
<br>**ネットワーク部とホスト部**
<br>ネットワーク部とは、**どのネットワークに所属しているかを示す数字です**！アパートで言う「〇〇ヒルツ」です(EX. **172.155.10**.1)。
<br>ホスト部は、**上記のネットワーク内の、どの特定のデバイスかを示す数字です**！
<br>アパートで言う「xxx号室」の所です(EX. 172.155.10.**1**)。
<br>※太字の部分がネットワーク部、ホスト部です
<br>
参考：[IPアドレス-「分かりそう」で「分からない」でも「分かった」気になれるIT用語辞典](https://wa3.i-3-i.info/word172.html)
<br>
<br>
※ちなみに、IPアドレスは国や地域ごとに決まっています！<br>
参考：[IPアドレス一覧【whoisサーバ一覧】-CMAN](https://www.cman.jp/network/support/IP_list.html)
<br>
<br>「IPアドレス」ってなんの略称だよ！って思ったそこのあなた！
<br>IP AddressはInternet Protocol Addressの略称です。
<br>(Protocolについては後ほど説明します！)
<br>ざっくり言うと、**インターネット上のお約束事(Protocol)を守った住所(Address)の記入方法**です！
<br>どこでIPアドレスが活用されるかは、後ほど説明します。<br>
<br>
**サブネットマスクの仕組み**
<br>
サブネットマスクとは、**ネットワーク部とホスト部の区分け方の説明書**です。
<br>参考：[サブネットマスク-「分かりそう」で「分からない」でも「分かった」気になれるIT用語辞典](https://wa3.i-3-i.info/word11975.html)
<br><br>
※サブネットマスクは計算で求められます。
<br>例えば、サブネットマスクが「255.255.255.0」だったとします。<br>これを**2進法**(0と1のみ)に変換すると「11111111.11111111.11111111.00000000」になります。
<br>これの「**11111111.11111111.11111111**.00000000」の部分がネットワーク部です。
<br>また、これの「11111111.11111111.11111111.**00000000**」の部分がホスト部です。

では、実際にネットワーク部とホスト部を分けてみましょう。<br>
①255.255.0.0 のときの 192.168.0.2<br>
②11111111.00000000.00000000.00000000 (2進法) のときの 192.168.163.1
