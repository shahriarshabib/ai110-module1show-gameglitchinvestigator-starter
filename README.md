# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

Ran the Streamlit game and observed multiple bugs in how the game behaved.

Identified issues with the New Game button not fully resetting the game state.

Debugged the secret number generation, which was changing unexpectedly.

Fixed the issue by storing the secret number in st.session_state so it stays consistent between reruns.

Investigated problems with the guess history only storing four previous guesses.

Debugged incorrect higher/lower hint logic that sometimes gave the wrong feedback.

Attempted to fix the Show Hint feature, which originally displayed nothing.

Tested and adjusted the attempts allowed for each difficulty mode.

Manually tested the number of attempts by repeatedly guessing to see if the correct limit was enforced.

Investigated a bug where the first hint did not appear until after the second guess because of indexing issues.

Fixed logic so that difficulty changes update both the secret number and difficulty settings.

Used AI (Claude) to help identify bugs and suggest fixes.

Verified bug fixes by running tests to see whether they passed or failed.

Performed manual testing of game behavior to confirm fixes worked in the UI.

Debugged UI interaction issues like needing to click buttons twice due to Streamlit reruns.

Learned how Streamlit reruns the entire script on every interaction.

Implemented session state storage to maintain game variables across reruns.

Reflected on how AI suggestions can sometimes remove important code if prompts are unclear.

Practiced debugging through trial-and-error testing and code adjustments.

## 📸 Demo

Game Glitch Investigator interface showing a number guessing game with dark theme. Left sidebar displays Settings with Difficulty set to Easy, range 1 to 20, and 6 attempts allowed. Main content area shows the game title with a purple game controller icon, subtitle An AI-generated guessing game. Something is off., and a Make a guess section with input field prompting Enter your guess. Three buttons are visible: Submit Guess, New Game, and Show hint. Below is an expanded Developer Debug Info section displaying Secret: 8, Attempts: 0, Score: 0, Difficulty: Easy, and History with an empty array. At the bottom, text states Built by an AI that claims this code is production-ready. A deployment indicator appears in the top right corner.

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, insert a screenshot of your Enhanced Game UI here]
