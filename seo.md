---

# Tutorial: SEO, Accessibility, and Deployment Masterclass

This tutorial will guide you through building a high-quality web page that is optimized for search engines, accessible to all users, and live on the internet.

---

## Phase 1: SEO Basics (The "Before and After")

Search Engine Optimization (SEO) helps search engines understand your content so users can find your site. We start by fixing a "bad" page that lacks context.

### What is a search engine? 

A search engine is a software system that helps users find information on the internet by indexing and retrieving relevant web content based on their queries.

### The "Bad" Example
```html
<!DOCTYPE html>
<html>
<head>
    <title>My Page</title> <!--issue 1-->

</head>
<body>
    <h1>Welcome</h1>
    <img src="logo.png"> <!--issue 2-3-->
    <p>Check out our products <a href="store.html">click here<!--issue 4--></a>.</p>
</body>
</html>
```

### Explanation

This page has several issues:

- The `<title>` "My Page" tells Google (and users) absolutely nothing about the content.
- There is no `<meta description>`.
-  The `<img>` tag lacks an `alt` attribute. If the image fails to load or a visually impaired person uses a screen reader, the context is lost.
- `` "Click here"`` is the ultimate SEO sin. It provides no topical relevance to the linked store.html.

### The "Fixed" SEO Example
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Organic Coffee Beans | RoastMaster City Hub</title><!--fixed1-->
    <meta name="description" content="Shop premium organic coffee beans sourced from sustainable farms. Fast delivery and brewing guides for every coffee lover."><!--fixed2-->
<body>
    <h1>Premium Organic Coffee Beans</h1>
    <img src="coffee-logo.png" alt="RoastMaster logo featuring a steaming coffee cup and green leaves"><!--fixed3-->
    <p>Explore our sustainable selection in our <a href="store.html">online coffee bean store</a>.</p><!--fixed4-->
</body>
</html>
```

### Explanation
- The `<title>` Use descriptive keywords, like "Organic Coffee Beans | RoastMaster City Hub. now this more unique, clear, and concise.
- The **meta description** provides a short summary that Google may use as a snippet.
- The image includes now **alt text** for accessibility and SEO and `<img src="logo.png" alt="Company Name Logo">`.
-  now has a better `<a href="store.html">`browse our winter collection</a> for whats the destnation is about.

---

## Phase 2: Accessibility

Accessibility ensures your site is **Operable** and **Perceivable** for everyone, including those using screen readers or keyboard-only navigation.

### Accessibility Example (Webpage with poor accessibility decisions)
```html
<!DOCTYPE html>
<html lang="en">

<!--new portion-->
<style>
    /* Color Contrast: Ensuring text stands out against the background */
    .accessible-text {
        color: red;
        background-color: green;
    }
</style>
<!--new portion-->

<head>
    <title>Organic Coffee Beans | RoastMaster City Hub</title>
    <meta name="description" content="Shop premium organic coffee beans sourced from sustainable farms. Fast delivery and brewing guides for every coffee lover.">
</head>
<body>
    <h1>Premium Organic Coffee Beans</h1>
    <img src="coffee-logo.png" alt="RoastMaster logo featuring a steaming coffee cup and green leaves">
    <p>Explore our sustainable selection in our <a href="store.html">online coffee bean store</a>.</p>
</body>

<!--new portion-->
<div class="accessible-text">
    <h2>Contact Us</h2>
    <!-- aria-label provides a label for screen readers when visible text isn't enough -->
    <button onclick="location.href='mailto:support@example.com'">
        Email Now
    </button>
</div>
<!--new portion-->

