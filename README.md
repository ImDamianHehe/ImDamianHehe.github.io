<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Aura Craft — Minecraft Store</title>

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Rajdhani:wght@400;600;700&display=swap" rel="stylesheet">

<style>
:root {
    --bg:#050814;
    --panel:#0c1528;
    --panel2:#111d35;
    --cyan:#00f7ff;
    --purple:#8a5cff;
    --white:#eafcff;
    --muted:#8aa4b8;
    --border:rgba(0,247,255,.25);
    --danger:#ff4c6d;
}
* {
    margin:0;
    padding:0;
    box-sizing:border-box;
}
html {
    scroll-behavior:smooth;
}
body {
    background:
    radial-gradient(
        circle at top,
        #172b55,
        #050814 60%
    );
    color:var(--white);
    font-family:
    "Rajdhani",
    sans-serif;
    min-height:100vh;
    overflow-x:hidden;
}
.cyber-grid {
    position:fixed;
    inset:0;
    z-index:-1;
    background-image:
    linear-gradient(
        rgba(0,247,255,.06) 1px,
        transparent 1px
    ),
    linear-gradient(
        90deg,
        rgba(0,247,255,.06) 1px,
        transparent 1px
    );
    background-size:
    45px 45px;
    animation:
    gridMove 12s linear infinite;
}
@keyframes gridMove {
    from {
        background-position:
        0 0;
    }
    to {
        background-position:
        0 45px;
    }
}
h1,
h2,
h3,
button,
.logo {
    font-family:
    "Orbitron",
    sans-serif;
    letter-spacing:
    .08em;
}
p {
    color:
    var(--muted);
}
section {
    width:100%;
    max-width:1100px;
    margin:auto;
    padding:
    5rem 1.5rem;
}
.divider {
    height:1px;
    background:
    linear-gradient(
        90deg,
        transparent,
        var(--cyan),
        transparent
    );
    opacity:.5;
}
::-webkit-scrollbar {
    width:10px;
}
::-webkit-scrollbar-track {
    background:
    var(--bg);
}
::-webkit-scrollbar-thumb {
    background:
    linear-gradient(
        var(--cyan),
        var(--purple)
    );
}
.btn {
    display:inline-block;
    padding:
    .85rem 2.5rem;
    margin:
    .5rem;
    text-decoration:none;
    cursor:pointer;
    font-family:
    "Orbitron",
    sans-serif;
    color:
    var(--cyan);
    border:
    1px solid var(--cyan);
    background:
    rgba(0,247,255,.05);
    position:relative;
    overflow:hidden;
    transition:
    .3s;
}
.btn:hover {
    background:
    var(--cyan);
    color:
    #001015;
    box-shadow:
    0 0 15px var(--cyan),
    0 0 45px rgba(0,247,255,.5);
    transform:
    translateY(-3px);
}
nav {
    position:fixed;
    top:0;
    left:0;
    right:0;
    z-index:100;
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:
    1.2rem 2rem;
    background:
    rgba(5,8,20,.75);
    backdrop-filter:
    blur(15px);
    border-bottom:
    1px solid var(--border);
}
.logo {
    text-decoration:none;
    color:
    var(--cyan);
    font-size:
    1.4rem;
    text-shadow:
    0 0 15px var(--cyan);
}
.nav-links {
    display:flex;
    gap:2rem;
    list-style:none;
}
.nav-links a {
    text-decoration:none;
    color:
    var(--muted);
    font-family:
    "Orbitron",
    sans-serif;
    font-size:
    .75rem;
    transition:
    .3s;
}
.nav-links a:hover {
    color:
    var(--cyan);
    text-shadow:
    0 0 10px var(--cyan);
}
.hero {
    min-height:
    100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:
    2rem;
}
.hero-content {
    max-width:
    900px;
}
.hero-tag {
    color:
    var(--cyan);
    font-family:
    "Orbitron",
    sans-serif;
    font-size:
    .8rem;
    letter-spacing:
    .35em;
    margin-bottom:
    1.5rem;
}
.hero h1 {
    font-size:
    clamp(
        3rem,
        12vw,
        8rem
    );
    line-height:
    .9;
    color:
    var(--white);
}
.hero h1 span {
    display:block;
    color:
    var(--cyan);
    text-shadow:
    0 0 15px var(--cyan),
    0 0 50px rgba(0,247,255,.5);
}
.hero-description {
    max-width:
    550px;
    margin:
    1.5rem auto;
    font-size:
    1.2rem;
}
.hero-buttons {
    margin-top:
    2rem;
}
</style>
</head>
<body>
<div class="cyber-grid"></div>
<nav>
    <a href="#" class="logo">
        ⚡ AURA CRAFT
    </a>
    <ul class="nav-links">
        <li>
            <a href="#products">
                Products
            </a>
        </li>
        <li>
            <a href="#how">
                How It Works
            </a>
        </li>
        <li>
            <a href="#order">
                Order
            </a>
        </li>
    </ul>
