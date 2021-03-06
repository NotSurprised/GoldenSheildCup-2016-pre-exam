# **OSI模型**
![](https://i.imgur.com/g2DLyo3.png)

# **NDP**
* 鄰居發現協議（Neighbor Discovery Protocol，NDP或ND）是TCP/IP協議層的一部分，主要與IPv6共同使用。
* 它工作在數據鏈路層，負責在鏈路上發現其他節點和相應的地址，並確定可用路由和維護關於可用路徑和其他活動節點的信息可達性。
* NDP協定工作在OSI模型的第二層(連結層)。

# **IPsec**
* 網際網路安全協定（Internet Protocol Security，IPsec）是一個協定組合，透過對IP協定的分組進行加密和認證來保護IP協定的網路傳輸協定族（一些相互關聯的協定的集合）。
* 由兩大部分組成：（1）建立安全分組流的金鑰交換協定；（2）保護分組流的協定。前者為網際網路金鑰交換（IKE）協定。
* 用於保證資料的機密性、來源可靠性（認證）、無連線的完整性並提供抗重播服務。
* IPsec被設計用來提供（1）入口對入口通訊安全，在此機制下，分組通訊的安全性由單個節點提供給多台機器（甚至可以是整個區域網路）；（2）端到端分組通訊安全，由作為端點的電腦完成安全操作。上述的任意一種模式都可以用來構建虛擬私人網路（VPN），而這也是IPsec最主要的用途之一。
* IPsec協定工作在OSI模型的第三層(網路層)，使其在單獨使用時適於保護基於TCP或UDP的協定（如安全套接子層（SSL）就不能保護UDP層的通訊流）。

# **ICMP**
* 網路控制消息協定（Internet Control Message Protocol，ICMP）是網路協議族的核心協議之一。它用於TCP/IP網絡中發送控制消息，提供可能發生在通信環境中的各種問題反饋，通過這些信息，令管理者可以對所發生的問題作出診斷，然後採取適當的措施解決。
* 它通常不由網絡程序直接使用，除了ping和traceroute這兩個特別的例子。
* 沒有埠號。
* ICMP協定工作在OSI模型的第三層(網路層)。

# **TLS**
* 傳輸層安全協議（Transport Layer Security，TLS），及其前身安全通訊協定（Secure Sockets Layer，縮寫：SSL）是一種安全協定，目的是為網際網路通訊，提供安全及資料完整性保障。
* 網景公司（Netscape）在1994年推出首版網頁瀏覽器，網景領航員時，推出HTTPS協定，以SSL進行加密，這是SSL的起源。

# **SSL**
* SSL包含記錄層（Record Layer）和傳輸層，記錄層協定確定了傳輸層資料的封裝格式。傳輸層安全協議使用X.509認證，之後利用非對稱加密演算來對通訊方做身分認證，之後交換對稱金鑰作為會談金鑰（Session key）。
* TLS協定的優勢在於它是與應用層協定獨立無關的。高層的應用層協定（例如：HTTP、FTP、Telnet等等）能透明的建立於TLS協定之上。
* 使用統一的TLS協定通訊埠（例如：用於HTTPS的埠443）

# **X.509**
* 在密碼學中，X.509是為公開金鑰基礎建設（PKI）與授權管理基礎建設（PMI）提出的產業標準。
* X.509標準，規範了公開金鑰認證、憑證吊銷列表、授權憑證、憑證路徑驗證演算法等。
* 表現層

# **POP**
* 郵局協議（Post Office Protocol，POP）是TCP/IP協定族中的一員。
* 本協定主要用於支援使用用戶端遠端管理在伺服器上的電子郵件。最新版本為POP3 （ Post Office Protocol - Version 3)，而提供了SSL加密的POP3協定被稱為POP3S。
* POP協定工作在OSI模型的第七層(應用層)。
* POP支援離線郵件處理。其具體過程是：郵件傳送到伺服器上，電子郵件用戶端呼叫郵件客戶機程式以連線伺服器，並下載所有未閱讀的電子郵件。
* 目前的POP3郵件伺服器大都可以「只下載郵件，伺服器端並不刪除」。
* 預設連接埠995。

# **FTP**
* 檔案傳輸協定（File Transfer Protocol，FTP）是用於在網路上進行檔案傳輸的一套標準協議。
* 密碼和檔案內容都使用明文傳輸，可能發生竊聽。
* 執行FTP服務的許多站點都開放匿名服務，在這種設定下，用戶不需要帳號就可以登入伺服器，預設情況下，匿名用戶的使用者名稱是：「anonymous」。
* 隨機空閒連接埠建立傳輸。
* FTP協定工作在OSI模型的第七層(應用層)。

# **SMTP**
* 簡單郵件傳輸協定 (Simple Mail Transfer Protocol， SMTP) 是在Internet傳輸email的標準。使用TCP埠25。
* 開始是基於純ASCII文字的，它在二進位檔案上處理得並不好，今大多數SMTP伺服器都支援8位元MIME擴充功能。
* SMTP是一個「推」的協定，它不允許根據需要從遠端伺服器上「拉」來訊息。要做到這點，郵件用戶端必須使用POP3或IMAP。
* SMTP協定工作在OSI模型的第七層(應用層)。

# **Telnet**
* Telnet協議是一種應用層協議，使用於網際網路及區域網中，使用虛擬終端機的形式，提供雙向、以文字字串為主的互動功能。
* 屬於TCP/IP協議族的其中之一，是Internet遠端登錄服務的標準協議和主要方式，常用於網頁伺服器的遠端控制，可供使用者在本地主機執行遠端主機上的工作。
* 傳統Telnet會話所傳輸的資料並未加密，帳號和密碼等敏感資料容易會被竊聽，因此很多伺服器都會封鎖Telnet服務，改用更安全的SSH。
* SSH協定工作在OSI模型的第七層(應用層)。

# **SSH**
* Secure Shell（縮寫為SSH），為一項建立在應用層和傳輸層基礎上的安全協定，為電腦上的Shell（殼層）提供安全的傳輸和使用環境。
* 傳統的網路服務程式，如rsh、FTP、POP和Telnet其本質上都是不安全的；因為它們在網路上用明文傳送資料、用戶帳號和用戶口令，很容易受到中間人（man-in-the-middle）攻擊方式的攻擊。
* 預設連接埠22。
* SSH協定工作在OSI模型的第七層(應用層)。
* SSH是目前較可靠，專為遠端登入對談和其他網路服務提供安全性的協定。對所有傳輸的資料進行加密，也能夠防止DNS欺騙和IP欺騙。
* 傳輸的資料可以是經過壓縮的，所以可以加快傳輸的速度。SSH有很多功能，它既可以代替Telnet，又可以為FTP、POP、甚至為PPP提供一個安全的「通道」。
* 因為受版權和加密演算法等等的限制，現在很多人都轉而使用OpenSSH。OpenSSH是SSH的替代軟體包，而且是開放源代碼且自由的。

# **HTTP/HTTPS**
* HTTP - 網路傳輸之封包為不加密明文。
* HTTPS - 網路傳輸之封包為加密文。

# **WIFI**
* 是一個建立於IEEE 802.11標準的無線局域網技術。
* 第一代802.11，1997年制定，只使用2.4GHz，最快2Mbit/s
* 第二代802.11b，只使用2.4GHz，最快11Mbit/s，正逐漸淘汰
* 第三代802.11g/a，分別使用2.4GHz和5GHz，最快54Mbit/s
* 第四代802.11n，可使用2.4GHz或5GHz，20和40MHz頻寬下最快72和150Mbit/s
* 第五代802.11ac，只使用5GHz
