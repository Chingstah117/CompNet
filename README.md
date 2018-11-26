# CompNet

Assignment 4
1.1
1. The memory of a shared-memory router needs to be able to support up to N enqueues and N dequeues on every tick so it can handle anything up to the worst case of a packet on each port.
2. Each memory of an output-queued router needs to be able to support up to N enqueues and 1 dequeue per tick. N seperate memories or 1 memory per output port is required.
3. Each memory of an input-queued router needs to be able to support up to 1 enqueue and 1 dequeue per tick. N seperate memories or 1 memory per input port is required. 
4. The advantage of using a shared-memory router is that it can dynamically allocate memories to the input/output ports. A disadvantage is that it requires up to N enqueues and N dequeues on every tick which can become memory intensive when compared to the N+1 and 1+1 required memory of output/input-queued routers respectively.
1.2
1. The optimal value is 1/N.
1.3
1. ALOHA requires a central authority to which users send data to one at a time whereas WiFi doesn’t have any sort of central authority.
This manifests itself in the design of ALOHA and WiFi MAC protocols through who gets the ability to choose who gets to transmit and when. ALOHA has the central authority dictating who and when by handing out time slots or channels. WiFi MAC protocols allow the users to choose who transmits and when through distribution. 
2. WiFi and Ethernet’s main difference is their forms. WiFi comes from a router and everybody connected that router will essentially share that router connection. This means that WiFi is a shared medium. Ethernet comes in the form of an Ethernet cable which limits its use to one computer. This allows the computer to be essentially connected to a private medium. 
3. This difference creates a difference in locality between their protocols. MAC protocols are local while congestion control is a global. MAC thus deals with the local network and optimizing the shared medium while Ethernet private use allows it to not be worried about a bottleneck on the local network.
1.4
1. “Carrier Sense” is the ability for one user on a shared medium to be able to tell if another user on that same medium is already transmitting data or not.
2. One implementation of carrier sense capability is
3. One example is when two users at opposite ends of a large area have the router in the middle of them and they attempt to upload large packets of data using that router. 
4. WiFi solves the hidden terminal problem by using RTS/CTS. Users sending data would first send a Request-to-Send. Because the RTS is short, there is a very low chance that two RTS would collide. The medium will then reply with a Clear-to-Send to the first RTS it receives and that user will be able to send their data first.
5. The Time Division Multiple Access protocol is when each user on a shared medium would use that medium for an allotted amount of time before the medium is given to the next user in round-robin order. Frequency Division Multiple Access protocol is when each user of a shared medium is given a portion of the frequency range or bandwidth of the medium. 
6. You would use the TDMA and FDMA protocols are commonly used in cellular networks.
7. They are different from how they do not use a distributed protocol to share a medium and how much longer typical TDMA/FDMA connections are.



Assignment 5
Michael Gao
Assignment 5 Design Report
	The project I am going to be designing is an automated blockchain payment application. The application will be a web-based system where users can either set up automatic payments or authorize payments. Ideally, this application would be used for companies billing customers for services such as electricity or gas. The idea would be to remove paper billing and to move to a more secure and transparent method of billing. 
	Each block of the blockchain will be able to be viewed by customers. The frequency of the blocks can be variable but the goal is for each user to either have a list of block signatures to know which block their transactions are in or to make the blocks infrequent enough so that it would be easy for them to find the blocks with something such as the date the transaction happened on. Of course, this would mean that the block sizes could be incredibly variable, possibly forcing the blocks to be large even if there are only a few transactions in the block. 
	Using basic blockchain concepts or even modifying it to make it easier in exchange for speed, each block would be easy to build. Each user would also need an account to link their transactions to. Each transaction would consist of multiple parts: amount, user_name or user_id, time, date, and possibly other bookkeeping things. The users would connect to the application server using sockets and for this assignment each account would simply have a user_name, a user_id, a balance, and a list of previous transactions. The list can either simply have a list of block signatures or a timestamp for each transaction. 

If this design seems infeasible, a simpler design report will follow:


	This project will be a simple chatbot that can be used for a video game called League of Legends. This bot will first take a list of champions that the user owns or wants to play as the first input. The bot will then request for a second input. The user can then specify a specific champion and role and then the bot will take the list of champions that the user owns or wants to play and then return an ordered list of the champions with the highest win rate champion at the start of the list. Next, the user can then input the champion they want to play, and the bot will return the skill order, runes, summoner spells, and item build for that champion for that matchup. 
The problem with most current LoL website is that they list all of the champions that they have enough data of matchups for. However, with over 140 champions in the game’s roster, many users will have difficulty reading through the list of champion “counters” and then finding a champ they want to play. This application seeks to make it simpler and hopefully quicker for users to figure out why they want to play and what runes to go. WIth there being a time limit in champion select for choosing a champion, building a rune page, and selecting summoner spells, it can become very stressful when someone is last pick and has less than a minute to both decide who to play and setting up the runes and summoner spells for that champion. Websites take time to load, there is a ton of data to read and go through, and not setting everything up in time can mean losing the entire game.
