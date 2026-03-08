# Secure-VPN-design
In this project i want to design a system wich vpn's could use to allow for the users to stay anonymous themselves, even to the vpn (or at least give as little info as possible). 
I like to assume total compromise of all parties(so no silly mistakes can be made)

The big lines are as follows:

The vpn company generates tokens, these tokens are 256-bits long(so they can be hashed with SHA-256*). 
  When a client wants to connect, they provide a token and establish a connection for a session with the vpn.
  *i do not know why this would be necessairy yet but it probably will in te future cuz its about safe design.
  
These tokens can be distributed to vendors and clients, who can continue selling or sharing them,
  meaning that a token should not be able to be traced to a single person or user by purchase. 
  -Tokens also eliminate the need for accounts, wich could be used to track behavior.

Flaws of this:
  1:How can two customers guarantee a trade of tokens without the seller keeping a copy of the token to use later.
      -a solution could lie in how the stock market or blockchain guarantee that trades follow trough?
  2:Is the ip-adress of the person not exposed? (Or is it just enough data to not be able to build a profile?)
      -This would either be a case of trust, policy or law.

Quick inventarisation:
-Server side code for rerouting, , and token generation and memorisation.
-Cient side code(Extension, add-on or straight up a https-site*) *it would mean that it reloads and instead of 
  reloading the vpn-site the vpn sends you the site you wanted to visit with the vpn. (They fetch and send the site without)
