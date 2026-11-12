---
title: "生化危机 爆发夜"
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
    <div style="background:#111;color:#fff;padding:8px 10px;border-radius:4px 4px 0 0;font-size:16px;">🎬篇1</div>
  </div>
  <div class="art-box" id="p2"></div>
    <div style="background:#111;color:#fff;padding:8px 10px;border-radius:4px 4px 0 0;font-size:16px;">🎬 篇2</div>
  </div>
</div>
<script>
const urls = [
  "https://pub-4f5a7f3da62e42ca96c7e87fd47cffe9.r2.dev/202611121619.mp4",
  "https://pub-4f5a7f3da62e42ca96c7e87fd47cffe9.r2.dev/202611121624.mp4",
];
const containers = ["#p1","#p2"];
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
