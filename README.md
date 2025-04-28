# Parallax Effect and Jump Animation

This project includes two TypeScript scripts . The scripts implement a parallax scrolling effect and a simple jump animation for the character. Below are details on both components:

## Components

### 1. ParallaxEffect.ts
- This script creates a parallax scrolling effect where three background images move from right to left. When an image moves off-screen, it is wrapped around to the right side to create an infinite scrolling effect. The scrolling speed can be controlled by the `gameSpeed` property.

#### Key Properties:
- `image1`, `image2`, `image3`: Nodes representing the background images.
- `gameSpeed`: Controls the speed of the scrolling.
- `Y`: The Y-coordinate for positioning the images.
  
#### Methods:
- `onLoad()`: Initializes image positions.
- `startUp()`: Sets up the initial positions and canvas width.
- `setImageStartingPositions()`: Positions the images at the start.
- `update(deltaTime)`: Updates the images' positions every frame.
- `moveImages(deltaTime)`: Moves the images based on `gameSpeed`.
- `checkAndWrapImages()`: Wraps images around when they move off-screen.

### 2. Jump.ts
- This script enables the character to jump when a button is clicked. The button triggers the jump animation on the charcter using the `Animation` component.

#### Key Properties:
- `jumpButton`: The button node that triggers the jump action.
- `CharacterAnim`: The `Animation` component controlling the Character's animation.

#### Methods:
- `start()`: Listens for the button click and triggers the `jump()` method.
- `jump()`: Plays the 'Jump' animation for the Charcter.

## How to Use

1. **ParallaxEffect.ts**
   - Attach this script to a Node in your scene.
   - Assign the `image1`, `image2`, and `image3` properties to background image nodes.
   - Adjust the `gameSpeed` and `Y` properties to control the movement.

2. **Jump.ts**
   - Attach this script to a Node in your scene.
   - Assign the `jumpButton` property to the jump button node.
   - Assign the `CharacterAnim` property to the Animation component controlling the Character.

## Requirements
- Cocos Creator (or any compatible game engine that supports TypeScript and Cocos)
  
## License
This project is licensed under the MIT License - see the LICENSE file for details.

