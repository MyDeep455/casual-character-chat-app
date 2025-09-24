# Casual Character Chat

Welcome! This application is a fully functional, 100% private app designed for creating, managing, and interacting with your own detailed AI characters. The core feature is the ability to engage in dynamic, text-based role-playing chats with the characters you build.

This app is a from-scratch development, inspired by many existing AI Chat platforms, but designed to include all the features most users want and offer maximum intuitiveness. My goal was to create a completely free, private, and uncensored character chat application that anyone can use forever on their own computer.

### Upcoming Features

Here are some of the features planned for future updates:

* AI-powered reply suggestions for users to help drive the conversation forward.
* A fully responsive design for a seamless experience on mobile devices.
* In-chat AI image generation to visualize characters and scenes.

---

### A Note on Your Data & Privacy

Your privacy is paramount. All of your data (including every character you create, all your chat histories, images, and your personal settings) is stored directly on your computer inside your browser's secure **IndexedDB** database. This means your data remains entirely on your device, is preserved even after you close the browser tab, and can never be accessed by anyone else.

---

## Bug Reports & Suggestions

If you find a bug or have an idea for a new feature, please let me know! The best way to do this is to open a new ticket in the [Issues tab of this repository](https://github.com/MyDeep455/casual-character-chat-app/issues) or click on the Help & FAQ button in the app and send me an anonymous message from there.

---

## 1. The Main Screen: Character Selection

This is the first screen you see when you open the app. From here, you can access all of your characters and core features.

### The Top Bar (Header)

The header provides access to the app's main functions:

* **🤖 + Create Character:** Click this to open the Character Editor and start building a new AI character from scratch.
* **🎭 Manage Personas:** This opens a panel where you can create and manage your different user profiles, or "Personas." A Persona defines who *you* are in a chat.
* **⚙️ App Settings:** This is where you enter your custom proxy URL and manage your list of available AI models.
* **⬆️ Import / ⬇️ Export:** These buttons allow you to save your entire collection (characters, personas, and app settings) into a single `.json` file for backup or migration.
* **🔄️ Update:** This link takes you to this GitHub repository, where you can check for new versions.
* **❓Help:** This button opens the detailed help and FAQ document.

### ⭐ The Favorites Bar

This bar gives you quick access to your most-used characters. To add a character, simply hover over their card in the main list and click the star icon (★).

### 🔎 The Search Bars

To find specific characters quickly, the app features two separate search bars:

* **Search Name:** Filters the character list in real-time as you type a character's name.
* **Search Tag:** Filters the list based on the tags you've assigned to your characters in the character editor.

### The Character List & Cards

All of your non-archived characters are displayed here as individual cards, automatically sorted in alphabetical order. Clicking a card takes you to that character's chat dashboard. When you hover over a card, two buttons appear:

* **Favorite Button (★):** Adds or removes the character from your Favorites Bar.
* **Archive Button (↓/↑):** Moves a character to the archive or restores them to the main list.

### 🗑️ Bulk Delete & 🗃️ Archive

* **Bulk Delete Button:** Opens a modal where you can select and delete multiple characters at once.
* **The Archive:** This collapsible section at the bottom holds all archived characters to keep your main screen clean. It only appears if you have at least one character in the archive.

---

## 2. The Chat Dashboard

After clicking on a character card, you land on their personal dashboard, the hub for all conversations with that character.

### Header & Management

* **← Back to Main Menu:** Returns to the character selection screen.
* **Delete Character:** Permanently deletes the character and all their chats (with confirmation).
* **Edit Character:** Opens the Character Editor for the current character.
* **Copy Character:** Creates an exact duplicate of the character (without chat history), perfect for creating variations.

### Saved Chats

This section lists all separate chat sessions with this character.

* **+ Start new Chat:** Begins a new conversation. If scenarios exist, you'll be prompted to choose one or start an empty chat.
* **Chat Entries:** Each saved chat can be individually **Renamed** or **Deleted**.

---


## 3. The Character Editor

This is where you bring your characters to life. All changes you make here take effect immediately, even in ongoing chats.

### Key Input Fields

* **Character Name & In-Chat Name:** The official name for the card and the (potentially shorter) name used in dialogue.
* **Avatar & Background URL:** Direct links or local file uploads (via the 📁 icon) for the character's profile picture and chat background.
* **Character Description:** The most crucial field. Describe identity, personality, appearance, abilities, speech style, and provide dialogue examples. A good length is between 500-1000 words.
* **Lorebook:** For deeper background information, world-building details, relationships, or any facts the AI should know that don't fit into the core personality description.
* **Tags:** Add comma-separated keywords to help you organize and find your characters (e.g., "anime, fantasy, villain").
* **AI Instructions:** General, system-level commands for the AI's behavior (e.g., "Write short and creative sentences."). If possible, keep your instructions concise. It will be easier then for the AI to follow your prompts. Less is more!
* **Character & Narrator Reminders:** Short, critical instructions attached to every message to prevent the AI from forgetting key details. Use the dynamic placeholder `{{char}}` to automatically insert the character's name for the AI. If the AI ignores some of your AI Instructions, you can put them here. Reminders have very high priority for the AI. But here too: keep it concise.

### Dynamic Scenario Management

Scenarios are pre-written starting points for a chat. Each scenario consists of a **Title** and a **Description** (the opening message). You can add, edit, and delete as many scenarios as you like for each character.

---

## 4. The Chat: Interacting with the AI

This is where the magic happens. The chat screen is designed to be immersive and give you full control over the conversation.

### The Chat Header

The top bar provides context and quick access to important features:

* **← Back Arrow:** Returns you to the character's chat dashboard.
* **Participant Icons:** In a group chat, icons of all participants appear here. Click an icon to remove that character.
* **Token Info (ℹ️):** Hover to see an estimate of the tokens being used in the current context.
* **Add Participant (👥+):** Opens a menu to add another character to the conversation.
* **Select Persona (🎭):** Allows you to choose one of your user profiles for the chat. This choice is final for the chat session to ensure consistency.
* **Settings (⚙️):** Toggles the settings panel for live customization.

### The Settings Panel

This panel lets you customize the chat's appearance and the AI's behavior on the fly:

* **Appearance:** Adjust font size, message spacing, chat bubble colors & opacity, a "frosted glass" blur effect, and the character's avatar size.
* **AI Behavior:**
    * **AI Model:** Select the AI model for the responses from the list you configured in the global App Settings.
    * **Temperature:** The most important slider for creativity. Lower values (e.g., 0.7) are more focused; higher values (e.g., 1.0+) lead to more creative but potentially chaotic responses.
    * **Frequency & Presence Penalty:** These sliders can help reduce repetition but are often ignored by a lot of free AI models. It's recommended to use Temperature for creative control.
* **Notification Sound:** A toggle for the sound effect when a message is received.

### Message Interaction

* **Editing:** **Double-click** any message bubble to open the message editor. Press `ENTER` or double-click outside the editor to save.
* **Deleting:** Hover over a message to reveal a trashcan icon (🗑️). Clicking it deletes that message **and all subsequent messages**, allowing you to rewind the story.
* **Response Variations:**
    * **Browse:** Use the `<` and `>` buttons (or Left/Right Arrow keys) to cycle through different AI-generated responses for the same prompt.
    * **Regenerate (⟳):** Generates a new response variation.
    * **Continue (»):** Prompts the AI to intelligently continue its last message, perfect for extending a good response.
* **AI Thoughts:** If the AI model provides them, its reasoning will appear in a collapsible `think;` block above the main message.

### The Input Area

* **💬 Character vs. 📖 Narrator:** Use the `Character` button for standard dialogue and the `Narrator` button for third-person, omniscient narration.
* **Stopping a Response (🟥):** A red stop button appears while the AI is generating a response. Click it to cancel the request immediately.
* **Empty Submission:** Clicking either send button with an empty input field prompts the AI to continue the story based on the last message.

---

## 5. Persona Management

While characters are the AI entities you talk to, a **Persona** is a reusable profile for **you**, the user. It defines your name, appearance, and role, giving the AI crucial context about who it's talking to.

### Managing Your Personas

* Click the **🎭 Manage Personas** button on the main screen to open the management window.
* From here, you can **Create**, **Edit**, and **Delete** your personas.
* The Persona Editor includes fields for a name, description, avatar URL, and a live token counter.

### Using a Persona

* In a new chat, click the **🎭 Select Persona** button in the header to choose a profile for that session.
* Once selected, your persona's avatar will appear next to your messages (if you linked/uploaded an avatar image), and its description will be included in the context sent to the AI.

---

## 6. Group Chats

You can turn any conversation into a group chat with multiple AI characters.

* **Adding Participants:** Click the **Add Participant (👥+)** button in the chat header to open a selection screen and add any of your other characters to the chat.
* **Removing Participants:** Click the small icon of a character in the chat header to remove them.
* **Addressing Specific Characters:** To direct your message to a specific character, start your message with a `/` followed by their name (e.g., `/Alice "What do you think?"`).
    * When the input field is empty, clickable **tag suggestions** will appear above it to make this easier.

---

## 7. Import, Export & Backups

Your data is stored locally in your browser, which is great for privacy but can be at risk if your browser data is cleared. This feature is the best way to safeguard your creations. Ideal for:

* **Backups:** Create a safe copy of all your characters, personas, and app settings.
* **Migration:** Easily move your entire collection to a different computer or browser.

### How to Export

Exporting creates a single `.json` file containing all your data, including uploaded images.

1.  Click the **⬇️ Export** button in the main screen header.
2.  Your browser will open a "Save File" dialog.
3.  Choose a safe location on your computer and click "Save". That's it!

### How to Import

1.  Click the **⬆️ Import** button in the header.
2.  Select the `.json` backup file from your computer.
3.  Confirm the import. The app will merge the data, adding new characters and personas without overwriting your existing ones.

---

## 8. Frequently Asked Questions (FAQ)

**Q: My AI's responses are weird/short/repetitive. What can I do?**
A: This depends on your prompts and settings. Try these steps:
* **Improve Prompts:** A detailed `Character Description` is the most important factor. Also, tell the AI in the Character Reminder to drive the plot forward to the next scene.
* **Adjust Temperature:** In the chat settings, a lower value is more focused, a higher value is more creative.
* **Regenerate:** Use the `⟳` button. The AI's second or third try is often better.
* **Change the Topic:** Introduce a new situation to give the AI fresh input.

**Q: The app is slow, or the AI isn't responding. What's wrong?**
A: This can happen if the free cloud server is waking up from sleep ("Cold Start") or experiencing high traffic. The app will retry automatically. Please be patient; the first message after a long break can take 20-50 seconds. Subsequent messages will be fast. This is a small price to pay for a completely free server of your own. Please note: In rare cases, the API provider (e.g., Openrouter) may experience technical difficulties. In such cases, we simply have to wait.

**Q: What's the difference between `Character Description` and `Lorebook`?**
A: The `Character Description` is the active personality—*who the character is*. The `Lorebook` is background knowledge—*what the character knows*. This separation helps the AI focus on role-playing while still having access to deeper context. However, the Lorebook can also be regarded as an all-knowing encyclopedia about the world and various individuals besides your character. Also, the lorebook can be much longer, with up to 5,000 words or even more, and the AI only picks out what is relevant for a particular scene.

**Q: Why are my Characters and Personas suddenly gone?**
A: This happens if your browser's site data was deleted. This can be caused by browser settings that clear data on close or by manually clearing your cache. Use the **Export** feature regularly to create backups!


### Quick Troubleshooting

* **Problem: My very first chat message fails with a 404 error or "AI Model did not respond after multiple retries"!**
  * **Solution:** This is normal. Your new server on Render needs about 60 seconds after the first deployment to be fully ready. Wait a minute and try sending the message again. It's a one-time effect and afterwards everything should work perfectly fine.

* **Problem: The deployment log on Render shows warnings.**
  * **Solution:** Warnings like `No license field` are completely harmless and can be ignored. As long as the log ends with `Server is running on port 3000 and is ready for connections`, everything is working perfectly.

---

## 9. Tutorial: Setup - API & Server (Required)

Everyone can do this easily within a few minutes! Do it and you'll have your own AI Chat platform on your computer forever.

To give you full control and keep this app free and private, you need to connect your own API key and setup a free server. This guide will walk you through the process.

The process has four easy parts:
1.  Download the app and open it - no installation needed!
2.  Get a free API Key from **OpenRouter** with a few clicks.
3.  Set up your own secure Backend Proxy with a single click using **Render**.
4.  Connect the app to your new proxy by copy & paste just one URL.

### Part 1: Downloading and Running the App

First, you need to download the app files to your computer.

1.  **Download the Code:** On the main page of this GitHub repository, click the green **<> Code** button and then select **Download ZIP**.
2.  **Unzip the File:** Find the downloaded `.zip` file on your computer (usually in your "Downloads" folder) and unzip/extract it. You will now have a folder with all the app files.
3.  **Open the App:** Open the new folder and simply double-click the **`index.html`** file. The app will open in your default web browser and is ready for the quick setup below.

### Part 2: Getting Your API Key from OpenRouter

1.  **Create an Account:** Go to [OpenRouter.ai](https://openrouter.ai) and create a free account.
2.  **Add Credits (recommended):** You get 50 messages per day for free. However, for regular use you should add 10 Credits ($10) only one time. Then you'll have 1,000 free meesages per day, forever, even if you spend your 10 Credits. Go to your **Settings -> Credit & Usage** to add the Credits with a one-time-payment.
3.  **Create a New Key:** Go to your **Keys** page, click "Create Key," and give it a name.
4.  **Copy Your Key:** Copy the key that starts with `sk-or-v1-...`. **You will not see the full key again after leaving this page, so save it somewhere safe!**

### Part 3: Setting up Your Personal Backend Proxy Server

Your API key must be kept secret. This one-click process sets up a secure "messenger" on the internet for free that safely holds your key. Without such a Server it would be highly unsafe. This is mandatory for your own protection, so that no one can ever see your secret API:

1.  **Click this Deploy Button:** This will take you to Render.com and automatically set up the proxy server code for you.

    [![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/MyDeep455/casual-character-chat)

2.  **Connect GitHub & Create a Render Account:** Render will ask you to connect a GitHub account to access the code. If you don't have one, you can create one for free. Then, sign up for a free Render account.

3.  **Configure the New Service:** Render will guide you through the setup. You only need to fill out two things:
    * **A unique name** for your service (e.g., `my-ai-chat-proxy-123`).
    * Under the **"Environment"** section, click **"Add Environment Variable"**:
        * **Key:** `OPENROUTER_API_KEY` (name it exactly like that!)
        * **Value:** Paste your API key from Part 1.

4.  **Deploy:** Scroll down, ensure the **"Free"** plan is selected, and click the final button **"Create Web Service"** (or you might see something like "Deploy" as final button). The deployment might take a few minutes.

5.  **Get Your URL:** Once successful, Render will show you the URL for your new service at the top of the page (e.g., `https://my-ai-chat-proxy-123.onrender.com`). **Copy this URL.**

PLEASE NOTE: After your server goes live for the first time, give it about a minute to fully initialize. Otherwise, your very first chat request to the new server may fail. In that case, simply try it again after a few minutes. This is a one-time effect that only occurs during the very first start.

### Part 4: Connecting the App to Your New Proxy

1.  **Open App Settings:** In the Casual Character Chat app, click the **⚙️ App Settings** button on the main screen.
2.  **Enter Your URL:** Paste the URL you just copied from Render into the **"Backend Proxy URL"** field.
3.  **Save Settings.** You're done! The app is now fully connected and you can start chatting with your characters. Enjoy!
