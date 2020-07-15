1. [.DS_Store禁止生成、恢复生成、删除](#ds_store)
<a id="ds_store"></a>
### .DS_Store禁止生成、恢复生成、删除
      DS_Store 是用来存储这个文件夹的显示属性的：比如文件图标的摆放位置。删除以后的副作用就是这些信息的失去。（当然，这点副作用其实不是太大）
  * 禁止.DS_Store文件生成
  
      ```defaults write com.apple.desktopservices DSDontWriteNetworkStores -bool TRUE```
  * 恢复.DS_Store文件生成
  
     ``` defaults delete com.apple.desktopservices DSDontWriteNetworkStores```
  * 删除现有的.DS_Store文件
  
      ```sudo find / -name ".DS_Store" -depth -exec rm {} \;```
