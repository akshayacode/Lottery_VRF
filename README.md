# Lottery_VRF

## Owner Address

0x5097267330F844B70BDBc5cbA4E42367D2b7766c

## LOT Contract Address

0x1487D135cA2fBA5F31Fa735C956e06e6c4F310D6

## Lottery contract Address

0xbdef81A0c5cF365CdE7929808245165A65c57295

## Pre deployment steps

Create VRF subscription and get the subscription id (2663)

## Steps to Run 

1. Deploy the LOT contract
2. Deploy Lottery contract by passing the parameter values like subscription id, vrf corrdinator address , token is the LOT token address and the ticket price(100)
3. Copy the lottery contract address and add it as a Consumer 
4. call the function ticketprice() in lottery contract
5. Transfer the ticketprice to the participant in LOT token contract 
6. Approve the spender(player1) with amount as ticket price
7. Approve the spender( Lottery contract address) with amount greater than ticket price( Since we have many participants ) 
8. Verify the allowance in LOT token contract 
9. Start the lottery
10. Participate in lottery ( For each participant repeat step - 5,6,7 and 8)
11. Check balance of each participant in LOT contract address ( Should transfer the ticketprice to lottery contract address)
12. end the lottery
13. Winner and the owner should get their percentage of tokens specified while initializing the lottery contract address
