<!doctype html>
<html lang="fr">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>The Girls’ Corner — boutique</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#f9f5f9;
  --card:#fff0f6;
  --text:#111;
  --muted:#666;
  --rose:#f4c2d1;
  --glitter:#ffd1dc;
  --accent:linear-gradient(135deg,var(--rose),var(--glitter));
  --shadow:0 8px 24px rgba(0,0,0,0.2);
}
*{box-sizing:border-box}
body{margin:0;padding:20px;font-family:Inter,system-ui,Segoe UI,Roboto,Arial;color:var(--text);background:var(--bg);}
header{display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;margin-bottom:20px;}
.brand h1{margin:0;}
.brand .tag{color:var(--muted);font-size:14px;}
.btn{padding:8px 12px;border-radius:10px;border:none;background:var(--accent);color:#111;font-weight:700;cursor:pointer;}
.container{display:flex;gap:20px;flex-wrap:wrap;}
.products{flex:2;display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:16px;}
.card{background:var(--card);padding:12px;border-radius:12px;box-shadow:var(--shadow);display:flex;flex-direction:column;align-items:center;text-align:center;}
.card img{width:100%;height:180px;object-fit:cover;border-radius:10px;}
.card h3{margin:10px 0 5px;}
.card .price{font-weight:800;color:var(--glitter);}
.card .desc{font-size:13px;color:var(--muted);}
.sidebar{flex:1;min-width:280px;background:#fff0f6;padding:14px;border-radius:12px;box-shadow:var(--shadow);}
.cart-list{display:flex;flex-direction:column;gap:10px;margin-top:10px;}
.cart-item{display:flex;gap:10px;align-items:center;}
.cart-item img{width:50px;height:50px;object-fit:cover;border-radius:8px;}
.total{font-weight:800;color:var(--glitter);margin-top:10px;}
.checkout{width:100%;padding:10px;border-radius:10px;border:none;background:var(--glitter);color:#111;font-weight:800;cursor:pointer;margin-top:10px;}
.modal{position:fixed;inset:0;display:flex;align-items:center;justify-content:center;background:rgba(0,0,0,0.5);visibility:hidden;opacity:0;transition:opacity .15s;}
.modal.open{visibility:visible;opacity:1;}
.modal-card{background:#fff0f6;padding:16px;border-radius:12px;max-width:600px;width:90%;box-shadow:var(--shadow);}
.modal-card img{width:100%;border-radius:10px;margin-bottom:10px;}
.close{background:transparent;border:none;color:#111;font-size:18px;cursor:pointer;position:absolute;top:12px;right:20px;}
.gallery{display:flex;flex-wrap:wrap;gap:10px;margin-top:10px;}
.gallery img{width:80px;height:80px;object-fit:cover;border-radius:8px;cursor:pointer;border:2px solid transparent;}
.gallery img.selected{border-color:var(--glitter);}
footer{text-align:center;margin-top:30px;color:var(--muted);font-size:13px;}
</style>
</head>
<body>

<header>
  <div class="brand">
    <h1>The Girls’ Corner</h1>
    <div class="tag">Bienvenue les queens — ici, on célèbre la beauté, la confiance et le plaisir 💋</div>
  </div>
  <div>
    <button class="btn" id="add-product-btn">Ajouter un article</button>
    <button class="btn" id="toggle-cart">Panier (<span id="cart-count">0</span>)</button>
  </div>
</header>

<div class="container">
  <div class="products" id="grid">
    <!-- produits -->
  </div>
  <div class="sidebar">
    <h3>Panier</h3>
    <div id="cart-empty">Ton panier est vide.</div>
    <div class="cart-list" id="cart-list"></div>
    <div class="total" id="cart-total">Total: 0 FC</div>
    <button class="checkout" id="checkout" disabled>Commander</button>
    <div class="small" style="margin-top:10px">Contact: <a href="mailto:mutulayuni@gmail.com">mutulayuni@gmail.com</a></div>
    <div class="small" style="margin-top:6px">By the queen Yuni</div>
  </div>
</div>

<!-- Modal ajout produit -->
<div id="admin-modal" class="modal">
  <div class="modal-card" style="position:relative;">
    <button class="close" id="admin-close">✕</button>
    <div id="admin-step-password">
      <input id="admin-password" placeholder="Mot de passe" style="width:100%;padding:8px;border-radius:8px;margin-bottom:10px;"/>
      <button class="btn" id="admin-pass-submit">Valider</button>
      <div id="admin-pass-feedback" style="color:red;margin-top:6px;display:none;">Mot de passe incorrect</div>
    </div>
    <div id="admin-form" style="display:none;">
      <input id="new-title" placeholder="Titre du produit" style="width:100%;padding:8px;margin-bottom:6px;"/>
      <input id="new-price" type="number" placeholder="Prix en FC" style="width:100%;padding:8px;margin-bottom:6px;"/>
      <input id="new-short" placeholder="Description courte" style="width:100%;padding:8px;margin-bottom:6px;"/>
      <textarea id="new-details" placeholder="Détails" style="width:100%;padding:8px;margin-bottom:6px;"></textarea>
      <input id="new-image" type="file" accept="image/*" style="margin-bottom:10px;"/>
      <button class="btn" id="admin-add-submit">Ajouter le produit</button>
    </div>
  </div>
</div>

<footer>
  © 2025 The Girls’ Corner
</footer>

<script>
// Storage
let products = [];
let cart = [];
const STORAGE_PRODUCTS='tg_products',STORAGE_CART='tg_cart',PASSWORD='bijouxyumba';

function saveProducts(){localStorage.setItem(STORAGE_PRODUCTS,JSON.stringify(products));}
function saveCart(){localStorage.setItem(STORAGE_CART,JSON.stringify(cart));}

// Charger
function loadProducts(){const p=localStorage.getItem(STORAGE_PRODUCTS);return p?JSON.parse(p):[];}
function loadCart(){const c=localStorage.getItem(STORAGE_CART);return c?JSON.parse(c):[];}

// Init
products=loadProducts();cart=loadCart();renderProducts();renderCart();

// Rendu
function renderProducts(){
  const grid=document.getElementById('grid');grid.innerHTML='';
  products.forEach(p=>{
    const card=document.createElement('div');card.className='card';
    card.innerHTML=`<img src="${p.img}" alt="${p.title}"><h3>${p.title}</h3><div class="price">${p.price} FC</div><div class="desc">${p.short||''}</div><button class="btn" data-id="${p.id}">Ajouter au panier</button>`;
    grid.appendChild(card);
  });
}

function renderCart(){
  const list=document.getElementById('cart-list');const empty=document.getElementById('cart-empty');const total=document.getElementById('cart-total');
  list.innerHTML='';if(cart.length===0){empty.style.display='block';total.textContent='Total: 0 FC';return;}empty.style.display='none';
  let sum=0;cart.forEach(c=>{
    sum+=c.price*c.qty;c.qty=c.qty||1;
    const el=document.createElement('div');el.className='cart-item';
    el.innerHTML=`<img src="${c.img}"><div>${c.title} x${c.qty}</div><div>${c.price*c.qty} FC</div>`;
    list.appendChild(el);
  });
  total.textContent='Total: '+sum+' FC';
}

// Ajouter produit
document.getElementById('grid').addEventListener('click',e=>{
  const btn=e.target.closest('button');if(!btn)return;
  const id=Number(btn.dataset.id);const p=products.find(x=>x.id===id);if(!p)return;
  const exist=cart.find(x=>x.id===id);if(exist)exist.qty++;else cart.push({...p,qty:1});
  saveCart();renderCart();alert('Produit ajouté au panier !');
});

// Modal admin
const modal=document.getElementById('admin-modal');
document.getElementById('add-product-btn').onclick=()=>modal.classList.add('open');
document.getElementById('admin-close').onclick=()=>{modal.classList.remove('open');document.getElementById('admin-step-password').style.display='block';document.getElementById('admin-form').style.display='none';};
document.getElementById('admin-pass-submit').onclick=()=>{
  const pass=document.getElementById('admin-password').value;
  if(pass===PASSWORD){document.getElementById('admin-step-password').style.display='none';document.getElementById('admin-form').style.display='block';document.getElementById('admin-pass-feedback').style.display='none';}
  else{document.getElementById('admin-pass-feedback').style.display='block';}
};

// Ajouter produit admin
document.getElementById('admin-add-submit').onclick=()=>{
  const title=document.getElementById('new-title').value;
  const price=Number(document.getElementById('new-price').value);
  const short=document.getElementById('new-short').value;
  const details=document.getElementById('new-details').value;
  const file=document.getElementById('new-image').files[0];
  if(!title||!price||!file){alert('Remplis tous les champs !');return;}
  const reader=new FileReader();
  reader.onload=()=>{const id=products.length?products[products.length-1].id+1:1;products.push({id,title,price,short,details,img:reader.result});saveProducts();renderProducts();modal.classList.remove('open');};
  reader.readAsDataURL(file);
};

// Checkout simulation
document.getElementById('checkout').onclick=()=>{
  let sum=cart.reduce((a,b)=>a+b.price*b.qty,0);
  let notif='Paiement simulé : merci pour votre achat !';
  if(sum>100000){notif+=' Réduction de 5% appliquée sur ton prochain panier !';}
  alert(notif);cart=[];saveCart();renderCart();
};

</script>

</body>
</html>
