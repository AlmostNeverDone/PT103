# Create a Simple Trojan with eLiTeWrap
使用 eLiTeWrap 建立簡易木馬

---------

<h2>Outline 簡介</h2>

This project demonstrates how executable wrapping techniques can be used to package multiple programs into a single executable file and control their execution behavior.

本專題示範如何利用可執行檔封裝技術，將多個程式打包成單一執行檔並控制其執行行為。

Using eLiTeWrap, a wrapper tool capable of extracting and executing embedded programs, we simulate how seemingly benign applications can trigger hidden or background processes when executed.

透過 eLiTeWrap (可將程式封裝並控制執行的工具)，本實驗模擬看似正常的應用程式在執行時觸發隱藏或背景程序的情境。

The objective is to understand how basic Trojan-like behavior can be constructed through executable packaging and execution control.

本專題的目標是理解如何透過程式封裝與執行控制來構建類似木馬的基本行為。

---------
<h2>Key Learning Outcomes 主要學習成果</h2>


* Understand how EXE wrapping works and how multiple programs can be embedded into a single executable.<br/>
  理解 EXE 封裝機制，以及如何將多個程式整合為單一執行檔。
  
* Learn how to configure execution behavior (visible vs hidden, synchronous vs asynchronous).<br/>
  學習設定程式執行方式 (可見/隱藏、同步/非同步)。
  
* Demonstrate how legitimate programs can be abused to simulate Trojan-like behavior.<br/>
  示範如何利用合法程式模擬木馬行為。
  
* Analyze process behavior using Task Manager to identify hidden execution.<br/>
  使用工作管理員分析程序行為並識別隱藏執行。

* Understand basic malware delivery concepts through executable packaging.<br/>
  理解透過可執行檔封裝進行惡意程式傳遞的基本概念。



---------

<h2>Tools and Concepts Covered 涵蓋工具與概念</h2>

<div align="center">
</p>

| Category 分類                  | Tools / Concepts 工具 / 概念                                 |
| ---------------------------- | -------------------------------------------------------- |
| Malware Simulation <br/>惡意程式模擬    | eLiTeWrap EXE wrapper                                    |
| Execution Control  <br/>執行控制        | Visible vs hidden execution, synchronous vs asynchronous <br/>可見執行與隱藏執行，同步執行與非同步執行 |
| Windows Internals Windows <br/>系統    | Process execution, background processes <br/>進程執行、後台程式                                       |
| System Monitoring <br/>系統監控        | Task Manager process analysis <br/>工作管理員流程分析                                                 |
| File Packaging <br/>檔案封裝           | Executable bundling, payload execution <br/>可執行檔案捆綁、有效載荷執行                               |
| Security Evasion <br/>檢測繞過         | Antivirus exclusion configuration <br/>防毒軟體排除配置                                               |
| Attack Concept <br/>攻擊概念           | Trojan behavior simulation <br/>木馬行為模擬                                                         |


</div>
<br/>



---------


<h2>Materials and Methods 材料與方法</h2>

[Environment]
* Hyper-V virtualization platform (虛擬化平台)</b>
* Kali Linux (attacker machine)</b>
* Metasploitable vulnerable VM (target system)</b>


[Tasks]
* Explore Available Wordlists in Kali Linux (探索 Kali Linux 內建字典檔)</b>
* Create a Custom Password Wordlist (建立自訂密碼字典檔)</b>
* Create a Custom Username Wordlist (建立自訂使用者名稱字典檔)</b>
* Identify Target Services with Nmap (使用 Nmap 掃描目標主機服務)</b>
* Perform Dictionary Attack Using Hydra (使用 Hydra 進行字典攻擊)</b>
* Alternative Attack via FTP (改透過 FTP 攻擊)</b>
* Discover Valid Credentials (取得有效登入憑證)</b>
* Access the Target System via SSH (透過 SSH 登入目標系統)</b>
* Verify System Access and Close Session (驗證系統存取並結束連線)</b>



---------

<h2>Practice 實踐</h2>

