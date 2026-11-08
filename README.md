# what-is-meaning-true-love-
AU Kimmy, Erine, Ribka X Reader
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Time Management - Kimmy, Erine, Ribka X Reader</title>
<style>
  body{font-family:Georgia,serif;background:#141019;color:#fff;max-width:600px;margin:auto;padding:20px;line-height:1.7}
  .card{background:#241a2e;padding:20px;border-radius:16px;margin:15px 0}
  button{background:#ff5c8a;border:none;color:#fff;padding:12px 20px;border-radius:999px;width:100%;margin-top:10px;font-size:16px;cursor:pointer}
  input{width:100%;padding:12px;border-radius:10px;border:none;margin-top:10px;box-sizing:border-box}
  .chat{background:#fff;color:#222;padding:10px 14px;border-radius:14px;margin:8px 0}
  .hidden{display:none}
  small{color:#c9b8d6}
</style>
</head>
<body>
<h1>Time Management</h1>
<p>Kimmy, Erine, Ribka X Reader (y/n)</p>
<small>AU by you</small>

<div id="lock" class="card">
  <h3>Masukin Passcode 🔒</h3>
  <p>Hint dari author: 1012</p>
  <input id="pass" type="password" placeholder="Passcode...">
  <button onclick="cekPass()">Buka AU</button>
  <p id="salah" style="color:#ff8fa3;display:none">Passcode salah, coba lagi ya :(</p>
</div>

<div id="start" class="card hidden">
  <h3>Siapa nama kamu?</h3>
  <p>Nama ini bakal dipake sebagai (y/n).</p>
  <input id="yourname" placeholder="Tulis nama kamu...">
  <button onclick="mulai()">Mulai Baca</button>
</div>

<div id="story" class="hidden">
  <div class="card">
    <p><b>CHAPTER 1 - TIME MANAGEMENT</b></p>
    <p>Jam di HP <span class="name">kamu</span> nunjukin 19:00. Di grup chat, 3 nama itu lagi ribut bareng.</p>
    <div class="chat"><b>Kimmy:</b> <span class="name">kamu</span>, besok kamu temenin aku latihan ya? Aku butuh kamu.</div>
    <div class="chat"><b>Erine:</b> Eh enak aja! Besok <span class="name">kamu</span> udah janji sama aku mau nonton film!</div>
    <div class="chat"><b>Ribka:</b> Kalian berdua apaan sih? <span class="name">kamu</span> udah janji minggu ini full buat aku. Jangan rebut-rebut.</div>
    <p>Lo cuma punya 24 jam buat bagi waktu ke mereka bertiga.</p>
  </div>
  <div class="card">
    <h3>Besok, siapa yang kamu temuin duluan, <span class="name">kamu</span>?</h3>
    <button onclick="pilih('KIMMY')">A. Kimmy - Latihan bareng</button>
    <button onclick="pilih('ERINE')">B. Erine - Nonton film</button>
    <button onclick="pilih('RIBKA')">C. Ribka - Janji yang udah lama</button>
  </div>
  <div id="hasilKIMMY" class="card hidden">
    <p><b>— KIMMY ROUTE —</b></p>
    <p>Lo pilih Kimmy. Di ruang latihan, dia diem aja dari tadi.</p>
    <p><i>"Aku tuh bukan mau latihan. Aku cuma mau ada alasan buat ketemu kamu."</i></p>
    <p><b>TO BE CONTINUED...</b></p>
  </div>
  <div id="hasilERINE" class="card hidden">
    <p><b>— ERINE ROUTE —</b></p>
    <p>Lo pilih Erine. Di bioskop, dia gak fokus nonton. Dia malah fokus liatin lo.</p>
    <p><i>"Cuma hari ini aku bisa punya kamu seharian tanpa dibagi-bagi."</i></p>
    <p><b>TO BE CONTINUED...</b></p>
  </div>
  <div id="hasilRIBKA" class="card hidden">
    <p><b>— RIBKA ROUTE —</b></p>
    <p>Lo pilih Ribka. Dia udah nunggu di tempat janji kalian.</p>
    <p><i>"Makasih ya udah nepati janji kamu ke aku."</i></p>
    <p><b>TO BE CONTINUED...</b></p>
  </div>
</div>

<script>
function cekPass(){
  let p = document.getElementById('pass').value;
  if(p === '1012'){
    document.getElementById('lock').classList.add('hidden');
    document.getElementById('start').classList.remove('hidden');
  } else {
    document.getElementById('salah').style.display = 'block';
  }
}
function mulai(){
  let nama = document.getElementById('yourname').value || 'kamu';
  document.querySelectorAll('.name').forEach(e => e.textContent = nama);
  document.getElementById('start').classList.add('hidden');
  document.getElementById('story').classList.remove('hidden');
}
function pilih(p){
  ['KIMMY','ERINE','RIBKA'].forEach(x => document.getElementById('hasil'+x).classList.add('hidden'));
  document.getElementById('hasil'+p).classList.remove('hidden');
}
</script>
</body>
</html>
