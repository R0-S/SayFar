# LexiMap – Vocabulary Builder

A modern, swipe-based vocabulary learning app with an interactive knowledge graph visualization.

## Features

- **Swipe Cards**: Rapidly learn vocabulary by swiping left (unknown), right (known), or up (study)
- **Knowledge Map**: Visualize word relationships and your learning progress as an interactive graph
- **Word Library**: Organize and review your learned words by status
- **Progress Stats**: Track mastery, study streak, and top-reviewed words
- **Offline Support**: Works offline with service worker caching
- **Dark Theme**: Beautiful, eye-friendly interface designed for long study sessions

## Quick Start

1. Open `index.html` in a modern web browser
2. Start swiping cards to build your vocabulary:
   - **→ Swipe Right**: Mark as known
   - **← Swipe Left**: Mark as unknown
   - **↑ Swipe Up**: Add to study library
3. Explore your learning journey in the **Map** tab
4. Check your progress in **Stats**

## App Structure

### Files

- **index.html** – Main app with all UI, styles, and JavaScript
- **manifest.json** – PWA configuration for installable app
- **sw.js** – Service worker for offline support
- **README.md** – This file

### Screens

1. **Cards** – Daily swipe-based learning session
2. **Library** – Browse and manage learned words by status
3. **Map** – Interactive knowledge graph showing word connections
4. **Stats** – Learning metrics and weekly streak

## Built With

- **HTML5/CSS3** – Layout and styling with CSS variables
- **Canvas API** – Force-directed graph physics simulation
- **Service Workers** – Offline functionality
- **LocalStorage** – Persistent learning data
- **Fonts** – DM Serif Display, DM Sans (Google Fonts)

## Word Data

The app includes 20 curated English vocabulary words with:
- Phonetic pronunciation
- Part of speech
- Russian translation
- Usage examples
- Semantic tags (for graph connections)

## Customization

### Adding More Words

Edit the `WORDS` array in `index.html`:

```javascript
{ 
  id: 21, 
  word: 'YourWord', 
  phonetic: '/fəˈnetɪk/', 
  pos: 'noun/verb/adjective', 
  translation: 'Russian translation', 
  example: 'Usage <em>example</em> here.', 
  tags: ['category1', 'category2'] 
}
```

### Changing Theme Colors

Update CSS variables in the `<style>` section:

```css
:root {
  --bg: #0a0a0f;
  --green: #4ade80;
  --blue: #60a5fa;
  /* etc. */
}
```

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Android)

## How to Install as PWA

1. Open the app in a supported browser
2. Look for "Install" or "Add to Home Screen" prompt
3. Follow the browser's installation flow
4. App will work offline after installation

## Learning Algorithm

Words are categorized by status:
- **Unseen** – New words from today's session
- **Unknown** – Words you marked as unknown
- **Studying** – Words in your active study library
- **Known** – Words you've mastered

Each session prioritizes unseen words first, then a mix of unknown and studying words.

## Data Storage

All progress is saved locally in browser storage:
- Word statuses and review counts
- Learning statistics
- Weekly streak tracking

Data is never sent to external servers.

## License

Created with ♥ for vocabulary learners.

## Tips for Best Learning

1. **Consistency** – Review daily to maintain your streak
2. **Active Recall** – Try to remember before looking at the translation
3. **Associations** – Use the Knowledge Map to understand word connections
4. **Spaced Repetition** – Review unknown words multiple times
5. **Context** – Pay attention to the usage examples
