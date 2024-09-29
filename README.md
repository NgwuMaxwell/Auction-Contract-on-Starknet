# Auction-Contract-on-Starknet
I built an auction contract, in this repository, using Cairo Programming Language on Starknet.
The project focuses on introducing writing testing and deploying smart contract using scarb and starknet foundry.
As part of the GIDA Academy’s blockchain development curriculum, This contract is written in cairo and is designed to allow users to bid on an item, with the highest bidder winning the auction. 

interface


#[starknet::interface]
trait IAuction<T>{fn register_item(ref self:T,item_name: ByteArray);

    fn unregister_item(ref self:T,item_name: ByteArray);

    fn bid(ref self:T,item_name:ByteArray,amount:u32);

    fn get_highest_bidder(self:@T, item_name:ByteArray)->u32;
    
    fn is_registered(self:@T, item_name:ByteArray)->bool;}
