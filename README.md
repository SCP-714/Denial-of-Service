# Denial of Service

## A look at different types of attacks

  ### - Which of the following best describes the key difference between DoS and DDoS?
    - Attackers use numerous computers and connections.
        - The DoS attacks that you probably hear the most about are distributed denial-of-service attacks (DDoS). The key difference is these attacks use numerous computers and numerous internet connections across the world to overload the target systems. DDoS attacks are usually executed through a network of devices that the attacker has gained control of.
        DoS attacks use a single connection to attack a single target. With all DoS attacks, the attacker sends a large number of legitimate-looking requests to the server in a way that the server cannot determine which requests are valid and which are not. This barrage of requests will overwhelm the system to the point that the server cannot manage the capacity, resulting in the server being inaccessible to other users.

  ### - An attacker may use compromised websites and emails to distribute specially designed malware to poorly secured devices. This malware provides an access point to the attacker, which he can use to control the device. Which of the following devices can the attacker use?
    - Any device that can communicate over the Internet can be hacked.
      - With the advancement of the Internet of Things, it's important to note that zombie devices aren't limited to desktops and laptops. Any device that can communicate over the Internet can be hacked. This includes security cameras, DVR players, and even kitchen appliances.

  ### - Which of the following motivates attackers to use DoS and DDoS attacks?

    - Hacktivism, profit, and damage reputation
      - The following are motivation for DoS and DDoS Attacks:
      Distraction
      Damage reputation
      Hacktivism
      Fun
      Profit

  ### - Which of the following is an attack where all traffic is blocked by taking up all available bandwidth between the target computer and the Internet?

    - Volumetric attack

      - Volumetric attacks block traffic by taking up all available bandwidth between the target and the Internet.
      
      Fragmentation attacks target a system's ability to reassemble fragmented packets.
      
      Amplification attacks exploit vulnerabilities in protocols and broadcast networks. The name is derived from the idea that the attacker uses intermediary computers and networks to amplify         the impact of their attack.
      
      Phlashing, also known as bricking, involves pushing incorrect updates to a system's firmware, causing irreversible damage and rendering the device about as useful as a brick.

  ### - Which of the following tools can be used to create botnets?

    - Shark, PlugBot, and Poison Ivy 
    
    - Botnets are typically used to carryout DoS and DDoS attacks. You can use the following tools to create botnets:
    
    Shark
    PlugBot
    Poison Ivy
    Trin00 is a set of programs used for DoS attacks.
    Jolt2 is a DoS tool that sends numerous fragmented packets to a Windows machine.
    Targa is a multifunctional tool that can execute WinNuke and teardrop attacks.
    Low Orbit Ion Cannon (LOIC) is a free and easy to use DoS tool.

  ### - A hacker has discovered UDP protocol weaknesses on a target system. The hacker attempts to send large numbers of UDP packets from a system with a spoofed IP address, which broadcasts out to the network in an attempt to flood the target system with an overwhelming amount of UDP responses. Which of the following DoS attacks is the hacker attempting to use?
  
  - Fraggle attack
  - A fraggle attack is a DoS attack that targets UDP protocol weaknesses. A large number of UDP packets from a spoofed IP address are broadcast to a network in an attempt to flood the target computer.

A Smurf attack is a DoS attack that targets ICMP protocol weaknesses.

A SYN flood exploits the TCP three-way handshake. An attacker creates SYN packets with a non-existent source address. When the target machine responds with a SYN-ACK, it goes to the non-existent address, causing the target machine to wait for a response that they will never get.

A Teardrop attack prevents TCP/IP packets from being reassembled. This is done by setting the flags on all frames to indicate that they are fragments and providing instructions to connect to another frame that doesn't actually exist.
    
  ### - The ping command is designed to test connectivity between two computers. There are several command options available to customize ping, making it a useful tool for network administrators. On Windows, the default number of ping requests is set is four. Which of the following command options will change the default number of ping requests?

  - -n
    
ping -n defines the number of echo requests to send.

ping -a is used to resolve adresses to hostnames.

ping -l is used to send the buffer size.

ping -f is used to set the don't fragment flag in packet.

  ### - You are using Wireshark to try and determine if a denial-of-service (DDoS) attack is happening on your network (128.28.1.1). You previously captured packets using the tcp.flags.syn==1 and tcp.flags.ack==1 filter, but only saw a few SYN-ACK packets. You have now changed the filter to tcp.flags.syn==1 and tcp.flags.ack==0. After examining the Wireshark results shown in the image, which of the following is the best reason to conclude that a DDoS attack is happening?

