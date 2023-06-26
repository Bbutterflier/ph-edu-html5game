<h1 align="center">
  <br>
  <a href="https://github.com/yandeu/phaser3-multiplayer-with-physics#readme"><img src="readme/phaser-with-nodejs.png" alt="header" width="400"></a>
  <br>
  Phaser 3 - Real-Time Multiplayer example with Physics
  <br>
</h1>

<h4 align="center">
A Real-Time Multiplayer example using 

---

## Key Features

- The physics is entirely calculated on the Server
- Automatically manages Rooms (new Phaser instances)
- Physics debugging version
- A nice Stats page

## Geckos.io

Why does this game example not use geckos.io?  
Well there are two reasons:

- Geckos.io did not exist back then.
- This example is deployed on heroku, which does not allow to forward UDP ports, geckos.io depends on.

## Matter Physics vs Arcade Physics

This example includes 2 different games. One with MatterJS and the other with Arcade. The MatterJS game has only one level. The Arcade one is a simple platformer game with 3 levels.

So in total, you can play 4 different levels. For each level, the server creates a new room, which creates a new Phaser instance, which are completely isolated from each other. There can be up to 4 players per room.

## Structure

```bash
├── src
│   ├── client  # Contains all the code the client will need
│   ├── physics # This is for debugging the physics (Arcade and MatterJS)
│   ├── server  # Contains the code running on the NodeJS server
│   └── stats   # The stats page will show useful information about the server
```
