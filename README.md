# Helesnake

Helesnake is a simple snake game written in JS in the browser.

## Game board

Game is rendered on the canvas.
Game is played on the board.
Board is a grid of cells.
Each cell is a square.

It should be controlable in the code by setting:
```js
const boardRows = 20;
const boardCols = 20;
```

Canvas size is defined in html element:
```html
<canvas id="gameCanvas" width="400" height="400"></canvas>
```

## Score

Score is displayed on the top of the screen.
Score is a number.
Score is increased or decreased by eating apples.
Score can be negative.

## Snake

Snake is a collection of cells.
Snake is controlled by the player.
Snake moves in the direction of the last key pressed.
Snake eats apples.
Each apple has it's own special effect.
If snake eats itself, game is over.
Snake's head is drawn from the image: /images/snake_hela.jgp
The head is drawn 100% larger then one cell, but it's center is in the middle of the cell. It still occupies only one cell.

## Apples

Apple is an object on the board that snake can eat.
Apple is placed randomly on the board.
Apple occupies 9 cells in the board in the 3x3 square.
Eating an apple on one place eats the whole apple.
There should be at least 3 apples on the board at all times.
Apples pop up randomly on the board.
Apples can't pop up on the snake or other apples.
Each apple will be displayed as an image, that should fit in the 3x3 square.

There are many apple types.

## Apple Ewa

Image: /images/apple_ewa.jpg
Reward: +10 points
Snake length: +1
Special effect: game speed increases by 2x for 5 seconds.
Constraints: If eaten by the snake, that already has this effect, the effect is prolonged by 5 seconds.

## Apple Dawid

Image: /images/apple_dawid.jpg
Reward: +20 points
Snake length: +1
Special effect: game speed decreases by 2x for 5 seconds.
Constraints:
- If eaten by the snake, that already has this effect, the effect is prolonged by 5 seconds.
- If eaten by the snake, that has the opposite effect, the effect is removed and snake speed is set to normal.

## Apple Pawel

Image: /images/apple_pawel.jpg
Reward: +30 points
Snake length: Make it half, with min 1

## Apple Ola

Image: /images/apple_ola.jpg
Reward: +100 points
Snake length: +1

## Apple Ala

Image: /images/apple_ala.jpg
Reward: -100 points
Snake length: +1

## Apple Kuba

Image: /images/apple_kuba.jpg
Reward: +50 points
Snake length: double the length

## Apple Maciek

Image: /images/apple_maciek.jpg
Reward: +50 points
Snake length: no change
Special effect:
- head of the snake is moved to the tail,
- snake moves in the opposite direction.

## Apple Ania

Image: /images/apple_ania.jpg
Reward: +50 points
Snake length: +1
Special effect: It generates 3 additional Apple Kluski on the board.

## Apple Kluski

Image: /images/apple_kluski.jpg
Reward: +100 points
Snake length: +1

## Apple Andrzej

Image: /images/apple_andrzej.jpg
Reward: +50 points
Snake length: +1
Special effect: It generates 3 additional random apples on the board.

