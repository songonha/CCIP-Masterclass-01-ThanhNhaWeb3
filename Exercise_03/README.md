# CCIP TIC TAC TOE

## CONTRACT ON FUJI: 

Command: npx hardhat run ./scripts/deployTicTacToe.ts --network avalancheFuji

✅ Tic Tac Toe Demo deployed at address 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 on avalancheFuji blockchain



Router FUJI: 0xF694E193200268f9a4868e4Aa017A0118C9a8177

Chain selector Fuji: 14767482510784806043


## CONTRACT ON SEPOLIA: 

Command: npx hardhat run ./scripts/deployTicTacToe.ts --network ethereumSepolia

✅ Tic Tac Toe Demo deployed at address 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 on ethereumSepolia blockchain



Router Sepolia: 0x0BF3dE8c5D3e8A2B34D2BEeB17ABfCeBaf363A59

Chain selector Sepolia: 16015286601757825753

### ROUTER UPDATE:

npx hardhat ttt-update-router --blockchain ethereumSepolia --contract 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --router 0x0BF3dE8c5D3e8A2B34D2BEeB17ABfCeBaf363A59

✅ Update successful, transaction hash: 0x02ee18bdd24ca8bfddb4a96655b98d1b768ec7a6f71b120cefc74930d9ca2943

npx hardhat ttt-update-router --blockchain avalancheFuji --contract 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --router 0xF694E193200268f9a4868e4Aa017A0118C9a8177

✅ Update successful, transaction hash: 0xd2e8fe94df509adbcdae95ca57ebbe0bd03be912dd96cb20d81d7952d555b94a

### DEPOSITE NATIVE TOKEN TO SMART CONTRACT

ON SEPOLIA: 0.1 ETH

ON FUJI: 2 AVAX

### START GAME BETWEEN SEPOLIA AND FUJI:

npx hardhat ttt-start --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

✅ Message sent, game session created! transaction hash: 0xaed281b5c52b2c15dc66e81af3ee38d1216f4a95e6a3aef9effddbefd510a682

### START GAME BETWEEN FUJI AND SEPOLIA:

npx hardhat ttt-start --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1




### Get session ID:

sessionId at index 0 is:

npx hardhat ttt-get-sessionId --blockchain ethereumSepolia --contract 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --index 0

sessionId at index 0 is: 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69

npx hardhat ttt-get-sessionId --blockchain avalancheFuji --contract 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --index 0



### Player 2 makes a move in Blockchain 2

#### Move 2: 
npx hardhat ttt-move --x 0 --y 1 --player 2 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain avalancheFuji --sender 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87 --destination-blockchain ethereumSepolia --receiver 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1



#### Move 4:
npx hardhat ttt-move --x 1 --y 2 --player 2 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain avalancheFuji --sender 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --destination-blockchain ethereumSepolia --receiver 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE

#### Move 6:
npx hardhat ttt-move --x 2 --y 1 --player 2 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain avalancheFuji --sender 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --destination-blockchain ethereumSepolia --receiver 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE

#### Move 8:
npx hardhat ttt-move --x 0 --y 2 --player 2 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain avalancheFuji --sender 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --destination-blockchain ethereumSepolia --receiver 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE

### Player 1 makes a move in Blockchain 1

#### Move 1: 
npx hardhat ttt-move --x 0 --y 0 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

✅ Message sent, you make a move! transaction hash: 0xf467b0ad69cde1dba714e0629b490c8bb21f2099416d1b11ad2a9773856747bd

#### Move 3: 
npx hardhat ttt-move --x 1 --y 1 --player 1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 --source-blockchain ethereumSepolia --sender 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --destination-blockchain avalancheFuji --receiver 0x5Cb1EFf2763065C7a8B0EA3bb45Bf669cBAFdB87

#### Move 5: 
npx hardhat ttt-move --x 2 --y 2 --player 1 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain ethereumSepolia --sender 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --destination-blockchain avalancheFuji --receiver 0x1a8110B7252d65E2C367e0B2285BE88DAe502486

#### Move 7: 
npx hardhat ttt-move --x 1 --y 0 --player 1 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain ethereumSepolia --sender 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --destination-blockchain avalancheFuji --receiver 0x1a8110B7252d65E2C367e0B2285BE88DAe502486

#### Move 9: 
npx hardhat ttt-move --x 2 --y 0 --player 1 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain ethereumSepolia --sender 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --destination-blockchain avalancheFuji --receiver 0x1a8110B7252d65E2C367e0B2285BE88DAe502486

### Check the winner

npx hardhat ttt-check-winner --blockchain ethereumSepolia --contract 0xDA63d08a3c32438d7bA2d762Be124b32B821FCd1 --session-id 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 

winner of sessionId 0xef5ae8233001b16f3aef789ab070b42cd03528a677501295a6a9b014346f7e69 is: 0x0000000000000000000000000000000000000000

npx hardhat ttt-check-winner --blockchain avalancheFuji --contract 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718


