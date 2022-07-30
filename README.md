# starknet-hackathon-game

Starknet Hackathon DevConnect Amsterdam 2022

At the Starknet Hackathon, My partner and I created a game on starknet, the game was the famous multiplayer game Agor.io. Where you are a player/ball that grows when you eat smaller players/balls.

We forked an existing version of this game and made cairo contracts where each ball was an NFT, and when you start you put an some amount of ETH in your ball, when you eat other players you receive the eth they have in their ball. Starknet made this game possible, because you need the possibility to have a lot of fast confirmed transactions in a row. When you eat multiple players subsequently.

The folder contains both the adapted forked front-end code as well as the necessary cairo smart-contracts contracts. What is left to-do, is using web3.js/ethers.js libraries to execute the smart contracts functions during the game. After that the code should be tested and fine-tuned.
