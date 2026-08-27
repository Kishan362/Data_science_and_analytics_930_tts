# What is Web Hosting?

**Web hosting** is a service that allows individuals and organizations to make their websites accessible on the internet. A web hosting provider allocates space on a server (computer) to store your website files (HTML, CSS, images, JavaScript) so that anyone with an internet connection can access your website by typing your domain name.

## How Does Web Hosting Work?

1. You create a website with HTML, CSS, JavaScript, and other files.
2. You purchase a hosting plan from a web hosting provider.
3. You upload your website files to the hosting server.
4. Your domain name is connected to the server (using DNS).
5. When someone types your domain name, the server delivers your website to their browser.

---

## Types of Web Hosting

### 1. Shared Hosting
- Multiple websites share the same server and its resources (CPU, RAM, bandwidth).
- Most affordable hosting option.
- Good for small websites and beginners.
- Limited performance and resources.
- Examples: Hostinger, Bluehost, GoDaddy, HostGator.

### 2. Virtual Private Server (VPS) Hosting
- A physical server is divided into virtual servers.
- Each website gets its own dedicated resources.
- Better performance and control than shared hosting.
- More expensive than shared hosting.
- Examples: DigitalOcean, Linode, Vultr, A2 Hosting.

### 3. Dedicated Server Hosting
- An entire server is dedicated to your website alone.
- Maximum performance, security, and control.
- Most expensive hosting option.
- Best for large, high-traffic websites.
- Examples: AWS Dedicated, OVH, Liquid Web.

### 4. Cloud Hosting
- Uses a network of virtual and physical cloud servers.
- Resources can be scaled up or down as needed (scalable).
- High uptime and reliability.
- Pay for only what you use.
- Examples: AWS, Google Cloud Platform, Microsoft Azure, Cloudflare.

### 5. Managed WordPress Hosting
- Specialized hosting optimized for WordPress websites.
- Includes automatic updates, backups, and security.
- Examples: WP Engine, Kinsta, SiteGround.

### 6. Free Hosting
- Free web hosting with limited features and resources.
- Usually includes ads on your website.
- Not recommended for professional websites.
- Examples: InfinityFree, 000Webhost, GitHub Pages.

---

## Popular Web Hosting Providers

| Provider | Starting Price | Best For |
|----------|---------------|----------|
| Hostinger | ~$1.99/month | Beginners |
| Bluehost | ~$2.95/month | WordPress sites |
| GoDaddy | ~$5.99/month | Small businesses |
| AWS | Pay as you go | Enterprise & Cloud |
| Google Cloud | Pay as you go | Cloud hosting |
| GitHub Pages | Free | Static websites & portfolios |

---

## How to Create a Live Data Analytics Portfolio

### What is a Data Analytics Portfolio?
A data analytics portfolio is a website that showcases your data analysis projects, skills, tools, and achievements. It helps potential employers or clients see your work and abilities.

### Steps to Create a Live Portfolio

#### Step 1: Plan Your Portfolio
Include these sections:
- **Home Page** - Your name, title, and a brief introduction.
- **About Me** - Your education, skills, and background.
- **Projects** - Details of your data analytics projects with screenshots.
- **Skills** - Tools and technologies you know (Excel, Python, SQL, Tableau, Power BI).
- **Resume** - Download link for your resume.
- **Contact** - Your email, LinkedIn, and other social links.

