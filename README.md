# Ex.07 Restaurant Website
# Date:02.10.2025
# AIM:
To develop a static Restaurant website to display the food items and services provided by them.

# DESIGN STEPS:
## Step 1:
Requirement collection.

## Step 2:
Creating the layout using HTML and CSS.

## Step 3:
Updating the sample content.

## Step 4:
Choose the appropriate style and color scheme.

## Step 5:
Validate the layout in various browsers.

## Step 6:
Validate the HTML code.

## Step 7:
Publish the website in the given URL.

# PROGRAM:
hotel.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Royal Restaurant</title>

  <style>
    /* Color scheme:
       Primary: #0f4c5c (Deep Teal)
       Accent : #ff7a59 (Coral)
       Background: #fff8f0 (Cream)
       Text: #2c3e50 (Charcoal)
    */

    :root{
      --primary:#0f4c5c;
      --accent:#ff7a59;
      --bg:#fff8f0;
      --text:#2c3e50;
      --muted:#6b7280;
    }

    *{box-sizing:border-box;margin:0;padding:0;font-family: 'Open Sans', Arial, sans-serif}
    body{background:var(--bg);color:var(--text);line-height:1.6}

    header{background:#f7f7f7;padding:18px 12px;border-bottom:1px solid #e6e6e6}
    .logo-title{display:flex;align-items:center;justify-content:center;gap:14px}
    .logo-title img{height:64px;width:64px;object-fit:cover;border-radius:8px}
    .logo-title h1{font-family: 'Playfair Display', serif;font-size:2.4rem;color:var(--primary);margin:0}

    nav{background:var(--primary);display:flex;justify-content:center;gap:18px;padding:12px 8px}
    nav a{color:#fff;text-decoration:none;font-weight:700;padding:8px 14px;border-radius:6px}
    nav a:hover{background:rgba(255,255,255,0.08)}

    .container{max-width:1100px;margin:24px auto;padding:0 16px}

    .hero{background-image:url('https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&w=1400&q=80');background-size:cover;background-position:center;color:white;text-align:center;padding:84px 20px;border-radius:10px}
    .hero .badge{background:rgba(0,0,0,0.45);display:inline-block;padding:8px 14px;border-radius:6px;font-weight:700}
    .hero h2{font-family:'Playfair Display',serif;font-size:2.8rem;margin:10px 0}
    .hero p{max-width:760px;margin:14px auto;background:rgba(0,0,0,0.45);padding:18px;border-radius:8px;line-height:1.7}

    .sections{display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap;margin-top:26px}
    .section{background:#fff;border-radius:10px;box-shadow:0 6px 20px rgba(15,76,92,0.06);flex:1;min-width:260px;padding:18px;transition:transform .25s}
    .section:hover{transform:translateY(-6px)}
    .section h3{font-family:'Playfair Display',serif;color:var(--accent);margin-bottom:10px}
    .section img{width:100%;height:160px;object-fit:cover;border-radius:8px;margin-bottom:12px}

    .menu-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px;margin-top:20px}
    .menu-item{background:#fff;padding:12px;border-radius:10px;box-shadow:0 4px 12px rgba(0,0,0,0.06);display:flex;gap:10px;align-items:center}
    .menu-item img{width:88px;height:68px;object-fit:cover;border-radius:8px}
    .menu-item .meta{flex:1}
    .menu-item .meta h4{margin-bottom:6px;font-size:1rem}
    .menu-item .meta p{font-size:0.9rem;color:var(--muted)}
    .price{font-weight:700;color:var(--primary)}

    .admin-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:16px;margin-top:18px}
    .admin-card{background:#fff;padding:12px;border-radius:10px;text-align:center;box-shadow:0 6px 18px rgba(15,76,92,0.05)}
    .admin-card img{width:110px;height:110px;border-radius:50%;object-fit:cover;margin:6px auto}
    .admin-card h4{margin-top:8px}
    .admin-card p{color:var(--muted);font-size:0.95rem}

    .contact{background:#fff;padding:18px;border-radius:10px;box-shadow:0 6px 20px rgba(0,0,0,0.04);display:flex;gap:18px;flex-wrap:wrap}
    .contact .left{flex:1;min-width:240px}
    .contact .right{flex:1;min-width:240px}
    .contact p{margin-bottom:8px}

    footer{display:flex;justify-content:space-between;align-items:center;padding:18px;background:var(--primary);color:white;border-radius:8px;margin:28px auto 60px;max-width:1100px}
    footer .center{flex:1;text-align:center}

    @media(max-width:700px){
      .hero{padding:44px 18px}
      .logo-title h1{font-size:1.6rem}
      footer{flex-direction:column;gap:8px;text-align:center}
    }
  </style>

  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Open+Sans&display=swap" rel="stylesheet">
</head>
<body>

  <header>
    <div class="logo-title">
      <img src="icon.webp" alt="logo">
      <h1>Royal Restaurant</h1>
    </div>
  </header>

  <nav>
    <a href="#home">Home</a>
    <a href="#menu">Menu</a>
    <a href="#admin">Administration</a>
    <a href="#contact">Contact Us</a>
  </nav>

  <main class="container">

    <!-- HOME -->
    <section id="home" class="hero">
      <div class="badge">25% Off This Weekend</div>
      <h2>Serving bold flavors and fresh ingredients</h2>
      <p>
        We’re your go-to spot for great eats and good vibes. Locally loved, globally inspired. Welcome to food that feels like home.
      </p>
    </section>

    <div class="sections">
      <div class="section">
        <img src="https://images.unsplash.com/photo-1600891964599-f61ba0e24092?auto=format&fit=crop&w=600&q=80" alt="New Menu">
        <h3>Our New Menu</h3>
        <p>Explore delicious new dishes added by our chefs. Fresh, seasonal, and full of flavor!</p>
      </div>

      <div class="section">
        <img src="https://images.unsplash.com/photo-1528605248644-14dd04022da1?auto=format&fit=crop&w=600&q=80" alt="Book a Table">
        <h3>Book a Table</h3>
        <p>Reserve your favorite spot online in just a few clicks. We’re excited to serve you!</p>
      </div>

      <div class="section">
        <img src="https://images.unsplash.com/photo-1498654896293-37aacf113fd9?auto=format&fit=crop&w=600&q=80" alt="Opening Hours">
        <h3>Opening Hours</h3>
        <p>Mon - Fri: 10am - 10pm<br>Sat - Sun: 9am - 11pm</p>
      </div>
    </div>

    <!-- MENU -->
    <section id="menu">
      <h2 style="margin-top:28px;font-family:'Playfair Display',serif;color:var(--primary)">Menu</h2>
      <p style="color:var(--muted);margin-top:6px">A selection of our chef's favorites — fresh, seasonal and made to order.</p>

      <div class="menu-grid">

        <div class="menu-item">
          <img src="grilled.jpg" alt="Grilled Salmon">
          <div class="meta">
            <h4>Grilled Salmon</h4>
            <p>Herb butter, lemon, seasonal greens</p>
          </div>
          <div class="price">₹399</div>
        </div>

        <div class="menu-item">
          <img src="pizza.jpg" alt="Margherita Pizza">
          <div class="meta">
            <h4>Margherita Pizza</h4>
            <p>San Marzano tomatoes, fresh basil, mozzarella</p>
          </div>
          <div class="price">₹299</div>
        </div>

        <div class="menu-item">
          <img src="pasta.jpg" alt="Pasta Primavera">
          <div class="meta">
            <h4>Pasta Primavera</h4>
            <p>Seasonal vegetables, garlic, olive oil</p>
          </div>
          <div class="price">₹259</div>
        </div>

        <div class="menu-item">
          <img src="chicken.jpg" alt="Chicken Tikka">
          <div class="meta">
            <h4>Chicken Tikka Masala</h4>
            <p>Smoky tomato gravy, basmati rice</p>
          </div>
          <div class="price">₹349</div>
        </div>

        <div class="menu-item">
          <img src="https://images.unsplash.com/photo-1543362906-acfc16c67564?auto=format&fit=crop&w=400&q=80" alt="Caesar Salad">
          <div class="meta">
            <h4>Classic Caesar</h4>
            <p>Romaine, parmesan, dressing</p>
          </div>
          <div class="price">₹199</div>
        </div>

        <div class="menu-item">
          <img src="burger.jpg" alt="Beef Burger">
          <div class="meta">
            <h4>Royal Beef Burger</h4>
            <p>Angus patty, caramelized onions, cheddar</p>
          </div>
          <div class="price">₹329</div>
        </div>

        <div class="menu-item">
          <img src="sushi.webp" alt="Sushi Platter">
          <div class="meta">
            <h4>Sushi Platter</h4>
            <p>Chef selection, wasabi, pickled ginger</p>
          </div>
          <div class="price">₹499</div>
        </div>

        <div class="menu-item">
          <img src="https://images.unsplash.com/photo-1551183053-bf91a1d81141?auto=format&fit=crop&w=400&q=80" alt="Ramen">
          <div class="meta">
            <h4>Shoyu Ramen</h4>
            <p>Slow-cooked broth, char siu, noodles</p>
          </div>
          <div class="price">₹279</div>
        </div>

        <div class="menu-item">
          <img src="https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&w=400&q=80" alt="Paneer Butter Masala">
          <div class="meta">
            <h4>Paneer Butter Masala</h4>
            <p>Creamy tomato gravy, butter naan</p>
          </div>
          <div class="price">₹249</div>
        </div>

        <div class="menu-item">
          <img src="momos.jpg" alt="Tacos">
          <div class="meta">
            <h4>Street Tacos (3 pcs)</h4>
            <p>Pick your filling: veg / chicken / fish</p>
          </div>
          <div class="price">₹179</div>
        </div>

        <div class="menu-item">
          <img src="https://images.unsplash.com/photo-1504674900247-0877df9cc836?auto=format&fit=crop&w=400&q=80" alt="Chocolate Cake">
          <div class="meta">
            <h4>Chocolate Lava Cake</h4>
            <p>Warm molten center, vanilla ice cream</p>
          </div>
          <div class="price">₹149</div>
        </div>

        <div class="menu-item">
          <img src="https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&w=400&q=80" alt="Smoothie Bowl">
          <div class="meta">
            <h4>Berry Smoothie Bowl</h4>
            <p>Seasonal berries, granola, honey</p>
          </div>
          <div class="price">₹189</div>
        </div>

      </div>
    </section>

    <!-- ADMINISTRATION -->
    <section id="admin">
      <h2 style="margin-top:28px;font-family:'Playfair Display',serif;color:var(--primary)">Administration</h2>
      <p style="color:var(--muted);margin-top:6px">Meet the team behind Royal Restaurant.</p>

      <div class="admin-grid">
        <div class="admin-card">
          <img src="girl.webp" alt="Owner">
          <h4>Mr. R. Kapoor</h4>
          <p>Owner & Founder</p>
        </div>
        <div class="admin-card">
          <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?auto=format&fit=crop&w=400&q=80" alt="Head Chef">
          <h4>Chef Anika</h4>
          <p>Head Chef</p>
        </div>
        <div class="admin-card">
          <img src="boy.webp" alt="Manager">
          <h4>Mr. Rahul</h4>
          <p>Restaurant Manager</p>
        </div>
        <div class="admin-card">
          <img src="author.jpg" alt="Marketing">
          <h4>Ms. Priya</h4>
          <p>Marketing Head</p>
        </div>
        <div class="admin-card">
          <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?auto=format&fit=crop&w=400&q=80" alt="HR">
          <h4>Ms. Kavita</h4>
          <p>Human Resources</p>
        </div>
        <div class="admin-card">
          <img src="boy 2.webp" alt="Operations">
          <h4>Mr. Sanjay</h4>
          <p>Operations</p>
        </div>
      </div>

    </section>

    <!-- CONTACT -->
    <section id="contact" style="margin-top:20px">
      <h2 style="font-family:'Playfair Display',serif;color:var(--primary)">Contact Us</h2>
      <p style="color:var(--muted);margin-top:6px">We'd love to hear from you — reservations, feedback or events.</p>

      <div class="contact">
        <div class="left">
          <h3 style="margin-bottom:6px">Address</h3>
          <p>Royal Restaurant, 12 Royal Street, MG Road, Bengaluru, Karnataka, 560001</p>

          <h3 style="margin-top:12px;margin-bottom:6px">Phone</h3>
          <p>+91 98765 43210</p>

          <h3 style="margin-top:12px;margin-bottom:6px">Email</h3>
          <p>contact@royalrestaurant.example</p>
        </div>

        <div class="right">
          <h3 style="margin-bottom:6px">Opening Hours</h3>
          <p>Mon - Fri: 10:00 — 22:00</p>
          <p>Sat - Sun: 09:00 — 23:00</p>
        </div>
      </div>
    </section>

  </main>

  <footer>
    <div class="left">© 2025 Royal Restaurant</div>
    <div class="center">Created by <strong>Dhivyashree .R</strong></div>
    <div class="right">Follow us: @royalrestaurant</div>
  </footer>

</body>
</html>  
```
# OUTPUT:
**home**
<img width="1920" height="1080" alt="Screenshot (45)" src="https://github.com/user-attachments/assets/f537b87d-f3e7-49a4-8318-9c0a24722687" />

**menu**
<img width="1920" height="1080" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/5d3a671d-f7e0-4d47-822d-9cc454808e52" />

**administation**
<img width="1920" height="1080" alt="Screenshot (47)" src="https://github.com/user-attachments/assets/b7cbee90-79cb-4af6-b606-f46cdf3f5d96" />

**contact us**
<img width="1920" height="1080" alt="Screenshot (48)" src="https://github.com/user-attachments/assets/2827fcdf-fa20-4352-8ecc-5a5a09ec5146" />

**full website**
<img width="1920" height="1080" alt="Screenshot (49)" src="https://github.com/user-attachments/assets/51a4de24-1419-4b7d-aea2-deb7d7694952" />

# RESULT:
The program for designing software company website using HTML and CSS is completed successfully
