---
title: "demo"
published: 2026-11-12
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/artplayer/dist/artplayer.css">
<script src="https://cdn.jsdelivr.net/npm/artplayer/dist/artplayer.js"></script>
<style>
.video-grid{display:grid;grid-template-columns: repeat(auto-fit, minmax(480px,1fr));gap:16px;margin:16px 0;}
.art-box{width:100%;height:420px;}
.lock-wrap{padding:2rem;text-align:center;border:1px dashed #666;border-radius:12px;margin:2rem 0;}
</style>

<div class="video-grid">
  <!-- 👉 无需密码：p1 p2 -->
  <div>
    <div class="art-box" id="p1"></div>
    <div style="background:#111;color:#fff;padding:8px 10px;border-radius:4px 4px 0 0;font-size:16px;">🎬  国产网红.fansly_莓莓莓事的_TS_猎奇_人妖_7分钟内连射6发！挑战人体极限！神仙啊 这哥们真不怕死啊</div>
  </div></div>
  </div>
  <div>
    <div class="art-box" id="p2"></div>
    <div style="background:#111;color:#fff;padding:8px 10px;border-radius:4px 4px 0 0;font-size:16px;">🎬femboy2</div>
  </div>
</div>

<!-- 密码解锁区域 -->
<div class="lock-wrap" id="lockBox">
  <h3>🔒 致各位精英哥布林：族人们，帮帮小哥布林，小哥布林为了做公益，为了族人们能更好的看片片就几乎没上广告，另外，不要相信任何广告避免上当受骗，还有要多学习多读书努力工作，找个母哥布林早日脱单，谢谢各位族人们！----你的族人，小哥布林。</h3>
  <input type="password" id="pwdInput" placeholder="输入访问密码【下列内容包括萝莉、重口味资源】" style="padding:8px;width:220px;">
  <button onclick="unlock()" style="padding:8px 16px;margin-left:8px;">解锁</button>
  <p id="errTip" style="color:red;display:none;">密码错误</p>
</div>

<!-- 👉 需要密码的容器（p3-p8，初始隐藏） -->
<div class="video-grid" id="secretArea" style="display:none;">
  <div>
    <div class="art-box" id="p3"></div>
    <div style="background:#111;color:#fff;padding:8px 10px;border-radius:4px 4px 0 0;font-size:16px;">🎬 视频3</div>
  </div>
  <div>
    <div class="art-box" id="p4"></div>
    <div style="background:#111;color:#fff;padding:8px 10px;border-radius:4px 4px 0 0;font-size:16px;">🎬 视频4</div>
  </div>
  <div>
    <div class="art-box" id="p5"></div>
    <div style="background:#111;color:#fff;padding:8px 10px;border-radius:4px 4px 0 0;font-size:16px;">🎬 视频5</div>
  </div>
  <div>
    <div class="art-box" id="p6"></div>
    <div style="background:#111;color:#fff;padding:8px 10px;border-radius:4px 4px 0 0;font-size:16px;">🎬 视频6</div>
  </div>
  <div>
    <div class="art-box" id="p7"></div>
    <div style="background:#111;color:#fff;padding:8px 10px;border-radius:4px 4px 0 0;font-size:16px;">🎬 视频7</div>
  </div>
  <div>
    <div class="art-box" id="p8"></div>
    <div style="background:#111;color:#fff;padding:8px 10px;border-radius:4px 4px 0 0;font-size:16px;">🎬完整版菊花写江山</div>
  </div>
</div>

<script>
// 你的视频链接数组
const urls = [
  "https://pub-4f5a7f3da62e42ca96c7e87fd47cffe9.r2.dev/femboy1.mp4",
  "https://pub-4f5a7f3da62e42ca96c7e87fd47cffe9.r2.dev/femboy2.mp4",
  "https://media.acg.haidaoqi.lol/Casey%20PL%20C1.mp4",
  "https://media.acg.haidaoqi.lol/Sgoil720.m4v",
  "https://pub-4f5a7f3da62e42ca96c7e87fd47cffe9.r2.dev/Y90.mp4",
  "https://pub-4f5a7f3da62e42ca96c7e87fd47cffe9.r2.dev/chick3.mp4",
  "https://pub-4f5a7f3da62e42ca96c7e87fd47cffe9.r2.dev/sm2.mp4",
  "https://pub-4f5a7f3da62e42ca96c7e87fd47cffe9.r2.dev/sm1.mp4",
];
const containers = ["#p1","#p2","#p3","#p4","#p5","#p6","#p7","#p8"];
const players = [];

// ✅ 页面加载直接初始化前2个播放器（不用密码）
new Artplayer({
  container: containers[0],
  url: urls[0],
  isAutoSize:true,
  playbackRate:true,
  theme:"#23ade5",
  setting:true
})
new Artplayer({
  container: containers[1],
  url: urls[1],
  isAutoSize:true,
  playbackRate:true,
  theme:"#23ade5",
  setting:true
})

// 密码
const pass = "123456";
function unlock(){
  const input = document.getElementById("pwdInput").value.trim();
  if(input === pass){
    // 隐藏密码框，显示后面视频区域
    document.getElementById("lockBox").style.display = "none";
    document.getElementById("secretArea").style.display = "grid";
    // 👉 【你问的这段代码放在这里！】解锁成功才执行后面p3~p8的播放器
    for(let i=2; i<urls.length; i++){
      players.push(new Artplayer({
        container: containers[i],
        url: urls[i],
        isAutoSize:true,
        playbackRate:true,
        theme:"#23ade5",
        setting:true
      }))
    }
  }else{
    document.getElementById("errTip").style.display = "block";
  }
}
</script>
