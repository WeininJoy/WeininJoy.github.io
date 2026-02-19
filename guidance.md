This is a great project. Christopher Lovell’s website is a classic **academic/portfolio site** (likely built with Jekyll or Hugo). It features a **two-column layout**: a fixed sidebar on the left (photo, navigation, links) and scrolling content on the right.

Since you are using **Claude Code** (the CLI tool), the best approach is to treat it like a senior developer sitting next to you. You shouldn't give it one massive command; instead, you should set the context and then iterate.

Here is a step-by-step guidance strategy to feed into Claude Code.

---

### Phase 1: Context & Analysis
*First, you need to let Claude understand what you have and what you want. Open your terminal in the folder where you downloaded your template and run `claude`.*

**Copy and paste this prompt first:**

> "I am working on a personal portfolio website hosted on GitHub Pages. I have downloaded a template in this directory.
>
> My goal is to modify this template to aesthetically and structurally resemble this website: https://www.christopherlovell.co.uk/
>
> Key design targets:
> 1. **Layout:** A fixed sidebar on the left containing my profile picture, name, navigation links, and social icons.
> 2. **Content:** A clean, minimal main content area on the right.
> 3. **Style:** Minimalist, academic aesthetic. Clean typography, white/grey background.
>
> First, please analyze the file structure of the current directory. Tell me what technology this template uses (e.g., plain HTML/CSS, Jekyll, Hugo, React) and propose a plan to convert this template into the target layout."

---

### Phase 2: Structural Transformation
*Once Claude analyzes the files, it will tell you if it's Jekyll, HTML, etc. Now, ask it to build the skeleton.*

**Prompt for the Layout:**

> "Let's start with the layout. I want to implement the 'Sidebar' design.
>
> Please modify the CSS and HTML (or layout templates) to create a two-column grid:
> 1. **Left Column (Sidebar):** Fixed width (approx 250-300px), fixed position. It should contain a placeholder for an image, a heading for my name, and a vertical navigation menu.
> 2. **Right Column (Main):** Takes up the remaining width and allows for scrolling.
>
> Please apply these changes now so I can verify the structure."

---

### Phase 3: Styling (CSS)
*After the layout is broken into two columns, it will likely look ugly. Now you style it to match the Lovell example.*

**Prompt for Styling:**

> "The layout structure is there, but the styling needs to match the reference. Please update the CSS to match https://www.christopherlovell.co.uk/ more closely.
>
> Focus on these tasks:
> 1. **Sidebar:** Darker background or distinct border, circular profile image styling, and clean social icons at the bottom.
> 2. **Typography:** Use a clean sans-serif font (like Roboto, Lato, or Helvetica) for headers and a readable serif or sans-serif for body text.
> 3. **Navigation:** Make the links in the sidebar look like clean text (no bullet points, change color on hover).
>
> Update the necessary stylesheets."

---

### Phase 4: Content & Personalization
*Now that it looks right, you need to add your actual data.*

**Prompt for Content:**

> "Now let's update the content.
>
> 1. Change the name in the sidebar to [Your Name].
> 2. Change the profile image source to [Your Image Filename] (I will place the image in the images folder).
> 3. Create navigation links for: 'Home', 'Research', 'CV', and 'Contact'.
> 4. In the main content area, create a 'About Me' section with some placeholder Lorem Ipsum text.
>
> If this is a static site generator (like Jekyll), please show me which config files (`_config.yml`) or markdown files I need to edit to make these changes permanent."

---

### Phase 5: GitHub Pages Configuration
*Finally, ensure it runs on GitHub.*

**Prompt for Deployment:**

> "I need to ensure this is ready for GitHub Pages.
>
> 1. Check if there are any specific configuration files (like `_config.yml` or `package.json`) that need to be updated to handle the base URL or build process.
> 2. If this requires a build step, please create a GitHub Actions workflow file (`.github/workflows/gh-pages.yml`) for me.
> 3. If it is just static HTML, confirm that the entry point is `index.html`."

---

### Tips for working with Claude Code

1.  **Iterate Small:** Don't ask for the whole website in one go. Do Layout -> Style -> Content.
2.  **Provide Feedback:** If Claude makes the sidebar too wide, say: *"The sidebar is too wide. Please reduce it to 250px and ensure it stays fixed when I scroll the main page."*
3.  **Read the Plan:** Claude Code usually lists what it's going to do before it does it. Read that list. If it plans to delete a file you think is important, tell it to stop.
4.  **The "Compact" Command:** If the conversation gets too long and Claude gets confused, type `/compact` (if available in your version) or simply start a new session, pointing it to the files it just modified.

**Do you know if the template you downloaded is plain HTML or a generator like Jekyll?** (If you don't know, running the Phase 1 prompt will figure that out for you).
