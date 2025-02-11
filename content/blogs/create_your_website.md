---
title: "How to Create a Personal Website for Your Data Portfolio Using Hugo Templates and GitHub Pages"
date: 2025-02-04T22:53:58+05:30
draft: false
github_link: "https://github.com/diegofernandezarista"
author: "Diego Fernandez Arista"
tags:
  - Hugo
  - GitHub Pages
  - Git
  - Terminal
image: /images/post_create_your_website.png
description: ""
toc: 
---

---

🔍 **Have You Considered Building a Personal Website to Showcase Your Data Portfolio?**  
<p style="text-align: justify;">Whether you are an experienced data professional or looking to break into fields like data analysis, data science, business intelligence, or related areas, having a strong portfolio to showcase your work is crucial. But there's something that can set you apart even further—<b>building a personal brand</b>. A personal website not only gives your projects a polished and professional presentation but also provides a platform to share your insights through a blog.</p>  

📚 **My Journey to Creating a Personal Website for My Portfolio**  
<p style="text-align: justify;">Two weeks ago, I started publishing my projects for my data portfolio. Naturally, my initial thought was to store it on <b>GitHub</b>, which is still a great option for hosting and sharing code.</p> 

<p style="text-align: justify;">However, during my research, I stumbled upon <b>Hugo Templates</b>, a fantastic tool that’s both open-source and completely free. <b>Hugo</b> is a static site generator that allows you to build fast, modern websites effortlessly.</p> 

<p style="text-align: justify;">What made it even better is that it’s fully supported by <b>GitHub Pages</b>, a free service from GitHub that lets you host static websites directly from your repositories. This discovery was a game-changer for me because it meant I could have a beautiful and fully functional personal website to display my portfolio and include a blog section to grow my personal brand.</p>  

### Why Hugo Templates and GitHub Pages?  
1. **💸 Cost-Free:** Both Hugo and GitHub Pages are free, making it an affordable solution.  
2. **🔧 Customization:** Hugo offers a wide range of templates to help you design a professional website without needing advanced coding skills.  
3. **🛠️ Seamless Hosting:** GitHub Pages easily integrates with Hugo, making deployment straightforward.  
4. **💼 Personal Branding:** A blog section allows you to share insights and build authority in your field.  

### What This Guide Covers  
<p style="text-align: justify;">I know there are official guides and documentation available, but I want to make it as straightforward as possible based on my own experience. Below, I’ll provide the exact steps I followed so that you can easily replicate the process and get your website up and running in no time.</p>  

<p style="text-align: justify;"><b>🚀 Ready to Build Your Personal Website?</b>     Let's dive into the step-by-step guide.</p>   

### 1. 🚀 Let's Start with What You Need for Success  

