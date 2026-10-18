# Mission Reflection

A host-based firewall protects a server by providing an additional layer of security directly on the machine. Even if an attacker is able to get past the physical or external network perimeter, the firewall can still block unauthorized incoming connections. In this mission, UFW was configured with a Default Deny policy, allowing only the services that were required, such as SSH and port 8080. This means that unauthorized traffic is blocked unless a specific rule allows it.

Managing open ports reduces the attack surface because every open port can potentially become an entry point for an attacker. Unnecessary ports and services may create security risks, so limiting access to only the ports that are needed makes the server more secure. The use of UFW helped demonstrate how controlling network access can reduce possible attack opportunities and support a more secure server configuration.

Exposing a database port such as 3306 publicly is dangerous because attackers from the internet may directly attempt to connect to the database server. They could try stolen credentials, weak passwords, or vulnerabilities in the database service. Keeping database ports private and allowing access only from trusted systems is a safer practice because it reduces unnecessary exposure and limits possible unauthorized access.

This mission changed my perspective because I realized that a server can become vulnerable through simple configuration choices, especially when unnecessary ports or services are exposed. I learned that cloud security is not only about passwords and applications but also about controlling network access. Applying a Default Deny policy showed me how basic firewall configuration can make a server more difficult to compromise.

With eight completed missions, my GitHub portfolio now shows a wider range of cloud computing skills and practical experience. Each completed mission provides evidence of the skills I have practiced and learned. Adding the Cloud Security Engineer mission makes my portfolio stronger because it demonstrates that I also understand basic server security, firewall configuration, and reducing the attack surface. Overall, this mission helped me understand that security should be considered from the beginning when managing cloud servers.

