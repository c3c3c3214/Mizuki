---
title: "测试页"
published: 2026-11-12
---

published:"2026-11.12"
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/artplayer/dist/artplayer.css">
<script src="https://cdn.jsdelivr.net/npm/artplayer/dist/artplayer.js"></script>
<style>
.video-grid{display:grid;grid-template-columns: repeat(auto-fit, minmax(480px,1fr));gap:16px;margin:16px 0;}
.art-box{width:100%;height:420px;}
</style>
<div class="video-grid">
  <div class="art-box" id="p1"></div>
  <div class="art-box" id="p2"></div>
  <div class="art-box" id="p3"></div>
  <div class="art-box" id="p4"></div>
</div>
<script>
const urls = [
  "https://media.acg.haidaoqi.lol/Casey%20PL%20C1.mp4",
  "https://media.acg.haidaoqi.lol/Sgoil720.m4v",
  "https://media.acg.haidaoqi.lol/%E5%9B%BD%E4%BA%A7%E7%BD%91%E7%BA%A22.fansly_%E8%8E%8E%E8%8E%8E%E4%BA%8B_TS_%E7%8C%8E%E5%A5%87_7%E5%88%86%E9%92%9F%E5%86%85%E8%BF%9E%E5%8F%916%E5%8F%91%EF%BC%81_%E6%8C%91%E6%88%98%E4%BA%BA%E4%BD%93%E6%9E%81%E9%99%90%EF%BC%81_%E7%A5%9E%E4%BB%99%E5%95%8A_%E8%BF%99%E5%93%A5%E4%BB%AC%E4%BB%AC%E4%B8%8D%E6%80%95%E6%AD%BB%E5%95%8A.mp4",
  "https://media.acg.haidaoqi.lol/%E6%9E%81%E5%93%81%E4%BA%9A%E9%9B%9B%E5%A6%9D_Mia_Meenaa_%E9%A2%9C%E5%80%BC%E8%BA%AB%E6%9D%90%E9%83%BD%E4%B8%8D%E9%94%99_%E4%BD%86%E5%B0%B1%E5%BE%88%E9%B8%A1%E9%B8%A1%E7%BA%AF%E5%BD%93%E4%B8%AA%E5%A5%B3%E4%BA%BA%E5%9C%A8%E6%8E%8F%E4%BA%86.mp4"
];
const containers = ["#p1","#p2","#p3","#p4"];
const players = [];
urls.forEach((url,i)=>{
  players.push(new Artplayer({
    container: containers[i],
    url: url,
    isAutoSize:true,
    playbackRate:true,
    theme:"#23ade5",
    setting:true
  }))
})
</script>
