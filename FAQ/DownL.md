## 下载
---
### 什么是密钥系统？它是怎么工作的？

密钥系统在BT客户端连接Tracker服务器时起到验证身份的作用。每一个用户都有一个系统随机生成的密钥。当用户下载某个种子文件时，他的私人密钥被添加到种子文件的Tracker服务器URL中。通过这种方式，你可以在家中或者办公室使用不同的IP来做种某个文件。 

---

### 什么时候我需要重置我的密钥?

*  如果你的密钥被泄漏，且别的用户正在使用这个密钥（即使用你的帐户）下载文件。在这种情况下，你能在你的详情页面看到你并未下载或上传的种子。
* 当你的客户端崩溃，或者你的连接并没有正常被终止。在这样的情况下，就算你已经关闭了你的客户端，你仍然在你的详情页面看到正在上传\/下载的记录。通常情况下这些“冗余种子”将在30分钟之内被自动清除，但是如果你马上继续你的下载而服务器又提示“You already are downloading the same torrent”的错误，那么你需要重置你的密钥，然后重新下载种子文件，之后继续下载过程。

---

### DHT是什么？为什么一定要关闭这个功能？

DHT必须从你的客户端被禁止。DHT可能导致你的数据被错误地记录，可以视为一种作弊行为。任何使用DHT的用户将因作弊而被系统禁止。

 幸运的是，目前Tracker服务器会自动分析用户上传的种子文件，强制去除DHT的支持。这也是为什么种子发布者必须重新下载种子才能正常做种的原因之一。 

---

### 为什么我的磁盘还有充足的空间，客户端却提示磁盘剩余空间不足？

很可能是因为你的磁盘分区的文件系统为FAT32，该文件系统不支持大于4GB的单个文件。如果你使用的是Windows系统，你可以在磁盘的属性中查看其文件系统信息。你可以将磁盘文件系统转换成更高级的NTFS来解决该问题。

---

### 我可以任意选择Bittorrent客户端软件么？

根据对常见BitTorrent客户端的测试，目前本站Tracker**只允许**使用以下的BitTorrent客户端软件。 

 **Windows:**

* [Azureus](http://azureus.sourceforge.net): 2.5.0.4, 3.0.5.0, 3.0.5.2及后续版本
* [uTorrent](http://www.utorrent.com): 1.6.1, 1.7.5, 1.7.6, 1.7.7, 1.8Beta\(Build 10364\), 2.0\(Build 17624\),3.0\(Build 25583\),3.1及后续版本
* [BitTorrent](http://www.bittorrent.com): 6.0.1, 6.0.2, 6.0.3及后续版本
* [Deluge](http://deluge-torrent.org): 0.5.9.1, 1.1.6及后续版本
* [Rufus](http://rufus.sourceforge.net): 0.6.9, 0.7.0及后续版本

**Linux:**

* [Azureus](http://azureus.sourceforge.net): 2.5.0.4, 3.0.5.0, 3.0.5.2及后续版本
* [Deluge](http://deluge-torrent.org): 0.5.9.1, 1.1.6及后续版本
* [Rufus](http://rufus.sourceforge.net): 0.6.9, 0.7.0及后续版本
* [Transmission](http://www.transmissionbt.com): 1.21及后续版本
* [rTorrent](http://libtorrent.rakshasa.no): 0.8.0（配合libtorrent 0.12.0或后续版本）及后续版本
* [Enhanced CTorrent](http://www.rahul.net/dholmes/ctorrent/): 3.3.2及后续版本

**MacOS X:**

* [Azureus](http://azureus.sourceforge.net): 2.5.0.4, 3.0.5.0, 3.0.5.2及后续版本
* [Transmission](http://www.transmissionbt.com): 1.21及后续版本
* [BitRocket](http://sourceforge.net/projects/bitrocket/): 0.3.3\(32\)及后续版本

**Symbian \(仅供测试\):**

* [SymTorrent](http://amorg.aut.bme.hu/projects/symtorrent): 1.41及后续版本

 **以上客户端在https支持方面**

* uTorrent 1.61: 无法准确解析https的tracker, 同时在使用会将自己标识为uTorrent 1.5
* Rufus: 没有https支持, 并且已经几年没有继续开发
* rtorrent: 需要手工设置SSL证书, 详细信息请自行查阅其官方网站说明

同时请尽量避免使用处于测试期的客户端软件, 如uTorrent 1.8.0B。 为了从本站得到最好的下载体验,我们高度推荐[uTorrent](http://www.utorrent.com/download.php) 以及[Azureus](http://azureus.sourceforge.net/download.php)这两个软件的最新稳定版。 

---

### 我该怎样续传文件或者给一个文件续种呢？

打开扩展名为.torrent的文件，当你的客户端软件询问保存的目录时，选择已经存在的文件存放的目录，它就能够开始续传\/续种了。 

---

### 100MB大小的种子，我怎么下了120MB的东西回来?

参见哈希验证失败的那个问题。如果你的客户端收到了错误的数据，那么它将会重新下载这一部分，因此总下载量有可能比种子大小略微大一些。确保“屏蔽发送错误数据的客户端”的那个选项被打开了，这样可以减少额外的下载。 
