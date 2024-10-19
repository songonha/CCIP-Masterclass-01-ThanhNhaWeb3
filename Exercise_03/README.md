# EXERCISE 03: CCIP TIC TAC TOE

## CONTRACT ON FUJI: 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

Command: npx hardhat run ./scripts/deployTicTacToe.ts --network avalancheFuji

✅ Tic Tac Toe Demo deployed at address 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 on avalancheFuji blockchain

https://testnet.snowtrace.io/address/0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

Router FUJI: 0xF694E193200268f9a4868e4Aa017A0118C9a8177

Chain selector Fuji: 14767482510784806043

## CONTRACT ON AMOY: 

Command: npx hardhat run ./scripts/deployTicTacToe.ts --network polygonAmoy

✅ Tic Tac Toe Demo deployed at address 0x1C929B974B48204DB9A385670F3029A4717D4e7A on polygonAmoy blockchain

Router Amoy: 0x9C32fCB86BF0f4a1A8921a9Fe46de3198bb884B2

Chain selector Amoy: 16281711391670634445


## CONTRACT ON SEPOLIA: 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1

Command: npx hardhat run ./scripts/deployTicTacToe.ts --network ethereumSepolia

✅ Tic Tac Toe Demo deployed at address 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 on ethereumSepolia blockchain

https://sepolia.etherscan.io/address/0xda63d08a3c32438d7ba2d762be124b32b821fcd1

Router Sepolia: 0x0BF3dE8c5D3e8A2B34D2BEeB17ABfCeBaf363A59

Chain selector Sepolia: 16015286601757825753

### ROUTER UPDATE:

npx hardhat ttt-update-router --blockchain ethereumSepolia --contract 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --router 0x0BF3dE8c5D3e8A2B34D2BEeB17ABfCeBaf363A59

✅ Update successful, transaction hash: 0x02ee18bdd24ca8bfddb4a96655b98d1b768ec7a6f71b120cefc74930d9ca2943

npx hardhat ttt-update-router --blockchain avalancheFuji --contract 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --router 0xF694E193200268f9a4868e4Aa017A0118C9a8177

✅ Update successful, transaction hash: 0xd2e8fe94df509adbcdae95ca57ebbe0bd03be912dd96cb20d81d7952d555b94a

npx hardhat ttt-update-router --blockchain polygonAmoy --contract 0x1C929B974B48204DB9A385670F3029A4717D4e7A --router 0x9C32fCB86BF0f4a1A8921a9Fe46de3198bb884B2



### DEPOSITE NATIVE TOKEN TO SMART CONTRACT

ON SEPOLIA: 0.1 ETH

ON FUJI: 2.5 AVAX

### START GAME BETWEEN SEPOLIA AND FUJI:

npx hardhat ttt-start --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

✅ Message sent, game session created! transaction hash: 0xaed281b5c52b2c15dc66e81af3ee38d1216f4a95e6a3aef9effddbefd510a682

https://ccip.chain.link/#/side-drawer/msg/0x8159f0d476758fcfadf469bdd04c5236cc26cc97bb1b55813b095b9375ad0e5e

### START GAME BETWEEN FUJI AND SEPOLIA:

npx hardhat ttt-start --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1

### Get session ID:

npx hardhat ttt-get-sessionId --blockchain ethereumSepolia --contract 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --index 0

sessionId at index 0 is: 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69

npx hardhat ttt-get-sessionId --blockchain avalancheFuji --contract 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --index 0

sessionId at index 0 is: 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69


### Player 2 makes a move in Blockchain 2

#### Move 2: 
npx hardhat ttt-move --x 0 --y 1 --player 2 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1

✅ Message sent, you make a move! transaction hash: 0xf338919014fd5b7cf4fd9f73d464ba1992c0dcd04118c31e6181db7ae3cffe50

https://ccip.chain.link/#/side-drawer/msg/0xf67342c1be819e3a87fe590a5a95aee2fbb5f6aec1b0a51a2180b097ebeaab9a

#### Move 4:
npx hardhat ttt-move --x 1 --y 2 --player 2 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1

#### Move 6:
npx hardhat ttt-move --x 2 --y 1 --player 2 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1

#### Move 8:
npx hardhat ttt-move --x 0 --y 2 --player 2 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1

### Player 1 makes a move in Blockchain 1

#### Move 1: 
npx hardhat ttt-move --x 0 --y 0 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

✅ Message sent, you make a move! transaction hash: 0xf467b0ad69cde1dba714e0629b490c8bb21f2099416d1b11ad2a9773856747bd

https://ccip.chain.link/#/side-drawer/msg/0x89530fb737ea08c723f2ef0dbfd9c28d8f350bd7c34aecc13c0d1dca23adb163

#### Move 3: 
npx hardhat ttt-move --x 1 --y 1 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

#### Move 5: 
npx hardhat ttt-move --x 2 --y 2 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

#### Move 7: 
npx hardhat ttt-move --x 1 --y 0 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

#### Move 9: 
npx hardhat ttt-move --x 2 --y 0 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

### Check the winner

npx hardhat ttt-check-winner --blockchain ethereumSepolia --contract 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 

#### winner of sessionId 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 is: 0x0000000000000000000000000000000000000000

npx hardhat ttt-check-winner --blockchain avalancheFuji --contract 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69


