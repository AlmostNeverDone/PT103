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
* Windows 10 (VM)</b>



[Tasks]
* Download and Verify eLiTeWrap (下載並驗證 eLiTeWrap)</b>
* Configure Antivirus Exclusions (設定防毒排除規則)</b>
* Prepare Payload Programs (準備封裝用程式)</b>
* Create a Wrapped file and Configure Execution Behaviour (建立封裝檔並配置執行行為)</b>
* Execute the Packed File and Analyse Process Behaviour (執行封裝檔並分析進程行為)</b>





---------

<h2>Practice 實踐</h2>

<p align="center">
<b>Task 1-1: Download File and Verify Integrity Using SHA256<br/> (下載檔案並使用 SHA256 驗證其完整性)</b><br/>
<img src="https://i.imgur.com/PIIR09U.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 1-2: Verify File Reputation via VirusTotal<br/> (使用 VirusTotal 驗證檔案信譽)</b><br/>
<img src="https://i.imgur.com/X2BmHGi.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
* This step extends the analysis from integrity validation to threat intelligence correlation, providing additional context for risk assessment. <br/>此步驟將分析從完整性驗證延伸至威脅情報關聯，提供額外的風險評估依據 <br/>
<br />
<br />
<b>Task 2: Configure Antivirus Exclusion<br/> (設定防毒排除)</b><br/>
<img src="https://i.imgur.com/14KHT7X.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 3: Prepare Payload Programs<br/> (準備封裝程式)</b><br/>
<img src="https://i.imgur.com/JrwDMX5.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 4: Create a Wrapped file and Configure Execution Behaviour<br/> (建立封裝檔並配置執行行為)</b><br/>
<img src="https://i.imgur.com/6qsorSJ.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 5: Execute the Packed File and Analyse Process Behaviour<br/> (執行封裝檔並分析進程行為)</b><br/>
<img src="https://i.imgur.com/lD3r5lY.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />



---------

<h2>Results 專題結論</h2>

This project demonstrates how executable wrapping techniques can be used to simulate basic Trojan behavior by packaging multiple programs into a single file and controlling their execution.

本專題展示了如何透過可執行檔封裝技術，將多個程式整合為單一檔案並控制其執行方式，以模擬基本木馬行為。

By embedding legitimate applications and configuring hidden execution, the wrapped file was able to trigger multiple processes, including background execution without direct user visibility.

透過嵌入合法程式並設定隱藏執行，封裝檔成功觸發多個程序，其中包含使用者不可見的背景執行行為。

Process analysis using Task Manager revealed abnormal behavior, such as a single executable spawning multiple processes and initiating hidden activities, which aligns with common characteristics of Trojan-based attacks.

透過工作管理員進行程序分析，觀察到異常行為，例如單一執行檔啟動多個程序並產生隱藏活動，這與典型木馬攻擊特徵一致。

In addition, file integrity verification and hash-based reputation checks were performed prior to execution, reinforcing secure analysis practices and ensuring reliable results.

此外，在執行前進行檔案完整性驗證與雜湊信譽查詢，強化了安全分析流程並確保分析結果的可靠性。

Overall, this project highlights how simple techniques can replicate real-world malware behavior and emphasizes the importance of process monitoring and behavioral analysis in detecting such threats.

總結而言，本專題展示了簡單技術如何重現真實世界的惡意程式行為，並強調透過程序監控與行為分析來偵測此類威脅的重要性。


---------

<h2>Security Insight 安全洞察</h2>

This project highlights the importance of verifying file integrity and assessing potential threats before execution, especially when dealing with externally sourced files.

本專題強調在執行外部來源檔案前，進行完整性驗證與潛在威脅評估的重要性。

By validating the SHA256 hash against a trusted source and cross-checking it with threat intelligence platforms such as VirusTotal, we ensured that the file had not been tampered with and did not match known malicious signatures.

透過比對 SHA256 雜湊值與可信來源，並進一步利用 VirusTotal 等威脅情報平台進行交叉驗證，我們確認該檔案未被竄改，且未匹配已知惡意樣本。

This demonstrates a critical security practice: hash-based validation serves as the first line of defense against supply chain attacks and malicious file distribution.

這展示了一項關鍵資安實務：基於雜湊值的驗證是防禦供應鏈攻擊與惡意檔案散佈的第一道防線。

Additionally, the workflow reinforces that static verification alone is not sufficient. Combining hash validation with reputation-based intelligence platforms improves confidence in file safety and reduces the risk of executing compromised binaries.

此外，本流程也強調僅依賴靜態驗證是不足的。結合雜湊驗證與信譽型威脅情報平台，能有效提升檔案安全性的判斷準確度，降低執行惡意程式的風險。

From a defensive perspective, this approach aligns with secure software handling practices, where every external artifact must be validated before being trusted within an environment.

從防禦角度來看，此方法符合安全軟體處理原則，即所有外部取得的檔案在被信任與使用前，都應進行驗證。

---------

<h2>Reference 參考</h2>

[UniSQ] [CSC6101 - Penetration Testing](https://handbook-guide.unisq.edu.au/course/2026/CSC6101)<br/>
[TryHackMe] [Cyber Kill Chain](https://tryhackme.com/room/cyberkillchainzmt)<br/>
<br/>
