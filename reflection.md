# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

I couldn't start a new game after a game played but the game resets attempts number.
When the answer was a higher number the game kept saying to go lower.
The game lets you go above and lower than the range/ out of the range (negative numbers)
When changing the game difficulty, the range doesn't reflect but the attempt does.

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").

---

## 2. How did you use AI as a teammate?

I used caludeAI. In the prompt I gave ClaudeAi to explain the bugs I found while testing the game. I then used AI to help locate where in the code that the issues were.

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

---

## 3. Debugging and testing your fixes

After adding the changes, I reran the app and tested them. If the tested outcome is what is expected, then I know it has been fixed.
One manual test was playing through a full game on Normal difficulty and guessing a number higher than the secret given, if the app said "Go LOWER" when it should have said "Go HIGHER," it confirmed the swapped message bug in check_guess.

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

Every time I interact with a Streamlit app,Streamlit reruns the entire Python script from the top. Without any protection, random.randint(low, high) would execute again on every rerun, generating a brand new secret each time. The original app also had a related problem: changing difficulty mid-game silently kept the old secret because there was no check for whether the difficulty had changed.

- In your own words, explain why the secret number kept changing in the original app.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
- What change did you make that finally gave the game a stable secret number?

---

## 5. Looking ahead: your developer habits

Before asking AI to fix a bug, I will first describe the symptoms I observed while testing. On this project, describing exactly what the game did wrong gave claudeAI enough context to pinpoint the issue.
The project helped me realize how AI can really help me debug my codes or pinpoint the mistakes I run into when testing an app.

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
