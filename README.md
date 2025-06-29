![gambar](https://github.com/user-attachments/assets/48678435-13da-4331-8372-894e1581cc23)

**In This DOCS:**

- [General Info](#youtube-livechat-dummmy-tester-v403)
- [Installation](#-installation--setup-guide)
- [Features](#-features)
- [JSON template](#json-template)
- [Tools That I Use](#tools-that-i-use)
- [Youtube custom CSS Tips & Tricks](#youtube-chat-custom-css-tips--tricks)
- [Update Logs](#update-logs)

# YouTube Livechat Dummmy Tester (v4.0.3)

This is YouTube dummy chat to test your customize YouTube chat CSS for streaming
purposes.

# 🚀 Installation & Setup Guide

Follow these steps to run the project locally on your machine:

### 1. 📥 Clone or Download the Repository

Using Git:

```bash
git clone https://github.com/AkbarFahreza/dummy-yt-livechat.git
```

Or, download the ZIP file from GitHub and extract it manually.

---

### 2. 🖥️ Using Node.js and `http-server`

If you have **Node.js** installed, you can serve the project using
[`http-server`](https://www.npmjs.com/package/http-server):

#### a. Install `http-server` globally (if not installed):

```bash
npm install -g http-server
```

#### b. Navigate to the project folder:

```bash
cd dummy-yt-livechat
```

#### c. Run the server:

```bash
http-server -p 5000 -s
```

> 🔒 The `-s` flag ensures proper routing by serving `index.html` for all paths
> — great for SPAs.

---

### 3. 🧪 Alternative: Using VSCode Live Server Extension

If you're using **Visual Studio Code**, you can run the project with the **Live
Server** extension:

1. Open the project folder in VSCode.
2. Install the **Live Server** extension (if not already).
3. Right-click `index.html` and choose **"Open with Live Server"**.
4. Your project will open in the browser, typically at:

```text
http://127.0.0.1:5500
```

---

### ✅ You're All Set!

You can now start editing the files and see live updates in your browser.

> For any issues or improvements, feel free to open an
> [issue](https://github.com/AkbarFahreza/dummy-yt-livechat/issues) or
> contribute via pull requests!

# ✨ Features

### 🧭 Available Shortcuts

```text
• Ctrl + Space      → Auto Complete
• Ctrl + F          → Find Text
• Ctrl + Shift + R  → Find & Replace
• Ctrl + /          → Toggle Comment
• Alt + Z           → Toggle Word Wrap
```

---

### 🛠️ Editor Capabilities

- 📏 **Resizable Panel**  
  Easily resize the editor panel by dragging its edge to suit your workflow.

- 🎨 **Custom CSS Area**  
  Replace the default code with your own CSS to preview live changes instantly.

- 💾 **Update and Save**  
  Click **"Update CSS"** to store your changes in local storage — no backend
  required.

- 🧪 **Live Background Preview**  
  Add a `background-color` to the `body` element to preview your design.  
  ⚠️ **Development Only** — set it to `transparent` when sending to your client
  for final use.

---

> Looking for more features? Fork the project and customize it to fit your
> needs!

# JSON Template

This is a JSON template for configurating Author name on Youtube chat
dummy/tester

```json
{
  "general-chat": {
    "viewer": {
      "author-name-viewer1": "Dekreza",
      "author-name-viewer2": "Dekreza2",
      "author-name-viewer3": "Dekreza3",
      "author-name-viewer4": "Dekreza4"
    },
    "moderator": {
      "author-name-moderator1": "Dekreza Mod",
      "author-name-moderator2": "Dekreza Mod2",
      "author-name-moderator3": "Dekreza Mod3"
    },
    "member": {
      "author-name-member1": "Member Reza1",
      "author-name-member2": "Member Reza",
      "author-name-member3": "Member Reza"
    },
    "owner": {
      "author-name-owner1": "Owner Reza1",
      "author-name-owner2": "Owner Reza2",
      "author-name-owner3": "Owner Reza3",
      "author-name-owner4": "Owner Reza4"
    }
  },
  "superchat": {
    "author-name-Superchat1": "asas",
    "author-name-Superchat2": "asasa",
    "author-name-Superchat3": "asasasas",
    "author-name-SuperSticker1": "asd",
    "author-name-SuperSticker2": "wew"
  }
}
```

you must only change the value <br/> example :

- change author name viewer 1 value Dekreza into Asep Yukimura
- change author name viewer 2 value Dekreza2 into Asep Yukimura masak

```json
{
 "general-chat": {
   "viewer": {
     "author-name-viewer1": "Dekreza",
     "author-name-viewer2": "Dekreza2",
     "author-name-viewer3": "Dekreza3",
     "author-name-viewer4": "Dekreza4"
```

```json
{
  "general-chat": {
    "viewer": {
      "author-name-viewer1": "Asep Yukimura",
      "author-name-viewer2": "Asep Yukimura masak",
      "author-name-viewer3": "Dekreza3",
      "author-name-viewer4": "Dekreza4"
```

# Tools That I Use

- Designing : [Figma](https://www.figma.com)
- Coding : [VSCode](https://code.visualstudio.com/)
- Convert PNG -> Base64 : [Base64-image](https://www.base64-image.de/)
- Convert SVG -> Base64 :
  [yoksel.github.io/url-encoder](https://yoksel.github.io/url-encoder/)

# Youtube Chat custom CSS Tips & Tricks

Centering event text on header

> Membership Event : Member Gift, Member Join, Member Achievement

```css
ytd-sponsorships-live-chat-header-renderer #header-content-primary-column *,
yt-live-chat-membership-item-renderer #header-content-primary-column * {
  text-align: center !important;
}
ytd-sponsorships-live-chat-header-renderer #content,
yt-live-chat-membership-item-renderer #header-content-primary-column {
  margin: auto !important;
}
```

> Superchat Event

```css
yt-live-chat-paid-message-renderer #single-line * {
  text-align: center !important;
  margin: auto !important;
}
yt-live-chat-paid-message-renderer #single-line {
  display: flex !important;
  flex-direction: column !important;
}
```

Iimportiingg fonts from loal (Installed Fonts)

```css
/* Next Bro is example font*/

@font-face {
  font-family: "Next Bro";
  src: url("Next Bro.ttf");
  src: local("Next Bro"), local("Next Bro"),
    url("Next Bro.ttf") format("truetype");
}

:root {
  --FontFams: "Next Bro", sans-serif;
}
```

Remove like button on the superchat

```css
#action-buttons {
  display: none !important;
}
```

Special code

```css
ytd-sponsorships-live-chat-header-renderer #primary-text,
yt-live-chat-membership-item-renderer #header-primary-text,
yt-live-chat-membership-item-renderer #header-subtext {
  font-family: var(--FontFams) !important;
  font-size: 18px !important;
  font-weight: 700 !important;
}

yt-live-chat-membership-item-renderer:not([show-only-header]) #header-subtext {
  display: none !important;
}
```

# Update Logs

- _1 May 2024_ :
  - **superchat** Removing "show-only-header" and "is-v2-style" attribute,
    adding like button on superchat.
- _2 February 2025_ :
  - **Main page** Added CSS Editor for on-site editing.
- _23 April 2025_ :
  - **Main page** Added Author name configuration to personalize the preview
    test to your audience.
- _01 June 2025_ :
  - Added resizable between preview and code editor
  - Changed the editor theme to Cattpuccin Mocha
  - Restyling autocomplete hints
- _29 June 2025_ :
  - Save the CSS code to local storage when updateing (you won't lose your code
    when refreshing the page)
  - Add reset code button
  - Add download code button