</nav>
<section class="hero">
<div class="hero-content">
<p class="hero-tag">

// CUSTOM ITEMS MINECRAFT STORE //
</p>
<h1>
AURA
<span>
CRAFT
</span>
</h1>
<p class="hero-description">
Upgrade your Minecraft experience with
ranks and custom prefixes.

</p>
<div class="hero-buttons">
<a href="#products" class="btn">
VIEW PRODUCTS
</a>
<a href="#order" class="btn">

PLACE ORDER
</a>
</div>
</div>
</section>
<div class="divider"></div>
<style>
.section-label {
    font-family:
    "Orbitron",
    sans-serif;
    font-size:
    .75rem;
    letter-spacing:
    .3em;
    color:
    var(--cyan);
    margin-bottom:
    .8rem;
}
.section-title {
    font-size:
    clamp(
        2rem,
        6vw,
        3.5rem
    );
    color:
    var(--white);
    margin-bottom:
    1rem;
}
.section-description {
    max-width:
    550px;
}
.products-grid {
    display:grid;
    grid-template-columns:
    repeat(
        auto-fit,
        minmax(
            230px,
            1fr
        )
    );
    gap:
    1.5rem;
    margin-top:
    3rem;
}
.product-card {
    background:
    rgba(
        13,
        22,
        40,
        .85
    );
    border:
    1px solid var(--border);
    padding:
    2rem 1.5rem;
    backdrop-filter:
    blur(15px);
    position:
    relative;
    transition:
    .35s;
}
.product-card:hover {
    transform:
    translateY(-8px);
    border-color:
    var(--cyan);
    box-shadow:
    0 0 25px rgba(0,247,255,.35),
    inset 0 0 20px rgba(0,247,255,.05);
}
.product-card.featured {
    border-color:
    var(--purple);
    box-shadow:
    0 0 30px rgba(138,92,255,.35);
}
.featured-tag {
    position:absolute;
    top:0;
    right:0;
    padding:
    .4rem 1rem;
    background:
    var(--purple);
    color:white;
    font-family:
    "Orbitron";
    font-size:
    .65rem;
}
.product-icon {
    font-size:
    2.5rem;
    margin-bottom:
    1rem;
}
.product-name {
    font-family:
    "Orbitron";
    font-size:
    1.25rem;
    color:
    var(--white);
}
.product-time {
    color:
    var(--cyan);
    font-family:
    "Orbitron";
    font-size:
    .75rem;
    margin:
    .5rem 0 1rem;
}
.product-price {
    font-family:
    "Orbitron";
    font-size:
    2.5rem;
    color:
    var(--cyan);
    text-shadow:
    0 0 15px var(--cyan);
}
.product-list {
    list-style:none;
    margin:
    1.2rem 0;
    color:
    var(--muted);
}
.product-list li {
    padding:
    .35rem 0;
}
.product-list li::before {
    content:
    ">> ";
    color:
    var(--cyan);
}
.product-button {
    width:
    100%;
    padding:
    .85rem;
    cursor:pointer;
    background:
    transparent;
    color:
    var(--cyan);
    border:
    1px solid var(--cyan);
    font-family:
    "Orbitron";
    transition:
    .3s;
}
.product-button:hover {
    background:
    var(--cyan);
    color:
    #001015;
    box-shadow:
    0 0 25px var(--cyan);
}
</style>
<section id="products">
<p class="section-label">

