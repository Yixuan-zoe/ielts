# IELTS Vocabulary App

A Vue 3 + Tailwind CSS static web application for learning IELTS vocabulary with study and quiz modes.

## Features

- **Study Mode**: Browse vocabulary words with meanings and examples
- **Quiz Mode**: Test your knowledge with interactive multiple-choice questions
- **Multiple Chapters**: Support for organizing vocabulary into chapters
- **Key Sentences**: Each chapter includes a key sentence using the vocabulary

## Files Structure

- `index.html` - Main application UI with Vue 3 + Tailwind CSS
- `vocabulary.txt` - Raw vocabulary data in structured text format
- `parser.py` - Python script to parse vocabulary.txt into vocabulary.js
- `vocabulary.js` - Auto-generated JavaScript file with vocabulary data

## Vocabulary Data Format

The `vocabulary.txt` file follows this format:

```
Chapter Title
+++
[KEY]Key Sentence
---
word|pos|meaning|example
word|pos|meaning|example
...
```

Example:
```
Sentence 04
+++
[KEY]There is considerable debate about whether we should be attempting to contact life forms from an alien civilisation.
---
considerable|adj.|important or large enough to be noticed|The project requires a considerable amount of time and effort.
debate|n.|a discussion involving different opinions|The debate about climate change continues in parliament.
```

## Usage

1. **Edit vocabulary**: Update `vocabulary.txt` with your vocabulary data
2. **Parse the data**: Run `python3 parser.py` to generate `vocabulary.js`
3. **Open the app**: Open `index.html` in a web browser

Or use a simple HTTP server:
```bash
python3 -m http.server 8080
# Then open http://localhost:8080 in your browser
```

## How to Add More Vocabulary

1. Open `vocabulary.txt`
2. Add a new chapter using the format above
3. Run `python3 parser.py` to update `vocabulary.js`
4. Refresh the page in your browser

## Study Mode

- View all vocabulary words from the selected chapter
- See the key sentence that uses the vocabulary
- Browse word meanings and example sentences
- Visual cards for easy studying

## Quiz Mode

- Multiple-choice questions for each word
- Instant feedback on answers
- Progress tracking
- Final score display
- Option to retry or return to study mode