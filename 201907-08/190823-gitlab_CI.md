# 190823-gitlab CI

- 完成vault password匯入到runner的部分
    - 忘記改project timed out max limit 預設是一小時所以在compile assets的部分因超時而失敗
    - 現在正在重跑一次，不知道會跑多久
    - 覺得流程應該可以簡化（docker、ansible、runner三者功能很多重複）
    - 想辦法把image push到docker hub，這樣就只要加ci.yml就可以build 而不用把docker-for-cool這個repo clone下來合併

