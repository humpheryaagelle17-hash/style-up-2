<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Style Up — Fashion & Accessories</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --pink:      #FDE8EF;
    --pink-mid:  #F9C8D8;
    --pink-deep: #E8869F;
    --pink-dark: #C4526D;
    --black:     #1A0A0F;
    --white:     #FFFFFF;
    --gray:      #9E8590;
    --border:    #F0CEDA;
    --shadow:    rgba(196,82,109,0.13);
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  body{background:var(--pink);font-family:'DM Sans',sans-serif;color:var(--black);min-height:100vh;}

/* ── HEADER ── */
header{background:var(–black);padding:0 2rem;display:flex;align-items:center;
justify-content:space-between;position:sticky;top:0;z-index:200;height:68px;
border-bottom:3px solid var(–pink-deep);}
.logo{font-family:‘Playfair Display’,serif;font-size:1.8rem;font-weight:900;
color:#fff;letter-spacing:3px;text-transform:uppercase;}
.logo span{color:var(–pink-deep);}
.header-right{display:flex;align-items:center;gap:.9rem;}
.phone-badge{background:var(–pink-deep);color:#fff;font-size:.72rem;font-weight:600;
padding:7px 14px;border-radius:30px;text-decoration:none;display:flex;align-items:center;
gap:6px;transition:background .2s;}
.phone-badge:hover{background:var(–pink-dark);}
.admin-btn{background:transparent;color:#888;border:1px solid #444;
font-family:‘DM Sans’,sans-serif;font-size:.72rem;letter-spacing:1.5px;
text-transform:uppercase;padding:7px 16px;cursor:pointer;border-radius:30px;transition:all .2s;}
.admin-btn:hover{color:#fff;border-color:#fff;}
.admin-btn.on{background:var(–pink-deep);color:#fff;border-color:var(–pink-deep);}

/* ── HERO ── */
.hero{background:linear-gradient(135deg,var(–black) 0%,#3a1020 100%);
color:#fff;padding:4rem 2rem 3.5rem;text-align:center;position:relative;overflow:hidden;}
.hero::before{content:’’;position:absolute;inset:0;
background:radial-gradient(ellipse at 50% -10%,rgba(232,134,159,.25) 0%,transparent 65%);}
.hero-tag{font-size:.68rem;letter-spacing:5px;text-transform:uppercase;color:var(–pink-deep);
margin-bottom:1rem;position:relative;}
.hero h1{font-family:‘Playfair Display’,serif;font-size:clamp(2.4rem,6vw,4.2rem);
font-weight:900;line-height:1.08;margin-bottom:1rem;position:relative;}
.hero h1 em{color:var(–pink-deep);font-style:italic;}
.hero p{color:rgba(255,255,255,.5);font-size:.95rem;max-width:420px;
margin:0 auto;line-height:1.7;position:relative;}

/* ── STORE FILTER TABS ── */
.store-tabs{display:flex;padding:0 2rem;border-bottom:2px solid var(–border);
background:var(–pink);overflow-x:auto;scrollbar-width:none;}
.store-tabs::-webkit-scrollbar{display:none;}
.stab{padding:1rem 1.3rem;font-size:.78rem;letter-spacing:1.5px;text-transform:uppercase;
font-weight:500;color:var(–gray);cursor:pointer;border-bottom:2px solid transparent;
margin-bottom:-2px;white-space:nowrap;transition:all .2s;background:none;
border-top:none;border-left:none;border-right:none;font-family:‘DM Sans’,sans-serif;}
.stab.on{color:var(–pink-dark);border-bottom-color:var(–pink-dark);}
.stab:hover{color:var(–pink-dark);}

/* ── MAIN ── */
main{max-width:1200px;margin:0 auto;padding:2.5rem 1.5rem;}

/* ══════════════════════════════
ADMIN PANEL
══════════════════════════════ */
.admin-panel{display:none;margin-bottom:2.5rem;animation:fadeDown .35s ease;}
.admin-panel.open{display:block;}
@keyframes fadeDown{from{opacity:0;transform:translateY(-12px)}to{opacity:1;transform:translateY(0)}}

/* Admin header bar */
.ap-head{background:var(–black);border-radius:14px 14px 0 0;padding:1.4rem 2rem;
display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:1rem;
border-bottom:2px solid var(–pink-deep);}
.ap-head h2{font-family:‘Playfair Display’,serif;font-size:1.25rem;color:#fff;letter-spacing:1px;}
.ap-head p{font-size:.78rem;color:var(–gray);margin-top:3px;}
.stats{display:flex;gap:1.5rem;}
.stat{text-align:center;}
.stat b{font-family:‘Playfair Display’,serif;font-size:1.6rem;font-weight:700;
color:var(–pink-deep);display:block;line-height:1;}
.stat s2{font-size:.63rem;letter-spacing:1.5px;text-transform:uppercase;
color:var(–gray);margin-top:3px;display:block;}

/* Admin body */
.ap-body{background:#fff;border-radius:0 0 14px 14px;border:1px solid var(–border);
border-top:none;overflow:hidden;}

/* Admin inner tabs */
.ap-tabs{display:flex;border-bottom:2px solid var(–border);background:#FFF5F8;}
.aptab{padding:.9rem 1.6rem;font-size:.78rem;letter-spacing:1.2px;text-transform:uppercase;
font-weight:600;color:var(–gray);cursor:pointer;border-bottom:2px solid transparent;
margin-bottom:-2px;background:none;border-top:none;border-left:none;border-right:none;
font-family:‘DM Sans’,sans-serif;transition:all .2s;display:flex;align-items:center;gap:6px;}
.aptab:hover{color:var(–pink-dark);}
.aptab.on{color:var(–pink-dark);border-bottom-color:var(–pink-dark);}

.ap-section{display:none;}
.ap-section.on{display:block;}

/* ── POST FORM ── */
.post-wrap{padding:1.5rem;}

/* Live preview */
.preview-card{background:var(–pink);border:1.5px dashed var(–border);border-radius:12px;
padding:1.2rem;display:flex;align-items:center;gap:1rem;margin-bottom:1.4rem;}
.prev-icon{width:56px;height:56px;border-radius:10px;background:var(–pink-mid);
display:flex;align-items:center;justify-content:center;font-size:1.8rem;flex-shrink:0;}
.prev-info .pv-name{font-family:‘Playfair Display’,serif;font-size:.95rem;font-weight:700;}
.prev-info .pv-meta{font-size:.78rem;color:var(–gray);margin-top:2px;}
.prev-info .pv-price{font-family:‘Playfair Display’,serif;font-size:1rem;
font-weight:700;color:var(–pink-dark);margin-top:3px;}
.prev-info .pv-colors{display:flex;gap:5px;margin-top:6px;flex-wrap:wrap;}
.pv-swatch{width:18px;height:18px;border-radius:50%;border:2px solid rgba(0,0,0,.1);flex-shrink:0;}

/* Form grid */
.fgrid{display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-bottom:1rem;}
.fgrid .full{grid-column:1/-1;}
.fg{display:flex;flex-direction:column;gap:.4rem;}
.fg label{font-size:.7rem;letter-spacing:1.8px;text-transform:uppercase;color:var(–gray);font-weight:600;}
.fg input,.fg select,.fg textarea{
background:var(–pink);border:1.5px solid var(–border);color:var(–black);
padding:10px 14px;font-family:‘DM Sans’,sans-serif;font-size:.9rem;
border-radius:8px;outline:none;transition:border-color .2s,box-shadow .2s;}
.fg input:focus,.fg select:focus,.fg textarea:focus{
border-color:var(–pink-deep);box-shadow:0 0 0 3px rgba(232,134,159,.15);}
.fg textarea{resize:vertical;min-height:76px;}
.fg select{cursor:pointer;}

/* Color picker row */
.color-row{display:flex;align-items:center;gap:.6rem;flex-wrap:wrap;}
.color-row input[type=color]{
width:38px;height:38px;border:2px solid var(–border);border-radius:8px;
cursor:pointer;padding:2px;background:var(–pink);}
.color-chips{display:flex;gap:.4rem;flex-wrap:wrap;align-items:center;}
.chip{width:26px;height:26px;border-radius:50%;border:2px solid rgba(0,0,0,.12);
cursor:pointer;position:relative;transition:transform .15s;}
.chip:hover{transform:scale(1.15);}
.chip .remove-chip{position:absolute;top:-5px;right:-5px;background:var(–pink-dark);
color:#fff;border:none;border-radius:50%;width:14px;height:14px;font-size:.55rem;
cursor:pointer;display:none;align-items:center;justify-content:center;line-height:1;}
.chip:hover .remove-chip{display:flex;}
/* ── IMAGE DROP ZONE ── */
.img-drop-zone{
border:2px dashed var(–border);border-radius:12px;
background:var(–pink);cursor:pointer;transition:border-color .2s,background .2s;
position:relative;overflow:hidden;min-height:130px;
display:flex;align-items:center;justify-content:center;}
.img-drop-zone:hover,.img-drop-zone.drag-over{
border-color:var(–pink-deep);background:var(–pink-mid);}
.img-drop-zone.drag-over{border-style:solid;}
.dz-idle{text-align:center;padding:1.5rem 1rem;pointer-events:none;}
.dz-icon{font-size:2.2rem;display:block;margin-bottom:.5rem;opacity:.6;}
.dz-main{font-size:.85rem;color:var(–gray);line-height:1.5;margin-bottom:.25rem;}
.dz-sub{font-size:.72rem;color:var(–border);letter-spacing:.5px;}
.dz-preview{width:100%;position:relative;display:flex;align-items:center;justify-content:center;}
.dz-preview img{width:100%;max-height:200px;object-fit:contain;border-radius:10px;display:block;}
.dz-remove{position:absolute;top:8px;right:8px;background:var(–pink-dark);color:#fff;
border:none;padding:5px 12px;border-radius:20px;font-size:.72rem;font-weight:600;
cursor:pointer;font-family:‘DM Sans’,sans-serif;transition:background .2s;z-index:2;}
.dz-remove:hover{background:#a03055;}

.add-color-btn{background:var(–pink-dark);color:#fff;border:none;
padding:8px 14px;border-radius:20px;font-size:.75rem;font-weight:600;
cursor:pointer;font-family:‘DM Sans’,sans-serif;transition:background .2s;white-space:nowrap;}
.add-color-btn:hover{background:var(–pink-deep);}

/* Buttons */
.form-actions{display:flex;gap:.8rem;flex-wrap:wrap;align-items:center;margin-top:.4rem;}
.btn-post{background:var(–pink-dark);color:#fff;border:none;padding:13px 30px;
font-family:‘DM Sans’,sans-serif;font-size:.85rem;font-weight:600;letter-spacing:1px;
text-transform:uppercase;cursor:pointer;border-radius:30px;transition:background .2s,transform .15s;}
.btn-post:hover{background:var(–pink-deep);}
.btn-post:active{transform:scale(.97);}
.btn-clear{background:transparent;color:var(–gray);border:1.5px solid var(–border);
padding:13px 22px;font-family:‘DM Sans’,sans-serif;font-size:.85rem;
border-radius:30px;cursor:pointer;transition:all .2s;}
.btn-clear:hover{border-color:var(–pink-deep);color:var(–pink-dark);}

/* ── MANAGE TAB ── */
.manage-toolbar{display:flex;align-items:center;gap:1rem;padding:1rem 1.5rem;
background:#FFF5F8;border-bottom:1px solid var(–border);flex-wrap:wrap;}
.msearch{flex:1;min-width:180px;position:relative;}
.msearch input{width:100%;background:#fff;border:1px solid var(–border);
padding:8px 14px 8px 36px;border-radius:30px;font-family:‘DM Sans’,sans-serif;
font-size:.85rem;color:var(–black);outline:none;transition:border-color .2s;}
.msearch input:focus{border-color:var(–pink-deep);}
.si{position:absolute;left:12px;top:50%;transform:translateY(-50%);
font-size:.85rem;color:var(–gray);pointer-events:none;}
.mfilters{display:flex;gap:.4rem;flex-wrap:wrap;}
.mfbtn{background:#fff;border:1px solid var(–border);color:var(–gray);
padding:6px 14px;border-radius:30px;font-size:.72rem;letter-spacing:1px;
text-transform:uppercase;cursor:pointer;font-family:‘DM Sans’,sans-serif;transition:all .2s;}
.mfbtn.on,.mfbtn:hover{background:var(–pink-deep);color:#fff;border-color:var(–pink-deep);}

.manage-list{padding:1rem 1.5rem;display:flex;flex-direction:column;gap:.7rem;
max-height:420px;overflow-y:auto;scrollbar-width:thin;scrollbar-color:var(–border) transparent;}
.mrow{display:grid;grid-template-columns:48px 1fr auto auto auto;
align-items:center;gap:1rem;background:var(–pink);border:1px solid var(–border);
border-radius:10px;padding:.8rem 1rem;transition:box-shadow .2s;animation:fadeUp .3s ease both;}
.mrow:hover{box-shadow:0 4px 16px var(–shadow);}
@keyframes fadeUp{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:translateY(0)}}
.mrow-icon{width:48px;height:48px;border-radius:10px;background:var(–pink-mid);
display:flex;align-items:center;justify-content:center;font-size:1.6rem;flex-shrink:0;}
.mrow-name{font-weight:600;font-size:.9rem;color:var(–black);margin-bottom:3px;}
.mrow-meta span{background:var(–border);padding:2px 8px;border-radius:20px;
font-size:.65rem;text-transform:uppercase;letter-spacing:.5px;}
.mrow-colors{display:flex;gap:3px;margin-top:4px;flex-wrap:wrap;}
.mrow-swatch{width:14px;height:14px;border-radius:50%;border:1.5px solid rgba(0,0,0,.1);}
.mprice{font-family:‘Playfair Display’,serif;font-size:1rem;font-weight:700;
color:var(–pink-dark);white-space:nowrap;}
.mprice small{font-family:‘DM Sans’,sans-serif;font-size:.65rem;color:var(–gray);font-weight:400;}
.stoggle{border:1px solid var(–border);padding:5px 13px;border-radius:20px;
font-size:.7rem;cursor:pointer;font-family:‘DM Sans’,sans-serif;
font-weight:500;transition:opacity .2s;white-space:nowrap;}
.stoggle.in{color:#2e7d32;border-color:#a5d6a7;background:#f1f8e9;}
.stoggle.out{color:var(–pink-dark);border-color:var(–pink-mid);background:#fff0f3;}
.stoggle:hover{opacity:.7;}
.del-btn{background:transparent;border:1px solid var(–border);color:var(–gray);
width:34px;height:34px;border-radius:8px;cursor:pointer;font-size:1rem;
display:flex;align-items:center;justify-content:center;transition:all .2s;flex-shrink:0;}
.del-btn:hover{background:var(–pink-dark);color:#fff;border-color:var(–pink-dark);}
.m-empty{text-align:center;padding:3rem 1rem;color:var(–gray);}
.m-empty .ei{font-size:2.5rem;margin-bottom:.6rem;opacity:.35;display:block;}
.ap-note{padding:.8rem 1.5rem;background:#FFF5F8;border-top:1px solid var(–border);
font-size:.75rem;color:var(–gray);}

/* ── STORE GRID ── */
.sec-head{display:flex;align-items:center;justify-content:space-between;
margin-bottom:1.5rem;flex-wrap:wrap;gap:.5rem;}
.sec-head h2{font-family:‘Playfair Display’,serif;font-size:1.8rem;font-weight:700;}
.cpill{background:var(–pink-mid);color:var(–pink-dark);font-size:.75rem;
font-weight:500;padding:4px 12px;border-radius:20px;}

.pgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:1.5rem;}

.pcard{background:#fff;border:1px solid var(–border);border-radius:14px;overflow:hidden;
transition:transform .25s,box-shadow .25s;animation:fadeUp .4s ease both;}
.pcard:hover{transform:translateY(-5px);box-shadow:0 16px 40px var(–shadow);}

.cimg{width:100%;aspect-ratio:4/3;
background:linear-gradient(135deg,var(–pink-mid),var(–pink));
display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden;}
.cimg img{width:100%;height:100%;object-fit:cover;display:block;}
.cemoji{font-size:3.8rem;opacity:.5;position:absolute;}
.sbadge{position:absolute;top:10px;left:10px;background:var(–pink-deep);color:#fff;
font-size:.6rem;letter-spacing:1.5px;text-transform:uppercase;
padding:4px 10px;border-radius:20px;font-weight:600;}
.sbadge.sold{background:#aaa;}

.ccat{font-size:.63rem;letter-spacing:2.5px;text-transform:uppercase;
color:var(–pink-deep);padding:1rem 1rem .3rem;font-weight:600;}
.cbody{padding:0 1rem 1rem;}
.cname{font-family:‘Playfair Display’,serif;font-size:1.05rem;
font-weight:700;margin-bottom:.35rem;line-height:1.3;}
.cdesc{font-size:.82rem;color:var(–gray);line-height:1.55;margin-bottom:.6rem;}
.ccolors{display:flex;gap:5px;flex-wrap:wrap;margin-bottom:.2rem;}
.cswatch{width:18px;height:18px;border-radius:50%;border:2px solid rgba(0,0,0,.1);}

.cfoot{display:flex;align-items:center;justify-content:space-between;
padding:.8rem 1rem;border-top:1px solid var(–border);background:#FFF8FA;}
.cprice{font-family:‘Playfair Display’,serif;font-size:1.1rem;
font-weight:700;color:var(–pink-dark);}
.cprice .cur{font-family:‘DM Sans’,sans-serif;font-size:.68rem;color:var(–gray);margin-right:2px;}
.order-btn{background:var(–black);color:#fff;border:none;padding:8px 16px;
font-size:.72rem;letter-spacing:.8px;text-transform:uppercase;
font-family:‘DM Sans’,sans-serif;font-weight:500;border-radius:30px;
cursor:pointer;text-decoration:none;display:inline-flex;align-items:center;
gap:4px;transition:background .2s;}
.order-btn:hover{background:var(–pink-dark);}

.empty-store{text-align:center;padding:5rem 2rem;color:var(–gray);grid-column:1/-1;}
.empty-store .ei{font-size:3rem;margin-bottom:1rem;opacity:.4;display:block;}
.empty-store h3{font-family:‘Playfair Display’,serif;font-size:1.4rem;margin-bottom:.5rem;}
.empty-store p{font-size:.88rem;}

/* ── BANNER ── */
.banner{background:var(–black);color:#fff;border-radius:14px;padding:2rem 2.5rem;
margin-top:3rem;display:flex;align-items:center;justify-content:space-between;
flex-wrap:wrap;gap:1rem;border-left:5px solid var(–pink-deep);}
.banner h3{font-family:‘Playfair Display’,serif;font-size:1.4rem;margin-bottom:.3rem;}
.banner p{color:rgba(255,255,255,.5);font-size:.88rem;}
.wa-btn{background:#25D366;color:#fff;border:none;padding:12px 24px;
font-family:‘DM Sans’,sans-serif;font-size:.85rem;font-weight:600;border-radius:30px;
cursor:pointer;text-decoration:none;display:inline-flex;align-items:center;
gap:8px;white-space:nowrap;transition:opacity .2s,transform .15s;}
.wa-btn:hover{opacity:.9;transform:scale(1.02);}

/* ── FOOTER ── */
footer{background:var(–black);color:var(–gray);text-align:center;padding:2rem;
font-size:.8rem;margin-top:4rem;border-top:2px solid var(–pink-deep);}
footer strong{color:var(–pink-deep);font-family:‘Playfair Display’,serif;}

/* ── TOAST ── */
.toast{position:fixed;bottom:2rem;right:2rem;background:var(–black);color:#fff;
padding:12px 22px;border-radius:30px;border-left:3px solid var(–pink-deep);
font-size:.85rem;z-index:999;opacity:0;transform:translateY(10px);
transition:all .3s;pointer-events:none;}
.toast.on{opacity:1;transform:translateY(0);}

@media(max-width:640px){
.mrow{grid-template-columns:42px 1fr auto;}
.mprice,.stoggle{display:none;}
.banner{flex-direction:column;text-align:center;}
.hero h1{font-size:2.1rem;}
.fgrid{grid-template-columns:1fr;}
.fgrid .full{grid-column:1;}
.stats{gap:1rem;}
}
</style>

</head>
<body>

<!-- HEADER -->

<header>
  <div class="logo">Style <span>Up</span></div>
  <div class="header-right">
    <a class="phone-badge" href="https://wa.me/233257176771" target="_blank">📞 +233 25 717 6771</a>
    <button class="admin-btn" id="adminBtn" onclick="toggleAdmin()">⚙ Admin</button>
  </div>
</header>

<!-- HERO -->

<section class="hero">
  <p class="hero-tag">✦ New Collection Available ✦</p>
  <h1>Dress to <em>Impress.</em><br>Shop Style Up.</h1>
  <p>Premium clothes, bags & accessories — handpicked for every occasion.</p>
</section>

<!-- STORE FILTER TABS -->

<div class="store-tabs">
  <button class="stab on"  onclick="storeFilter('all',this)">All Items</button>
  <button class="stab"     onclick="storeFilter('clothes',this)">Clothes</button>
  <button class="stab"     onclick="storeFilter('bags',this)">Bags</button>
  <button class="stab"     onclick="storeFilter('accessories',this)">Accessories</button>
  <button class="stab"     onclick="storeFilter('shoes',this)">Shoes</button>
  <button class="stab"     onclick="storeFilter('other',this)">Others</button>
</div>

<main>

  <!-- ═══ ADMIN PANEL ═══ -->

  <div class="admin-panel" id="adminPanel">

```
<div class="ap-head">
  <div>
    <h2>🌸 Admin Dashboard</h2>
    <p>Post new products or manage existing listings.</p>
  </div>
  <div class="stats">
    <div class="stat"><b id="sTotal">0</b><s2>Total</s2></div>
    <div class="stat"><b id="sIn">0</b><s2>In Stock</s2></div>
    <div class="stat"><b id="sOut">0</b><s2>Sold Out</s2></div>
  </div>
</div>

<div class="ap-body">

  <!-- Inner tabs -->
  <div class="ap-tabs">
    <button class="aptab on" id="t1" onclick="switchTab('post')">✦ Post Product</button>
    <button class="aptab"    id="t2" onclick="switchTab('manage')">📋 Manage</button>
  </div>

  <!-- POST SECTION -->
  <div class="ap-section on" id="secPost">
    <div class="post-wrap">

      <!-- Live preview -->
      <div class="preview-card">
        <div class="prev-icon" id="pvIcon">🛍️</div>
        <div class="prev-info">
          <div class="pv-name"  id="pvName">Product name will appear here</div>
          <div class="pv-meta"  id="pvMeta">Category · Availability</div>
          <div class="pv-price" id="pvPrice">GHS —</div>
          <div class="pv-colors" id="pvColors"></div>
        </div>
      </div>

      <div class="fgrid">
        <div class="fg full">
          <label>Product Name *</label>
          <input type="text" id="pName" placeholder="e.g. Floral Midi Dress" oninput="livePreview()">
        </div>
        <div class="fg">
          <label>Category *</label>
          <select id="pCat" onchange="livePreview()">
            <option value="clothes">👗 Clothes</option>
            <option value="bags">👜 Bags</option>
            <option value="accessories">💍 Accessories</option>
            <option value="shoes">👠 Shoes</option>
            <option value="other">🛍️ Other</option>
          </select>
        </div>
        <div class="fg">
          <label>Price (GHS) *</label>
          <input type="number" id="pPrice" placeholder="e.g. 150" oninput="livePreview()">
        </div>
        <div class="fg full">
          <label>Product Image</label>
          <div class="img-drop-zone" id="imgDropZone"
            onclick="document.getElementById('imgFileInput').click()"
            ondragover="dzDragOver(event)"
            ondragleave="dzDragLeave(event)"
            ondrop="dzDrop(event)">
            <input type="file" id="imgFileInput" accept="image/*" style="display:none" onchange="dzFileChange(event)">
            <div class="dz-idle" id="dzIdle">
              <span class="dz-icon">🖼️</span>
              <p class="dz-main">Drop image here, click to browse,<br>or paste from clipboard</p>
              <p class="dz-sub">JPG · PNG · WEBP · GIF</p>
            </div>
            <div class="dz-preview" id="dzPreview" style="display:none">
              <img id="dzImg" src="" alt="Preview">
              <button class="dz-remove" onclick="removeImg(event)" title="Remove image">✕ Remove</button>
            </div>
          </div>
        </div>
        <div class="fg">
          <label>Availability</label>
          <select id="pStatus" onchange="livePreview()">
            <option value="available">✓ In Stock</option>
            <option value="sold">✕ Sold Out</option>
          </select>
        </div>

        <!-- COLOR FIELD -->
        <div class="fg full">
          <label>Available Colours</label>
          <div class="color-row">
            <input type="color" id="colorPicker" value="#E8869F" title="Pick a colour">
            <button class="add-color-btn" onclick="addColor()">+ Add Colour</button>
            <div class="color-chips" id="colorChips"></div>
          </div>
        </div>

        <div class="fg full">
          <label>Description</label>
          <textarea id="pDesc" placeholder="Brief description of the product..."></textarea>
        </div>
      </div>

      <div class="form-actions">
        <button class="btn-post"  onclick="postProduct()">🌸 Post Product</button>
        <button class="btn-clear" onclick="clearForm()">Clear</button>
      </div>

    </div>
  </div><!-- end secPost -->

  <!-- MANAGE SECTION -->
  <div class="ap-section" id="secManage">
    <div class="manage-toolbar">
      <div class="msearch">
        <span class="si">🔍</span>
        <input type="text" id="msInput" placeholder="Search products..." oninput="renderList()">
      </div>
      <div class="mfilters">
        <button class="mfbtn on" onclick="setMFilter('all',this)">All</button>
        <button class="mfbtn"    onclick="setMFilter('available',this)">In Stock</button>
        <button class="mfbtn"    onclick="setMFilter('sold',this)">Sold Out</button>
      </div>
    </div>
    <div class="manage-list" id="manageList"></div>
    <div class="ap-note">💡 Click the stock badge to toggle availability. Use ✕ to remove.</div>
  </div><!-- end secManage -->

</div>
```

  </div>
  <!-- ═══ END ADMIN PANEL ═══ -->

  <!-- STORE -->

  <div class="sec-head">
    <h2 id="secTitle">All Products</h2>
    <span class="cpill" id="cPill">0 items</span>
  </div>
  <div class="pgrid" id="pgrid"></div>

  <!-- BANNER -->

  <div class="banner">
    <div>
      <h3>Ready to Order?</h3>
      <p>WhatsApp us to place your order, ask about sizes, or get styling advice.</p>
    </div>
    <a class="wa-btn" href="https://wa.me/233257176771" target="_blank">💬 WhatsApp Us Now</a>
  </div>

</main>

<footer>
  <strong>Style Up</strong> &nbsp;·&nbsp; Premium Fashion &amp; Accessories &nbsp;·&nbsp; +233 25 717 6771
</footer>

<div class="toast" id="toast"></div>

<script>
/* ────────────────────────────────────────────────
   STATE
──────────────────────────────────────────────── */
const PHONE   = '233257176771';
let products  = [];          // starts EMPTY — admin fills it
let pendingColors = [];      // colours added to current form
let curStoreFilter = 'all';
let curMFilter     = 'all';

const emojiMap = { clothes:'👗', bags:'👜', accessories:'💍', shoes:'👠', other:'🛍️' };

/* ────────────────────────────────────────────────
   ADMIN PANEL OPEN/CLOSE
──────────────────────────────────────────────── */
function toggleAdmin(){
  const panel = document.getElementById('adminPanel');
  const btn   = document.getElementById('adminBtn');
  const open  = !panel.classList.contains('open');
  panel.classList.toggle('open', open);
  btn.classList.toggle('on', open);
  if(open){ refreshStats(); renderList(); livePreview(); }
}

/* ────────────────────────────────────────────────
   INNER TAB SWITCH
──────────────────────────────────────────────── */
function switchTab(tab){
  document.getElementById('t1').classList.toggle('on', tab==='post');
  document.getElementById('t2').classList.toggle('on', tab==='manage');
  document.getElementById('secPost').classList.toggle('on', tab==='post');
  document.getElementById('secManage').classList.toggle('on', tab==='manage');
  if(tab==='manage') renderList();
}

/* ────────────────────────────────────────────────
   COLOUR LOGIC
──────────────────────────────────────────────── */
function addColor(){
  const hex = document.getElementById('colorPicker').value;
  if(pendingColors.includes(hex)){ toast('Colour already added.'); return; }
  if(pendingColors.length >= 10){ toast('Max 10 colours per product.'); return; }
  pendingColors.push(hex);
  renderChips();
  livePreview();
}

function removeColor(hex){
  pendingColors = pendingColors.filter(c=>c!==hex);
  renderChips();
  livePreview();
}

function renderChips(){
  const wrap = document.getElementById('colorChips');
  wrap.innerHTML = pendingColors.map(c=>`
    <div class="chip" style="background:${c}" title="${c}">
      <button class="remove-chip" onclick="removeColor('${c}')">✕</button>
    </div>
  `).join('');
}

/* ────────────────────────────────────────────────
   LIVE PREVIEW
──────────────────────────────────────────────── */
function livePreview(){
  const name   = document.getElementById('pName').value.trim();
  const price  = document.getElementById('pPrice').value;
  const cat    = document.getElementById('pCat').value;
  const status = document.getElementById('pStatus').value;

  const pvIcon = document.getElementById('pvIcon');
  if(pendingImgDataUrl){
    pvIcon.innerHTML = `<img src="${pendingImgDataUrl}" style="width:100%;height:100%;object-fit:cover;border-radius:10px;">`;
  } else {
    pvIcon.textContent = emojiMap[cat]||'🛍️';
  }
  document.getElementById('pvName').textContent  = name  || 'Product name will appear here';
  document.getElementById('pvMeta').textContent  = `${cat} · ${status==='available'?'In Stock':'Sold Out'}`;
  document.getElementById('pvPrice').textContent = price ? `GHS ${Number(price).toLocaleString()}` : 'GHS —';

  const pvColors = document.getElementById('pvColors');
  pvColors.innerHTML = pendingColors.map(c=>
    `<div class="pv-swatch" style="background:${c}"></div>`
  ).join('');
}

/* ────────────────────────────────────────────────
   CLEAR FORM
──────────────────────────────────────────────── */
function clearForm(){
  ['pName','pPrice','pDesc'].forEach(id=>document.getElementById(id).value='');
  document.getElementById('pCat').value    = 'clothes';
  document.getElementById('pStatus').value = 'available';
  pendingColors = [];
  renderChips();
  // reset image zone
  pendingImgDataUrl = '';
  document.getElementById('dzImg').src = '';
  document.getElementById('dzPreview').style.display = 'none';
  document.getElementById('dzIdle').style.display    = 'block';
  document.getElementById('imgFileInput').value = '';
  livePreview();
}

/* ────────────────────────────────────────────────
   POST PRODUCT
──────────────────────────────────────────────── */
function postProduct(){
  const name   = document.getElementById('pName').value.trim();
  const price  = parseFloat(document.getElementById('pPrice').value);
  const cat    = document.getElementById('pCat').value;
  const desc   = document.getElementById('pDesc').value.trim();
  const img    = pendingImgDataUrl;
  const status = document.getElementById('pStatus').value;

  if(!name)           { toast('⚠ Please enter a product name.'); return; }
  if(!price||price<=0){ toast('⚠ Please enter a valid price.');  return; }

  products.unshift({
    id: Date.now(),
    name, cat, price,
    desc: desc || 'Quality product from Style Up.',
    status, img,
    colors: [...pendingColors]
  });

  refreshStats();
  renderGrid();
  toast(`🌸 "${name}" posted to the store!`);
  clearForm();
}

/* ────────────────────────────────────────────────
   STATS
──────────────────────────────────────────────── */
function refreshStats(){
  document.getElementById('sTotal').textContent = products.length;
  document.getElementById('sIn').textContent    = products.filter(p=>p.status==='available').length;
  document.getElementById('sOut').textContent   = products.filter(p=>p.status==='sold').length;
}

/* ────────────────────────────────────────────────
   MANAGE FILTER
──────────────────────────────────────────────── */
function setMFilter(f,el){
  curMFilter = f;
  document.querySelectorAll('.mfbtn').forEach(b=>b.classList.remove('on'));
  el.classList.add('on');
  renderList();
}

/* ────────────────────────────────────────────────
   RENDER ADMIN LIST
──────────────────────────────────────────────── */
function renderList(){
  const inp = document.getElementById('msInput');
  const q   = inp ? inp.value.toLowerCase() : '';
  const list = products.filter(p=>{
    const mf = curMFilter==='all' || p.status===curMFilter;
    const mq = p.name.toLowerCase().includes(q) || p.cat.includes(q);
    return mf && mq;
  });

  const el = document.getElementById('manageList');
  if(!el) return;

  if(!list.length){
    el.innerHTML = `<div class="m-empty"><span class="ei">${products.length?'🔍':'📦'}</span>
      <p>${products.length?'No products match.':'No products yet — post one!'}</p></div>`;
    return;
  }

  el.innerHTML = list.map((p,i)=>`
    <div class="mrow" style="animation-delay:${i*.04}s">
      <div class="mrow-icon">${emojiMap[p.cat]||'🛍️'}</div>
      <div>
        <div class="mrow-name">${p.name}</div>
        <div class="mrow-meta"><span>${p.cat}</span></div>
        ${p.colors&&p.colors.length?`<div class="mrow-colors">${p.colors.map(c=>`<div class="mrow-swatch" style="background:${c}"></div>`).join('')}</div>`:''}
      </div>
      <div class="mprice"><small>GHS</small> ${Number(p.price).toLocaleString()}</div>
      <button class="stoggle ${p.status==='available'?'in':'out'}" onclick="toggleStatus(${p.id})">
        ${p.status==='available'?'✓ In Stock':'✕ Sold Out'}
      </button>
      <button class="del-btn" onclick="delProduct(${p.id})">✕</button>
    </div>
  `).join('');
}

/* ────────────────────────────────────────────────
   TOGGLE STATUS
──────────────────────────────────────────────── */
function toggleStatus(id){
  const p = products.find(x=>x.id===id);
  if(!p) return;
  p.status = p.status==='available'?'sold':'available';
  refreshStats(); renderList(); renderGrid();
  toast(`✓ "${p.name}" → ${p.status==='available'?'In Stock':'Sold Out'}`);
}

/* ────────────────────────────────────────────────
   DELETE
──────────────────────────────────────────────── */
function delProduct(id){
  const p = products.find(x=>x.id===id);
  if(!p||!confirm(`Remove "${p.name}" from the store?`)) return;
  products = products.filter(x=>x.id!==id);
  refreshStats(); renderList(); renderGrid();
  toast(`✓ "${p.name}" removed.`);
}

/* ────────────────────────────────────────────────
   STORE FILTER TABS
──────────────────────────────────────────────── */
function storeFilter(f,el){
  curStoreFilter = f;
  document.querySelectorAll('.stab').forEach(t=>t.classList.remove('on'));
  el.classList.add('on');
  const labels={all:'All Products',clothes:'Clothes',bags:'Bags',
    accessories:'Accessories',shoes:'Shoes',other:'Other Items'};
  document.getElementById('secTitle').textContent = labels[f]||'Products';
  renderGrid();
}

/* ────────────────────────────────────────────────
   RENDER STORE GRID
──────────────────────────────────────────────── */
function renderGrid(){
  const grid     = document.getElementById('pgrid');
  const filtered = curStoreFilter==='all'
    ? products
    : products.filter(p=>p.cat===curStoreFilter);

  document.getElementById('cPill').textContent =
    `${filtered.length} item${filtered.length!==1?'s':''}`;

  if(!filtered.length){
    grid.innerHTML = `
      <div class="empty-store">
        <span class="ei">🛍️</span>
        <h3>No products yet</h3>
        <p>New arrivals coming soon — check back later!</p>
      </div>`;
    return;
  }

  grid.innerHTML = filtered.map((p,i)=>`
    <div class="pcard" style="animation-delay:${i*.06}s">
      <div class="cimg">
        ${p.img?`<img src="${p.img}" alt="${p.name}" onerror="this.style.display='none'">`: ''}
        <span class="cemoji">${emojiMap[p.cat]||'🛍️'}</span>
        <span class="sbadge ${p.status==='sold'?'sold':''}">${p.status==='sold'?'Sold Out':'In Stock'}</span>
      </div>
      <div class="ccat">${p.cat}</div>
      <div class="cbody">
        <div class="cname">${p.name}</div>
        <div class="cdesc">${p.desc}</div>
        ${p.colors&&p.colors.length?`
          <div class="ccolors">
            ${p.colors.map(c=>`<div class="cswatch" style="background:${c}" title="${c}"></div>`).join('')}
          </div>`:''
        }
      </div>
      <div class="cfoot">
        <div class="cprice"><span class="cur">GHS</span>${Number(p.price).toLocaleString()}</div>
        <a class="order-btn"
          href="https://wa.me/${PHONE}?text=Hi%20Style%20Up!%20I%27m%20interested%20in%20*${encodeURIComponent(p.name)}*%20(GHS%20${p.price}).%20Is%20it%20available%3F"
          target="_blank">Order ↗</a>
      </div>
    </div>
  `).join('');
}

/* ────────────────────────────────────────────────
   TOAST
──────────────────────────────────────────────── */
function toast(msg){
  const t=document.getElementById('toast');
  t.textContent=msg; t.classList.add('on');
  setTimeout(()=>t.classList.remove('on'),3000);
}

/* ────────────────────────────────────────────────
   IMAGE DROP ZONE
──────────────────────────────────────────────── */
let pendingImgDataUrl = ''; // base64 data URL of chosen image

function dzDragOver(e){
  e.preventDefault();
  document.getElementById('imgDropZone').classList.add('drag-over');
}
function dzDragLeave(e){
  document.getElementById('imgDropZone').classList.remove('drag-over');
}
function dzDrop(e){
  e.preventDefault();
  document.getElementById('imgDropZone').classList.remove('drag-over');
  const file = e.dataTransfer.files[0];
  if(file && file.type.startsWith('image/')) loadImgFile(file);
}
function dzFileChange(e){
  const file = e.target.files[0];
  if(file) loadImgFile(file);
}
function loadImgFile(file){
  const reader = new FileReader();
  reader.onload = ev => showDzPreview(ev.target.result);
  reader.readAsDataURL(file);
}
function showDzPreview(src){
  pendingImgDataUrl = src;
  document.getElementById('dzImg').src = src;
  document.getElementById('dzIdle').style.display    = 'none';
  document.getElementById('dzPreview').style.display = 'flex';
  livePreview();
}
function removeImg(e){
  e.stopPropagation();
  pendingImgDataUrl = '';
  document.getElementById('dzImg').src = '';
  document.getElementById('dzPreview').style.display = 'none';
  document.getElementById('dzIdle').style.display    = 'block';
  document.getElementById('imgFileInput').value = '';
  livePreview();
}
// Paste from clipboard anywhere on the page
document.addEventListener('paste', e => {
  const items = e.clipboardData && e.clipboardData.items;
  if(!items) return;
  for(const item of items){
    if(item.type.startsWith('image/')){
      const file = item.getAsFile();
      if(file){ loadImgFile(file); break; }
    }
  }
});

/* INIT — empty store, waiting for admin */
renderGrid();
</script>

</body>
</html>
