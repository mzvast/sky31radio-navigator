# 提取步骤

资源全部在https://radio.sky31.com/api/all 的回包data中。

我们关心的数据是data.seasons数组. 每一个season下面都有programs，这里面是每一季的节目单。

因此下类似指令即可

```
programs.filter(item=>item['audio']).map(item=>item.audio.src+' --out='+item.title+'.mp3').join('\n')
```
