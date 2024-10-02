sequenceDiagram
    participant Attacker
    participant BotNet
    participant WebServer
    participant Firewall

    Attacker->>BotNet: Instruct to initiate attack
    BotNet->>WebServer: Send overwhelming traffic
    WebServer->>Firewall: Forward traffic for filtering
    Firewall->>WebServer: Allow legitimate traffic
    WebServer->>Firewall: Report high traffic alert
    Firewall->>BotNet: Block malicious traffic
    BotNet->>Attacker: Report attack status

Detailed Explanation:

Attacker Instructs BotNet to Initiate Attack: 
Attacker: The individual or group orchestrating the DDoS attack. They control the botnet and send commands to initiate the attack.
BotNet: A network of compromised computers (bots) controlled by the attacker. These bots are used to generate a massive amount of traffic aimed at the target.
Action: The attacker sends instructions to the botnet to start the attack on the web server.

BotNet Sends Overwhelming Traffic to WebServer:
BotNet: Executes the attack by sending a flood of traffic to the target web server. This traffic can be in the form of HTTP requests, UDP packets, or other types of data.
WebServer: The target of the attack, which is overwhelmed by the sheer volume of incoming traffic.
Action: The botnet generates and sends a large volume of traffic to the web server, aiming to exhaust its resources and make it unavailable to legitimate users.

WebServer Forwards Traffic for Filtering:
WebServer: Receives the incoming traffic and forwards it to the firewall for filtering.
Firewall: A security device that monitors and controls incoming and outgoing network traffic based on predetermined security rules.
Action: The web server forwards the traffic to the firewall to filter out malicious requests and allow legitimate ones.

Firewall Allows Legitimate Traffic:
Firewall: Analyzes the incoming traffic and filters out malicious requests based on predefined rules and patterns.
WebServer: Receives the filtered traffic from the firewall.
Action: The firewall allows legitimate traffic to pass through to the web server while blocking malicious traffic.

WebServer Reports High Traffic Alert:
WebServer: Monitors the traffic load and detects unusual spikes in traffic volume.
Firewall: Receives alerts from the web server about high traffic volumes.
Action: The web server reports high traffic alerts to the firewall, indicating a potential DDoS attack.

Firewall Blocks Malicious Traffic:
Firewall: Takes action to block the malicious traffic identified as part of the DDoS attack.
BotNet: Continues to send traffic, but much of it is now blocked by the firewall.
Action: The firewall blocks the malicious traffic from the botnet, preventing it from reaching the web server.

BotNet Reports Attack Status to Attacker:
BotNet: Monitors the status of the attack and reports back to the attacker.
Attacker: Receives updates on the effectiveness of the attack.
Action: The botnet reports the status of the attack to the attacker, including any defensive measures encountered.
