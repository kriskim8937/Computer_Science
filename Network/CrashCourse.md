## Computer network
- How to send and recieve data over a global telecommunications network?
## History of network
- The first computer networks appeared in the 1950 and 60s
- They were generally used within an organization like a company or research lab facilitate 
- It makes exchange of information between different people and computers much faster.
- A second benefit of networks was the ability to share physical resources. 
- These relatively small networks of close-by computers are called Local Area Networks, **LAN**
- Although many LAN technologies were developed and deployed, the most famous and succesful was Ethernet, developed in the early 1970s at Xerox PARC, and still widely used today. 
- **Ethernet** In its simplest form, a series of computers are connected to a single, common ethernet cable.
- When a computer wants to transmit data to another computer, it writes the data, as an electrical signal, onto the cable.

> Hi, I’m Carrie Anne, and welcome to CrashCourseComputer Science!The internet is amazing.
> In just a few keystrokes, we can stream videoson Youtube -- Hello! -- read articles on Wikipedia,order supplies on amazon, video chat withfriends, and tweet about the weather.
> Without a doubt, the ability for computers,and their users, to send and receive informationover a globaltelecommunications network forever changedthe world.
> 150 years ago, sending a letter from Londonto California would have taken two to threeweeks, and that’s if you paid for expressmail.
> Today, that email takes a fraction of a second.
> This million fold improvement in latency,that’s the time it takes for a message totransfer, juiced up the global economy helpingthe modern world to move at the speed of lighton fiber optic cables spanning the globe.
> You might think that computers and networksalways went hand in hand, but actually mostcomputers pre-1970 were humming away all alone.
> However, as big computers began popping upeverywhere, and low cost machines startedto show up on people’s desks, it becameincreasingly useful to share data and resources,and the first networks of computers appeared.
> Today, we’re going to start a three-episodearc on how computer networks came into beingand the fundamental principles and techniquesthat power them.
> INTROThe first computer networks appeared in the1950s and 60s.
> They were generally used within an organization– like a company or research lab – tofacilitate the exchange of information betweendifferent people and computers.
> This was faster and more reliable than theprevious method of having someone walk a pileof punch cards, or a reel of magnetic tape,to a computer on the other side of a building‒ which was later dubbed a sneakernet.
> A second benefit of networks was the abilityto share physical resources.
> For example, instead of each computer havingits own printer, everyone could share oneattached to the network.
> It was also common on early networks to havelarge, shared, storage drives, ones too expensiveto have attached to every machine.
> These relatively small networks of close-bycomputers are called Local Area Networks,or LANs.
> A LAN could be as small as two machines inthe same room, or as large as a universitycampus with thousands of computers.
> Although many LAN technologies were developedand deployed, the most famous and succesfulwas Ethernet, developed in the early 1970sat Xerox PARC, and still widely used today.
> In its simplest form, a series of computersare connected to a single, common ethernet cable.
> When a computer wants to transmit data toanother computer, it writes the data, as anelectrical signal, onto the cable.
> Of course, because the cable is shared, everycomputer plugged into the network sees thetransmission, but doesn’t know if data isintended for them or another computer.
> To solve this problem, Ethernet requires thateach computer has a unique Media Access Controladdress, or MAC address.
> This unique address is put into a header thatprefixes any data sent over the network.
> So, computers simply listen to the ethernetcable, and only process data when they seetheir address in the header.
> This works really well; every computer madetoday comes with its own unique MAC addressfor both Ethernet and WiFi.
> The general term for this approach is CarrierSense Multiple Access, or CSMA for short.
> The “carrier”, in this case, is any sharedtransmission medium that carries data – copperwire in the case of ethernet, and the aircarrying radio waves for WiFi.
> Many computers can simultaneously sense thecarrier, hence the “Sense” and “MultipleAccess”, and the rate at which a carriercan transmit data is called its Bandwidth.
> Unfortunately, using a shared carrier hasone big drawback.
> When network traffic is light, computers cansimply wait for silence on the carrier, andthen transmit their data.
> But, as network traffic increases, the probabilitythat two computers will attempt to write dataat the same time also increases.
> This is called a collision, and the data getsall garbled up, like two people trying totalk on the phone at the same time.
> Fortunately, computers can detect these collisionsby listening to the signal on the wire.
> The most obvious solution is for computersto stop transmitting, wait for silence, thentry again.
> Problem is, the other computer is going totry that too, and other computers on the networkthat have been waiting for the carrier togo silent will try to jump in during any pause.
> This just leads to more and more collisions.
> Soon, everyone is talking over one anotherand has a backlog of things they need to say,like breaking up with a boyfriend over a familyholiday dinner.
> Terrible idea!Ethernet had a surprisingly simple and effectivefix.
> When transmitting computers detect a collision,they wait for a brief period before attemptingto re-transmit.
> As an example, let’s say 1 second.
> Of course, this doesn’t work if all thecomputers use the same wait duration -- they’lljust collide again one second later.
> So, a random period is added: one computermight wait 1.3 seconds, while another waits1.5 seconds.
> With any luck, the computer that waited 1.3seconds will wake up, find the carrier tobe silent, and start transmitting.
> When the 1.5 second computer wakes up a momentlater, it’ll see the carrier is in use,and will wait for the other computer to finish.
> This definitely helps, but doesn’t totallysolve the problem, so an extra trick is used.
> As I just explained, if a computer detectsa collision while transmitting, it will wait1 second, plus some random extra time.
> However, if it collides again, which suggestsnetwork congestion, instead of waiting another1 second, this time it will wait 2 seconds.
> If it collides again, it’ll wait 4 seconds,and then 8, and then 16, and so on, untilit’s successful.
> With computers backing off, the rate of collisionsgoes down, and data starts moving again, freeingup the network.
> Family dinner saved!This “backing off” behavior using an exponentiallygrowing wait time is called Exponential Backoff.
> Both Ethernet and WiFi use it, and so do manytransmission protocols.
> But even with clever tricks like ExponentialBackoff, you could never have an entire university’sworth of computers on one shared ethernetcable.
> To reduce collisions and improve efficiency,we need to shrink the number of devices onany given shared carrier -- what’s calledthe Collision Domain.
> Let go back to our earlier Ethernet example,where we had six computers on one shared cable,a.k.a. one collision domain.
> To reduce the likelihood of collisions, wecan break this network into two collisiondomains by using a Network Switch.
> It sits between our two smaller networks,and only passes data between them if necessary.
> It does this by keeping a list of what MACaddresses are on what side of the network.
> So if A wants to transmit to C, the switchdoesn’t forward the data to the other network– there’s no need.
> This means if E wants to transmit to F atthe same time, the network is wide open, andtwo transmissions can happen at once.
> But, if F wants to send data to A, then theswitch passes it through, and the two networksare both briefly occupied.
> This is essentially how big computer networksare constructed, including the biggest oneof all – The Internet – which literallyinter-connects a bunch of smaller networks,allowing inter-network communication.
> What’s interesting about these big networks,is that there’s often multiple paths toget data from one location to another.
> And this brings us to another fundamentalnetworking topic, routing.
> The simplest way to connect two distant computers,or networks, is by allocating a communicationline for their exclusive use.
> This is how early telephone systems worked.
> For example, there might be 5 telephone linesrunning between Indianapolis and Missoula.
> If John picked up the phone wanting to callHank, in the 1910s, John would tell a humanoperator where he wanted to call, and they’dphysically connect John’s phone line intoan unused line running to Missoula.
> For the length of the call, that line wasoccupied, and if all 5 lines were alreadyin use, John would have to wait for one tobecome free.
> This approach is called Circuit Switching,because you’re literally switching wholecircuits to route traffic to the correct destination.
> It works fine, but it’s relatively inflexibleand expensive, because there’s often unusedcapacity.
> On the upside, once you have a line to yourself– or if you have the money to buy one foryour private use – you can use it to itsfull capacity, without having to share.
> For this reason, the military, banks and otherhigh importance operations still buy dedicatedcircuits to connect their data centers.
> Another approach for getting data from oneplace to another is Message Switching, whichis sort of like how the postal system works.
> Instead of dedicated route from A to B, messagesare passed through several stops.
> So if John writes a letter to Hank, it mightgo from Indianapolis to Chicago, and thenhop to Minneapolis, then Billings, and thenfinally make it to Missoula.
> Each stop knows where to send it next becausethey keep a table of where to pass lettersgiven a destination address.
> What’s neat about Message Switching is thatit can use different routes, making communicationmore reliable and fault-tolerant.
> Sticking with our mail example, if there’sa blizzard in Minneapolis grinding thingsto a halt, the Chicago mail hub can decideto route the letter through Omaha instead.
> In our example, cities are acting like networkrouters.
> The number of hops a message takes along aroute is called the hop count.
> Keeping track of the hop count is useful becauseit can help identify routing problems.
> For example, let’s say Chicago thinks thefastest route to Missoula is through Omaha,but Omaha thinks the fastest route is throughChicago.
> That's bad, because both cities are goingto look at the destination address, Missoula,and end up passing the message back and forthbetween them, endlessly.
> Not only is this wasting bandwidth, but it’sa routing error that needs to get fixed!This kind of error can be detected becausethe hop count is stored with the message andupdated along its journey.
> If you start seeing messages with high hopcounts, you can bet something has gone awryin the routing!This threshold is the Hop Limit.
> A downside to Message Switching is that messagesare sometimes big.
> So, they can clog up the network, becausethe whole message has to be transmitted fromone stop to the next before continuing onits way.
> While a big file is transferring, that wholelink is tied up.
> Even if you have a tiny, one kilobyte emailtrying to get through, it either has to waitfor the big file transfer to finish or takea less efficient route.
> That’s bad.
> The solution is to chop up big transmissionsinto many small pieces, called packets.
> Just like with Message Switching, each packetcontains a destination address on the network,so routers know where to forward them.
> This format is defined by the “InternetProtocol”, or IP for short, a standard createdin the 1970s.
> Every computer connected to a network getsan IP Address.
> You’ve probably seen these as four, 8-bitnumbers written with dots in between.
> For example,172.217.7.238 is an IP Addressfor one of Google’s servers.
> With millions of computers online, all exchangingdata, bottlenecks can appear and disappearin milliseconds.
> Network routers are constantly trying to balancethe load across whatever routes they knowto ensure speedy and reliable delivery, whichis called congestion control.
> Sometimes different packets from the samemessage take different routes through a network.
> This opens the possibility of packets arrivingat their destination out of order, which isa problem for some applications.
> Fortunately, there are protocols that runon top of IP, like TCP/IP, that handle thisissue.
> We’ll talk more about that next week.
> Chopping up data into small packets, and passingthese along flexible routes with spare capacity,is so efficient and fault-tolerant, it’swhat the whole internet runs on today.
> This routing approach is called Packet Switching.
> It also has the nice property of being decentralized,with no central authority or single pointof failure.
> In fact, the threat of nuclear attack is whypacket switching was developed during thecold war!Today, routers all over the globe work cooperativelyto find efficient routings, exchanging informationwith each other using special protocols, likethe Internet Control Message Protocol (ICMP)and the Border Gateway Protocol (BGP).
> The world's first packet-switched network,and the ancestor to the modern internet, wasthe ARPANET, named after the US agency thatfunded it, the Advanced Research ProjectsAgency.
> Here’s what the entire ARPANET looked likein 1974.
> Each smaller circle is a location, like auniversity or research lab, that operateda router.
> They also plugged in one or more computers– you can see PDP-1’s, IBM System 360s,and even an ATLAS in London connected overa satellite link.
> Obviously the internet has grown by leapsand bounds in the decades since.
> Today, instead of a few dozen computers online,it’s estimated to be nearing 10 billion.
> And it continues to grow rapidly, especiallywith the advent of wifi-connected refrigeratorsand other smart appliances, forming an “internetof things”.
> So that’s part one – an overview of computernetworks.
> Is it a series of tubes?Well, sort of.
> Next week we’ll tackle some higher-leveltransmission protocols, slowly working ourway up to the World Wide Web.

