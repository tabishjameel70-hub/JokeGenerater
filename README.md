import React, { useState } from 'react';

const Jokes = [
  "Why don't scientists trust atoms? Because they make up everything!😂",
  "I told my wife she was drawing her eyebrows too high. She looked surprised.😂",
  "What do you call a fish with no eyes? Fsh.😂",
  "What do you call a fake noodle? An impasta.😂",
  "Why did the scarecrow win an award? Because he was outstanding in his field!😂",
  "I'm reading a book about anti-gravity. It's impossible to put down!😂",
  "Did you hear about the two guys who stole a calendar? They each got six months.😂",
  "What's orange and sounds like a parrot? A carrot.😂",
  "Why can't you hear a Pterodactyl go to the bathroom? Because the 'P' is silent.😂",
  "What do you call a boomerang that won't come back? A stick.😂"
];

// Function to get a random joke
const getRandomJoke = () => {
  const randmIDX = Math.floor(Math.random() * Jokes.length);
  return Jokes[randmIDX];
};

const JokeGenerater = () => {
  // 1. Initial State: Changed to a string (an empty string or an initial joke)
  const [joke, setJoke] = useState("Click the button to generate a joke!");

  // Handler for the button click
  const handleGenerateJoke = () => {
    // We call setJoke with the result of getRandomJoke()
    setJoke(getRandomJoke());
  };

  return (
    <>
      <div>
        <h1 className='text-8xl'>Joke Generator</h1>
        
        {/* The joke is displayed here */}
        <h4 className='text-8xl'>{joke}</h4>
        
        {/* 3. Correct onClick: Pass a function reference */}
        <button onClick={handleGenerateJoke}>Generate!</button>
      </div>
    </>
  );
};

export default JokeGenerater;
