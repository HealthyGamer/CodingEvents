# How Does the Internet Actually Work?

Unfortunately, this is going to be a terminology-heavy topic. The concepts themselves are comparatively simple. The challenge for most people is that these simple components have names that aren't always easy to recognize.

## Simple Networks

The simplest network is just two computers connected directly. We still do this sometimes when you connect two devices with a USB cable. Some devices, like my ReMarkable, even use a web interface to facilitate communication.

The problem with this is it becomes way too many cables (or wifi/BlueTooth channels) far too quickly and there's no way to connect every device to every other device and maintain a network of any size.

## Routers

We use routers to keep it to one "cable" per device. The one in your house probably has many more features than we are talking about here, but it serves this primary purpose. A router routes the data to different devices based on an address, and we can even connect routers to other routers to create an expandible network. The one we are most familiar with is IP addresses.

## Internet Service Providers

While routers can connect us to as many computers as we want, they only connect devices we control. It doesn't get us to external servers. To do that, we pay ISPs to join us in the outside world. There are three tiers of ISPs based on how much area they can cover, but the Tier 1 ones are the "most important" in creating the internet. These are the large tech companies, and they are the ones that own things like the network cables that cross oceans, which is sometimes called the internet backbone. Tier 2 and 3 also own their infrastructure, but over a much smaller area.

## Internet Exchange Points

ISPs often need to connect between their network and systems owned by a different tier 1 provider. While they will sometimes negotiate directly, there are also connection points known as IXPs or internet exchange points. These are usually run by some form of a neutral party, like non-profits, governments, or a separate company. These locations allow different tier 1 ISPs to connect to any other ISP without needing a contract with that ISP directly.

### TCP/IP

TCP/IP stands for Transmission Control Protocol/Internet Protocol. The vast majority of internet traffic uses this protocol to communicate. Its main goal is to ensure reliable communication. A similar protocol, UDP, drops the reliability in favor of a lot less back-and-forth for exchanging information.

TCP consists of four layers.

1. Datalink Layer: These are the physical devices—cables, routers, network cards, etc.
2. Internet Layer: This is made up of things like ISPs and DNS services-- the way that machines are connected.
3. Transport Layer: Once the connection is made, the transport layer is where the conversation happens that transfers the data. In TCP there are several steps to ensure the data is sent accurately.
4. Application Layer: The application layer is the one you interact with. This is things like a web browser, email client, or even Discord.

## IP Addresses

An IP address is just that, an address. Every internet-connected device in the world has an IP address. There are a couple of ways to divide this up.

### IPv4 vs IPv6

The first is IPv4 vs. IPv6. The internet grew up on IPv4, and it's the one most people know. This is the four-section set of numbers like 192.168.1.1. However, we've long since created more internet-connected devices than this system can handle. There are quite a few ways this has been dealt with, but one of the primary ones is IPv6. Those addresses are a lot harder to read: 2001:0db8:3c4d:0015:0000:0000:1a2f:1a2b. From a technical perspective, though, all those extra characters drastically increase the number of addresses available. There are 2^128 possible addresses, enough to outlive humans. That being said, the IP addresses we use most of the time as tech professionals are still IPv4.

### Public vs. Private IP Addresses

Public IP addresses are available to the external internet. Private ones exist inside of a private network.

There are three sets of IPv4 addresses that are reserved for private use.

- 10.0.0.0 to 10.255.255.255
- 172.16.0.0 to 172.31.255.255
- 192.168.0.0 to 192.168.255.255

The way it often works in the real world is because an internet-connected system will have a single public address, which is then routed to any number of internal devices that each have a private IP. You can see this in your home network. Unless you have a special setup, if you loop up your IP address on Google or a similar service, you will get the same public IP on every device. This is the device's IP address that actually connects to the internet. From there, your router will assign each device a private IP address.

## Domain Name System

IP addresses would suck to memorize, so instead, we use domains. However, that requires translating that domain into an IP address. This involves the maintenance of enormous routing tables, where every domain is mapped to a specific IP address.

Many ISPs will keep their own copies of these tables in order to speed up requests, but just like they share IXP services, there are also a set of DNS servers that hold the "official" version of these tables.

The part you might see as a setting on your computer or router is the address of the DNS resolver you want to use. A couple of common ones are Google (8.8.8.8), Cloudflare (1.1.1.1), and OpenDNS (208.67.222.222). These resolvers look at the top-level domain (TLD), like .com, .net, or .gg and send the request to the specific TLD server.

ICANN (Internet Corporation for Assigned Names and Numbers) assigns these TLDs to specific companies to manage. For example, VeriSign has the official version of every .com address on the internet.

### Domain Registrars

The final piece of this puzzle is the domain registrars. These are companies like Namecheap that act as a go-between for people looking to register a domain and TLD services like VeriSign.

There is a lot more depth to this topic, but hopefully, that gives you an idea of some of these basic concepts you hear about all the time in the tech industry.
