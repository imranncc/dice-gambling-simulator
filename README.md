# Dice Gambling Simulator

This program simulates a gambling scenario between two gamblers using dice rolls. It includes classes for Dice and Gambler, as well as methods to facilitate the gambling process.

## Files

- `DiceGambling.java`: Main Java file containing the implementation of the Dice and Gambler classes, along with methods for simulating gambling.

## Classes

### 1. Dice

The `Dice` class represents a standard six-sided die.

#### Methods

- `rollDice()`: Rolls the dice once and returns the value of the roll.

### 2. Gambler

The `Gambler` class represents a player in the gambling scenario. Each gambler has an amount of money and a die to roll.

#### Fields

- `money`: Amount of money the gambler possesses.
- `die`: An instance of the `Dice` class.

#### Constructor

- `Gambler(int initial_money)`: Initializes a gambler with the specified initial amount of money.

#### Static Method

- `gambling(Gambler gambler_1, Gambler gambler_2, int stake)`: Conducts a gambling activity between two gamblers. Each gambler rolls a die, and the one with the higher roll wins the stake. This process continues until one gambler cannot afford the stake. Returns `true` if gambling can continue and `false` otherwise.

#### Static Method

- `keepGambling(Gambler gambler_1, Gambler gambler_2, int stake, int max_gambling_times)`: Continues gambling between two gamblers until one gambler cannot afford the stake or until a maximum number of gambling rounds is reached. Prints the amount of money of each gambler after each round of gambling, as well as the value of rolled dice for each gambler in each round.

## Usage

To use this program, run the `main` method in the `Q1_DiceGambling` class. Customize the initial money, stake amount, and maximum gambling times as needed.

```java
public static void main(String[] args) {
    int initial_money = 10;
    int stake = 5;
    int max_gambling_times = 10;

    Gambler gambler1 = new Gambler(initial_money);
    Gambler gambler2 = new Gambler(initial_money);

    keepGambling(gambler1, gambler2, stake, max_gambling_times);
}
```

### Notes
- The program will print the results of each gambling round, including the amount of money for each gambler and the value of the rolled dice.
- Gambling will continue until one gambler cannot afford the stake or until the maximum number of gambling rounds is reached.
- Ensure the Java environment is properly set up to compile and run the program.

