# you.home - A Personal Homepage Template

Welcome to `you.home`, a simple, elegant, and highly customizable three-page website template. Perfect for creating a personal portfolio, a landing page, or a small corner on the internet to call your own. The entire template is configured through a single object in each HTML file, making customization easy and code-free.

This template was created by [Lunar.sh](https://www.google.com/search?q=https://me.lunar-sh.de).

## Features

* **Fully Configurable:** No need to dig through HTML. All personal information, content, and settings are managed in a single `config` object in each file.
* **Three Essential Pages:** Includes templates for a Home, About Me, and Projects page.
* **Multiple Layouts:** The "About Me" page comes with several pre-built templates (like `techFocus`, `timeline`, and `gallery`) that you can switch between instantly.
* **Interactive Background:** A beautiful, animated starfield background that subtly reacts to the user's mouse movements.
* **Customizable Theme:** Easily change the background gradient colors to match your personal style.
* **Built-in Credits:** A simple, unobtrusive modal to give credit for any icons or images used.
* **Responsive Design:** Looks great on desktops, tablets, and mobile devices.

## How to Use

Customizing your site is incredibly simple. Just open any of the HTML files (`index.html`, `about.html`, `projects.html`) and find the `<script>` tag at the bottom. Inside, you will see a `config` object. This is where you'll make all your changes.

### 1\. Basic Configuration (`index.html`)

Open `index.html` and edit the `config` object to change your main page.

```javascript
const config = {
    // The base name for your site (e.g., "yourname")
    name: "demo",

    // The name displayed prominently on the page
    username: "DemoUser",

    // Your personal tagline
    tagline: "A demonstration of a configurable template.",

    // Customize the background gradient
    background: {
        colorTop: "#0d0c1d",    // Top color
        colorBottom: "#1e1b4b" // Bottom color
    },

    // A list of your interests that appear on the side
    interests: [
        { name: "Design", tooltip: "Creating beautiful and intuitive user interfaces." },
        { name: "Technology", tooltip: "Exploring new frameworks and building cool things." },
        { name: "Coffee", tooltip: "The fuel that powers creativity." },
    ],

    // Add credits for any assets used
    credits: [
        {
            name: "Favicon Star by Twitter Twemoji",
            link: "https://twemoji.twitter.com/"
        }
    ]
};
```

### 2\. Customizing the "About Me" Page

Open `about.html`. Here you can choose from different templates for your "About Me" section. Simply change the `template` value to one of the available options (`plainText`, `techFocus`, `timeline`, `gallery`, etc.) and fill in the corresponding data.

```javascript
const config = {
    name: "demo",
    background: {
        colorTop: "#0d0c1d",
        colorBottom: "#1e1b4b"
    },
    aboutPage: {
        // CHOOSE YOUR TEMPLATE HERE
        template: "techFocus", // Options: "plainText", "techFocus", "timeline", "gallery"...

        // Fill in the data for the template you chose
        techFocus: {
            title: "My Journey",
            intro: "My journey started with...",
            outro: "This site is my personal playground.",
            languages: [
                { name: "C#", details: "Developed by Microsoft" },
                { name: "Go", details: "Created at Google" },
            ]
        },
        // ... other template configurations
    }
};
```

### 3\. Adding Projects

Open `projects.html`. You can list all of your projects in the `projects` array. To add a new project, just copy and paste one of the blocks. For projects with a banner, provide the image URL; otherwise, leave it as an empty string (`""`).

```javascript
const config = {
    name: "demo",
    background: {
        colorTop: "#0d0c1d",
        colorBottom: "#1e1b4b"
    },
    projectsPage: {
        title: "My Creations",
        projects: [
            {
                title: "Project Alpha",
                // Add a URL for a banner, or leave empty
                banner: "https://images.unsplash.com/photo-1517694712202-14dd9538aa97",
                description: "A sleek, modern dashboard for tracking important metrics.",
                tags: ["JavaScript", "HTML/CSS", "Web"],
                link: "#" // Link to your project
            },
            {
                title: "Project Beta",
                banner: "", // No banner for this one
                description: "A console-based, text-adventure game where every choice matters.",
                tags: [".NET", "C#", "Console App"],
                link: "#"
            },
        ],
        // ... credits
    }
};
```

## Live Examples

Here are a few websites built using a similar structure.

**Note:** These examples were created with an earlier, less-configurable version of this template, so they may not reflect all the current features 1:1.

* [kolbenik.lunar-sh.de](https://kolbenik.lunar-sh.de)
* [me.lunar-sh.de](https://me.lunar-sh.de)
* [cookie.lunar-sh.de](https://cookie.lunar-sh.de)
* [bomb.lunar-sh.de](https://bomb.lunar-sh.de)