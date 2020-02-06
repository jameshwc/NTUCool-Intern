# 191021 -rspec 成功 (8hrs)
目前在跑rspec，它跑得比我想像中的久很多…下班前不知道有沒有機會看到它結束
紀錄一下這陣子都卡在同一個地方，就是NetConnectionNowAllowed的error，是在用docker-compose跑rspec的時候遇到的，本來以為是webmock沒有allow localhost的連線，早上嘗試改了所有有include webmock的.rb檔但還是沒有用
後來看[document](https://github.com/instructure/canvas-lms/blob/master/doc/docker/developing_with_docker.md)發現好像是要先把selenium container開起來，這有夠坑爹的，它順序是先講怎麼測試再說怎麼開selenium，根本不會想到要先將selenium開起來…
目前只跑了一次，我把步驟記錄一下，之後再重新跑一次看看步驟有沒有正確記錄


1. 把canvas架起來（./script/docker_dev_setup.sh，或是docker-compose build && docker-compose up -d應該都可以，就是要確定canvas可以成功連線）
2. 編輯 `.env`
    `COMPOSE_FILE=docker-compose.yml:docker-compose/selenium.override.yml`
3. 開啟selenium: `docker-compose up selenium-chrome`
4. 進web container (`docker-compose run` `--``rm web bash`)
5. `cp config/security.yml.example config/security`.yml（避免遺漏encryption）
6. rspec spec 或是rspec spec/selenium/dashboard_spec.rb（這裡可以先執行後者，因為test整個spec的資料夾很花時間，先rspec 某個.rb確定有沒有錯比較好）
7. ???? 我還沒跑完rspec spec….跑了一個多小時了

4~6應該可以在container外面完成，但應該要先build(?) 不確定，之後有空再試
心得: 果然還是要上一整天的班比較有效率，但是大部分時間都在等build/test的結果出來，沒事做很無聊

