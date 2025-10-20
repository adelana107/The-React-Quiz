🧠 React Quiz App

A fun and interactive quiz application built with React and powered by a local JSON API using json-server.
The app dynamically fetches quiz questions, tracks your progress, scores, and even includes a countdown timer!

🚀 Features

🎯 Multiple-choice quiz questions

⏱️ Countdown timer for each question (30 seconds)

🧮 Points system and highscore tracking

🔁 Restart functionality

⚡ State management with useReducer

🔄 Data fetched from a local JSON API

🧩 Project Structure
src/
│
├── App.js
├── Header.js
├── Main.js
├── Loader.js
├── Error.js
├── StartScreen.js
├── Question.js
├── NextButton.js
├── Progress.js
├── FinishScreen.js
├── Footer.js
└── Timer.js


Each component handles a specific part of the quiz logic or UI — making the app modular and easy to extend.

⚙️ How It Works

On startup, the app fetches quiz questions from a JSON API (http://localhost:8000/questions).

The user can start the quiz, answer questions, and watch the timer tick down.

The app keeps track of:

Current question index

Total points

Correct answers

Highscore (persisted in state)

When the quiz is complete, the user’s score and highscore are displayed.

🧠 State Flow (useReducer)

The app uses a reducer to manage all state transitions:

Action Type	Description
dataReceived	Data successfully loaded from the API
dataFailed	Error fetching questions
start	Start the quiz
newAnswer	Store the user’s answer and calculate points
nextQuestion	Move to the next question
finish	End the quiz
restart	Restart the quiz
tick	Update the timer every second
🔌 Setting Up the Local JSON API

Install JSON Server

npm install -g json-server


Create the JSON file

In your project folder, make a file:

data/questions.json


Paste in something like:

{
  "questions": [
    {
      "question": "What is React?",
      "options": ["A library", "A framework", "A language", "A database"],
      "correctOption": 0,
      "points": 10
    },
    {
      "question": "Which hook manages state?",
      "options": ["useReducer", "useEvent", "useState", "useForm"],
      "correctOption": 2,
      "points": 10
    }
  ]
}


Start the server

npx json-server --watch data/questions.json --port 8000


The API will be available at:

http://localhost:8000/questions


Run your React app

npm start

🖥️ Tech Stack

React 18+

JavaScript (ES6)

JSON Server

CSS Modules / Global Styles

🧾 Future Improvements

✅ Add localStorage to persist highscores

✅ Add a settings screen for quiz category and difficulty

✅ Add sound or animation feedback for correct/incorrect answers

✅ Integrate an online API (like Open Trivia DB)

💡 Author

Adelana Oluwafunmibi Cornelius
📍 Nigeria
💻 Passionate about clean UI, creative problem-solving, and scalable React apps.