<p align="center">
<b>Task 1: Explore Available Wordlists in Kali Linux<br/> (探索 Kali Linux 內建字典檔)</b><br/>
<img src="https://i.imgur.com/8XNQ45l.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 2: Create a Custom Password Wordlist<br/> (建立自訂密碼字典檔)</b><br/>
<img src="https://i.imgur.com/L9COezx.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 3: Create a Custom Username Wordlist<br/> (建立自訂使用者名稱字典檔)</b><br/>
<img src="https://i.imgur.com/BfvI0ec.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
* Credential enumeration preparation <br/>(憑證列舉準備) <br/>
<br />
<br />
<b>Task 4: Identify Open Services with Nmap<br/> (使用 Nmap 掃描目標主機服務)</b><br/>
<img src="https://i.imgur.com/5yOi4HF.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 5-1: Attempt SSH Dictionary Attack with Hydra<br/> (嘗試對 SSH 進行字典攻擊)</b><br/>
<img src="https://i.imgur.com/7R7g8jE.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 5-2: Perform FTP Dictionary Attack<br/> (使用 FTP 進行字典攻擊)</b><br/>
<img src="https://i.imgur.com/xsCMWyc.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 5-3: Resolve SSH Key Exchange Compatibility Issue<br/> (解決 SSH 金鑰交換相容性問題)</b><br/>
<img src="https://i.imgur.com/co8e8HW.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 6: Attempt SSH Login with Discovered Credentials<br/> (使用取得的帳密嘗試 SSH 登入)</b><br/>
<img src="https://i.imgur.com/BBGaJf8.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


---------

<h2>Results 專題結論</h2>

This project demonstrated how a dictionary attack can be used to obtain valid credentials from exposed network authentication services.

本專題展示了如何透過字典攻擊取得網路認證服務中的有效帳號與密碼。

During the reconnaissance phase, Nmap scanning identified that the target system exposed several network services, including SSH and FTP.

在偵察階段中，透過 Nmap 掃描確認目標主機開放多個網路服務，包括 SSH 與 FTP。

An initial dictionary attack against the SSH service failed due to a key exchange algorithm incompatibility between the modern SSH client and the legacy target system. The attack was then redirected to the FTP service, which successfully revealed valid credentials through Hydra. After resolving the SSH algorithm compatibility issue on the client side, the discovered credentials were used to successfully authenticate to the target system.

最初對 SSH 服務發動的字典攻擊因現代 SSH 客戶端與舊版目標系統之間的金鑰交換演算法不相容而失敗。因此攻擊改為針對 FTP 服務進行，並透過 Hydra 成功取得有效帳號與密碼。在調整 SSH 客戶端以支援舊版加密演算法後，成功使用取得的帳密登入目標系統。

Overall, this experiment illustrates how weak credentials and exposed authentication services can lead to unauthorized system access.

總體而言，本實驗展示了弱密碼與暴露的認證服務如何導致未授權系統存取。


---------

<h2>Security Insight 安全洞察</h2>

This exercise highlights several important security considerations related to authentication services.

本次實作揭示了多項與網路認證服務相關的重要安全議題。

First, dictionary attacks remain highly effective when users rely on weak or commonly used passwords.

首先，當使用者使用弱密碼或常見密碼時，字典攻擊仍然非常有效。

Second, exposing multiple authentication services such as SSH and FTP increases the attack surface of a system.

其次，同時暴露多個認證服務（例如 SSH 與 FTP）會增加系統的攻擊面。

Third, legacy systems that rely on outdated cryptographic algorithms may introduce compatibility issues and security risks.

第三，依賴過時加密演算法的舊版系統不僅可能造成相容性問題，也可能帶來安全風險。

To mitigate these risks, organizations should enforce strong password policies, implement account lockout mechanisms, and restrict unnecessary authentication services.

為降低這些風險，組織應實施強密碼政策、登入失敗鎖定機制，並限制不必要的認證服務。

Additionally, legacy protocols and outdated cryptographic algorithms should be phased out to improve overall system security.

此外，應逐步淘汰舊版協定與過時的加密演算法，以提升整體系統安全性。

---------

<h2>Reference 參考</h2>

[UniSQ] [CSC6101 - Penetration Testing](https://handbook-guide.unisq.edu.au/course/2026/CSC6101)<br/>
[TryHackMe] [Cyber Kill Chain](https://tryhackme.com/room/cyberkillchainzmt)<br/>
[TryHackMe] [Nmap: The Basics](https://tryhackme.com/room/nmap)<br/>
[TryHackMe] [Hydra](https://tryhackme.com/room/hydra)<br/>
<br/>