**a. Git**  
- Download Git from this link: [Git Download](https://git-scm.com/downloads)  

**b. PowerShell (not Windows PowerShell, which is different)**  
- I used PowerShell. To install it, open a terminal (Windows PowerShell or Command Prompt) and run the following command:  
```bash
  winget install --id Microsoft.Powershell --source winget
```
- For **_macOS_**, just use the built-in Terminal instead.

**c. Code Editor**
- I recommend [VS Code](https://code.visualstudio.com/)  

**d. Go**
- Download it from this link: [Go Installation Guide](https://go.dev/doc/install)  

**e. Hugo**
- To install Hugo, run PowerShell as an administrator and use this command:
```bash
  winget install Hugo.Hugo.Extended
```
- For **_macOS_**, use:
```bash
  brew install hugo
```

**f. Dart Sass**
- No need to install separately. Dart Sass is included when you install Hugo Extended.

---

### 2. 🗒 Creating the Website

**a. Choose a Theme**
- Visit [Hugo Themes](https://themes.gohugo.io/) and pick a theme you like.

**b. Create a New Hugo Site**
- Open PowerShell (on Windows, the one we installed earlier) or Terminal (on macOS), and run:
  ```sh
  hugo new site personalwebsite
  ```
  ✨ This command will create the base structure for your site.

**c. Navigate to the Themes Folder**
  ```sh
  cd personalwebsite
  cd themes
  ```

**d. Clone the Theme Repository**
- Go to the theme's GitHub page, click **Code**, copy the HTTPS link, and run:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Clone Repository](/images/create_your_website/clone_repository.png)

  ```sh
  git clone <theme-repo-link>
  ```
- Example for the theme I used:
  ```sh
  git clone https://github.com/gurusabarish/hugo-profile.git
  ```
- Once you do that, inside the theme folder—where we are located after step C—you will find a folder named after the template, containing all the files you just cloned (as shown in the photos below).

&nbsp;&nbsp;&nbsp;&nbsp; ![Check clone files](/images/create_your_website/check_clone_files_done.png) ![Check clone files2](/images/create_your_website/check_clone_files2_done.png)

**e. Copy the Configuration File**
- Go to the `exampleSite` folder inside the theme directory, located in `\personalwebsite\themes\hugo-profile\exampleSite\`.
- Look for a configuration file with a `.yaml` or `.toml` extension, such as `config.yaml`, `config.toml`, `hugo.yaml`, or `hugo.toml`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Seek yaml toml](/images/create_your_website/seek_yaml_toml.png)

- Copy this file to the root directory of your new site `\personalwebsite\`:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Where copy yaml toml](/images/create_your_website/where_copy_yaml_toml.png)

- **Important**: <p style="text-align: justify;">When you create your new Hugo website, you'll have a `.toml` or `.yaml` configuration file by default. Delete this file, as you'll be using the one copied from the `exampleSite` folder. If both files exist simultaneously, <b>Step G</b> won’t work.<br><br>
Additionally, if the `exampleSite` folder is not present in the repository you cloned, the configuration for the chosen theme may differ. In that case, please follow the instructions provided in the theme's repository.</p>

**f. Edit the Configuration File**
- Open the file in your code editor and update it with your information.

**g. Preview the Website**
- To see how your site looks, run:
  ```sh
  hugo server
  ```
  ✨ This will create a local server where you can view your site.

<p style="text-align: justify;"><b>NOTE</b>: At this point, most things should work except for images and documents. Let me give you some useful tips to avoid these issues.</p>

**h. Useful Tips**

###### Adding Images
- Place the images inside the `static/images` folder. Just so you know, the static folder is located at the root path where you created your new website. In this example, it's named `\personalwebsite\`.
- First, create the `images` subfolder if it doesn't exist.
- Now you can put images in that folder and reference them using the following path `/images/photo.png`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Add images](/images/create_your_website/add_images.png)

###### Adding Images to Blog Posts
- Create a subfolder inside `images` named after your blog post file.
- Example: If your post is `first_post.md`, create an `images/first_post` folder.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Add images to post](/images/create_your_website/add_images_to_post.png)

- To add an image, use the following format in your post's markdown file:
  ```md
  ![Image Description](/images/first_post/photo.png)
  ```

###### Adding Downloadable Documents
- Create a `documents` subfolder inside `static`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Add documents](/images/create_your_website/add_documents.png)


- Place your file there, then reference it like this:
  ```md
  [Your Resume](documents/your_resume.pdf)
  ```

###### Extra Tip: Adding Blog Sections or Any Other Content
- To create posts or add different pages the template provides, check the `exampleSite` directory to see how the documents are organized and replicate that structure in your main root directory (`\personalwebsite\`). For example, to create a post with the theme I chose, I need to add it to the `content` folder in the root directory where I created my new Hugo website.

---

### 3. 🌐 Hosting Your Website on GitHub Pages

**a. Create a GitHub Account**
- If you don’t have one yet, create an account at [GitHub](https://github.com/).

**b. Create a New Repository**
- Click the + symbol and select **New Repository**.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Create repository1](/images/create_your_website/create_repository1.png)

**c. Repository Name**
- You will see a page prompting you to name your repository.
- To have your page structured as `www.yourname.github.io`, name your repository as `username.github.io` (make sure to include `.github.io` as it’s required for GitHub Pages).
- Select the option to add a **README** file.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Repository name](/images/create_your_website/repository_name.png)

**d. Clone the Repository**
- Open GitHub Desktop and log in with your GitHub account.
- Go to **File > Clone Repository**, select the repository you just created (`username.github.io`), and click **Clone**.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Clone repository github desktop](/images/create_your_website/clone_repository_gituhub_desktop.png) ![Clone repository github desktop select](/images/create_your_website/clone_repository_gituhub_desktop_select.png)

**e. Locate the Cloned Repository Folder**
- A folder with the name `username.github.io` will be created in your Documents on OneDrive (as shown in the photo, unless you selected a different path).

**f. Copy Website Files**
- Copy all the files from your new Hugo website, where you’ve already edited the content based on the information you want to share on your website, into the cloned repository folder.
- **Do NOT copy the .git hidden folders.**
  - To see hidden files, go to **View > Show > Hidden Items** in File Explorer.
  - **Hidden .git folders** can be found inside the **themes folder** and possibly the **root folder** of your Hugo site.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Copy files](/images/create_your_website/copy_files.png)

**g. Commit and Push Changes**
- In GitHub Desktop, you will see all the new files listed as changed because you just copied them.
- Write a commit message (e.g., "Initial commit"), then click **Commit to Main**.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Initial commit](/images/create_your_website/initial_commit.png)

- On the right side of your screen, click **Push to Origin**.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Push origin](/images/create_your_website/push_origin.png)

**h. Verify on GitHub**
- Go to your browser, navigate to your GitHub account, and open the repository. You should see your documents listed.

**i. Configure GitHub Pages**
- Go to **Settings > Pages**, then select **GitHub Actions** as the source.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Github actions](/images/create_your_website/github_actions.png)

**j. Set Up GitHub Actions Workflow**
- Navigate to `OneDrive/Documents/GitHub/username.github.io/` where your repository is located on your computer (based on the example in this guide).
- Create a folder named **.github**, and inside it, another folder called **workflows**.
- Inside **workflows**, create a file named **hugo.yaml**.
- Copy the following code into **hugo.yaml** (you can also find it in the official [Hugo documentation](https://gohugo.io/hosting-and-deployment/hosting-on-github/), specifically in Step 6):

```yaml
# Sample workflow for building and deploying a Hugo site to GitHub Pages
name: Deploy Hugo site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches:
      - main

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

# Default to bash
defaults:
  run:
    shell: bash

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.141.0
    steps:
      - name: Install Hugo CLI
        run: |
          wget -O ${{ runner.temp }}/hugo.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.deb \
          && sudo dpkg -i ${{ runner.temp }}/hugo.deb
      - name: Install Dart Sass
        run: sudo snap install dart-sass
      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: recursive
          fetch-depth: 0
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v5
      - name: Install Node.js dependencies
        run: "[[ -f package-lock.json || -f npm-shrinkwrap.json ]] && npm ci || true"
      - name: Build with Hugo
        env:
          HUGO_CACHEDIR: ${{ runner.temp }}/hugo_cache
          HUGO_ENVIRONMENT: production
          TZ: America/Los_Angeles
        run: |
          hugo \
            --gc \
            --minify \
            --baseURL "${{ steps.pages.outputs.base_url }}/"
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./public

  # Deployment job
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

**k. Verify Workflow Execution**
- Go to the Actions menu on GitHub in your browser. You should see the workflow running and wait until it completes.

![Add workflows](/images/create_your_website/add_workflow.png)

**l. Check Your Live Site**
- Return to Settings > Pages, and you should see that your site is live.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Your live website](/images/create_your_website/your_live_website.png)

---

### Conclusion: Get Started on Your Website Today! 🌟

<p style="text-align: justify;">Building a personal website is an excellent way to showcase your projects, enhance your portfolio, and build a personal brand 💼. With the help of Hugo and GitHub Pages, you can create a professional site that stands out, and it's completely free! 🎉 Follow the steps provided, and in no time, you’ll have a stunning online presence 🌐.</p>

Feel free to reach out if you have any questions along the way 💬—good luck, and enjoy the process! 🚀