// AVAILABLE PRODUCTS //
</p>
<h2 class="section-title">
Premium Products
</h2>
<p class="section-description">
Choose your product purchase.
Purchase, send payment, and receive your Minecraft product through our support system in discord.

</p>
<div class="products-grid">

<div class="product-card">
<div class="product-icon">
⚔️
</div>
<div class="product-name">
Custom Prefix
</div>
<div class="product-time">
30 DAYS ACCESS
</div>
<div class="product-price">
$3
</div>
<ul class="product-list">
<li>
Custom in-game prefix
</li>
<li>
Custom color
</li>
<li>
Custom name style
</li>
</ul>
<button class="product-button"
onclick="selectPackage('Custom Prefix — 30-Days — $3')">
BUY NOW
</button>
</div>

<div class="product-card">
<div class="product-icon">
🌌
</div>
<div class="product-name">
Donator Rank
</div>
<div class="product-time">
30 DAYS ACCESS
</div>
<div class="product-price">
$4
</div>
<ul class="product-list">
<li>
Donator badge
</li>
<li>
Special display
</li>
<li>
Extra commands
</li>
</ul>
<button class="product-button"
onclick="selectPackage('Donator Rank — 30-Days — $4')">
BUY NOW
</button>
</div>
<div class="product-card">
<div class="product-icon">
💠
</div>
<div class="product-name">
Custom Prefix+
</div>
<div class="product-time">
60 DAYS ACCESS
</div>
<div class="product-price">
$5
</div>
<ul class="product-list">
<li>
Extended prefix duration
</li>
<li>
Custom color
</li>
<li>
Custom name style
</li>
</ul>
<button class="product-button"
onclick="selectPackage('Custom Prefix+ — 60-Days — $5')">
BUY NOW
</button>
</div>

<div class="product-card">
<div class="product-icon">
👑
</div>
<div class="product-name">
Donator Rank+
</div>
<div class="product-time">
60 DAYS ACCESS
</div>
<div class="product-price">
$6
</div>
<ul class="product-list">
<li>
Premium donator badge
</li>
<li>
Enhanced display
</li>
<li>
Extra commands
</li>
</ul>
<button class="product-button"
onclick="selectPackage('Donator Rank+ — 60-Days — $6')">
BUY NOW
</button>
</div>

<div class="product-card featured">
<div class="featured-tag">
⭐ MOST POPULAR
</div>
<div class="product-icon">
⚡
</div>
<div class="product-name">
Custom Prefix-
</div>
<div class="product-time">
15 DAYS ACCESS
</div>
<div class="product-price">
$2
</div>
<ul class="product-list">
<li>
Custom in-game prefix
</li>
<li>
Custom color
</li>
<li>
Custom name style
</li>
</ul>
<button class="product-button"
onclick="selectPackage('Custom Prefix- — 15-Days — $2')">
BUY NOW
</button>
</div>
</div>
</section>

<div class="divider"></div>

<style>
.steps {
    display:grid;
    grid-template-columns:
    repeat(
        auto-fit,
        minmax(
            220px,
            1fr
        )
    );
    gap:
    2rem;
    margin-top:
    3rem;
}
.step {
    background:
    rgba(
        13,
        22,
        40,
        .7
    );
    border:
    1px solid var(--border);
    padding:
    1.8rem;
    backdrop-filter:
    blur(10px);
    transition:
    .3s;
}
.step:hover {
    border-color:
    var(--cyan);
    box-shadow:
    0 0 20px rgba(0,247,255,.25);
    transform:
    translateY(-5px);
}
.step-number {
    font-family:
    "Orbitron";
    font-size:
    2.5rem;
    color:
    var(--cyan);
    text-shadow:
    0 0 15px var(--cyan);
}
.step-title {
    font-family:
    "Orbitron";
    margin:
    .8rem 0;
    color:
    var(--white);
}
</style>

