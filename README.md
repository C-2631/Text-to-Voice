# 🎙️ Text-to-Voice Generator

> **Transform Your Text Into Natural Speech with Ease**

A modern, interactive web application that converts text into speech using the Web Speech API. Built with HTML, CSS, and JavaScript to provide a seamless and user-friendly experience.

---

## ✨ Features

- 🗣️ **Text-to-Speech Conversion** - Convert any text input into natural-sounding speech
- 🎯 **Multiple Voice Options** - Choose from various system voices and accents
- 🎨 **Modern UI Design** - Beautiful gradient interface with intuitive controls
- ⚡ **Real-time Voice Selection** - Switch between voices instantly
- 📱 **Responsive Design** - Works smoothly on desktop and mobile devices
- 🚀 **Lightweight & Fast** - No heavy dependencies, pure JavaScript implementation

---

## 📋 Table of Contents

- [Demo](#demo)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [How to Use](#how-to-use)
- [API Reference](#api-reference)
- [Browser Compatibility](#browser-compatibility)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

---

## 🎬 Demo

Simply visit the project and:
1. Type or paste any text in the textarea
2. Select your preferred voice from the dropdown menu
3. Click the **Listen** button to hear the speech

The application uses the native Web Speech API to synthesize and play audio in real-time.

---

## 💻 Technologies Used

| Technology | Purpose | Usage |
|-----------|---------|-------|
| **HTML5** | Markup & Structure | Semantic HTML with textarea and select elements |
| **CSS3** | Styling & Design | Modern gradients, flexbox, and responsive layouts |
| **JavaScript (ES6+)** | Functionality | Web Speech API integration and event handling |

### Language Composition
- **CSS**: 55.7% - Rich styling and gradient effects
- **JavaScript**: 22.3% - Speech synthesis logic
- **HTML**: 22% - Semantic markup structure

---

## 📁 Project Structure

```
Text-to-Voice/
├── index.html          # Main HTML file with markup
├── style.css           # Stylesheet with modern design
├── script.js           # JavaScript logic for speech synthesis
├── play.png            # Play button icon
├── dropdown.png        # Dropdown menu icon
└── README.md          # Project documentation
```

---

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/C-2631/Text-to-Voice.git
   cd Text-to-Voice
   ```

2. **Open in your browser**
   - Simply open `index.html` in your web browser
   - No installation or build process required!

3. **Optional: Use a local server**
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Python 2
   python -m SimpleHTTPServer 8000
   
   # Using Node.js (with http-server)
   npx http-server
   ```
   Then visit `http://localhost:8000`

---

## 📖 How to Use

### Step 1: Enter Your Text
Type or paste the text you want to convert into speech in the textarea input field.

```
📝 Example: "Hello, this is a text-to-speech converter!"
```

### Step 2: Select a Voice
Click on the dropdown menu to choose from available voices. The menu displays all system voices supported by your browser.

### Step 3: Play Audio
Click the **Listen** button with the play icon to synthesize and play the text in the selected voice.

### Tips
- ✏️ You can change the text and play it again anytime
- 🔄 Switch voices mid-way through to hear different variations
- 🔊 The audio plays through your system's default speaker

---

## 🔧 API Reference

### Web Speech API - SpeechSynthesisUtterance

The project uses the **Web Speech API**, specifically the `SpeechSynthesisUtterance` interface:

#### Properties

| Property | Type | Description |
|----------|------|-------------|
| `text` | String | The text to be synthesized |
| `voice` | SpeechSynthesisVoice | The voice used for synthesis |
| `rate` | Number | Speech rate (0.1 to 10, default: 1) |
| `pitch` | Number | Pitch level (0 to 2, default: 1) |
| `volume` | Number | Volume level (0 to 1, default: 1) |

#### Methods

```javascript
// Get available voices
window.speechSynthesis.getVoices()

// Speak the utterance
window.speechSynthesis.speak(utterance)

// Pause speech
window.speechSynthesis.pause()

// Resume speech
window.speechSynthesis.resume()

// Cancel speech
window.speechSynthesis.cancel()
```

#### Code Implementation

```javascript
// Create a new utterance
let speech = new SpeechSynthesisUtterance();

// Listen for when voices are loaded
window.speechSynthesis.onvoiceschanged = () => {
    voices = window.speechSynthesis.getVoices();
    speech.voice = voices[0]; // Set default voice
};

// Speak the text
speech.text = "Your text here";
window.speechSynthesis.speak(speech);
```

---

## 🌐 Browser Compatibility

The Web Speech API is supported on most modern browsers:

| Browser | Support | Notes |
|---------|---------|-------|
| **Chrome/Edge** | ✅ Full Support | Excellent compatibility |
| **Firefox** | ✅ Full Support | Works well |
| **Safari** | ✅ Full Support | iOS 14.5+ for speech synthesis |
| **Opera** | ✅ Full Support | Based on Chromium |
| **IE 11** | ❌ Not Supported | Use modern browser |

**Recommended**: Use Chrome, Edge, or Firefox for the best experience.

---

## ⚙️ Configuration

### Customizing Voice Properties

Edit `script.js` to modify speech properties:

```javascript
// Adjust speech rate (default: 1)
speech.rate = 1.2;  // Faster speech

// Adjust pitch (default: 1)
speech.pitch = 1.5;  // Higher pitch

// Adjust volume (default: 1)
speech.volume = 0.8;  // Lower volume

// Add event listeners
speech.onstart = () => console.log("Speech started");
speech.onend = () => console.log("Speech ended");
speech.onerror = (e) => console.log("Error:", e.error);
```

### Styling Customization

Modify `style.css` to change:
- Background gradient colors
- Button and input styling
- Typography and spacing
- Voice dropdown appearance

---

## 🎨 Design Highlights

### Color Scheme
- **Primary Gradient**: Deep purple to dark blue (#010758 → #490d61)
- **Accent Color**: Hot pink (#ff2963)
- **Secondary Background**: Muted purple (#403d84)
- **Text Color**: White (#fff)

### UI Components
- **Textarea**: Large input field with custom styling
- **Voice Dropdown**: Styled select with custom icon
- **Play Button**: Modern rounded button with icon
- **Responsive Layout**: Flexbox-based, centered design

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Ideas for Enhancement
- 🎚️ Add volume and pitch controls
- 🔴 Add pause/resume functionality
- 💾 Save favorite texts with voice settings
- 📱 Improve mobile responsiveness
- 🌐 Support for multiple languages
- 🎵 Add background music options

---

## 📝 License

This project is open source and available under the MIT License. Feel free to use, modify, and distribute this project as needed.

---

## 🙏 Acknowledgments

- Built with the **Web Speech API**
- Inspired by modern web design principles
- Thanks to all contributors and users!

---

## 📞 Support

If you encounter any issues or have questions:
- Open an issue on GitHub
- Check browser console for error messages
- Ensure your browser supports the Web Speech API
- Try a different browser if issues persist

---

## 🔮 Future Roadmap

- [ ] Export audio files (MP3, WAV)
- [ ] Voice rate, pitch, and volume controls
- [ ] Language selection
- [ ] Text formatting options
- [ ] Dark/Light theme toggle
- [ ] Keyboard shortcuts
- [ ] Progressive Web App (PWA) support

---

<div align="center">

**Made with ❤️ by [C-2631](https://github.com/C-2631)**

[⭐ Star this repo](https://github.com/C-2631/Text-to-Voice) if you found it helpful!

</div>