</html>
```

### Things to Add / Fix
- Ensuring text is properly legible, and color contrasts are easy on the eyes
- Ensuring that images/media has alt text, both for SEO as well as accessibility
- Using `aria-label` on interactive parts of your site, like buttons, to help accessibility.

### Explanation
- High **color contrast** improves readability for users with low vision.
- The `aria-label` gives screen readers a clear description of the button’s purpose.
- Tools like the **Accessibility Inspector** help verify structure, contrast, and keyboard navigation.

---

## Phase 3: Deploying to GitHub Pages

Once your code is ready, you can host it for free using GitHub Pages.

### Step-by-Step Repository Setup

1. **Create a Repository:** Log into GitHub and create a new repository, or you can create a repository through Visual Studio Code (When creating through Visual Studio Code, a repository is already made for you in GitHub).
2. **Naming Convention:** For a personal site, name the repository `username.github.io`.
3. **Local Setup:** Use these commands to push your code. You can also create a repository on GitHub through Visual Studio Code, through Source Control, and commiting and publishing the branch. When creating through Visual Studio Code, don't forget to include the commit message.
   ```bash
   git init
   git add .
   git commit -m "Initial SEO and Accessibility update"
   git branch -M main
   git remote add origin <Link to GitHub Repo>
   git push -u origin main
   ```

### Enabling the Live Site

1. Go to **Settings** in your GitHub repository.
2. Select **Pages** from the sidebar.
3. Under "Build and deployment," choose **Deploy from a branch** and select `main`. Make sure to press `save`.
4. Your site will be live at:  
   `https://username.github.io`  
   *(It may take up to 10 minutes to appear.)*

---

## 6 Things to Remember

1. **The Title Link:** Google uses the `<title>` element and headings to generate the clickable headline.
2. **The Snippet:** A good `<meta description>` is a 1–2 sentence summary that encourages clicks.
3. **POUR Principles:** Accessibility relies on being **Perceivable, Operable, Understandable, Robust**.
4. **Color Contrast:** WCAG AA requires **4.5:1** for normal text and **3:1** for large text.
5. **Alt Text & Links:** Always use descriptive `alt` text and avoid vague link text like "click here".
6. **GitHub Pages Setup:** Personal sites must use the `username.github.io` repository name.
---
=======
---

# Tutorial: SEO, Accessibility, and Deployment Masterclass

This tutorial will guide you through building a high-quality web page that is optimized for search engines, accessible to all users, and live on the internet.

---

## Phase 1: SEO Basics (The "Before and After")

Search Engine Optimization (SEO) helps search engines understand your content so users can find your site. We start by fixing a "bad" page that lacks context.

### The "Bad" Example
```html
<!DOCTYPE html>
<html>
<head>
    <title>My Page</title>
</head>
<body>
    <h1>Welcome</h1>
    <img src="logo.png">
    <p>Check out our products <a href="store.html">click here</a>.</p>
</body>
</html>
```

### Explanation
This page has several issues:

- The `<title>` is too vague for Google to create a useful "title link".
- There is no `<meta description>`.
- The image has no `alt` text.
- The link text ("click here") doesn't describe the destination.

### The "Fixed" SEO Example
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Organic Coffee Beans | RoastMaster City Hub</title>
    <meta name="description" content="Shop premium organic coffee beans sourced from sustainable farms. Fast delivery and brewing guides for every coffee lover.">
</head>
<body>
    <h1>Premium Organic Coffee Beans</h1>
    <img src="coffee-logo.png" alt="RoastMaster logo featuring a steaming coffee cup and green leaves">
    <p>Explore our sustainable selection in our <a href="store.html">online coffee bean store</a>.</p>
</body>
</html>
```

### Explanation
- The `<title>` is now unique, clear, and concise.
- The **meta description** provides a short summary that Google may use as a snippet.
- The image includes **alt text** for accessibility and SEO.
- The link text is descriptive and meaningful out of context.

---

## Phase 2: Accessibility

Accessibility ensures your site is **Operable** and **Perceivable** for everyone, including those using screen readers or keyboard-only navigation.

### Accessibility Example
```html
<!DOCTYPE html>
<html lang="en">

<!--new portion-->
<style>
    /* Color Contrast: Ensuring text stands out against the background */
    .accessible-text {
        color: #222222; /* Dark grey */
        background-color: #FFFFFF; /* White */
        /* Ratio is well above the 4.5:1 requirement for normal text */
    }