<section id="how">
<p class="section-label">
// SYSTEM PROCESS //
</p>
<h2 class="section-title">
How It Works
</h2>
<p class="section-description">
Four simple steps to activate your Aura Craft upgrade.
</p>
<div class="steps">
<div class="step">
<div class="step-number">
01
</div>
<h3 class="step-title">
Choose Upgrade
</h3>
<p>
Select the Minecraft product you want and press Buy Now.
</p>
</div>
<div class="step">
<div class="step-number">
02
</div>
<h3 class="step-title">
Complete Order
</h3>
<p>
Enter your Minecraft username and select your payment method.
</p>
</div>
<div class="step">
<div class="step-number">
03
</div>
<h3 class="step-title">
Send Payment
</h3>
<p>
Complete your payment and save your transaction proof.
</p>
</div>
<div class="step">
<div class="step-number">
04
</div>
<h3 class="step-title">
Receive Upgrade
</h3>
<p>
Create a ticket on discord and receive your product.
</p>
</div>
</div>
</section>
<div class="divider"></div>

<style>
.order-box {
    background:
    rgba(
        13,
        22,
        40,
        .85
    );
    border:
    1px solid var(--border);
    padding:
    3rem 2rem;
    backdrop-filter:
    blur(15px);
    box-shadow:
    0 0 30px rgba(0,247,255,.08);
}
.form-grid {
    display:grid;
    grid-template-columns:
    repeat(
        2,
        1fr
    );
    gap:
    1.5rem;
    margin-top:
    2rem;
}
.field {
    display:flex;
    flex-direction:column;
    gap:.5rem;
}
.field.full {
    grid-column:
    1 / -1;
}
label {
    font-family:
    "Orbitron";
    font-size:
    .7rem;
    color:
    var(--cyan);
    letter-spacing:
    .15em;
}
input,
select,
textarea {
    width:100%;
    padding:
    .85rem;
    background:
    #08111f;
    border:
    1px solid var(--border);
    color:
    var(--white);
    font-family:
    "Rajdhani";
    font-size:
    1rem;
    outline:none;
}
input:focus,
select:focus,
textarea:focus {
    border-color:
    var(--cyan);
    box-shadow:
    0 0 15px rgba(0,247,255,.25);
}
textarea {
    min-height:
    120px;
    resize:
    vertical;
}
.form-submit {
    grid-column:
    1 / -1;
}
.submit-button {
    width:100%;
    padding:
    1rem;
    background:
    linear-gradient(
        90deg,
        var(--cyan),
        var(--purple)
    );
    border:none;
    color:
    #001015;
    font-family:
    "Orbitron";
    cursor:pointer;
    transition:.3s;
}
.submit-button:hover {
    box-shadow:
    0 0 30px var(--cyan);
    transform:
    translateY(-3px);
}
@media(max-width:700px){
.form-grid {
    grid-template-columns:
    1fr;
}
.nav-links {
    display:none;
}
}
</style>

<section id="order">
<p class="section-label">
// PURCHASE PRODUCT //
</p>
<h2 class="section-title">
Place Your Order
</h2>
<div class="order-box">
<div class="form-grid">
<div class="field">
<label>
Minecraft Username
</label>
<input 
id="ign"
type="text"
placeholder="Your Minecraft IGN">
</div>
<div class="field">
<label>
Package
</label>
<select id="package">
<option value="">
-- Select Package --
</option>
<option>
Custom Prefix — 30-Days — $3
</option>
<option>
Donator Rank — 30-Days — $4
</option>
<option>
Custom Prefix+ — 60-Days — $5
</option>
<option>
Donator Rank+ — 60-Days — $6
</option>
<option>
Custom Prefix- — 15-Days — $2
</option>
</select>
</div>

