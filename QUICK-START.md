# 🚀 AI TWIN - QUICK START GUIDE

**Get your AI Twin running in 10 minutes**

---

## Step 1: Deploy GAS Backend (5 minutes)

1. **Open Google Apps Script**
   - Go to https://script.google.com
   - Create new project: "AI Twin Backend"

2. **Create 3 Script Files:**
   - **Code.gs** - Paste the code from Code.gs
   - **GeminiService.gs** - Paste the code from GeminiService.gs  
   - **SheetsDB.gs** - Paste the code from SheetsDB.gs

3. **Configure API Key:**
   - In `GeminiService.gs`, line 1:
   - Replace `YOUR_GEMINI_API_KEY_HERE` with your actual Gemini API key

4. **Deploy as Web App:**
   - Click **Deploy** → **New Deployment**
   - Type: **Web App**
   - Execute as: **Me**
   - Who has access: **Anyone**
   - Click **Deploy**
   - **Copy the Web App URL** (looks like: `https://script.google.com/macros/s/...`)

---

## Step 2: Configure Frontend (2 minutes)

1. **Open index.html**
   - Find line 93: `API_URL: 'YOUR_GAS_WEB_APP_URL_HERE'`
   - Replace with your Web App URL from Step 1

2. **Create Icons (Optional)**
   - Create simple 192x192 and 512x512 PNG icons
   - Name them `icon-192.png` and `icon-512.png`
   - Or skip for now (app will still work)

---

## Step 3: Deploy Frontend (3 minutes)

### Option A: GitHub Pages (Free, Easy)
1. Create new GitHub repo: "ai-twin"
2. Upload files:
   - index.html
   - service-worker.js
   - manifest.json
   - icon-192.png (optional)
   - icon-512.png (optional)
3. Go to Settings → Pages
4. Source: Deploy from main branch
5. Your URL: `https://yourusername.github.io/ai-twin`

### Option B: Netlify (Free, Even Easier)
1. Drag and drop your folder to https://app.netlify.com/drop
2. Done! You get instant URL

### Option C: Local Testing
1. Install simple HTTP server:
   ```bash
   npm install -g http-server
   ```
2. Run in your folder:
   ```bash
   http-server
   ```
3. Open: http://localhost:8080

---

## Step 4: Test It! (2 minutes)

1. **Open your deployed URL**
2. **Try typing a message:**
   - "Hey, this is Graham testing!"
   - Should get a response from Gemini

3. **Try voice recording:**
   - Hold the mic button 🎤
   - Speak
   - Release
   - Should transcribe and send

4. **Check Google Sheets:**
   - Your conversation should be logging
   - Personality should start evolving

---

## Step 5: Install as PWA (1 minute)

### On Android (Honor x6b):
1. Open in Chrome
2. Tap menu (⋮)
3. "Add to Home Screen"
4. Name it "AI Twin"
5. Tap Add

### On iPhone:
1. Open in Safari
2. Tap Share button
3. "Add to Home Screen"
4. Name it "AI Twin"
5. Tap Add

### On Desktop:
1. Look for install icon in address bar
2. Click "Install"
3. Done!

---

## Troubleshooting

### "API_URL not configured"
- You forgot to replace the URL in index.html line 93
- Go back to Step 2

### "Failed to fetch"
- Check your GAS deployment is public ("Anyone" can access)
- Check the Web App URL is correct
- Try redeploying the GAS script

### "Microphone not working"
- Grant microphone permissions when prompted
- Check browser supports WebRTC (Chrome, Edge, Safari do)
- Try using HTTPS (required for mic access)

### "Messages not saving"
- Check browser supports IndexedDB (all modern browsers do)
- Clear site data and try again
- Check console for errors (F12)

---

## What's Next?

### Customize It:
1. **Change colors:** Edit CSS in index.html (lines 46-200)
2. **Add personality:** Edit system prompt in GeminiService.gs
3. **Add features:** Voice commands, reminders, etc.

### Monitor It:
1. **Check Google Sheets:** See conversations and personality evolution
2. **Apps Script Logs:** View → Executions (to see API calls)
3. **Browser Console:** F12 → Console (to see frontend logs)

---

## Usage Tips

### Voice Recording:
- **Hold** the mic button while speaking
- **Release** when done
- Works offline! (will transcribe when back online)

### Typing:
- Just type and hit Enter or click Send
- Works exactly like any chat app

### Offline Mode:
- PWA works offline
- Messages queue and sync when back online
- You'll see "Offline" status indicator

---

## You're Live! 🎉

Your AI Twin is now:
- ✅ Accessible 24/7
- ✅ Learning from every conversation
- ✅ Building your personality profile
- ✅ Working offline
- ✅ Installable as an app

**Total time: ~10 minutes**  
**Total cost: $0**

---

## Need Help?

1. Check the console (F12) for errors
2. Check Apps Script logs
3. Make sure all URLs are configured
4. Try the troubleshooting section above

**You did it, Graham!** 💪🔥
