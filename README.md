#Prompt Injection Firewall

A layered security firewall designed to protect AI agents from prompt-injection attacks, unauthorized tool usage, and sensitive-data exfiltration. The project treats the AI model as an untrusted component and applies security controls around its inputs, actions, and outputs.



##Why Do We Need This?

AI agents can be manipulated through malicious prompts or untrusted content.
A successful prompt injection can cause an agent to ignore its intended instructions.
It may also lead to unauthorized tool usage or sensitive-data leakage.
This firewall adds multiple security layers to reduce these risks.



##Five Layers
1.### Normalization

Normalizes and analyzes different representations of input, including Unicode and encoded content.

2. ###Ingress Inspection

Detects and evaluates potentially malicious prompt-injection instructions entering the system.

3. ###Trust Tracking

Maintains the distinction between trusted instructions and untrusted data throughout the request.

4. ###Tool Authorization

Controls and validates AI-requested tool actions before they are executed.

5. ###Secure Egress

Prevents sensitive information and unsafe data from leaving the protected system.



##Technologies Used
Python
FastAPI
Pydantic
Docker
Docker Compose
Pytest



##Quick Start
1. Clone the repository
```bash 
git clone https://github.com/akki-p010/prompt-injection-firewall.git
cd prompt-injection-firewall
```

2. Create the environment file

Windows PowerShell:
```powershell
Copy-Item .env.example .env
```

Linux/macOS:
```bash
cp .env.example .env
```

3. Start the project

Make sure Docker Desktop is running, then:
```bash
just arena
```

4. Open the application
```text
http://127.0.0.1:33572
```

5. Run tests
```bash
just check
```