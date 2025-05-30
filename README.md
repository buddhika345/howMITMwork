
 🔐 Encrypted SMS Chat Simulation – MITM Attack Demonstration

This project demonstrates a simple **Python-based client-server SMS messaging system** with:

- ✅ Real-time communication over TCP
- ✅ Simulated **MITM attack** using Wireshark or proxy tools
- ✅ **Fernet encryption (AES-128)** to secure messages
- ✅ A decryption tool to inspect captured traffic
- ✅ Educational purpose to understand **how encryption protects against MITM**


🧠 Project Goal

The primary goal is to **demonstrate how attackers can intercept plaintext messages** and **how encryption secures communication**, preventing unauthorized reading—even when traffic is captured.

 🛠️ Technologies Used

- Python 3.x
- `socket` (for TCP chat)
- `cryptography` (for AES encryption using Fernet)
- Wireshark (for packet capture)
- MITM tools (optional): e.g., `mitmproxy`
  
 📁 Project Structure

├── encryption.py # Encryption & decryption logic
├── server.py # Server script
├── client.py # Client script
├── decryptor.py # Tool to decrypt captured messages

Steps you want to follow :
 1.pip install cryptography
 2.python server.py
 3.python client.py
 4.open wireshark
 5.Start capturing on lo (loopback) or your active interface.
 6.set filter(tcp.port == 12345)
 7.Send a message in the chat using client1 and client2
 8.wireshark > Right-click the message packet → Data → Show packet bytes > copy
 9.python decryptor.py
10.paste and > enter

🔒 How Secure is It?
*Messages are encrypted using AES-128 in CBC mode (via Fernet)
*Only parties with the correct key can decrypt messages
*MITM attackers cannot read messages even if captured

🎓 Learning Outcomes
*How TCP communication works
*How MITM attacks can be simulated
*How encryption protects against packet sniffing
*Real-world example of secure communication

⭐ Credits
Developed by Pradeep Buddika Wijerathna
Guided by cybersecurity and networking best practices.



