# 2021年8月28日-29日基礎漏洞分析與測試

```
教育部先進資通安全實務人才培育計畫
校園資安深耕營Advanced Happy CyberSecurity Day

課程名稱：基礎漏洞分析與測試

課程大綱：
-本次課程將涵蓋幾種漏洞分析與測試，包括緩衝區溢位(buffer overflow, BOF)及格式化字串攻擊(Format String Attack)。
-課程將從基礎的分析開始並進行安全測試，也將涵蓋ROP(Return Oriented Programming)的攻擊與測試分析。
-課程內容尚包括安全機制(Security Options)的說明與檢視工具(checksec)，涵蓋RELRO、Stack Canary、NX、
 PIE、ASLR(Address Space LayoutRandomization)等安全機制，同時也將觸及繞過這些安全機制的攻擊手法。
-本課程將使用底下工具nc / ncat, objdump, gdb, radare2, gdb-vmmap, pwntools, readelf, ROPgadget, 
one_gadget進行測試。

講師：臺灣好厲駭資深學長陳憶賢

先備知識：
(1)本課程對高中職學生具有一定程度的難度，請積極學習。
(2)曾參與HappyPythonDay並熟悉python程式設計與pwntools技術尤佳。
(3)曾參與HappyLinuxDay並熟悉基礎Linux指令尤佳。
(4)另外建議先熟悉基礎逆向工程技術(objdump, gdb, radare2)與基礎組合語言指令!

學員證書發放說明：
(1)學員需完成指定題目達17題(含)以上。 
(2)證書只提供給具本國籍國中高中職五專在學學生(含應屆畢業生)。  
(3)證書於9月6日後由郵局掛號寄出。  
(4)本主辦單位保有最終修改、變更、活動解釋及取消之權利。     

✪指導單位：教育部資訊及科技教育司
✪主辦單位：教育部先進資通安全實務人才培育計畫推動辦公室、崑山科技大學、國立宜蘭大學、國立臺中高工
✪聯絡窗口：陳小姐0928-155-602 / E-mail:samtn125@gmail.com或洽FB粉絲頁(高中職生資安研習營)
```

# 環境安裝影片
```
(1)環境安裝影片：https://youtu.be/Q9-ruKH032U
(2)(未有VM軟體者首先安裝)Oracle VM VirtualBox下載連結：https://www.virtualbox.org/wiki/Downloads
(3)image下載連結：https://drive.google.com/file/d/17Q6EAH0n8PKZIoajuCBkrJtT6Pezbkqp/view?usp=sharing
VM帳號及密碼都是user
```
# 課程簡報下載

[漏洞攻擊從入門到放棄.pdf](https://github.com/MyFirstSecurity2020/MyfirstPWN/blob/main/%E6%BC%8F%E6%B4%9E%E6%94%BB%E6%93%8A%E5%BE%9E%E5%85%A5%E9%96%80%E5%88%B0%E6%94%BE%E6%A3%84.pdf)

# 非經取得本單位或講者授權，不得任意轉載或公開傳輸

# [CTF平台](https://140.110.112.229/)
```
(此為正式平台，簡報上為測試平台，請使用此平台)
一人一隊，請自行註冊(並請記得註冊EMAIL與帳號將提供驗證核發證書使用)
平台連結：https://140.110.112.229/
```

# [Discord課程聊天室](https://discord.gg/HvFuP7Qx)
```
學員可以聊天室上互相提問學習(講師也會不定時上線)
https://discord.gg/HvFuP7Qx
```

# [課程問題提問表單](https://forms.gle/bavE1Z8gD9cdXDw78)
```
學員對課程上或解題上有任何問題的可以在表單上提問直播時講師會解答
https://forms.gle/bavE1Z8gD9cdXDw78
```
# 線上簽到

```
(1)時間：8月28日11:30-12:00與8月29日16:00-16:30 直播現場
(2)辦理方式：請在google meet裡的訊息裡留下"學校-姓名"當作簽到。

```

# 8月28日(星期六)課程表與影片/直播連結

|時間|章節名稱|上課方式|影片/直播連結|
|:----:|:----:|:------|:-------------|
|09:00-10:30|預錄|(CH1)Program Structure + Security Option|https://youtu.be/ZraMzBnT-94|
|10:30-11:30|預錄|(CH2)Tools|https://youtu.be/DZ8c81Gck2k |
|11:30-12:00|直播&簽到|講師線上直播解講及QA|https://meet.google.com/bhz-djus-yai|
|13:00-14:00|預錄|(CH3-1)Bof - Local Variable|https://youtu.be/UmLr0_B6yqc |
|--|預錄|(CH3-2)Bof - Local Variable|https://youtu.be/UqqqxYYeGXA |
|14:00-15:30|預錄|(CH4-1)Bof - ret2code|https://youtu.be/Db_BQsv9MmA |
|--|預錄|(CH4-2)Bof - ret2code|https://youtu.be/9wvb09WNwn0 |
|--|預錄|(CH5-1)Bof - ret2sc|https://youtu.be/VABqxI20ySE|
|--|預錄|(CH5-2)Bof - ret2sc|https://youtu.be/KKZ8YkSSb8I|
|15:30-16:30|直播|講師線上直播解講及QA|https://meet.google.com/tdb-wixc-ixs|


# 8月29日(星期日)課程表與影片/直播連結
|時間|章節名稱|上課方式|影片/直播連結|
|:----:|:----:|:------|:-------------|
|09:00-10:30|預錄|(CH6-1)Bof - ret2libc|https://youtu.be/lR0-nQpX56c |
|--|預錄|(CH6-2)Bof - ret2libc|https://youtu.be/H21YofSTazY |
|10:30-11:30|預錄|(CH7-1)ROP|https://youtu.be/EsbUdf0_EY8 |
|--|預錄|(CH7-2)ROP|https://youtu.be/XsC5GxYGUmU|
|11:30-12:00|直播|講師線上直播解講及QA|https://meet.google.com/byz-nusm-wqt |
|13:00-14:30|預錄|(CH8-1)Format String|https://youtu.be/vfHs9kxh0_A|
|--|預錄|(CH8-2)Format String|https://youtu.be/kgA2ZNpwic4 |
|--|預錄|(CH8-3)Format Stringc|https://youtu.be/-0dYnQtMjBU |
|--|預錄|(CH8-4)Format Stringc|https://youtu.be/RGalgUT2VFM |
|14:30-16:00|預錄|(CH9-1)Stack Migration|https://youtu.be/LibVsrE20R0 |
|--|預錄|(CH9-2)Stack Migration|https://youtu.be/f7YMBK2MY84 |
|16:00-16:30|直播&簽到|講師線上直播解講及QA|https://meet.google.com/jwf-gsjk-hdn |




# [證書核發](https://forms.gle/oyfB1JWYKg1rDYnS6)
```
(1)證書於9月6日後掛號寄出
(2)8月29日請填寫問卷：https://forms.gle/oyfB1JWYKg1rDYnS6
```

# 題目
```
(1)任選平台裡其中17題題目完成即可進行證書發放審查。
(2)解題截止時間：8/31(二) 17:00

01.張元 Pwn6 
02.張元 Pwn7
03.張元 Pwn1 
04.pass
05.張元 Pwn8 
06.Angelboy Pwn1
07.gohome
08.registration
09.Angelboy Pwn2 
10.張元 Pwn9
11.Angelboy Pwn3 
12.oob3 Sean Pwn3
13.張元 Pwn10 
14.echo_server
15.fmtstr 
16.fmt-1
17.fmt-2 
18.fmt-3
19.secret
20.Angelboy Pwn7

```
