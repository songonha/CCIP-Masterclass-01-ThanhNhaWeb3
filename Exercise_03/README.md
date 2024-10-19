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

## PLAY MAP

1 (Move 1: 0 - 0) 2 (Move 2: 0 - 1) 2 (Move 8: 0 - 2)

1 (Move 7: 1 - 0) 1 (Move 3: 1 - 1) 2 (Move 4: 1 - 2)

1 (Move 9: 2 - 0) 2 (Move 6: 2 - 1) 1 (Move 5: 2 - 2)

### Player 2 makes a move in Blockchain 2

#### Move 2: 0 1
npx hardhat ttt-move --x 0 --y 1 --player 2 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1

✅ Message sent, you make a move! transaction hash: 0xf338919014fd5b7cf4fd9f73d464ba1992c0dcd04118c31e6181db7ae3cffe50

https://ccip.chain.link/#/side-drawer/msg/0xf67342c1be819e3a87fe590a5a95aee2fbb5f6aec1b0a51a2180b097ebeaab9a

#### Move 4: 1 2
npx hardhat ttt-move --x 1 --y 2 --player 2 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1

✅ Message sent, you make a move! transaction hash: 0xecaf5120332d99d42b63532b03431d122e3e76754ce7daa16d325980a4952a08

https://ccip.chain.link/#/side-drawer/msg/0x0d7fa7a3abf9db4e7e88494b8e224c19411e68af67cd63f3dfe925c9224cf72c

#### Move 6: 2 1
npx hardhat ttt-move --x 2 --y 1 --player 2 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1

✅ Message sent, you make a move! transaction hash: 0x4a16cfea5f1bc3ee6d0528fc07fde3c88ab80c2f39f277989bf3370bd028bbf9

https://ccip.chain.link/#/side-drawer/msg/0x1f145ed932df0df790339a3ebde98a54875c25ea9eef9af18113cddda97ea797

#### Move 8: 0 2
npx hardhat ttt-move --x 0 --y 2 --player 2 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1

✅ Message sent, you make a move! transaction hash: 0x94a96d8f8efb296801b4bff15e4a7f32927eabe05a1c6dc25e992c4eac2a73f8

https://ccip.chain.link/#/side-drawer/msg/0x15d469fd3d033d3f3f48eaecad04b3c93fd911f82396331500143657cd3c958f

### Player 1 makes a move in Blockchain 1

#### Move 1: 0 0
npx hardhat ttt-move --x 0 --y 0 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

✅ Message sent, you make a move! transaction hash: 0xf467b0ad69cde1dba714e0629b490c8bb21f2099416d1b11ad2a9773856747bd

https://ccip.chain.link/#/side-drawer/msg/0x89530fb737ea08c723f2ef0dbfd9c28d8f350bd7c34aecc13c0d1dca23adb163

#### Move 3: 1 1
npx hardhat ttt-move --x 1 --y 1 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

✅ Message sent, you make a move! transaction hash: 0x5f3c34b1d2db4d628bfcc19553de97fb325b1f58e927c829b1bebcfdec40676f

https://ccip.chain.link/#/side-drawer/msg/0xb12462796133d739a889de747e00b21998224635447c60dd3c21cf5490bbefdb

#### Move 5: 2 2
npx hardhat ttt-move --x 2 --y 2 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

✅ Message sent, you make a move! transaction hash: 0x06b8bcb9f86b7aaa69f2db440279f472a15213863295feb34938310e25056d9f

https://ccip.chain.link/#/side-drawer/msg/0xe8a68d903167912c5c63ddd346630686ddf22f94b76bd4f6f846c9a81cc2a6e7

#### Move 7: 1 0
npx hardhat ttt-move --x 1 --y 0 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

✅ Message sent, you make a move! transaction hash: 0xcf0254edf3ca9e7ac0b14e2c14f3db7b9ef8922ed452ee82732bcfee74a7c7b8

https://ccip.chain.link/#/side-drawer/msg/0x46c0eae3e2f1524522bd813ccbdb483930e48f9a0ff4628907bfb9b461320240

#### Move 9: 2 0
npx hardhat ttt-move --x 2 --y 0 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

✅ Message sent, you make a move! transaction hash: 0x5339ae596759fbc3eb639e829c69c8c5e52ef03e28f0f95a3c2f8ed6ab1a0c57

https://ccip.chain.link/#/side-drawer/msg/0xf1bc59965f9ea8508876b8f3f9193587a6eccd59acf78c57a40f372c39cf8ee6

### Check the winner

npx hardhat ttt-check-winner --blockchain ethereumSepolia --contract 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 

#### winner of sessionId 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 is: 0x1e74DC196C1372C3535d070574e9509513b7DF85

npx hardhat ttt-check-winner --blockchain avalancheFuji --contract 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69


