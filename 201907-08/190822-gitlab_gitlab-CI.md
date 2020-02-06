# 190822-gitlab/gitlab-CI

- gitlab改走http
    修改config/gitlab.rb
![](https://paper-attachments.dropbox.com/s_7B8CC06406610EEF3A1A2E209B039DB4DC5165A65FBCA31CE02F2E8F9D5760D5_1566563698386_.png)


左邊是現行版本，右邊是走https時的版本
另外右邊的檔案名稱為gitlab.rb.bak，如果之後出於某些狀況想恢復https的話可以參考
如果要reload config 可以大膽的docker-compose down && docker-compose up -d
obstacle: 憑證一直有unable to get local issuer certificate的問題
fixed: 昊昕後來發現是nginx的ssl檔案要把chain的內容合併 可以參考[+190822](https://paper.dropbox.com/doc/190822-0WMJLHHInpGb3JUWUPDvu) 


- gitlab ssh clone
    - 基本上做的事情和昊昕差不多 所以可以直接參考他寫的


- 把docker-for-cool的image push上docker hub 省得CI/CD build的時間
        參考docker-compose.yml


- #TODO:
        把canvas架起來
        寫dockerfile的單元測試（如果兩個dockerfile有變動的話就在runner裡面build並push）


