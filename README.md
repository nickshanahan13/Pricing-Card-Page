# Sample Subscription Page

### HTML 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Pricing Card Page</title>
</head>
<body>
    <div class="banner">
        <p class="banner-text-light">Your current plan</p>
        <p class="card-header">Starter Trial * 500MAUs</p>
    </div>
    <h1 class="title">Choose a Plan</h1>
    <div id="pricing">
        <div class="price-card">
            <p class="card-header">Starter</p>
            <p class="card-price">$19</p>
            <ul>
                <li>500 MAUs</li>
                <li>3 Projects</li>
                <li>Unlimited guides</li>
                <li>Unlimited flows</li>
                <li>Unlimited branded themes</li>
                <li>Email support</li>
            </ul>
            <button class="price-btn" id="price-1-btn">Choose Plan</button>
        </div>
        <div class="price-card">
            <p class="card-header">Pro</p>
            <p class="card-price">$99<span class="month"><span>/</span>month</span></p>
            <ul>
                <li>All starter features, plus:</li>
                <li>Unlimited projects</li>
                <li>Unlimited fully customizable themes</li>
                <li>A dedicated Customer Success Manager</li>
            </ul>
            <button class="price-btn active" id="price-2-btn">Choose Plan</button>
        </div>
        <div class="price-card">
            <p class="card-header">Enterprise</p>
            <p class="card-price">Let's Talk!</p>
            <ul>
                <li>All Pro features</li>
                <li>Unlimited MAUs</li>
                <li>Dedicated enviornment</li>
                <li>Enterprise account administration</li>
                <li>Premium support and services</li>
            </ul>
            <button class="price-btn" id="price-3-btn">Contact Us</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### CSS

```css

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: sans-serif;
}

:root {
    --black: #191b1d;
    --dark-grey: #22262c;
    --pink: #bc1e4a; 
}

body {
    background-color: var(--black);
    max-width: 90%;
    margin: 0 auto;
    color: white;
    padding-top: 100px;
}

.title{
    text-align: center;
    margin: 60px 0;
}

.price-card {
    background-color: var(--dark-grey);
    border-radius: 5px;
    padding: 60px 40px;
    text-align: center;
}

#pricing {
    color: white;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 10px;

}

.card-header {
    font-size: 18px;
    margin: 20px 0 15px 0;
    text-align: center;
}

.card-price {
    font-size: 48px;
    text-align: center;
    font-weight: bold;
}

.month {
    font-size: 14px;
    font-weight: 500;
    margin-left: 5px;
}

.month > span {
    margin-right: 5px;
}

ul {
    list-style: none;
    margin: 60px 0;
    text-align: left;
    height: 250px;
    margin-left: 2rem;
}

li {
    margin-bottom: 15px;
}

ul li::before {
    content: "\2022";
    font-size: 18px;
    color: var(--pink);
    font-weight: bold;
    display: inline-block;
    width: 1em;
    margin-left: -1em;
}

.price-btn {
    border: 1px solid var(--pink);
    padding: 12px;
    border-radius: 3px;
    background-color: inherit;
    color: white;
    width: 200px;
}


.price-btn.active {
    background-color: var(--pink);
}

.banner {
    background-color: var(--pink);
    border-radius: 00 10px 10px;
    text-align: center;
    padding: 10px;
    width: 400px;
    margin: 0 auto 10px auto;
    left: calc(50% - 200px);
    position: fixed;
    top: 0;
}

.banner-text-light {
    font-size: 14px;
    font-weight: 100;
    margin-bottom: 2px;
    opacity: 0.7;
}

@media only screen and (max-width: 800px) {
    #pricing {
        grid-template-columns: 1fr;
        gap: 10px;
    
    }
};
```
