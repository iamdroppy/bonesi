![http://madm.dfki.de/lib/tpl/dfki/images/logo.jpg](http://madm.dfki.de/lib/tpl/dfki/images/logo.jpg)

**BoNeSi**, the DDoS Botnet Simulator is a Tool to simulate Botnet Traffic in a testbed environment on the wire. It is designed to study the effect of DDoS attacks.

_What traffic can be generated?_

**BoNeSi** generates ICMP, UDP and TCP (HTTP) flooding attacks from a defined botnet size (different IP addresses). **BoNeSi** is highly configurable and rates, data volume, source IP addresses, URLs and other parameters can be configured.

_What makes it different from other tools?_

There are plenty of other tools out there to spoof IP addresses with UDP and ICMP, but for TCP spoofing, there is no solution. **BoNeSi** is the first tool to simulate HTTP-GET floods from large-scale bot networks. **BoNeSi** also tries to avoid to generate packets with easy identifiable patterns (which can be filtered out easily).


_Where can I run **BoNeSi**?_

We highly recommend to run **BoNeSi** in a closed testbed environment. However, UDP and ICMP attacks could be run in the internet as well, but you should be carefull. HTTP-Flooding attacks can not be simulated in the internet, because answers from the webserver must be routed back to the host running **BoNeSi**.

_How does TCP Spoofing work?_

**BoNeSi** sniffs for TCP packets on the network interface and responds to all packets in order to establish TCP connections. For this feature, it is necessary, that all traffic from the target webserver is routed back to the host running **BoNeSi**

_How good is the perfomance of **BoNeSi**?_

We focused very much on performance in order to simulate big botnets. On an AMD Opteron with 2Ghz we were able to generate up to 150,000 packets per second. On a more recent AMD Phenom II X6 1100T with 3.3Ghz you can generate 300,000 pps (running on 2 cores).

_Are **BoNeSi** attacks successful?_

Yes, they are very successful. UDP/ ICMP attacks can easily fill the bandwidth and HTTP-Flooding attacks knock out webservers fast. We also tested **BoNeSi** against state-of-the-art commercial DDoS mitigation systems and where able to either crash them or hiding the attack from being detected.

<b>A demo video of BoNeSi in action can be found <a href='http://madm.dfki.de/projects/netcentricsecurity'>here</a>.</b>