#### Step 2: Create the HTML File

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Data Analytics Portfolio - John Doe</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }
        body {
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 40px 20px;
        }
        header h1 {
            font-size: 2.5em;
        }
        header p {
            font-size: 1.2em;
            margin-top: 10px;
        }
        nav {
            background-color: #34495e;
            text-align: center;
            padding: 10px;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-size: 1em;
        }
        nav a:hover {
            color: #1abc9c;
        }
        .container {
            max-width: 900px;
            margin: 30px auto;
            padding: 0 20px;
        }
        section {
            background-color: white;
            margin-bottom: 20px;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        section h2 {
            color: #2c3e50;
            margin-bottom: 15px;
            border-bottom: 2px solid #1abc9c;
            padding-bottom: 5px;
        }
        .project {
            background-color: #ecf0f1;
            padding: 15px;
            margin: 10px 0;
            border-radius: 5px;
        }
        .project h3 {
            color: #2c3e50;
        }
        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        .skills-list span {
            background-color: #1abc9c;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9em;
        }
        footer {
            text-align: center;
            padding: 20px;
            background-color: #2c3e50;
            color: white;
        }
    </style>
</head>
<body>

<header>
    <h1>John Doe</h1>
    <p>Data Analyst | Excel | Python | SQL | Tableau</p>
</header>

<nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#projects">Projects</a>
    <a href="#skills">Skills</a>
    <a href="#contact">Contact</a>
</nav>

<div class="container">

    <section id="home">
        <h2>Welcome to My Portfolio</h2>
        <p>Hello! I am John Doe, a passionate Data Analyst with experience in transforming raw data into actionable insights. I specialize in data visualization, statistical analysis, and business intelligence.</p>
    </section>

    <section id="about">
        <h2>About Me</h2>
        <p>I have completed my Bachelor's degree in Computer Science and hold a Google Data Analytics Professional Certificate. I enjoy working with data to solve real-world problems and help businesses make data-driven decisions.</p>
    </section>

    <section id="projects">
        <h2>My Projects</h2>

        <div class="project">
            <h3>Sales Data Analysis</h3>
            <p>Analyzed 2 years of sales data using Excel and Python. Created interactive dashboards to track revenue, profit margins, and regional performance.</p>
        </div>

        <div class="project">
            <h3>Customer Segmentation</h3>
            <p>Used SQL and Python to segment customers based on purchasing behavior. Identified key customer groups for targeted marketing campaigns.</p>
        </div>

        <div class="project">
            <h3>HR Analytics Dashboard</h3>
            <p>Built a Power BI dashboard to visualize employee attrition, satisfaction scores, and performance metrics for a company of 500+ employees.</p>
        </div>
    </section>

    <section id="skills">
        <h2>Skills & Tools</h2>
        <div class="skills-list">
            <span>Excel</span>
            <span>Python</span>
            <span>SQL</span>
            <span>Tableau</span>
            <span>Power BI</span>
            <span>Google Sheets</span>
            <span>Pandas</span>
            <span>NumPy</span>
            <span>Matplotlib</span>
            <span>Statistics</span>
        </div>
    </section>

    <section id="contact">
        <h2>Contact Me</h2>
        <p>Email: john.doe@email.com</p>
        <p>LinkedIn: linkedin.com/in/johndoe</p>
        <p>GitHub: github.com/johndoe</p>
    </section>

</div>

<footer>
    <p>&copy; 2026 John Doe. All Rights Reserved.</p>
</footer>

</body>
</html>
```

#### Step 3: Host Your Portfolio (Free Options)

**Option A: GitHub Pages (Recommended - Free)**
1. Create a GitHub account at github.com.
2. Create a new repository named `yourusername.github.io`.
3. Upload your `index.html` file to the repository.
4. Go to Settings > Pages > Select the main branch.
5. Your portfolio is now live at `https://yourusername.github.io`.

**Option B: Netlify (Free)**
1. Create an account at netlify.com.
2. Drag and drop your folder containing `index.html`.
3. Netlify will provide a live URL for your portfolio.

**Option C: Vercel (Free)**
1. Create an account at vercel.com.
2. Import your project from GitHub or upload files.
3. Vercel deploys it and gives you a live link.

---

## Short Answer

Web hosting is a service that stores your website files on a server and makes them accessible on the internet. Types of hosting include Shared, VPS, Dedicated, Cloud, and Free hosting. A data analytics portfolio can be created using HTML/CSS and hosted for free on GitHub Pages, Netlify, or Vercel.
