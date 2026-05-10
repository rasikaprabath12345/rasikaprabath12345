# 😂 Random Joke Generator

A simple and fun random joke generator web application using the **JokeAPI** external API.

## Features

✨ **Key Features:**
- 🎲 Fetch random jokes with a single click
- 😄 Support for single-part and two-part jokes
- 📤 Share jokes via Web Share API or copy to clipboard
- 🎨 Beautiful gradient UI with smooth animations
- 📊 Track total jokes loaded
- ⚠️ Error handling with user-friendly messages
- 📱 Fully responsive design

## Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with gradients and animations
- **Vanilla JavaScript** - No dependencies required
- **JokeAPI** - External API for fetching jokes

## How to Use

1. Open `index.html` in your web browser
2. Click the **"Get New Joke"** button to fetch a random joke
3. Read and enjoy the joke!
4. Use the **"Share Joke"** button to:
   - Share via native share dialog (mobile/desktop)
   - Copy the joke to clipboard

## API Reference

### JokeAPI
- **Endpoint:** `https://v2.jokeapi.dev/joke/Any`
- **Response Types:**
  - **Single:** `{ "type": "single", "joke": "..." }`
  - **TwoPart:** `{ "type": "twopart", "setup": "...", "delivery": "..." }`

## Project Structure

```
joke-generator/
├── index.html      # HTML structure
├── style.css       # Styling and animations
├── script.js       # JavaScript logic
└── README.md       # Documentation
```

## Code Highlights

### Fetching Jokes
```javascript
async function fetchJoke() {
    const response = await fetch('https://v2.jokeapi.dev/joke/Any?type=single');
    const data = await response.json();
    // Display joke...
}
```

### Sharing Jokes
```javascript
function shareJoke() {
    if (navigator.share) {
        navigator.share({
            title: '😂 Check out this joke!',
            text: currentJoke,
        });
    } else {
        copyToClipboard(currentJoke);
    }
}
```

## Browser Support

- ✅ Chrome/Chromium (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)

## Responsive Design

The application is fully responsive and works great on:
- 📱 Mobile devices
- 💻 Tablets
- 🖥️ Desktop screens

## Features in Detail

### Error Handling
- Displays user-friendly error messages
- Handles network failures gracefully
- Disables buttons during loading

### User Experience
- Loading spinner during API calls
- Smooth animations and transitions
- Joke counter to track engagement
- Disabled state feedback on buttons

## Future Enhancements

- [ ] Filter jokes by category
- [ ] Add joke history
- [ ] Dark mode toggle
- [ ] Joke favorites/bookmarks
- [ ] Multiple language support

## License

Open source project - Feel free to use and modify!

---

**Made with ❤️ by Rasika Prabath**
