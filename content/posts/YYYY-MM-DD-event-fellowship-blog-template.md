---
author: "Your name as you'd like it to be shown on the website"
date: 2025-05-20 # format is YYYY-MM-DD
draft: true
category: 
 - community
 - event-fellowship
 - travel-fellowship
cover:
  image: /wp-content/uploads/YYYY/YYYY-MM-DD-cover-image-name.png
  alt: "Image description for accessibility"

tag:
 - community
 - event-fellowship
 - travel-fellowship

title: "Title of Your Blogpost"
url: /YYYY/MM/DD/YYYY-MM-DD-your-name-blog-title/
---

---
Welcome to the OBF Blog Submission Template!

📌 PLEASE READ CAREFULLY:
Do NOT edit this template file directly. Instead, follow the steps below to submit your blog post.

---

## How to Submit Your Blog Post

### 1. Create a GitHub Account (if needed)

If you don’t have a GitHub account, create one at https://github.com/signup

---

### 2. Fork the OBF Website Repository

Go to the OBF website repository:  
 https://github.com/OBF/OBF.github.io

Click the **"Fork"** button (top right) to create a copy under your GitHub account.

---

### 3. Create a New Blog Post Markdown File

In your forked repository:

1. Navigate to `content/posts/`
2. Click **"Add file" → "Create new file"**
3. Name your file based on the date using the format:  
 `YYYY-MM-DD-your-name-blog-title.md`  
 _Example:_ `2025-04-29-your-name-nfcore-nextflow-hackathon.md`

4. View template raw, and Copy and paste all the contents of this template into the new file.
5. Replace the placeholder text (date, title, author, content, image name, etc.) with your actual blog content.

---

### 4. Upload Your Images

1. Navigate to the folder: `static/img/YYYY/` for the current year
2. Click **"Add file" → "Upload files"**
3. Upload your image(s) here using the format YYYY-MM-DD-image-name.jpg

To insert images in your blog post, use the following format (without the static prefix):

```markdown
![Your image caption](/img/YYYY/YYYY-MM-DD-image-name.jpg)
```

---

### 5. Submit a Pull Request (PR)

Once your edits are complete:

1. Go to your fork’s main page on GitHub
2. Click **"Contribute" → "Open pull request"**
3. Make sure it targets the `main` branch of  
  https://github.com/OBF/OBF.github.io
4. Use the title: `New blog post: [your title] by [your name]`
5. Click **"Create pull request"**

We will review your post, help with final edits, and publish it for you.

---


##  Paste the Reviewed Content below and use the instructions to add images, URLs, etc

Delete the instructions above once you are ready to submit your blog post. Feel free to structure your content as you like, but here are some suggestions to get you started.


# Your Blog Post (do not inlude this line or repeat the title here)

**_The_** [**_Open Bioinformatics Foundation (OBF) Event Fellowship program_**](/travel-awards) **_aims to promote diverse participation at events promoting open-source bioinformatics software development and open science practices in the biological research community. [FULL NAME],_** _**a [YOUR POSITION, e.g., MSc/PhD researcher] at**_ _**[YOUR INSTITUTION]**_, **_was awarded an OBF Event Fellowship to attend_** _**the**_ **_[EVENT NAME](EVENT URL)_**.



## Introduction

Write an engaging intro! What was the event? Where did you go? Why was it exciting?

## Background or Context

What motivated you to apply or attend? How does this relate to your work or goals?

## Key Highlights

Describe the sessions, people, activities, or discoveries that stood out, emphasising how they relate to open science in bioinformatics.

- You can use bullet points
- Or numbered lists
- Or paragraphs with images and links

(Keep this section brief! You're not writing a grant proposal!)

### Add Images

Upload your images to `static/img/YYYY/` for the current year.
Then use the following without the static prefix:

```markdown
![Alt text](/img/YYYY/YYYY-MM-DD-image-name.jpg)
```
#### Add an image to your first paragraph

Due to a quirk in the way our web templating system is set up, you need to include an image in the opening paragraph in order to have it show up on the [Posts page](https://www.open-bio.org/blog/).
You can put a good image (ideally, one that shows you at the conference, and is more wide than tall) at the end of the canned text about the OBF Event Fellowship,
on the next line but with no blank line in between.
See, for example, https://github.com/OBF/OBF.github.io/blob/main/content/posts/2025-08-25-Tayyaba-Alvi-ISMB2025.md.

### Add Links

```markdown
[Link text](https://example.com)
```

Example: [OBF Event Fellowship](https://www.open-bio.org/event-awards/)

### Add Code Blocks

There's probably no need to add code blocks to a blog post, but if you do, use fenced blocks:

\`\`\`bash
nextflow run awesome-workflow.nf
\`\`\`

### Add Videos

You can embed a video with a simple link or screenshot and description.

Example:

[Watch on YouTube](https://www.youtube.com/watch?v=ju_-yUELgAc)

---

## Reflections

What did you learn? Who did you connect with? How will you promote open science in Bioinformatics?

---

## Acknowledgements

Thank your funders, mentors, collaborators, or community members.

---

Ready to Submit?  
Follow the pull request steps above under “ How to Submit Your Blog Post”
