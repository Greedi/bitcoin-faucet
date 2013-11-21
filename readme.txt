bitcoin faucet public release
------------------------------------------
Forum Thread: https://bitcointalk.org/index.php?topic=101407.0
this is the simplest version of it, other might get released in time

made by Greedi 2012 (c)
updated by Joseph White 2013-2014 (c) joesfreicoinpool@gmail.com http://pool.cr.rs


INSTALL
===============
Clone this repository with git
Put files in www dir (or subdirectory if you so wish)
Edit core/config.php with proper values (server address, username, bitcoin rpc info)

Create the faucet database
$ mysql -u username -p -h host faucet < faucet.sql
> create database faucet;

Import faucet.sql into mysql

$ mysql -u username -p -h host faucet < faucet.sql

If you wish to be able to see your servers statistics then you need to edit the
$yourIP in the config file is your private ip address of the computer you will access the faucet with
set you're IP, so you can access the server.php page

Create a faucet donation account on bitcoind as well as a a sendout account
"FaucetDonations" - Faucet donation account
$ bitcoind getnewaddress FaucetDonations

"SendOut" - Sendout account
$ bitcoind getnewaddress SendOut

NOTE: Some wil maybe have to create the faucet donation account in there bitcoind
account have to be FaucetDonations and/or SendOut

NOTES
===============
This should work for any coin that uses RPC commands, just change the rpc ports and passwords
as needed.

This has been noted to work on FreiCoin and properly takes demurrage in to account

This updated code has not been throughly tested, use at your own risk.

Do make sure to add more security checks. This is most likely still insecure.



Donations
===============
Greedi's addresses 
LTC: Lh4c3cYcmvoksUNJLFT2Z5zsUmKUFgAUF5
BTC: 1MFH5dY85Ve4Q6KYPGJnfPmiHP2UxmXend

Joe's address (FreiCoin FRC Please)
FRC: 1FRCJoeWXbYe47cmuW3do8VoqAr9HuWbpJ

Joe's FreiCoin Faucet (running a much more heavily modified and secured version of this script)
http://frc.now.im
