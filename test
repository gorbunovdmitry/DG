<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Кредит — настройка</title>
  <!-- Roboto -->
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --c-black:#000;
      --c-red:#EF3124;
      --c-bg:#FFF;
      --c-light:#F3F4F5;
      --c-line:#E6E6E6;
      --c-grey:#747474;
    }
    *{box-sizing:border-box;margin:0;padding:0}
    body{font-family:'Roboto',sans-serif;background:var(--c-bg);color:var(--c-black);display:flex;justify-content:center;min-height:100vh}

    /* wizard wrapper */
    .wizard{width:100%;max-width:414px;position:relative;overflow:hidden}

    /* slides */
    .slides{display:flex;transition:transform .4s ease}
    .slide{width:100%;flex-shrink:0;min-height:100vh;padding:24px 20px 96px;display:flex;flex-direction:column}

    .img-wrap{width:220px;height:220px;margin:0 auto}
    .img-wrap img{width:100%;height:auto}

    h2{font-size:20px;font-weight:700;margin-top:16px;line-height:1.25;text-align:left}
    p{font-size:14px;color:var(--c-grey);margin-top:4px}

    /* input blocks */
    .input-block{margin-top:24px}
    label{font-size:14px;color:var(--c-grey)}
    .range-output{margin-top:8px;font-size:16px;font-weight:500}
    input[type=range]{-webkit-appearance:none;width:100%;height:8px;border-radius:4px;background:var(--c-line)}
    input[type=range]::-webkit-slider-thumb{-webkit-appearance:none;width:24px;height:24px;border-radius:50%;background:var(--c-red);cursor:pointer}
    input[type=range]::-moz-range-thumb{width:24px;height:24px;border-radius:50%;background:var(--c-red);cursor:pointer;border:none}
    input[type=number]{width:100%;margin-top:12px;padding:12px 16px;border:1px solid var(--c-line);border-radius:12px;font-size:16px}

    /* toggles */
    .toggle{display:flex;justify-content:space-between;align-items:center;padding:12px 0}
    .toggle span{font-size:16px}
    .toggle input{-webkit-appearance:none;width:40px;height:22px;background:var(--c-line);border-radius:11px;position:relative;cursor:pointer;transition:.3s}
    .toggle input:checked{background:var(--c-red)}
    .toggle input::before{content:"";position:absolute;left:3px;top:3px;width:16px;height:16px;background:#fff;border-radius:50%;transition:.3s}
    .toggle input:checked::before{transform:translateX(18px)}

    /* offers */
    .offers{display:flex;flex-direction:column;gap:12px;margin-top:12px}
    .offer{padding:16px;border:1px solid var(--c-line);border-radius:12px;background:var(--c-light)}
    .offer h3{font-size:20px;font-weight:700}
    .offer small{display:block;font-size:14px;color:var(--c-grey);margin:2px 0}
    .offer button{margin-top:8px;width:100%;padding:12px 0;border:none;border-radius:8px;background:var(--c-red);color:#fff;font-size:15px;font-weight:500;cursor:pointer}

    /* nav bar */
    .nav{position:fixed;bottom:0;left:0;right:0;width:100%;max-width:414px;margin:0 auto;padding:12px 20px;background:var(--c-bg);box-shadow:0 -2px 10px rgba(0,0,0,.06);display:flex;align-items:center;gap:12px}
    .back,.next{border:none;cursor:pointer;font-size:16px;font-weight:500;border-radius:12px}
    .back{width:44px;height:44px;font-size:24px;background:none;color:var(--c-black)}
    .next{flex:1;padding:14px 0;background:var(--c-black);color:#fff}
    .next.hidden{display:none}
  </style>
</head>
<body>
  <div class="wizard" id="wizard">
    <div class="slides" id="slides">
      <!-- 1. Payment -->
      <section class="slide">
        <header>
          <div class="img-wrap"><img src="data:image/webp;base64,UklGRiIAAABXRUJQVlA4WAoAAAAQAAAACwAALwAASUNDUMogwEIPoVYQi1cPDqOgkX5nAyFZG5SM4wTGUaxxef+HS3SblMi7P8nHS6vKziChwMz//F/0Lmw1gAA" alt="money"></div>
          <h2>Сколько вы готовы платить в месяц?</h2>
          <p>Укажите максимальную сумму платежа</p>
          <div class="input-block">
            <label>Сумма, ₽</label>
            <input type="range" id="range-payment" min="10000" max="250000" step="1000" value="16000">
            <div class="range-output" id="out-payment">16 000 ₽</div>
            <input type="number" id="num-payment" min="10000" max="250000" step="1000" value="16000">
          </div>
        </header>
      </section>
      <!-- 2. Assets -->
      <section class="slide">
        <header>
          <div class="img-wrap"><img src="data:image/webp;base64,UklGRnIAAABXRUJQVlA4WAoAAAAQAAAADwAALwAASUNDUMogi9IwMDAYURBSTc0wi/cDIPx1Jqdbhbk/BCRyO0/2jDQwMDAwMDACEQBYQmDQHCohzC0wxAAA=" alt="house"></div>
          <h2>Есть ли у вас собственность?</h2>
          <p>Укажите, чем готовы поручиться</p>
          <div class="input-block">
            <div class="toggle"><span>Автомобиль</span><input type="checkbox" id="has-auto"></div>
            <div class="toggle"><span>Недвижимость</span><input type="checkbox" id="has-real"></div>
          </div>
        </header>
      </section>
      <!-- 3. Amount -->
      <section class="slide">
        <header>
          <div class="img-wrap"><img src="data:image/webp;base64,UklGRkQAAABXRUJQVlA4WAoAAAAQAAAADgAALwAASUNDUMogi4WAAAAJAAAADwAALwMD///hsiAnQAA" alt="bag"></div>
          <h2>Сумма кредита</h2>
          <p>Сколько хотите получить?</p>
          <div class="input-block">
            <label>Сумма, ₽</label>
            <input type="range" id="range-amount" min="10000" max="1700000" step="10000" value="700000">
            <div class="range-output" id="out-amount">700 000 ₽</div>
            <input type="number" id="num-amount" min="10000" max="1700000" step="10000" value="700000">
          </div>
        </header>
      </section>
      <!-- 4. Term -->
      <section class="slide">
        <header>
          <div class="img-wrap"><img src="data:image/webp;base64,UklGRjIAAABXRUJQVlA4WAoAAAAQAAAADgAALwAASUNDUMogCUiB0BmAAAADAAAAHgAEAAA" alt="calendar"></div>
          <h2>Срок кредита</h2>
          <p>На сколько лет берёте?</p>
          <div class="input-block">
            <label>Лет</label>
            <input type="range" id="range-term" min="1" max="20" step="1" value="7">
            <div class="range-output" id="out-term">7 лет</div>
            <input type="number" id="num-term" min="1" max="20" step="1" value="7">
          </div>
        </header>
      </section>
      <!-- 5. Offers -->
      <section class="slide">
        <header>
          <div class="img-wrap"><img src="data:image/webp;base64,UklGRkoAAABXRUJQVlA4ICoAAAAQAAAADQAAKQAAQUxQSCIAAAABBQAAAFZQOAiAAAAT" alt="offer"></div>
          <h2>На своих условиях</h2>
          <div class="offers" id="offers"></div>
        </header>
      </section>
    </div>
    <!-- nav -->
    <div class="nav">
      <button class="back" id="btn-back" aria-label="Назад">←</button>
      <button class="next" id="btn-next">Следующий шаг</button>
    </div>
  </div>

  <script>
    (function(){
      const slidesEl=document.getElementById('slides');
      const slides=[...document.querySelectorAll('.slide')];
      const btnNext=document.getElementById('btn-next');
      const btnBack=document.getElementById('btn-back');
      let index=0;

      function updateNav(){
        btnBack.style.visibility=index===0?'hidden':'visible';
        btnNext.classList.toggle('hidden',index===slides.length-1);
      }
      function goto(i){index=i;slidesEl.style.transform=`translateX(-${100*i}%)`;updateNav();if(index===slides.length-1)calcOffers();}
      btnNext.addEventListener('click',()=>{if(index<slides.length-1)goto(index+1);});
      btnBack.addEventListener('click',()=>{if(index>0)goto(index-1);});

      // sync inputs helper
      function link(idRange,idNum,idOut,postfix=''){const r=document.getElementById(idRange);const n=document.getElementById(idNum);const o=document.getElementById(idOut);const fmt=v=>Number(v).toLocaleString('ru-RU')+postfix;const sync=v=>{o.textContent=fmt(v);};r.addEventListener('input',e=>{n.value=e.target.value;sync(e.target.value);});n.addEventListener('input',e=>{r.value=e.target.value;sync(e.target.value);});sync(r.value);}      
      link('range-payment','num-payment','out-payment',' ₽');
      link('range-amount','num-amount','out-amount',' ₽');
      link('range-term','num-term','out-term',' лет');

      function calcOffers(){
        const pay=parseInt(document.getElementById('num-payment').value,10);
        const amt=parseInt(document.getElementById('num-amount').value,10);
        const termY=parseInt(document.getElementById('num-term').value,10);
        const months=termY*12;
        const hasAuto=document.getElementById('has-auto').checked;
        const hasReal=document.getElementById('has-real').checked;
        const annuity=(P,rate)=>{const r=rate/12/100;return Math.round(P*r/(1-Math.pow(1+r,-months)))};
        const arr=[{rate:30,cond:'Без залога'},{rate:28,cond:'Под залог авто',show:hasAuto},{rate:25,cond:'Под залог недвижимости',show:hasReal}];
        const offersDiv=document.getElementById('offers');offersDiv.innerHTML='';
        arr.filter(o=>o.show===undefined||o.show).forEach(o=>{
          const m=annuity(amt,o.rate).toLocaleString('ru-RU');
          const wrap=document.createElement('div');wrap.className='offer';
          wrap.innerHTML=`<h3>${m} ₽/мес</h3><small>${amt.toLocaleString('ru-RU')} ₽ • ${termY} лет</small><small>${o.cond}</small><button>Выбрать</button>`;
          offersDiv.appendChild(wrap);
        });
      }

      // init
      updateNav();
    })();
  </script>
</body>
</
