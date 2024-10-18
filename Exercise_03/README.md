# CCIP TIC TAC TOE

## CONTRACT ON FUJI: 

Command: npx hardhat run ./scripts/deployTicTacToe.ts --network avalancheFuji





Router FUJI: 0xF694E193200268f9a4868e4Aa017A0118C9a8177

Chain selector Fuji: 14767482510784806043


## CONTRACT ON SEPOLIA: 

Command: npx hardhat run ./scripts/deployTicTacToe.ts --network ethereumSepolia





Router Sepolia: 0x0BF3dE8c5D3e8A2B34D2BEeB17ABfCeBaf363A59

Chain selector Sepolia: 16015286601757825753

### ROUTER UPDATE:

npx hardhat ttt-update-router --blockchain ethereumSepolia --contract 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --router 0x0BF3dE8c5D3e8A2B34D2BEeB17ABfCeBaf363A59



npx hardhat ttt-update-router --blockchain avalancheFuji --contract 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --router 0xF694E193200268f9a4868e4Aa017A0118C9a8177



### DEPOSITE NATIVE TOKEN TO SMART CONTRACT

ON SEPOLIA: 0.1 ETH

ON FUJI: 2 AVAX

### START GAME BETWEEN SEPOLIA AND FUJI:

npx hardhat ttt-start --source-blockchain ethereumSepolia --sender 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --destination-blockchain avalancheFuji --receiver 0x1a8110B7252d65E2C367e0B2285BE88DAe502486



### START GAME BETWEEN FUJI AND SEPOLIA:

npx hardhat ttt-start --source-blockchain avalancheFuji --sender 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --destination-blockchain ethereumSepolia --receiver 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE




### Get session ID:

sessionId at index 0 is:

npx hardhat ttt-get-sessionId --blockchain ethereumSepolia --contract 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --index 0

npx hardhat ttt-get-sessionId --blockchain avalancheFuji --contract 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --index 0



### Player 2 makes a move in Blockchain 2

#### Move 2: 
npx hardhat ttt-move --x 0 --y 1 --player 2 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain avalancheFuji --sender 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --destination-blockchain ethereumSepolia --receiver 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE



#### Move 4:
npx hardhat ttt-move --x 1 --y 2 --player 2 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain avalancheFuji --sender 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --destination-blockchain ethereumSepolia --receiver 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE

#### Move 6:
npx hardhat ttt-move --x 2 --y 1 --player 2 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain avalancheFuji --sender 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --destination-blockchain ethereumSepolia --receiver 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE

#### Move 8:
npx hardhat ttt-move --x 0 --y 2 --player 2 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain avalancheFuji --sender 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --destination-blockchain ethereumSepolia --receiver 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE

### Player 1 makes a move in Blockchain 1

#### Move 1: 
npx hardhat ttt-move --x 0 --y 0 --player 1 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain ethereumSepolia --sender 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --destination-blockchain avalancheFuji --receiver 0x1a8110B7252d65E2C367e0B2285BE88DAe502486



#### Move 3: 
npx hardhat ttt-move --x 1 --y 1 --player 1 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain ethereumSepolia --sender 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --destination-blockchain avalancheFuji --receiver 0x1a8110B7252d65E2C367e0B2285BE88DAe502486

#### Move 5: 
npx hardhat ttt-move --x 2 --y 2 --player 1 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain ethereumSepolia --sender 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --destination-blockchain avalancheFuji --receiver 0x1a8110B7252d65E2C367e0B2285BE88DAe502486

#### Move 7: 
npx hardhat ttt-move --x 1 --y 0 --player 1 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain ethereumSepolia --sender 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --destination-blockchain avalancheFuji --receiver 0x1a8110B7252d65E2C367e0B2285BE88DAe502486

#### Move 9: 
npx hardhat ttt-move --x 2 --y 0 --player 1 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 --source-blockchain ethereumSepolia --sender 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --destination-blockchain avalancheFuji --receiver 0x1a8110B7252d65E2C367e0B2285BE88DAe502486

### Check the winner

npx hardhat ttt-check-winner --blockchain ethereumSepolia --contract 0x4726E37410e20C86a4DA66FdF53f419BBF4E64fE --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718 


npx hardhat ttt-check-winner --blockchain avalancheFuji --contract 0x1a8110B7252d65E2C367e0B2285BE88DAe502486 --session-id 0xbb9ae76f71906dbfbdddc3f3ad5fd0f456def88953723700d04ab4d19bc7f718