</style>
<!--new portion-->

<head>
    <title>Organic Coffee Beans | RoastMaster City Hub</title>
    <meta name="description" content="Shop premium organic coffee beans sourced from sustainable farms. Fast delivery and brewing guides for every coffee lover.">
</head>
<body>
    <h1>Premium Organic Coffee Beans</h1>
    <img src="coffee-logo.png" alt="RoastMaster logo featuring a steaming coffee cup and green leaves">
    <p>Explore our sustainable selection in our <a href="store.html">online coffee bean store</a>.</p>
</body>

<!--new portion-->
<div class="accessible-text">
    <h2>Contact Us</h2>
    <!-- aria-label provides a label for screen readers when visible text isn't enough -->
    <button aria-label="Send an email to support" onclick="location.href='mailto:support@example.com'">
        Email Now
    </button>
</div>
<!--new portion-->

</html>
```

### Explanation
- High **color contrast** improves readability for users with low vision.
- The `aria-label` gives screen readers a clear description of the button’s purpose.
- Tools like the **Accessibility Inspector** help verify structure, contrast, and keyboard navigation.

---

## Phase 3: Deploying to GitHub Pages

Once your code is ready, you can host it for free using GitHub Pages.

### Step-by-Step Repository Setup

1. **Create a Repository:** Log into GitHub and create a new repository, or you can create a repository through Visual Studio Code.
2. **Naming Convention:** For a personal site, name the repository `username.github.io`.
3. **Local Setup:** Use these commands to push your code. You can also create a repository on GitHub through Visual Studio Code, through Source Control, and commiting and publishing the branch. When creating through Visual Studio Code, don't forget to include the commit message.
   ```bash
   git init
   git add .
   git commit -m "Initial SEO and Accessibility update"
   git remote add origin <Link to GitHub Repo>
   git push origin main
   ```

### Enabling the Live Site

1. Go to **Settings** in your GitHub repository.
2. Select **Pages** from the sidebar.
3. Under "Build and deployment," choose **Deploy from a branch** and select `main`. Make sure to press `save`.
4. Your site will be live at:  
   `https://username.github.io`  
   *(It may take up to 10 minutes to appear.)*

---
how to commit
https://www.youtube.com/watch?v=OVfptJqx_RI
how to open live pages
https://www.youtube.com/watch?v=e5AwNU3Y2es
## 6 Things to Remember

1. **The Title Link:** Google uses the `<title>` element and headings to generate the clickable headline.
2. **The Snippet:** A good `<meta description>` is a 1–2 sentence summary that encourages clicks.
3. **POUR Principles:** Accessibility relies on being **Perceivable, Operable, Understandable, Robust**.
4. **Color Contrast:** WCAG AA requires **4.5:1** for normal text and **3:1** for large text.
5. **Alt Text & Links:** Always use descriptive `alt` text and avoid vague link text like "click here".
6. **GitHub Pages Setup:** Personal sites must use the `username.github.io` repository name.

---

---
## How To Create And push A Github Repository
In order to Initialize a repositiry in git hub you'll need a few things first you have to have github downloaded and signed in second you'll select create new repository on the home screen of github.com and insert 
```html```
-
1. echo "# test" >> README.md
2. git init
3. git add README.md
4. git commit -m "first commit"
5. git branch -M main
6. git remote add origin https://github.com/Tyler-F28/test.git
7. git push -u origin main
```html```

into the console, and obvously the link won't remain the same as it varies by user name and the name of the reposotory in question.
--
## Enabiling pages and live URL
In order to enable pages and live urls you must,

1. install the live preview and live server extentions.

2. you then select the go live option in the bottom right hand corner of the screen.

3. this will open the page in your perferred browser and this will also reflect any changes made in vs code in the webpage.
>>>>>>> 81076cd86b6c4ab9ca494786d2ccbd38cd94def2
