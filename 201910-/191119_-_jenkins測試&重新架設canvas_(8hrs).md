# 191119 - jenkins測試&重新架設canvas (8hrs)

- 之前在github上發的issue被回覆了，雖然早就解決了（沒有開selenium的docker），但回覆者有提到他們已經在這幾天把CI流程移到jenkins，所以就想說試看看jenkins↔gitlab的workflow
    - 但經過一陣摸索之後，發現gitlab 必須是EE版本（企業版，CE for free）才有支援整合jenkins的功能，白白浪費了一個早上…
- 發現他們有在github上更新docker安裝的shell script，所以就先重新架起來（因為VM被重開了也得重架一個），不過這個真的很浪費時間…

