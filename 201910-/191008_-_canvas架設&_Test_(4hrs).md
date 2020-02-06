# 191008 - canvas架設& Test (4hrs)

- 用VM架設canvas-lms成功
    - 之前在我Azure的機器上因不明原因失敗，可能是環境太髒(?)
    - 連線: http://10.99.100.211 帳號b07902001@ntu.edu.tw 密碼b07902001
- 試試[Canvas Wiki寫的測試方法](https://github.com/instructure/canvas-lms/blob/master/doc/docker/developing_with_docker.md)，目前會有Error: 
![](https://paper-attachments.dropbox.com/s_1E566504657116E9DC5B467B4DC5F27ECFEB4A07E6BBD92BC30D5EED3BC0B897_1570525810624_.png)

    - 爬文的推測是需要加allowlocalhost，但不確定要加在哪裡
    - 之後可能要去研究 RSpec，或去問冠賢（因為是Ruby的語法）

