# My Awesome Semester

This is a website about your semester — a home page plus one page per course,
each describing the class and the professor teaching it. You will build the
whole thing here, on GitHub.com, in your web browser. You don't need to
download or install anything. Every change you make gets typed and saved
directly on this website.

## A few words you'll see

You don't need to memorize these — just glance back here if one of them
comes up below.

- **Repository** (or "repo") — this project. Everything for the site —
  its pages, its settings, its look — lives in the list of files and
  folders you see when you open this repository on GitHub.
- **File** — one piece of content, like one course's page. You'll open files,
  change their text, and save your changes.
- **Commit** — GitHub's word for "save." Every time you save a change to a
  file, you're making a commit, and you'll type a short note describing
  what you changed (like "Add page for course 3").
- **Front matter** — a small block of settings at the top of a file,
  between two lines that look like `---`. You'll see this in every course
  file — it's covered in detail below.
- **Actions / build** — every time you commit a change, GitHub
  automatically checks that it didn't break anything, then republishes the
  live site. You don't have to do anything to trigger this — it just
  happens.

## The three things you'll do

1. **Set up your site's basic info** — the title, and the address it lives
   at — in one settings file, `_config.yml`.
2. **Write your five course pages** — one file per course, in the
   `_courses` folder, describing the class and researching the professor
   who teaches it.
3. **(Optional, but expected) Customize the look** — colors and fonts, by
   prompting HokieAI.

Each is explained step by step below.

---

## Step 1: Set up your site's basic info (`_config.yml`)

`_config.yml` is the file that holds your site's name, tagline, and web
address. You'll edit it once, near the start.

