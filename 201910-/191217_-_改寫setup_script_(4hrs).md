# 191217 - 改寫setup script (4hrs)

- 改寫script/docker_dev_setup.sh 把prompt的部分移除
- 研究production start的內容改寫成dockerfile，但後面apache的設定有點複雜…而且不確定要不要為了做CI還建一個smtp server，所以會先以quick start，也就是docker_dev_setup.sh的東西來做改動

