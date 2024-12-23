# Number Guessing Game

This project is a simple number guessing game implemented in TypeScript. The computer generates a random number, and the user has to guess it. The result is displayed based on whether the user's guess matches the computer's random number.

---

## Features

1. **Random Number Generation**: The computer generates a random number between 1 and 6.
2. **User Interaction**: Users input their guess using a command-line interface.
3. **Result Evaluation**: Compares the user's guess with the computer's random number and displays a success or failure message.

---

## Installation

1. Clone the repository:

   ```bash
   git clone <repository_url>
   cd <repository_directory>
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Compile TypeScript to JavaScript:

   ```bash
   npx tsc
   ```

---

## Usage

1. Run the game:

   ```bash
   node dist/index.js
   ```

2. Follow the prompt to input your guessed number.

3. The game will inform you whether you won or lost.

---

## Code Overview

### Main Logic

The game uses the `inquirer` package to prompt the user for their guess and generates a random number using:

```typescript
const randomNumber = Math.floor(Math.random() * 6 + 1);
```

The user's input is compared to the random number:

```typescript
if (answers.userGuessedNumber === randomNumber) {
    console.log("Congratulations! You Won.");
} else {
    console.log("Unfortunately! You lost.");
}
```

---

## File Structure

```
Number-Guessing-Game/
├── node_modules/
├── src/
│   └── index.ts
├── dist/
│   └── index.js
├── package.json
├── tsconfig.json
└── README.md
```

---

## Dependencies

- **[inquirer](https://www.npmjs.com/package/inquirer)**: For interactive command-line prompts.

Install it using:

```bash
npm install inquirer
```

---

## Future Enhancements

1. Allow the user to select the range of numbers.
2. Add a scoring system based on the number of attempts.
3. Allow multiple rounds and display a final score.
4. Include error handling for invalid inputs.

---

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it.

---

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue for suggestions and bug fixe.