<div class="field full">
<label>
Payment Method
</label>
<div class="payment-grid">
<div class="payment-option" 
id="pay-paypal"
onclick="selectPayment('paypal')">
<input 
type="radio"
name="payment"
hidden>
<h3>
💳 PayPal
</h3>
<p>
daminafemboy@email.com
</p>
</div>
<div class="payment-option"
id="pay-gcash"
onclick="selectPayment('gcash')">
<input
type="radio"
name="payment"
hidden>
<h3>
📱 GCash
</h3>
<p>
09XX-XXX-XXXX
</p>
</div>
<div class="payment-option"
id="pay-maya"
onclick="selectPayment('maya')">
<input
type="radio"
name="payment"
hidden>
<h3>
🔴 Visa/Mastercard
</h3>
<p>
09XX-XXX-XXXX
</p>
</div>
</div>
</div>
<div class="field full">
<label>
Additional Notes
</label>
<textarea 
id="notes"
placeholder="Extra information or requests...">
</textarea>
</div>
<div class="form-submit">
<button 
class="submit-button"
onclick="submitOrder()">
⚡ CONFIRM ORDER
</button>
</div>
</div>
</div>
</section>
<div class="divider"></div>
<style>
.payment-grid {
    display:grid;
    grid-template-columns:
    repeat(
        auto-fit,
        minmax(
            180px,
            1fr
        )
    );
    gap:
    1rem;
    margin-top:
    .5rem;
}
.payment-option {
    padding:
    1.2rem;
    background:
    rgba(
        0,247,255,.03
    );
    border:
    1px solid var(--border);
    cursor:pointer;
    transition:.3s;
}
.payment-option:hover {
    border-color:
    var(--cyan);
    box-shadow:
    0 0 15px rgba(0,247,255,.25);
}
.payment-option.selected {
    border-color:
    var(--cyan);
    background:
    rgba(
        0,247,255,.12
    );
    box-shadow:
    0 0 20px rgba(0,247,255,.3);
}
.payment-option h3 {
    font-family:
    "Orbitron";
    color:
    var(--white);
    font-size:
    1rem;
}
.payment-option p {
    margin-top:
    .4rem;
    color:
    var(--cyan);
}
</style>