![Screenshot 2024-05-14 at 2 20 02 PM](https://github.com/SCP-714/Denial-of-Service/assets/113054208/4c76d674-7ef2-47a0-b688-d58a017eae60)

  - There are multiple SYN packets with different source addresses destined for 128.28.1.1
  - Explanation
The captured and filtered packets show many SYN packets being sent from many different sources, but all destined for the same target or destination address. This is a strong indication that a DDoS attack is currently happening.

Whether they are legitimate or created by a hacker, SYN packets have a hex value of 0x002.

Since a DDoS flood is happening, there isn't time or bandwidth available to see many (if any) matching SYN-ACK packets.

  ### - You suspect that an ICMP flood attack is taking place from time to time, so you have used Wireshark to capture packets using the tcp.flags.syn==1 filter. Initially, you saw an occasional SYN or ACK packet. After a short while, however, you started seeing packets as shown in the image.

Using the information shown, which of the following explains the difference between normal ICMP (ping) requests and an ICMP flood?

![Screenshot 2024-05-14 at 2 21 22 PM](https://github.com/SCP-714/Denial-of-Service/assets/113054208/6d57629c-020a-4dc5-a8d4-db0acad50fb6)

  - With the flood, all packets come from the same source IP address in quick succession.
  - Explanation
In comparison to the occasional ICMP ping requests that can be seen on a network, when an ICMP flood attack is happening, the ICMP packets are sent in quick succession from the same source IP address. As a result, there is little bandwidth available to receive many (if any) ACK or SYN packets.

As can be seen from the packets captured, normal ICMP packets can come from different source addresses, such as 192.168.0.33 and 192.168.0.31.

The ping command will send 4 by default if -n isn't used.

  ### - Which of the following best describes a DoS attack?

  - A hacker overwhelms or damages a system and prevents users from accessing a service.
  - Explanation
A DoS attack is an attack on the availability of a service by disrupting, denying, or otherwise interfering with the ability to keep a service available. The more you understand what a DoS attack is and what can happen, the better prepared you are to use countermeasures.

Impersonating an authorized user by gaining access to their tokens is a way to gain unauthorized access by using a cryptographic attack.

Using every character, word, or letter to gain unauthorized access is also known as a brute-force attack.

Intercepting traffic is a type of sniffing, which does not cause a DoS attack.

  ### - Which of the following best describes a reverse proxy method for protecting a system from a DoS attack?

  - Redirects all traffic before it is forwarded to a server, so the redirected system takes the impact.
    - Explanation
When a DoS attack occurs and a proxy server takes the impact, this is known as a Reverse Proxy DoS protection method. This method redirects all traffic to the reverse proxy before it is forwarded to the real server.

Creating an area of the network called a black hole, where offending traffic is forwarded and dropped, is another attack protection method called Black Hole Filtering.

Enabling router throttling can limit the potential impact of a DoS attack and can provide a bit of additional time for administrators to respond to an attack.

Adding extra services, such as load balancing and excess bandwidth, can help provide too many platforms for the attacker to be able to flood. This method is called absorbing the attack.

  ### - Creating an area of the network where offending traffic is forwarded and dropped is known as _________?

  - Black hole filtering
  - Explanation
Black hole filtering creates an area of the network called a black hole where offending traffic is forwarded and dropped.

Router throttling limits the potential impact of a DoS attack and can provide a bit of additional time for administrators to respond to an attack.

All traffic is redirected to the reverse proxy before being forwarded to the real server. In the event of an attack, the proxy takes the impact.

Anti-spoofing measures ensure that spoofed packets are unable to infiltrate your network.

  ### - It is important to be prepared for a DoS attack. These attacks are becoming more common. Which of the following best describes the response you should take for a service degradation?

  - Services can be set to throttle or even shut down.
  - Explanation
To respond to a service degradation, services can be set to throttle or even shut down in the event of an attack.

You should have more than one upstream connection to use as a failover in the event of a flooding attack.

To absorb an attack, add extra services such as load balancing and excess bandwidth so that you have too much on your network for the attacker to execute a flood attack.

Your response plan should include a checklist of all the threat assessment tools and hardware protections that you have in place.
  

### Skills Learned
[Bullet Points - Remove this afterwards]

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

