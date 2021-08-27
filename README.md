# 2021年8月28日-29日基礎漏洞分析與測試

```
教育部先進資通安全實務人才培育計畫
校園資安深耕營Advanced Happy CyberSecurity Day

課程名稱：基礎漏洞分析與測試

課程大綱：本次課程將涵蓋幾種漏洞分析與測試，包括緩衝區溢位(buffer overflow, BOF)及格式化字串攻擊(Format String Attack)。課程將從基礎的分析開始並進行安全測試，也將涵蓋ROP(Return Oriented Programming)的攻擊與測試分析。課程內容尚包括安全機制(Security Options)的說明與檢視工具(checksec)，涵蓋RELRO、Stack Canary、NX、PIE、ASLR(Address Space LayoutRandomization)等安全機制，同時也將觸及繞過這些安全機制的攻擊手法。本課程將使用底下工具nc / ncat, objdump, gdb, radare2, gdb-vmmap, pwntools, readelf, ROPgadget, one_gadget進行測試。

講師：臺灣好厲駭資深學長陳憶賢

先備知識：
(1)本課程對高中職學生具有一定程度的難度，請積極學習。
(2)曾參與HappyPythonDay並熟悉python程式設計與pwntools技術尤佳。
(3)曾參與HappyLinuxDay並熟悉基礎Linux指令尤佳。
(4)另外建議先熟悉基礎逆向工程技術(objdump, gdb, radare2)與基礎組合語言指令!

事先需安裝之軟體：
(1)環境安裝參考影片：https://youtu.be/Q9-ruKH032U
(2)(未有VM軟體者首先安裝)Oracle VM VirtualBox下載連結：https://www.virtualbox.org/wiki/Downloads
(3)image下載連結：https://drive.google.com/file/d/17Q6EAH0n8PKZIoajuCBkrJtT6Pezbkqp/view?usp=sharing
VM帳號及密碼都是user


學員證書發放說明：
(1)學員需完成指定題目達17題(含)以上。 
(2)證書只提供給具本國籍國中高中職五專在學學生(含應屆畢業生)。  
(3)證書於9月6日後由郵局掛號寄出。  
(4)本主辦單位保有最終修改、變更、活動解釋及取消之權利。     

✪指導單位：教育部資訊及科技教育司
✪主辦單位：教育部先進資通安全實務人才培育計畫推動辦公室、崑山科技大學、國立宜蘭大學、國立臺中高工
✪聯絡窗口：陳小姐0928-155-602 / E-mail:samtn125@gmail.com或洽FB粉絲頁(高中職生資安研習營)
```
# 8月28日(星期六)課程表與影片/直播連結

|時間|章節名稱|上課方式|影片/直播連結|
|:----:|:----:|:------|:-------------|
|09:00-10:30|預錄|(CH1)Program Structure + Security Option|https://youtu.be/ZraMzBnT-94|
|10:30-11:30|預錄|(CH2)Tools|https://youtu.be/DZ8c81Gck2k |
|11:30-12:00|直播|講師線上直播解講及QA|https://meet.google.com/bhz-djus-yai|
|13:00-14:00|預錄|(CH3-1)Bof - Local Variable|https://youtu.be/UmLr0_B6yqc |
|--|預錄|(CH3-2)Bof - Local Variable|https://youtu.be/UqqqxYYeGXA |
|14:00-15:30|預錄|(CH4-1)Bof - ret2code + ret2sc|https://youtu.be/Db_BQsv9MmA |
|--|預錄|(CH4-2)Bof - ret2code + ret2sc|https://youtu.be/9wvb09WNwn0 |
|--|預錄|(CH5-2)Bof - ret2code + ret2sc|https://youtu.be/VABqxI20ySE|
|--|預錄|(CH5-2)Bof - ret2code + ret2sc|https://youtu.be/KKZ8YkSSb8I|
|15:30-16:30|直播|講師線上直播解講及QA|https://meet.google.com/tdb-wixc-ixs|


第二天
09:00-10:30 (預錄)Bof - ret2libc
10:30-11:30 (預錄)ROP
11:30-12:00 (同步)講師線上直播解講及QA
13:00-14:30 (預錄)Format String
14:30-16:00 (預錄)Stack Migration
16:00-16:30 (同步)講師線上直播解講及QA

# 8月29日(星期日)課程表與影片/直播連結
|時間|章節名稱|上課方式|影片/直播連結|
|---|:---------|:------|:-------------|
|09:00-10:30|預錄|Bof - ret2libc|https://youtu.be/ZraMzBnT-94|
|10:30-11:30|預錄|Tools|https://youtu.be/DZ8c81Gck2k |
|11:30-12:00|直播|講師線上直播解講及QA|https://meet.google.com/bhz-djus-yai|
|13:00-14:00|預錄|(CH3-1)Bof - Local Variable|https://youtu.be/UmLr0_B6yqc |
|--|預錄|(CH3-2)Bof - Local Variable|https://youtu.be/UqqqxYYeGXA |
|14:00-15:30|預錄|(CH4-1)Bof - ret2code + ret2sc|https://youtu.be/Db_BQsv9MmA |
|--|預錄|(CH4-2)Bof - ret2code + ret2sc|https://youtu.be/9wvb09WNwn0 |
|15:30-16:30|直播|講師線上直播解講及QA|https://meet.google.com/tdb-wixc-ixs|



# 課程問題提問表單
```
學員對課程上或解題上有任何問題的可以在表單上提問直播時講師會解答

```
# CTF平台
```
一人一隊，請自行註冊(並請記得註冊EMAIL與帳號將提供驗證核發證書使用)
平台連結
```