<style>
.confirmation-box {
    display:none;
    margin-top:
    2rem;
    padding:
    2rem;
    border:
    1px solid var(--cyan);
    background:
    rgba(
        0,247,255,.05
    );
    box-shadow:
    0 0 25px rgba(0,247,255,.2);
}
.confirmation-box h3 {
    font-family:
    "Orbitron";
    color:
    var(--cyan);
    margin-bottom:
    1rem;
}
.confirmation-text {
    background:
    #07101d;
    border:
    1px solid var(--border);
    padding:
    1.2rem;
    margin-top:
    1rem;
    white-space:
    pre-line;
    font-family:
    "Rajdhani";
    color:
    var(--white);
}
</style>
<div 
class="confirmation-box"
id="confirmation">
<h3>
⚡ ORDER RECEIVED
</h3>
<p>
Your order has been created.
Complete your payment using the details below.
</p>
<div 
class="confirmation-text"
id="payment-details">
</div>
<p style="margin-top:1rem">
After payment, send your screenshot and order details
through your support ticket.
</p>
</div>
<footer>
<div class="footer-logo">
⚡
</div>
<h3>
AURA CRAFT
</h3>
<p>
© 2026 Aura Craft — All Rights Reserved.
</p>
<p>
Not affiliated with Mojang Studios or Microsoft.
</p>
</footer>
<style>
footer {
    text-align:center;
    padding:
    3rem 1.5rem;
    border-top:
    1px solid var(--border);
    background:
    rgba(
        5,8,20,.6
    );
}
.footer-logo {
    font-size:
    2rem;
    color:
    var(--cyan);
    text-shadow:
    0 0 20px var(--cyan);
}
footer h3 {
    font-family:
    "Orbitron";
    color:
    var(--white);
    margin:
    .8rem 0;
}
footer p {
    font-size:
    .9rem;
    color:
    var(--muted);
}
</style>
<script>
let selectedPayment = "";
function selectPackage(packageName){
    const packageBox =
    document.getElementById("package");
    packageBox.value =
    packageName;
    document
    .getElementById("order")
    .scrollIntoView({
        behavior:"smooth"
    });
}
function selectPayment(method){
    selectedPayment =
    method;
    document
    .querySelectorAll(".payment-option")
    .forEach(option=>{
        option.classList.remove(
            "selected"
        );
    });
    document
    .getElementById(
        "pay-" + method
    )
    .classList.add(
        "selected"
    );
}
function getAmount(packageName){
    if(packageName.includes("$2"))
        return "$2";
    if(packageName.includes("$3"))
        return "$3";
    if(packageName.includes("$4"))
        return "$4";
    if(packageName.includes("$5"))
        return "$5";
    if(packageName.includes("$6"))
        return "$6";
    return "Unknown";
}
function submitOrder(){
    const ign =
    document.getElementById(
        "ign"
    ).value.trim();
    const packageName =
    document.getElementById(
        "package"
    ).value;
    if(!ign){
        alert(
            "Please enter your Minecraft username."
        );
        return;
    }
    if(!packageName){
        alert(
            "Please select a package."
        );
        return;
    }
    if(!selectedPayment){
        alert(
            "Please select a payment method."
        );
        return;
    }
    const amount =
    getAmount(packageName);
    let instructions = "";
    if(selectedPayment === "paypal"){
        instructions =
`PAYMENT METHOD: PayPal
Send payment to:
daminafemboy@email.com
Amount:
${amount}
Message:
${ign} - ${packageName}`;
    }
    if(selectedPayment === "gcash"){
        instructions =
`PAYMENT METHOD: GCash
GCash Number:
09XX-XXX-XXXX
Amount:
${amount}
Name:
YOUR NAME
Message:
${ign} - ${packageName}`;
    }
    if(selectedPayment === "Visa/Mastercard"){
        instructions =
`PAYMENT METHOD: Visa/Mastercard
Maya Number:
09XX-XXX-XXXX
Amount:
${amount}
Name:
YOUR NAME
Message:
${ign} - ${packageName}`;
    }
    document
    .getElementById(
        "payment-details"
    )
    .innerText =
    instructions;
    const box =
    document.getElementById(
        "confirmation"
    );
    box.style.display =
    "block";
    box.scrollIntoView({
        behavior:"smooth"
    });
}
document.addEventListener(
"mousemove",
function(e){
    const x =
    e.clientX /
    window.innerWidth *
    100;
    const y =
    e.clientY /
    window.innerHeight *
    100;
    document.body.style.background =
    `
    radial-gradient(
        circle at ${x}% ${y}%,
        rgba(0,247,255,.15),
        transparent 35%
    ),
    radial-gradient(
        circle at top,
        #172b55,
        #050814 60%
    )
    `;
});
document
.querySelectorAll(
    ".btn,.product-button,.submit-button"
)
.forEach(button=>{
    button.addEventListener(
    "click",
    ()=>{
        button.style.transform =
        "scale(.96)";
        setTimeout(()=>{
            button.style.transform =
            "";
        },120);
    });
});
window.addEventListener(
"load",
()=>{
    document.body.classList.add(
        "loaded"
    );
});
const packageSelector =
document.getElementById(
    "package"
);
if(packageSelector){
    packageSelector.addEventListener(
    "change",
    ()=>{
        console.log(
            "Selected:",
            packageSelector.value
        );
    });
}
document
.querySelectorAll("form")
.forEach(form=>{
    form.addEventListener(
    "submit",
    e=>{
        e.preventDefault();
    });
});
</script>
<style>
@media(max-width:900px){
    nav {
        padding:
        1rem;
    }
    .hero h1 {
        font-size:
        4rem;
    }
    .products-grid {
        grid-template-columns:
        repeat(
            2,
            1fr
        );
    }
}
@media(max-width:600px){
    body {
        font-size:
        16px;
    }
    nav {
        justify-content:
        center;
    }
    .nav-links {
        display:
        none;
    }
    .hero {
        min-height:
        90vh;
        padding:
        1rem;
    }
    .hero h1 {
        font-size:
        3rem;
    }
    .hero-description {
        font-size:
        1rem;
    }
    .products-grid {
        grid-template-columns:
        1fr;
    }
    section {
        padding:
        3rem 1rem;
    }
    .order-box {
        padding:
        1.5rem;
    }
    .payment-grid {
        grid-template-columns:
        1fr;
    }
}
body {
    opacity:
    1;
    transition:
    opacity .5s ease;
}
</style>
<script>
function choosePackage(name){
    selectPackage(name);
}
function selectPackage(packageName){
    const selector =
    document.getElementById(
        "package"
    );
    if(selector){
        selector.value =
        packageName;
    }
    const order =
    document.getElementById(
        "order"
    );
    if(order){
        order.scrollIntoView({
            behavior:
            "smooth"
        });
    }
}
function clearPayment(){
    selectedPayment = "";

    document
    .querySelectorAll(
        ".payment-option"
    )
    .forEach(item=>{
        item.classList.remove(
            "selected"
        );
    });
}
</script>
<script>
const ignInput =
document.getElementById(
      "ign"
);
if(ignInput){
    ignInput.addEventListener(
    "input",
    ()=>{
        ignInput.value =
        ignInput.value
        .replace(
            /[^a-zA-Z0-9_]/g,
            ""
        );
    });
}
document
.querySelectorAll(
    ".payment-option"
)
.forEach(option=>{
    option.addEventListener(
    "click",
    ()=>{
        document
        .querySelectorAll(
            ".payment-option"
        )
        .forEach(x=>{
            x.classList.remove(
                "selected"
            );
        });
        option.classList.add(
            "selected"
        );
    });
});
document
.querySelectorAll(
    ".payment-option"
)
.forEach(option=>{

    option.tabIndex = 0;
    option.addEventListener(
    "keydown",
    event=>{
        if(event.key === "Enter"){
            option.click();
        }
    });
});
</script>
<style>
.product-card,
.step,
.order-box,
.payment-option {
    border-radius:
    6px;
}
.product-card::before,
.step::before {
    content:"";
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:2px;
    background:
    linear-gradient(
        90deg,
        transparent,
        var(--cyan),
        transparent
    );
    opacity:.7;
}
.product-card {
    overflow:hidden;
}
.logo:hover {
    text-shadow:
    0 0 10px var(--cyan),
    0 0 30px var(--cyan);
}
.section-title {
    text-shadow:
    0 0 15px rgba(0,247,255,.25);
}
.confirmation-box {
    animation:
    pulseGlow 2s infinite alternate;
}
@keyframes pulseGlow {
    from {
        box-shadow:
        0 0 15px rgba(0,247,255,.15);
    }
    to {
        box-shadow:
        0 0 35px rgba(0,247,255,.45);
    }
}
footer {
    position:relative;
    overflow:hidden;
}
footer::before {
    content:"";
    position:absolute;
    top:0;
    left:-100%;
    width:100%;
    height:1px;
    background:
    linear-gradient(
        90deg,
        transparent,
        var(--cyan),
        transparent
    );
    animation:
    footerScan 4s infinite;
}
@keyframes footerScan {
    0% {
        left:-100%;
    }
    100% {
        left:100%;
    }
}
</style>
</body>
</html>
