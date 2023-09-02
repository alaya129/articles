# The best way to acquire knowledge from readings
![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled-278f62136fe5d8d7792f86f9d1d75c63.png)

本文重點[​](#本文重點 "Direct link to 本文重點")
------------------------------------

> 將筆記視覺化的目的，是對你所學的知識建立深度理解。如果你的每一個筆記都非常長、如果你沒有把知識打碎、原子化，你能透過視覺化獲得的理解就會非常有限。真正的深度理解並不存在於「二本書之間的關聯性」裡頭，而是存在於「二本書中的所有概念之間的關聯性」裡頭。
> 
> 只有當你將筆記原子化時，你才能透過筆記視覺化對你在乎的主題獲得深度理解。原子化指的並非你不能有很長的筆記，而是指每個概念筆記都只應包含一個概念，並以其內文來支撐這個概念。你必須能將每張概念卡片的核心概念用一句話總結，並以這句話當做是卡片標題以確保你一眼就能知道它在講什麼。

前言[​](#前言 "Direct link to 前言")
------------------------------

身為一個時常閱讀的人，閱讀最讓我感到困擾的地方在於那些最好的書往往包含大量的內容，要完全地將這些內容消化、與我的既有知識整合有時並不容易。就算我將內容消化了，時間一久，當我在工作時突然想用以前所學的知識時，往往也很難單靠大腦記憶就回想起過去的所學。

這個問題不只發生在我身上，也發生在我認識的許多人身上。我想這也是大部分筆記軟體（又稱知識管理軟體）想要解決的問題。但不幸的是，我覺得大部分的筆記軟體都過度專注在教你用什麼架構去保存筆記（例：階層、網狀、資料庫），卻沒有在**吸收知識（acquisition）、留存知識（retention）和應用知識（application）**等學習過程中最關鍵的環節提出改善方案。

在這篇文章中，我會分享我自身學習的實際案例，展示我設計的一個用 Heptabase 來有效獲取、留存和應用知識的方法。這個方法雖然不是學習的唯一方法，但是一個我驗證過極為有效的方法，而且我相信大部分的人都可以很快地學會將它應用在自己的學習中。

方法簡介[​](#方法簡介 "Direct link to 方法簡介")
------------------------------------

著名的費曼學習法認為深度學習一個主題最好的方式，就是嘗試把你在學習的主題教給小孩。我的想法是不管你想要教別人什麼，你都必須先**釐清你要教的知識架構，並且有辦法把這樣的架構清楚地陳述出來**。在我提出的方法中，我們可以透過五個簡單的步驟達到這件事情：

1.  將閱讀的過程中看到的所有重要段落記錄下來
2.  將紀錄下來的重要段落拆解成顆粒度更小的概念
3.  畫出概念之間的關聯性
4.  將相似的概念群組起來
5.  將這些新學到的概念與過去所學的已知概念整合

下面這支影片是我實踐前四個步驟的過程。這支影片是一個真實案例的錄影，完全沒有經過事先的規劃。在這支影片中，我示範了我怎麼拆解 **_Mindstorms: Children, Computers, and Powerful Ideas_** 這本書的概念、獲得深度的理解。你不需要把影片看完（因為它長達四小時），但快速的看過影片中的不同段落會讓你更清楚我從書本提取想法和建立理解的方式。如果你想玩玩看我在影片裡建立的白板，可以點擊這個[連結](https://app.heptabase.com/w/d229915bd30fbf3b7af9db9a539856e73ebcb13c7d89012a891b9e15be1343d7)。

第一步：將閱讀的過程中看到的所有重要段落記錄下來[​](#第一步將閱讀的過程中看到的所有重要段落記錄下來 "Direct link to 第一步：將閱讀的過程中看到的所有重要段落記錄下來")
-----------------------------------------------------------------------------------------------

在我的方法論的第一步中，我們會需要把在閱讀過程中看到的重要段落記錄下來並且按照章節整理。這個過程的實作方式可能會根據你使用的工具而有所不同。如果你用的是電腦的閱讀器，你可以直接將文字從電子書複製貼上到一張 Heptabase 的卡片裡頭。如果你使用的是 Kindle 或 iPad 閱讀器，你可以把所有 Highlight 匯出成 Markdown 檔案再匯入到 Heptabase 裡頭。如果你讀的是實體書，你可以在每一個章節讀完時做一次筆記。

不管你採用哪種方式做筆記，你只要確保最終會產出一張書籍卡片，裡頭包含書中你在不同章節所紀錄的重要段落即可。

![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled%201-79735bf80dd1940d10048bbd8bd598a6.png)

第二步：將這些紀錄下來的重要段落拆解成顆粒度更小的概念[​](#第二步將這些紀錄下來的重要段落拆解成顆粒度更小的概念 "Direct link to 第二步：將這些紀錄下來的重要段落拆解成顆粒度更小的概念")
--------------------------------------------------------------------------------------------------------

當你將讀書筆記整理到一張書籍卡片以後，你可以創建一個白板，並透過 Heptabase 右上角的 Import Panel 將書籍卡片從 Card Library 匯進這個白板裡頭。舉例來說，我在 **Reading Notes** 這個母白板下創建了 **Mindstorm** 這個子白板，並且將 **_Mindstorms_** 這本書的卡片筆記放到了這個子白板上。

![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled%202-4b3fe7ce72d64eac5cc014b5f2773bd4.png)

當我卡片放好之後，我會把它開到右側欄讓我更方便地瀏覽裡面的內容。我通常會先快速掃過一遍這張卡片的所有內容，然後將裡面所有重要的概念識別出來。當我決定要把一個概念萃取出來時，**我會把與這個概念有關的區塊選取起來一口氣拖曳到白板上變成一張新的「概念卡片」。** 

![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled%203-03a7f4edc3610d33430893115750d900.png)

光是創建卡片還不夠，**我還會將這張卡片的核心概念用一句話總結，並以這句話當做是卡片標題**以確保我一眼就能知道它在講什麼。接下來，我會將這張概念卡片裡頭的內容重新組織，讓它的結構更符合我的直覺；我也會看一下原本的書籍卡片裡頭有沒有其他與這張概念卡片相關的區塊，如果有的話，我就會把它們也拖進這張概念卡片裡頭。

![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled%204-4088eba008c1948e327f61c57c25e544.png)

第三步：畫出這些概念之間的關聯性[​](#第三步畫出這些概念之間的關聯性 "Direct link to 第三步：畫出這些概念之間的關聯性")
-----------------------------------------------------------------------

當我從書籍卡片中萃取出愈來愈多概念卡片後，**我就會開始在這些概念卡片之間畫箭頭，或是把內容相近的卡片放在一起**。如果我發現有二張概念卡片的內容在討論相同的想法，我會將它們合併；如果我發現一張概念卡片裡頭包含的資訊量太大，我會把它拆解成多張更小的概念卡片來保持卡片的顆粒度。

![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled%205-cfa5a48a4eeab6a96dd33c977238ff5b.png)

第四步：將相似的概念群組[​](#第四步將相似的概念群組 "Direct link to 第四步：將相似的概念群組")
-----------------------------------------------------------

在將所有書籍卡片的內容都轉成概念卡片後，我會關掉右側欄，開始專心把這些概念卡片之間的關聯性和群組關係建立起來。當我發現有多張概念卡片都跟某個子題有關時，我會將它們用 Section 包起來，並給這個 Section 一個名字。我在為 Section 取名時會跟為概念卡片下標題時一樣謹慎，因為這些名稱將會是未來回顧這個白板時第一眼看到的東西。

![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled%206-a8bd15b8f46d8de61b9732daff4e1a91.png)

完整走完第二步到第四步通常會花上一小時到一天的時間，這個時間取決於這本書的長度和深度。當你產出最終的白板後，吸收知識的階段就結束了。在這個過程中，真正有價值的並不是你最終產出的這個白板，而是你在執行第二步到第四步的過程中**建立知識架構、給每張概念卡片和 Section 下標題所投入的思考過程**。深度的理解和洞察往往源自於將知識分解、重組、用自己的話語描述的這個過程。**只有在走過這個過程後，這些知識才會真正變成你的知識**。

在完成最終的白板排版（包含所有的箭頭和 Section）後，我會把原本的書籍卡片開到白板的右側欄，並將所有概念卡片和 Section 的連結重新貼回這張書籍卡片上。從下圖可以發現，這張書籍卡片中的每個連結顯示的內容都是某張概念卡片的標題。這也是為什麼在第二步的時候，我會將每張概念卡片用一句話總結，並用這句話當作它的標題。唯有這麼做，我才可以在看書籍卡片時，不用把這些概念卡片的連結點開就知道它的重點是什麼。

![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled%207-278f62136fe5d8d7792f86f9d1d75c63.png)

舉例來說，如果我把一張概念卡片的標題命名為「工程師的次文化」（Engineers’ subculture），過了幾個月後回頭看，我很難想起這張卡片具體在講什麼。但如果我把這張概念卡片的標題命名為「覺得 BASIC 語言很簡單的工程師形成了一種次文化，這種次文化影響著教育界，導致教師們偏愛那些喜歡這種次文化的學生。」（Engineers who find BASIC easy to learn formed a subculture that is influencing the world of education to favor students who are most like that subculture.），那我未來回頭看時，就算不看內文也能回想起它的核心概念。

第五步：將這些新學到的概念與過去所學的已知概念整合[​](#第五步將這些新學到的概念與過去所學的已知概念整合 "Direct link to 第五步：將這些新學到的概念與過去所學的已知概念整合")
--------------------------------------------------------------------------------------------------

截至目前為止，我已經透過在白板上拆解並重組 **_Mindstorms_** 這本書的核心概念，對這本書的知識獲得了深度理解。但是光是理解這本書還不夠，我還想要真正做到將我在過去、現在和未來所學的知識全部整合起來。換句話說，我想要將這本書的概念卡片與我以前為其他書和課程所寫的概念卡片整合再一起。

在做這件事情之前，我想先分享一個重要的學習觀念：**只有當你將筆記原子化時，你才能透過筆記視覺化對你在乎的主題獲得深度理解。** 

很多人在第一次使用 Heptabase 這種視覺化筆記軟體時，會沿用舊的思維為每一本書或每一堂課寫一個筆記，這些筆記的內容都非常長、包含非常多要點。當你的筆記是這種型態時，你就很難從視覺化中獲得價值。

舉例來說，下面這張圖中有二張書籍卡片，每一張都有非常多內容。這二本書的內容確實是有關聯的，但是當我把它們的書籍卡片放在白板上相連時，這樣的視覺化並沒有帶給我新的價值，因為這麼做的效果跟把它們放在同一個資料夾中是一模一樣的。

![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled%208-ef02c4682f7a12057beacbf4438a885a.png)

將筆記視覺化的目的，是對你所學的知識建立深度理解。**如果你的每一個筆記都非常長、如果你沒有把知識打碎、原子化，你能透過視覺化獲得的理解就會非常有限，因為真正的深度理解並不存在於「二本書之間的關聯性」裡頭，而是存在於「二本書中的所有概念之間的關聯性」裡頭。** 你要關聯的不是書籍卡片，而是你透過前面的四個步驟從這些書中拆解出來的、一張又一張獨立的概念卡片。

舉例來說，我最近在研究如何設計一種以計算機驅動的動態媒介，而 **_Mindstorms_** 和 **_The Early History of Smalltalk_** 這二本書的內容都與這個研究主題有高度相關。為了更好地做這個研究，我創建了一個叫「動態媒介」的白板，並將這二本書中與「動態媒介」有關的概念卡片復用進來，使用心智圖的功能去組織它們，建立一個我自己獨一無二的理解架構。

正是因為我過去在閱讀這二本書時，有將裡頭最重要的知識和想法原子化、寫成一張張可以被我在未來復用的概念卡片，我現在才能在做研究輕易地將我過去的所學應用於新的題目上。**我過去的所學不再只是靜靜地躺在資料夾中，而是可以成為我新的研究的基石**。

![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled%209-f8f8592d9d7932a7767f2bf91d22ddb2.png)

註：原子化指的並非你不能有很長的筆記，而是指每個概念筆記都只應包含一個概念，並以其內文來支撐這個概念。如果內文很長，但全都能被用來支撐標題的概念，那麽這則筆記仍然是一個原子化的概念筆記。

如何學習和做研究[​](#如何學習和做研究 "Direct link to 如何學習和做研究")
------------------------------------------------

前面講了學習方法論在 Heptabase 的實踐，現在我想來總結一下這套方法論底層的核心思想：

*   我認為學習和研究的本質是將不同書籍、文獻、課程、經驗中學到的重要知識和想法拆解出來，用自己的方式去關聯、理解、內化，進而對人類已知和未知的事物建立深度理解。
*   我認為工作時寫的計畫和研究時寫的論文都是在將這些深度理解轉化成可以被執行和傳播的形式。

在這樣的核心思想下，學習、研究、計畫、產出的過程其實可以用下面這張示意圖來完整地呈現：

![](https://wiki.heptabase.com/assets/images/the-best-way-to-acquire-knowledge-from-readings-Untitled%2010-cf63ae3de42b543f735145734197fb37.png)

在這張圖中，最左邊是「素材」，也就是那些你在上課或閱讀的當下所寫下的「文獻卡片」。

我在學習和研究的過程中，會從這些文獻卡片中萃取出對我有用的重要概念，進而打造原子化的「概念卡片」。每個概念卡片都會在標題用一句話來描述這個概念，而內文會引用一到多份文獻的內容來支撐這句話，每一次的引用都會加深我對這個概念的理解和反思。

在學習和研究的過程中，文獻卡片的原始內容會逐漸地被替換成一堆概念卡片的連結。而當我一步步地將這些概念卡片從文獻卡片中萃取出來後，我需要找到一個合適的心智結構來安放它們。只有當我找到這個結構時，我才算是真正理解、內化了這這個主題。

在未來，不管我是在寫學術論文、工作計畫或網路文章時，我在做的其實都是在將這些概念卡片用線性的方式重組成專門給外人閱讀的、文章形式的「產出卡片」。隨著我在做研究時吸收並拆解愈多「素材」，我在中間的「理解」便能持續深化，右邊的「產出」自然也會有愈來愈高的品質。

結語[​](#結語 "Direct link to 結語")
------------------------------

雖然這篇文章的主題在談**吸收、留存和應用知識**的方法論，但我最後想強調一下工具選擇的重要性，因為工具的設計往往會在潛意識下改變我們對學習的看法，並養成一些學習的好習慣和壞習慣。

Seymour Papert 是人工智慧和教育建構主義運動的先驅之一，他在 _Mindstorms_ 這本書中探討了工具如何影響思考的想法：

> 對我而言，寫作意味著草擬一個初稿，並在相當長的時間內對其進行修改和完善。我對自己作為一名作家的形象包含了一個「不被接受」的初稿，這個初稿會隨著持續的編輯而被打磨成最終呈現的形式。但如果我是一名三年級學生，我無法想像這樣的作法，因為寫作的物理行為相當緩慢和費力，而且我沒有秘書能幫我寫字。對於大多數孩子來說，重寫一篇文章是如此費力，以至於第一稿就成了最終的版本，這使得他們沒辦法培養用批判性地眼光重新檢視自己寫的初稿的能力。但是當孩子們有了文字編輯器後，這種情況會有戲劇性的改變。初稿變成是在鍵盤上創作的。糾正錯誤變得容易。當前的版本總是乾淨整潔的。我見過一個孩子在開始使用電腦寫作幾週後，從完全拒絕寫作到積極參與（並伴隨著品質的快速提升）。當孩子們因生理缺陷而手寫困難或甚至不可能時，這種情況變得更加戲劇性。
> 
> 文字編輯器可以讓孩子的寫作體驗更像真正的作家。但如果身邊的成年人無法欣賞作家的感受，這一點就會受到削弱。例如，人們很容易想象成年人（包括老師）會表達這樣的觀點：修改和重新編輯文本是浪費時間的（「為什麼不做些新的事情呢？」或「你沒有讓它變得更好，為什麼不修正你的拼寫？」）。
> 
> 寫作、音樂創作、技巧遊戲、複雜圖形等等，都可以用同樣的方式來看待：電腦不是一個獨立的文化，但它可以用於推進非常不同的文化和哲學觀點。

在打造 [Heptabase](https://heptabase.com/) 時，我們的目標是設計讓你可以將大腦學習知識的過程外部化的環境，讓你可以用眼睛和手去對概念進行識別、拆解、連接和分組。這就是為什麼我們開發拆解卡片、在卡片之間移動區塊、在白板上建立卡片關係、在多個白板之間重複使用卡片等功能。這些功能共同構成了一個環境，讓你能更好地運用人類的視覺理解和視覺記憶能力以及電腦的資料持久性和檢索能力來學習。當你愈常使用這個工具來對你的所學建立架構，你就會下意識地將這篇文章中描述的學習方法變成自己的習慣，而這才是最重要的 — 工具不只能讓你記筆記，更讓你成為一個擅長學習的人。