# 課程簡報

# 非經取得本單位或講者授權，不得任意轉載或公開傳輸

# 環境安裝影片
```

```

# 8月28日(六)課程YouTube連結[7/13 17:00將刪除]

# 非經取得本單位或講者授權，不得任意轉載或公開傳輸

|章節|影片|片長|影片連結|
|---|:-----|:----:|:--------------------------|
|0|CH0_Introduction|30:38|https://youtu.be/pyMNBDuDJMM |
|1|CH1_Classical_Cipher|17:43|https://youtu.be/ykfwIWxB3Y4|
|2|CH2_PRNG|15:06|https://youtu.be/r_MPQVFSr08 |		
|2|CH2-2_LCG解題|18:29|https://youtu.be/gUYItO35l0k |
|3|CH3_Hash|15:23|https://youtu.be/n78-aG9lXzo  |
|4|CH4_BlockCipher|28:19| https://youtu.be/WAxoWwf2k4M |
|4|CH4-2_LAB_CBC_講解題目|5:41|https://youtu.be/GmksFQwl7Wg|			
|4|CH4-3_LAB_CBC_解題|12:46|https://youtu.be/7RDKk5Ry6vI |
|5|CH5_StreamCipher|18:17|     https://youtu.be/d-fnsAYGQFY 	 |	
|5|CH5-2_LAB題目講解|3:53|	https://youtu.be/FbXI7KmKib8  |		
|5|CH5-3_LAB_OWO_解題流程|11:33|https://youtu.be/NVOJICD3mtc  |
|6|CH6_非對稱式 | 56:53|	https://youtu.be/LtrnPj7bPaE 	|	
|6|CH6-2_非對稱式_解題| 13:28 |   https://youtu.be/ti2RKP3gf6o  |
|7|CH7_橢圓曲線| 38:01| https://youtu.be/6SN1FjYt7kg  |		
|7|CH7-2_橢圓曲線| 7:17|https://youtu.be/gfhckN_Te9g  |
|8| CH8-第一天結語|  2:25 | https://youtu.be/VJizItDC_tg  |

# 8月29日(日)課程YouTube連結[7/13 17:00將刪除]

# 非經取得本單位或講者授權，不得任意轉載或公開傳輸

|章節|影片|片長|影片連結|
|---|:--------|:----:|:--------------------------|
|9|CH9_RSA攻擊|13:04|https://youtu.be/kxu3eYA2fO8  |
|9|CH9-2_太難了|17:53|https://youtu.be/Zre0xp4VPb0  |
|9|CH9-3_費馬因式分解題目|4:32|	https://youtu.be/60Utm-atWGY |		
|9|CH9-4_費馬因式分解解題與小技巧|7:40|https://youtu.be/I5sx-wE6X6M  |
|9|CH9-5_SmoothPrime講解+解題|17:04| https://youtu.be/5fyinS2FQdk  |
|9|CH9-6_SmoothPrime修BUG|2:55|https://youtu.be/Q4iRR1lUmgQ 	| 	
|9|CH9-7_E的問題+Yang2講解|15:01|https://youtu.be/90PL0ZOCBTo 	|
|9|CH9-8Common_modulus 講解題目|5:49|https://youtu.be/VWc4KoDeef0 	|	
|9|CH9-9_Common_modulus 解題|6:49| https://youtu.be/EHnQ1SOPM-A  |		
|9|CH9-10_CRT+講解題目|9:51|https://youtu.be/FhjL8ge2LSU 	|		
|9|CH9-11_CRT_解題|2:37| https://youtu.be/IyOoumSEc7M  |
|10|CH10-1_LEA+題目講解|17:20|https://youtu.be/98ooRXyZ7x8  | 
|10|CH10-2_LEA_ATTACK解題|9:39|https://youtu.be/vb8-oDN_f_o  | 
|11|CH11_CUT_PASTE+題目講解|5:18|https://youtu.be/AQrxqL7urlI  | 
|11|CH11-2_CUT_PASTE解題|7:18|https://youtu.be/fR29kuvUtpg  | 
|11|CH11-3_POODLE講解+講題目|18:12|https://youtu.be/wrErsgU75uE  | 
|END|結語|0:39|https://youtu.be/Szbr_tMokx0  |

# 7月11日(日)15:00線上簽到與難題解說與Q&A直播

```
(1)請學員到通話中的訊息留下 /學校及姓名/ 簽到，謝謝
(2)14:50開放進入會議室
(3)會議連結：https://meet.google.com/twg-ygdu-aor

```

# 證書核發
```
(1)證書於7月19日後掛號寄出
(2)問卷調寫：https://forms.gle/PaS7gQd5uwo6q5vg6
```

# 指定題目
```
(1)(更新)任選13題題目完成即可進行證書發放審查。
(2)解題截止時間：7/12(一) 13:00(延長至7/14星期三17:00)

01. AIS3_Pre_exam_2015-Crypto2
02. CBC
03. Chinese Remainder Theorem
04. ECB
05. LCG
06. OWO_Nonsense-Machine
07. OWO_Apple Shop
08. Padding Oracle
09. RSA 後門 (1)
10. Simplest_ECC
11. Smooth_Prime
12. YANG_RSA-1
13. YANG_RSA-2
14. YANG_RSA_4
15. common_factor_attack_rsa
16. RSA Factorization
17. babyDSA (直播解題)
```