1. At the top of this repository's file list, click on **`_config.yml`**.
2. On the page that opens, look at the top-right corner of the file and
   click the **pencil icon** (hover over it and it will say "Edit this
   file"). The file becomes editable, with line numbers down the left
   side.
3. Find these lines near the top and change the text after each colon
   (`:`) — leave everything else, including the quotation marks, exactly
   where it is:

   ```yaml
   title: My Awesome Semester
   tagline: A COMM major's course lineup, one class at a time
   description: >-
     A Jekyll template for building a "My Awesome Semester" course-and-teacher
     site. Each course gets its own page with the class details plus a profile
     of the professor teaching it -- their research interests, publications,
     and service and outreach work. Replace this description with your own.
   ```

   - `title` — the name of your site, as it will appear in the browser
     tab and at the top of the home page.
   - `tagline` — a one-line subtitle under the title.
   - `description` — a few sentences about your site. This block spans
     several indented lines (notice the `>-` and the indent) — you can
     rewrite all of those lines, just keep each new line indented the
     same amount as the ones you're replacing.

4. A little further down, find these two lines:

   ```yaml
   url: "https://your-username.github.io"
   baseurl: "/myawesomesemester"
   ```

   These two lines together form your site's web address, and they need
   to match this repository exactly:

   - `url` — look at your browser's address bar right now. It reads
     something like `github.com/YOUR-USERNAME/myawesomesemester`.
     Replace `your-username` inside the quotes with that `YOUR-USERNAME`
     part (everything right after `github.com/`). Keep the quotation
     marks and the rest of the text (`https://` and `.github.io`) exactly
     as it is.
   - `baseurl` — this should already read `"/myawesomesemester"`, which
     matches this repository's name, so you can usually leave it alone.
     Only change it if you renamed the repository — in that case, replace
     `myawesomesemester` with the repository's new name, keeping the
     leading `/` and the quotation marks.

5. Optionally, further down, fill in your own name and email:

   ```yaml
   author: Your Name
   email: your-email@vt.edu
   ```

6. Scroll all the way to the bottom of the page. You'll see a box titled
   **"Commit changes"**:
   - Type a short note in the first box, like `Set up my site info`.
   - Leave **"Commit directly to the `main` branch"** selected.
   - Click the green **Commit changes** button.

Your site's basic info is now set. A build will start automatically — see
[Checking your build](#checking-your-build) below if you want to watch it
finish.

---

## Publishing settings

This site deploys to GitHub Pages automatically, through a workflow file
already included in this repository. Before your very first publish,
someone with access to this repository's settings needs to turn it on:

1. Go to this repository's **Settings** tab, then click **Pages** in the
   left sidebar.
2. Under **Build and deployment → Source**, choose **GitHub Actions**.

After that, every commit to `main` builds and publishes the site
automatically — no further action needed. (Step 4 above already covered
getting `url` and `baseurl` set correctly in `_config.yml`, which this
depends on.)

---

## Step 2: Write your five course pages

Each course has its own file in the `_courses` folder: `course-01.md`
through `course-05.md`. You'll repeat the same steps for each one. This
step has two parts for every course: describing the class, and researching
the professor who teaches it.

### Editing one course page

1. In this repository, click the **`_courses`** folder to open it.
2. Click on a file, for example **`course-01.md`**.
3. Click the **pencil icon** in the top-right corner to start editing.
4. At the top of the file, between the two `---` lines, you'll see the
   **front matter** — the course's settings:

   ```yaml
   ---
   course_number: 1
   course_code: "COMM XXXX"
   course_title: "Course Title 1"
   meeting_time: "MWF 10:10–11:00 AM"
   location: "Building Room ###"
   instructor_name: "Professor Name"
   instructor_title: "Assistant Professor"
   instructor_department: "Department Name"
   ---
   ```

   Replace the placeholder values, keeping the quotation marks around each
   text field:

   | Field | What to put there | Example |
   |---|---|---|
   | `course_number` | Leave this matching the file's number (`course-01.md` → `1`, `course-02.md` → `2`, and so on). It controls the order courses appear in on the home page. | `course_number: 1` |
   | `course_code` | The course's official code, in quotation marks. | `course_code: "COMM 2004"` |
   | `course_title` | The course's title, in quotation marks. | `course_title: "Foundations of Communication Studies"` |
   | `meeting_time` | When the class meets, in quotation marks. | `meeting_time: "MWF 10:10–11:00 AM"` |
   | `location` | Where the class meets, in quotation marks. | `location: "Shanks Hall 130"` |
   | `instructor_name` | Your professor's name, in quotation marks. | `instructor_name: "Dr. Jamie Rivera"` |
   | `instructor_title` | Your professor's academic title, in quotation marks. | `instructor_title: "Associate Professor"` |
   | `instructor_department` | Your professor's department, in quotation marks. | `instructor_department: "Department of Communication"` |

5. Below the second `---` line, delete the placeholder paragraphs and
   write your content in Markdown. The starting sections are:
   - **About this course** — what the class covers and why you're taking
     it.
   - **About [Professor Name]** — a short bio.
   - **Research interests** — what your professor researches.
   - **Publications** — a few of their notable publications.
   - **Service and outreach** — committee work, community partnerships,
     public scholarship, or similar work beyond research and teaching.

   You can rename these headings, reorder them, or add your own — this is
   just a starting point. See the Markdown reference below if you want to
   bold text, add a link, or make a bulleted list.

6. Scroll to the bottom of the page. In the **"Commit changes"** box:
   - Type a short note, like `Add page for course 1`.
   - Leave **"Commit directly to the `main` branch"** selected (or choose
     **"Create a new branch and start a pull request"** if your class is
     having reviews check work before it goes live).
   - Click the green **Commit changes** (or **Propose changes**) button.

### Researching your professor

Before you can write the research sections, you'll need to look some
things up. Good places to start:

- Your professor's **faculty profile page** on their department's website
  — usually has a short bio and a list of degrees.
- Their **personal or lab website**, if they have one — often has the most
  detail on current research.
- **Google Scholar** — search their name to find a list of their
  publications and how often they're cited.
- Their **department's news or "spotlight" pages** — sometimes cover
  outreach, awards, or public-facing work.
- The **syllabus** for the course itself, which sometimes includes a short
  instructor bio.

Write what you find in your own words — don't copy and paste from these
sources. A sentence or two per section is plenty.

### Repeat for all five

Do the same for `course-02.md` through `course-05.md`. You can do them in
any order, and in as many separate visits as you like — each file is
saved the moment you commit it.

### Quick Markdown reference

Your course pages are written in Markdown, a simple way to format text
with plain characters:

| You type | You get |
|---|---|
| `## Heading` | a section heading |
| `**bold text**` | **bold text** |
| `*italic text*` | *italic text* |
| `[link text](https://example.com)` | a clickable link |
| `- item` on its own line | a bulleted list item |
| A blank line between two lines of text | a new paragraph |

---

## Checking your build

Every time you commit a change, GitHub automatically tries to rebuild your
site, whether the commit went straight to `main` or into a pull request.
This catches mistakes — like a missing `---` or a stray quotation mark —
before they can break the live site.

1. Click the **Actions** tab near the top of the repository.
2. Find your commit in the list — it will have the note you typed.
3. Look at the icon next to it:
   - ✅ A green checkmark means the site built successfully.
   - ❌ A red X means something's wrong. Click into that run and read the
     error message — it will usually point at the exact line to fix. Go
     back, edit the file again, and commit the fix the same way.

---

## Step 3: Customize the look with HokieAI

This template ships with a deliberately plain, basic black-and-white
theme — no color, no card layouts, nothing fancy. That's on purpose:
**you're expected to redesign it yourself**, and you're expected to do it
by prompting **HokieAI**, Virginia Tech's instance of NebulaOne, rather
than writing CSS by hand.

The site's colors, fonts, and other visual details are controlled by one
small block of settings near the top of a file called
**`assets/css/main.scss`**, called the **`:root` block**. It looks like
this:

```css
:root {
  --color-bg: #ffffff;
  --color-surface: #ffffff;
  --color-ink: #111111;
  --color-ink-soft: #555555;
  --color-line: #cccccc;
  --color-accent: #000000;
  --color-white: #ffffff;

  --font-body: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
  --font-display: Georgia, "Times New Roman", serif;

  --radius: 0px;
  --shadow: none;
}
```

Every color and font on the site is built from these values, so changing
them re-skins the whole site — no other file needs to change. You don't
need to know CSS to do this. Here's how to get HokieAI to do it for you.

### Finding HokieAI

HokieAI is available to Virginia Tech students through [ai.vt.edu](https://ai.vt.edu)
(log in with your VT credentials). It's the same underlying model family as
tools like ChatGPT or Claude, run on Virginia Tech's own instance, which is
why your class asks you to use it here instead of a generic outside tool.

### Writing your prompt

1. In this repository, open **`assets/css/main.scss`** and copy the
   `:root { ... }` block shown above (or however it currently reads).
2. Open a new HokieAI chat and paste in a prompt like this one — fill in
   the bracketed part with the look you're going for:

   > I have a Jekyll website's CSS custom properties, shown below, for a
   > "My Awesome Semester" course-and-teacher site built for a Virginia
   > Tech COMM major. Right now it's a deliberately plain black-and-white
   > theme. I want the site to feel more like
   > `[describe the look you want — e.g. "a Virginia Tech maroon-and-orange game day feel", "a minimalist academic journal", "a warm library reading room", "a modern tech startup"]`.
   >
   > Please give me back the exact same `:root { ... }` block, with the
   > same variable names, but with new values that achieve that look. Keep
   > `--font-body` and `--font-display` as web-safe font stacks (no
   > external font files, since GitHub Pages needs everything to load
   > without extra setup). Briefly explain what each variable controls.
   >
   > ```css
   > [paste the :root block here]
   > ```

3. Read HokieAI's explanation of what it changed, and ask follow-up
   questions if something isn't clear — for example, "make `--color-accent`
   a bit less bright" or "give me two more color options to compare."
4. Copy the final `:root` block HokieAI gives you.
5. Back on GitHub.com, click the pencil icon on `assets/css/main.scss`,
   select the old `:root { ... }` block and delete it, then paste in the
   new one. **Keep the variable names exactly as they are** — only the
   values after each colon should change — otherwise the rest of the
   stylesheet won't know what to use.
6. Scroll down and commit your change, the same way you did in Steps 1
   and 2. Check the Actions tab for the green checkmark, then refresh the
   live site to see the new look.

### A few prompt variations to try

If you're not sure where to start, try asking HokieAI for a few different
directions and compare them before committing to one:

- *"Make it feel like game day at Lane Stadium — bold, high energy, but
  still readable."*
- *"Make it feel like a minimalist academic CV — restrained, serious,
  lots of whitespace."*
- *"Make it feel like a cozy study nook — warm, soft, slightly informal."*
- *"Keep it black and white, but make the typography more distinctive."*

You can also ask HokieAI to explain *why* a color palette works (or
doesn't) for readability and contrast — that's useful context for
deciding between options, and it's a fair question to ask any LLM you use
for design work.

### What not to change here

The **content** of your course pages — the course descriptions and the
research on your professors — needs to be your own work, not something an
LLM writes for you. Use HokieAI (or any LLM) for the visual design in this
step; keep the research and writing in Steps 1 and 2 in your own words.

---

## Provenance

This repository — the site's structure, theme, and this README — was built
with [Claude](https://claude.ai/code), Anthropic's AI coding assistant.
