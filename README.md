# Project – Matador Game

A Java-based Matador game (inspired by Monopoly) with a GUI and multilingual support.

## Project Origin and Context
- Project retrieved from my GitHub account created with my student email, due to loss of access.
- Student Github url: https://github.com/s185736?tab=repositories.
- Originally completed as part of the course during the 1st semester in 2021.
- Re-uploaded to this GitHub repository for reference and portfolio purposes.

## Features
- GUI-based gameplay with dice rolls, property buying/selling, chance cards, and jail.
- Supports 2–6 players with customizable names and token types.
- Starting balance: 30,000 DKK; passing the Start field: +4,000 DKK.
- Winner determined by total property value and cash.

## Game Board Fields
- **Property:** Can be purchased; other players pay rent.
- **Jail:** Players can be sent to jail.
- **Start:** Players receive money when passing this field.
- **Tax:** Income and state tax fields.
- **Shipping Companies:** Special fields with rent.
- **Chance Cards:** Draw a card with a random effect.

## Chance Cards
- Drawn from the **ChanceDeck**, shuffled automatically.
- Can move players, give or deduct money, send to jail, or impose fines.
- Dynamic actions are executed automatically via the GUI.

## Players
- **Player** class: Tracks name, balance, get-out-of-jail cards, token type, and owned properties.
- Includes **TurnActions** for special turn-related actions.
- Players go bankrupt if their balance drops below 0.

## Dice
- Standard 6-sided dice, configurable.
- `roll()` generates a random value for movement.

## Bank/Stash
- Keeps track of player funds.
- Methods: `addAmount(int)`, `getAmount()`.

## Main
- Starts the game:
```java
public static void main(String[] args) {
    new Game().playMatador();
}
