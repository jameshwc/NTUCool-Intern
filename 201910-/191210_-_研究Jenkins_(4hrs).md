# 191210 - 研究Jenkins (4hrs)

- 去研究github上 官方canvas的jenkinsfile，記錄一些遇到的坑，結論後面補
    - 官方團隊使用gerrit作為code review工具，有在jenkinsfile以環境變數寫入gerrit host，我已經懶得再架一個gerrit server了，這是我放棄研究jenkins的主因
    - pipeline使用agent label: “canvas-docker”，一直出現jenkins沒有這個agent的錯誤訊息，查很久才知道在jenkins要另外新增節點，這個跟gitlab-CI需要runner、drone CI需要agent是一樣的意思
    - 在build/new-jenkins/groovy/credential.groovy有需要ssh key和username，我本來以為是node (或說runner)的資訊，研究半天才發現其實是gerrit的
- 結論：算是白忙了四小時，不過對他們寫的jenkinsfile算了解不少了，然後官方團隊好像沒有想把CI流程generalized…還是用gitlab CI自己刻可能比較實在

