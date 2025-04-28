# T-Pot-HoneyPot-Setup
![Image](https://github.com/user-attachments/assets/5c7c76c6-8f95-402e-b2e8-15cd5707e7b0) <br> <br>
Deployed and configured T-Pot Honeypot, a multi-honeypot platform on Ubuntu Server to monitor and analyze malicious network activities using Elastic Stack dashboards. This repository will help you to setup T-Pot on Ubuntu Server 24.04 Live server less than 10 minutes. <br><br>

## REQUIREMENTS:

- [Ubuntu Server 24.04 ISO](https://ubuntu.com/download/server)
- Atleast 8-16 GB RAM, 128 GB free disk space to install T-Pot
- Vitual-box [You can deploy it to a VPS instead to see more interactions from the attackers]
<br>

## Installation Process:
- You need to install docker and docker compose, you can refer this [document](https://wiki.kitpro.us/en/articles/docker-script) and run this [script](https://wiki.kitpro.us/install-docker.sh) from [KeepItTechie](https://www.youtube.com/@KeepItTechie) to automate the installation as manually installing docker has multiple steps.
- Clone the repository: <br>
``` git clone https://github.com/telekom-security/tpotce.git ```

- Move into the folder tpotce
``` cd tpotce ```

- Run the installation script. This will pull all the necessary docker images of all the available honeypots.
``` ./install.sh ```

- Select your desired T-Pot Type: <br>

```
1. Hive   - Standard/ HIVE Installation - This includes everything you need for a distributed setup with sensors.
2. Sensor - T-Pot Sensor installation - Optimized for a distributed installation, without WebUI, Elasticsearch and Kibana.
3. LLM    - T-Pot LLM installation - Uses LLM based honeypots Beelzebub & Galah, Requires Ollama or ChatGPT subscription
4. Mini   - T-Pot Mini installation - Run 30+ honeypots with just a couple of honeypot daemons.
5. Mobile - T-pot Mobile installation - Includes everything to run T-pot Mobile
6. Tarpit - T-pot Tarpit installation - Feed data endlessly to attackers, bots and scanners. Also runs a Denial of Service Honeypot (ddospot).
```
- I've selected Hive installation and for the user configuration enter the username and password to access the WebGui

- NOTE: After the installation, the SSH port will be changed from 22 to 64295. You can reconnect by explicitly mentioning this port

- Reboot the system.

<br>

## Accessing the WEBGUI:

- Open your webbrowser and go to your server IP with port 64295. <br>
``` https://[server-ip]:64295 ```

- Type in your username and password

- You will have access to powerful tools like Kibana, Cyberchef, and the Attack Map.

<br>

## Demo:

I ran a nmap scan on the server in order to check the honeypot. As you can see, from the location, to the source ip of the attack is captured and showcased via dashboard.
<br><br>
![Image](https://github.com/user-attachments/assets/61608747-0aee-416c-9d5c-4aa6e5395850)
<br><br>

![Image](https://github.com/user-attachments/assets/eb5b631e-041b-4d40-856b-3d9bd334ffd0)

