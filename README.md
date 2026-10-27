# Book Store Web Application

A front-end website for an online book store, made with HTML, CSS and JavaScript. It is built on the free [Booksaw](https://templatesjungle.com/) template by TemplatesJungle, with extra pages added: sign-up / login, user profile, book search, shopping cart, checkout and book detail pages.

There is **no back-end or database**. All books, prices and user data are written directly in the HTML and JavaScript, so nothing is saved.

## Pages

| Page | File | What it does |
|---|---|---|
| Home | `index.html` | Store home page from the template: banner, featured books, popular books, offers, articles. The top bar links to **Account**, **Search** and **Cart**. |
| Search | `sorting_page.html` | List of 6 books. You can search by title and filter by genre and minimum star rating. The list updates as you type or choose. |
| Account | `prof.html` | User profile with name, phone number, credit, liked books and bought books (example data). |
| Cart | `cart.html` | Shopping cart with 2 example books, quantity boxes, promo code field and total price. Buttons go back to the home page or to checkout. |
| Checkout | `checkout.html` | Checkout form: name, payment card details, shipping method (Fedex, post, or pick up at shop), address with city (Tehran, Isfahan, Shiraz) and an order summary. |
| Sign-up / Login | `signupandlogin.html` | Choose between **Sign-Up** and **Login**. |
| Sign-up | `signup.html` | Form with first name, family name, email, phone, user ID and password (twice). If the passwords don't match, it shows an alert. If they match, it goes to the home page. The data is only printed to the browser console. |
| Login | `login.html` | Login form with user ID and password. It is meant to accept one test account: `testUser` / `testPass` (see [Known issues](#known-issues)). |
| Book pages | `simpleWayLife.html`, `OnceUpon.html`, `theLady.html`, `greatTravel.html` | One page per book with title, short story, author and star rating. |

**Note:** the sign-up / login pages and the 4 book pages are not linked from the home page. Open them directly (see [How to run](#how-to-run)).

## Tech

- HTML, CSS, JavaScript
- Bootstrap (5.3.1 on most pages, 3.4.1 on cart and checkout), loaded from a CDN
- jQuery 1.11 and the template's plugins (in `js/`)
- Font Awesome 4.7 (star ratings on book pages), loaded from a CDN

## Project structure

```
index.html                 # Home page (template)
sorting_page.html          # Search and filter books
prof.html                  # User profile
cart.html                  # Shopping cart
checkout.html              # Checkout
signupandlogin.html        # Choose sign-up or login
signup.html, login.html    # Sign-up and login forms
script.js, styles.css      # Code and style for sign-up / login
simpleWayLife.html, OnceUpon.html, theLady.html, greatTravel.html   # Book pages
style.css, css/, js/       # Template styles and scripts
images/, icomoon/          # Images and icon font
```

## How to run

You only need a web browser. No install or build step is needed.

**Option 1: open the file**

Open `index.html` in your browser (double-click it).

**Option 2: use a local server**

From the project folder, run:

```bash
python -m http.server 8000
```

(On macOS/Linux, use `python3` instead of `python`.) Then open <http://localhost:8000> in your browser.

**You need an internet connection** for the page styles to load fully, because Bootstrap and Font Awesome come from a CDN.

**To open pages that are not linked from the home page**, open the file directly, or add its name to the address. For example:

- `http://localhost:8000/signupandlogin.html`
- `http://localhost:8000/OnceUpon.html`

## Known issues

- **Login does not work.** `login.html` and `signup.html` share one `script.js`. On the login page, the script first looks for the sign-up form, which is not on that page, and stops with an error. Because of this, the login code never runs, and even `testUser` / `testPass` only reloads the page. Sign-up is not affected.
- **Some menu links are broken.** The *Pages* menu on the home page links to pages from the paid version of the template (About, Blog, Shop, Contact, …). These files are not in this repo.
- Cart, checkout and profile show fixed example data. Buttons like *Pay* and *Add to cart* don't do anything.

## Credits

Website template: [Booksaw](https://templatesjungle.com/) by TemplatesJungle. See `readme.txt` for the template's license terms.
