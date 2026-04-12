# huaren-africaAdd file → Upload files[index.html](https://github.com/user-attachments/files/26660817/index.html)
Win + Rnotepad
<!DOCTYPE html>
<html lang="zh">
<head>
<meta charset="UTF-8">
<title>非洲通 - 华人信息平台</title>
<style>
body {font-family: Arial; margin:0; background:#f5f5f5;}
.header {background:#007bff; color:white; padding:15px; text-align:center;}
.search {padding:10px;}
input {width:100%; padding:10px;}
.nav {display:flex; justify-content:space-around; background:white; padding:10px;}
.nav div {padding:10px; cursor:pointer;}
.box {background:white; margin:10px; padding:10px; border-radius:8px;}
.btn {background:#007bff; color:white; padding:8px; display:inline-block; margin-top:5px; cursor:pointer;}
.hidden {display:none;}
</style>
</head>

<body>

<div class="header">
<h2>🌍 非洲通</h2>
<p>在非洲的中国人信息平台</p >
</div>

<div class="search">
<input id="searchInput" placeholder="搜索：租房 / 招聘 / 服务" onkeyup="search()">
</div>

<div class="nav">
<div onclick="show('house')">🏠租房</div>
<div onclick="show('job')">👷招聘</div>
<div onclick="show('service')">🚚服务</div>
<div onclick="show('post')">📝发布</div>
</div>

<!-- 租房 -->
<div id="house">

<div class="box">
🏠 市中心公寓<br>
💰 5000元/月<br>
📍 达喀尔<br>
📞 微信：abc123
</div>

<div class="box">
🏠 华人区单间<br>
💰 3000元/月<br>
📍 达喀尔<br>
📞 微信：xyz888
</div>

</div>

<!-- 招聘 -->
<div id="job" class="hidden">

<div class="box">
👷 招法语翻译<br>
💰 面议<br>
📍 达喀尔<br>
📞 微信：aaa111
</div>

<div class="box">
👷 招司机<br>
💰 4000-6000<br>
📞 微信：bbb222
</div>

</div>

<!-- 服务 -->
<div id="service" class="hidden">

<div class="box">
🚚 清关物流服务<br>
✔ 中国→非洲<br>
📞 微信：ccc333
</div>

</div>

<!-- 发布 -->
<div id="post" class="hidden">

<div class="box">
<h3>发布信息（示例）</h3>
<input placeholder="标题"><br><br>
<input placeholder="联系方式"><br><br>
<button class="btn">提交（暂未接入数据库）</button>
</div>

</div>

<script>

function show(id){
document.getElementById('house').classList.add('hidden');
document.getElementById('job').classList.add('hidden');
document.getElementById('service').classList.add('hidden');
document.getElementById('post').classList.add('hidden');
document.getElementById(id).classList.remove('hidden');
}

function search(){
let val = document.getElementById('searchInput').value;
let boxes = document.getElementsByClassName('box');

for(let i=0;i<boxes.length;i++){
let text = boxes[i].innerText;
if(text.includes(val)){
boxes[i].style.display = '';
}else{
boxes[i].style.display = 'none';
}
}
}

</script>

</body>
</html>
