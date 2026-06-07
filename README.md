<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<style>
*{box-sizing:border-box}
body{font-family:Arial;background:#0f172a;color:#e2e8f0;margin:0;padding:16px}
h1{text-align:center;color:#38bdf8;font-size:20px;margin-bottom:2px}
.sub{text-align:center;color:#64748b;font-size:11px;margin-bottom:14px}
.kpi{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-bottom:14px}
.k{background:#1e293b;border-radius:8px;padding:12px;text-align:center;border:1px solid #334155}
.v{font-size:18px;font-weight:bold}
.l{font-size:10px;color:#94a3b8;margin-top:2px}
.cg{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.cb{background:#1e293b;border-radius:8px;padding:14px;border:1px solid #334155}
.cf{grid-column:1/-1}
.ct{font-size:10px;font-weight:bold;color:#38bdf8;text-transform:uppercase;margin-bottom:4px}
.cd{font-size:9px;color:#64748b;margin-bottom:10px;font-style:italic}
.ins{background:#0f2744;border-left:3px solid #38bdf8;padding:8px 12px;font-size:10px;margin-top:6px;line-height:1.5}
.warn{background:#2d1515;border-left:3px solid #ef4444;padding:8px 12px;font-size:10px;margin-top:6px;line-height:1.5}
.good{background:#0f2d1a;border-left:3px solid #4ade80;padding:8px 12px;font-size:10px;margin-top:6px;line-height:1.5}
</style>

<h1>DASHBOARD VAT TU NHAP XUAT TON - T01/2013</h1>
<p class="sub">Du lieu da clean | Quality Score: 82/100 | 130+ mat hang | 01/01 - 31/01/2013</p>

<div class="kpi">
  <div class="k"><div class="v" style="color:#38bdf8">2,239 ty</div><div class="l">Ton dau ky</div></div>
  <div class="k"><div class="v" style="color:#fbbf24">68.4 tr</div><div class="l">Nhap trong ky</div></div>
  <div class="k"><div class="v" style="color:#4ade80">180.7 tr</div><div class="l">Xuat trong ky</div></div>
  <div class="k"><div class="v" style="color:#f87171">2,127 ty</div><div class="l">Ton cuoi ky</div></div>
  <div class="k"><div class="v" style="color:#38bdf8">130+</div><div class="l">Tong SKU</div></div>
  <div class="k"><div class="v" style="color:#4ade80">14</div><div class="l">SKU co xuat</div></div>
  <div class="k"><div class="v" style="color:#f87171">116+</div><div class="l">SKU khong xuat</div></div>
  <div class="k"><div class="v" style="color:#fbbf24">8.07%</div><div class="l">Turnover Rate</div></div>
</div>

<div class="cg">

  <div class="cb cf">
    <div class="ct">1. XUAT KHO THEO MAT HANG (Horizontal Bar)</div>
    <div class="cd">Horizontal Bar: nhan dai, doc ngang de hon. So sanh nhieu hang cung luc ro rang nhat.</div>
    <canvas id="c1" height="110"></canvas>
    <div class="ins">Thep hop vuong xuat 46.5M - nhieu nhat. Thep goc xuat 100% ton kho. Top 3 chiem 57% tong xuat.</div>
  </div>

  <div class="cb">
    <div class="ct">2. TY TRONG XUAT THEO NHOM HANG (Doughnut)</div>
    <div class="cd">Doughnut: 5 nhom, the hien % tong the ro rang nhat.</div>
    <canvas id="c2"></canvas>
    <div class="ins">Thep chiem 86.6% tong xuat. Son 6.8%. Cong ty kinh doanh thep la chu yeu.</div>
  </div>

  <div class="cb">
    <div class="ct">3. TON DAU KY vs TON CUOI KY (Grouped Bar)</div>
    <div class="cd">Grouped Bar: so sanh 2 gia tri cung 1 mat hang. Thay ro hang nao ban duoc.</div>
    <canvas id="c3"></canvas>
    <div class="ins">Thep hop vuong giam 79M xuong 33M (ban 58%). Thep goc ve 0 (ban het). Ton lanh giam it - ban cham.</div>
  </div>

  <div class="cb cf">
    <div class="ct">4. TURNOVER RATE % - MA MAU RUI RO (Color Bar)</div>
    <div class="cd">Color Bar: chieu cao = ty le ban, mau sac = muc do rui ro. 1 bieu do noi 2 thu.</div>
    <canvas id="c4" height="70"></canvas>
    <div class="good">XANH 50%+: Thep goc, Son nuoc, Thep tam 4ly, Thep hop vuong, Thep la LG - BAN CHAY</div>
    <div class="ins">VANG 25-50%: Thep la, Thep hop X0.9, Thep tam 5ly, Thep tron 16, Thep tam 6ly - BINH THUONG</div>
    <div class="warn">CAM 10-25%: Thep tam 8ly, Ton lanh - CHAM | DO duoi 10%: Xang, Que han, Thep tam - NGUY HIEM</div>
  </div>

  <div class="cb cf">
    <div class="ct">5. NHAP vs XUAT TRONG KY (Grouped Bar)</div>
    <div class="cd">Grouped Bar: dong tien vao-ra. Hang nao xuat nhieu hon nhap = can nhap gap.</div>
    <canvas id="c5" height="80"></canvas>
    <div class="warn">NGUY HIEM: Thep hop vuong xuat 46.5M nhung KHONG NHAP - sap het hang! Thep tron 16 xuat 31.9M khong nhap!</div>
    <div class="ins">TOT: Thep la LO nhap 30.3M xuat 20.4M - can bang. Son trong nhap 8.75M chua xuat - hang moi.</div>
  </div>

  <div class="cb cf">
    <div class="ct">6. MA TRAN RUI RO - TON KHO vs TURNOVER (Bubble Chart)</div>
    <div class="cd">Bubble Chart: X=ton kho, Y=toc do ban, Kich thuoc=muc rui ro. 3 bien cung luc.</div>
    <canvas id="c6"></canvas>
    <div class="warn">GOC TRAI DUOI = NGUY HIEM: Thep tam(170M), Thep tron 8(155M), Thep tron 20(133M), Xi mang(107M) - ~565 trieu dong dong von!</div>
    <div class="good">GOC PHAI TREN = HIEU QUA: Thep hop vuong, Thep la LO, Thep tam 4ly - hang tao doanh thu thuc su.</div>
  </div>

</div>

<script>
Chart.defaults.color = '#94a3b8';
Chart.defaults.borderColor = '#334155';

new Chart(document.getElementById('c1'), {
  type: 'bar',
  data: {
    labels: ['Thep hop vuong','Thep tron 16','Thep la LO','Thep goc','Ton lanh','Thep tam 5ly','Thep la LG','Thep tam 4ly','Thep tam 6ly','Thep la','Thep hop X0.9','Thep tam 8ly','Xang 92','Que han'],
    datasets: [{
      data: [46.54,31.87,20.42,27.03,12.31,10.25,7.08,7.25,6.37,3.52,2.46,2.14,0.30,0.35],
      backgroundColor: ['#3b82f6','#6366f1','#10b981','#f59e0b','#06b6d4','#8b5cf6','#ec4899','#14b8a6','#f97316','#84cc16','#38bdf8','#a78bfa','#fb923c','#4ade80'],
      borderRadius: 4
    }]
  },
  options: {
    indexAxis: 'y',
    responsive: true,
    plugins: { legend: { display: false } },
    scales: { x: { ticks: { callback: function(v) { return v + 'M'; } } } }
  }
});

new Chart(document.getElementById('c2'), {
  type: 'doughnut',
  data: {
    labels: ['Thep 86.6%','Son 6.8%','Khac 6.2%','Que han 0.2%','Xang 0.2%'],
    datasets: [{
      data: [156.4,12.4,11.3,0.35,0.3],
      backgroundColor: ['#3b82f6','#10b981','#f59e0b','#ef4444','#8b5cf6'],
      borderWidth: 2,
      borderColor: '#0f172a'
    }]
  },
  options: {
    responsive: true,
    plugins: { legend: { position: 'bottom', labels: { font: { size: 10 } } } }
  }
});

new Chart(document.getElementById('c3'), {
  type: 'bar',
  data: {
    labels: ['Thep hop vuong','Thep tron 16','Thep la LO','Ton lanh','Thep tam 5ly','Thep la LG','Thep tam 4ly','Thep tam 6ly','Thep la','Thep hop X0.9'],
    datasets: [
      { label: 'Ton dau ky', data: [79.41,122.85,0,114.46,26.48,0,10.92,24.99,7.23,6.13], backgroundColor: '#3b82f6', borderRadius: 3 },
      { label: 'Ton cuoi ky', data: [32.88,90.99,9.91,102.16,16.23,7.92,3.67,18.63,3.71,3.67], backgroundColor: '#f87171', borderRadius: 3 }
    ]
  },
  options: {
    responsive: true,
    plugins: { legend: { position: 'top', labels: { font: { size: 10 } } } },
    scales: { y: { ticks: { callback: function(v) { return v + 'M'; } } } }
  }
});

var labels4 = ['Thep goc','Son nuoc','Thep tam 4ly','Thep hop vuong','Thep la LG','Thep la','Thep hop X0.9','Thep tam 5ly','Son lot','Thep la LO','Thep tron 16','Thep tam 6ly','Thep tam 8ly','Ton lanh','Xang 92','Que han','Thep tam'];
var data4 = [100,100,66.5,58.6,52.8,48.7,40.1,38.7,33.3,32.7,25.9,25.5,19.1,10.7,4.1,0.7,0.68];
new Chart(document.getElementById('c4'), {
  type: 'bar',
  data: {
    labels: labels4,
    datasets: [{
      data: data4,
      backgroundColor: function(c) {
        var d = c.raw;
        return d >= 50 ? '#4ade80' : d >= 25 ? '#fbbf24' : d >= 10 ? '#f97316' : '#ef4444';
      },
      borderRadius: 4
    }]
  },
  options: {
    responsive: true,
    plugins: { legend: { display: false } },
    scales: { y: { max: 110, ticks: { callback: function(v) { return v + '%'; } } } }
  }
});

new Chart(document.getElementById('c5'), {
  type: 'bar',
  data: {
    labels: ['Thep la LO','Thep la LG','Thep hop vuong','Thep tron 16','Ton lanh','Thep tam 5ly','Thep tam 4ly','Thep tam 6ly','Thep la','Son trong','Son nuoc','Son lot'],
    datasets: [
      { label: 'Nhap trong ky', data: [30.34,15.0,0,0,0,0,0,0,0,8.75,3.04,1.69], backgroundColor: '#3b82f6', borderRadius: 3 },
      { label: 'Xuat trong ky', data: [20.42,7.08,46.54,31.87,12.31,10.25,7.25,6.37,3.52,0,0,1.13], backgroundColor: '#4ade80', borderRadius: 3 }
    ]
  },
  options: {
    responsive: true,
    plugins: { legend: { position: 'top', labels: { font: { size: 10 } } } },
    scales: { y: { ticks: { callback: function(v) { return v + 'M'; } } } }
  }
});

new Chart(document.getElementById('c6'), {
  type: 'bubble',
  data: {
    datasets: [
      {
        label: 'Rui ro cao',
        data: [{x:170.35,y:0.68,r:20},{x:154.93,y:0,r:18},{x:132.9,y:0,r:16},{x:106.55,y:0,r:14},{x:74.29,y:0,r:12},{x:60.0,y:0,r:10},{x:49.93,y:0.7,r:9}],
        backgroundColor: 'rgba(239,68,68,0.7)'
      },
      {
        label: 'Can theo doi',
        data: [{x:102.16,y:10.7,r:13},{x:90.99,y:25.9,r:12},{x:18.63,y:25.5,r:8},{x:16.23,y:38.7,r:8}],
        backgroundColor: 'rgba(251,191,36,0.7)'
      },
      {
        label: 'Hieu qua',
        data: [{x:46.54,y:58.6,r:10},{x:9.91,y:67.3,r:7},{x:7.92,y:47.2,r:6},{x:3.67,y:66.4,r:5},{x:0,y:100,r:4}],
        backgroundColor: 'rgba(74,222,128,0.7)'
      }
    ]
  },
  options: {
    responsive: true,
    plugins: { legend: { position: 'top', labels: { font: { size: 10 } } } },
    scales: {
      x: { title: { display: true, text: 'Ton kho (trieu dong)', color: '#94a3b8' }, ticks: { callback: function(v) { return v + 'M'; } } },
      y: { title: { display: true, text: 'Turnover Rate %', color: '#94a3b8' }, ticks: { callback: function(v) { return v + '%'; } } }
    }
  }
});
</script>
