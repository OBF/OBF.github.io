---
author: yourusername
date: yyyy-mm-dd
draft: true
category: 
 - community
 - event-fellowship
 - travel-fellowship
cover:
  image: /wp-content/uploads/YYYY/your-cover-image.png
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
3. Name your file using the format:  
 `YYYY-MM-DD-your-name-blog-title.md`  
 _Example:_ `2025-04-29-your-name-nfcore-nextflow-hackathon.md`

4. Copy and paste all the contents of this template into the new file.
5. Replace the placeholder text (title, author, content, image name, etc.) with your actual blog content.

---

### 4. Upload Your Images

1. Navigate to the folder: `static/img/2025/`
2. Click **"Add file" → "Upload files"**
3. Upload your image(s) here.

To insert images in your blog post, use the following format:

```markdown
![Your image caption](/wp-content/uploads/YYYY/your-image-name.jpg)
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


# Your Blog Post

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

### Add Images

Upload your images to `static/img/2025/`  
Then use:

```markdown
![Alt text](/wp-content/uploads/YYYY/your-photo.jpg)
```

Example:

![Group photo at hackathon](/wp-content/uploads/YYYY/hackathon-group.jpg)

### Add Links

```markdown
[Link text](https://example.com)
```

Example: [OBF Event Fellowship](https://www.open-bio.org/event-awards/)

### Add Code Blocks

Use fenced blocks:

\`\`\`bash
nextflow run awesome-workflow.nf
\`\`\`

### Add Videos

Embed a video with a simple link or screenshot and description.

Example:

[Watch on YouTube](https://www.youtube.com/watch?v=ju_-yUELgAc)

---

## Reflections

What did you learn? Who did you connect with? How will you promote open science in Bioinformatics?

---

## Acknowledgements

Thank your funders, mentors, collaborators, or community members.

> "Thank you OBF Event Fellowship for supporting my travel to [Event Name]!"

---

Ready to Submit?  
Follow the pull request steps above under “ How to Submit Your Blog Post”
