# PILOT Class

# **“How the Internet, Computers & Email Work: A Hands-On Intro”**

---

## 1. CLASS OVERVIEW

**Title**: *“How the Internet, Computers & Email Work: A Hands-On Intro”*

**Audience**: Young adults, ages 14+, with an interest in tech; minimal prior knowledge required.

**Duration**: 2–3 hours

**Goal**:

- Provide a foundational understanding of how devices connect to the internet, how DNS and DHCP work, and how basic computer hardware (CPU/RAM) operate.
- Explain the journey of an email—from sending via Gmail to its delivery through DNS, MX records, and authentication protocols.

---

## 2. SESSION AGENDA (we should discuss)

| Time (mins) | Activity |
| --- | --- |
| **0–10** | 1. **Welcome & Icebreaker** |
| **10–25** | 2. **Intro to the Internet & Computers** (Slides + Discussion) |
| **25–40** | 3. **DNS & DHCP Basics** (Slides + Hands-On Demo) |
| **40–50** | 4. **Break** |
| **50–65** | 5. **How Email Works** (Slides, Diagram of Email Journey, Demo using nslookup) |
| **65–80** | 6. **CPU & RAM Basics** (Slides + Demo using Task Manager/Terminal) |
| **80–95** | 7. **Mini Troubleshooting Activity** (Network & Email troubleshooting) |
| **95–110** | 8. **Q&A, Feedback, and Wrap-Up** |

*Note: You can adjust each segment to suit the pace of the class.*

---

## 3. DETAILED LESSON FLOW & TEACHER NOTES

### 1. Welcome & Icebreaker (0–10 minutes)

**Purpose**: Create a relaxed atmosphere, gauge prior knowledge, and spark curiosity.

- **Introduction**:
    - Welcome students, share your background briefly, and outline the day’s objectives.
    - **Slide 1**: Title slide with the class name and goals.
- **Icebreaker**:
    - Ask: “What’s one thing about the internet, computers, or even email that you’ve always wondered about?”
    - Encourage brief open sharing to gauge interest and experience.

---

### 2. Intro to the Internet & Computers (10–25 minutes)

**Purpose**: Provide a high-level overview of how computers connect to the internet and how they process data.

- **Slides to Create**:
    - **Slide 2**: “What is the Internet?” – A simple definition: a network of networks.
    - **Slide 3**: Basic Internet Diagram – *Client → ISP Router → Internet → Server*.
    - **Slide 4**: Brief Introduction to Computer Hardware – Focus on the CPU (the “brain”) and RAM (short-term memory).
- **Key Talking Points**:
    - “When you type a website into your browser, your device sends a request to a server which returns data to be displayed.”
    - Introduce the idea that everything happens in data “packets” traveling through networks.
    - Highlight that behind every email and webpage, there’s a combination of hardware processing and network communication.
- **Demo/Discussion**:
    - Run a quick command (e.g., `ping google.com`) to show connectivity and round-trip time

---

### 3. DNS & DHCP Basics (25–40 minutes)

**Purpose**: Explain how devices obtain IP addresses and how domain names are resolved.

- **Slides to Create**:
    - **Slide 5**: “DNS in a Nutshell” – Use a phonebook analogy to show how domain names (like [www.example.com](http://www.example.com/)) map to IP addresses.
    - **Slide 6**: “DHCP in a Nutshell” – Explain the Discover → Offer → Request → Acknowledge cycle using a hotel front desk analogy.
- **Hands-On Demo**:
    - Open Command Prompt/Terminal:
        - Use `ipconfig /all` (Windows) or `ifconfig`/`ip addr show` (Linux/Mac) to show DHCP lease info.
        - Run `nslookup google.com` to demonstrate how a domain resolves to an IP address.
    - Discuss what happens when DHCP fails (e.g., receiving a “169.x.x.x” address).
- **Teacher Note**:
    - Emphasize that DHCP is what gives every device its unique “address” on the network, and DNS is like looking up a contact in a phone directory.

---

### 4. Break (40–50 minutes)

Allow students a 10-minute break to stretch, refresh, and process the material so far.

---

### 5. How Email Works (50–65 minutes)

**Purpose**:

Explore the complete journey of an email—from clicking “send” to its arrival in the recipient’s inbox—by explaining the roles of SMTP, DNS, and MX records, and by introducing basic email authentication concepts.

- **Slides to Create**:
    - **Slide 7**: *“What Happens When You Send an Email?”*
    Outline the sequential steps of the email process:
        - **Sender**: Your email client (e.g., Gmail, Outlook) initiates the sending process.
        - **SMTP Server**: The email client connects to an SMTP server responsible for relaying the email.
        - **DNS Lookup**: The SMTP server performs a DNS lookup to retrieve the MX (Mail Exchange) records.
        - **MX Record**: MX records indicate which server handles email for the recipient’s domain.
        - **Recipient Mail Server**: The email is delivered to the recipient’s mail server, where it awaits retrieval.
    - **Slide 8**: *Email Journey Diagram*
    Provide a visual flowchart that clearly depicts:
        - Sender → SMTP Server → DNS Lookup → MX Record → Recipient Mail Server
- **Key Talking Points**:
    - **SMTP Fundamentals**:
        - **Definition**: Explain that SMTP stands for Simple Mail Transfer Protocol, which governs how emails are sent.
        - **Roles**: Clarify the roles:
            - **SMTP Client**: The component within your email app that sends the email.
            - **SMTP Server**: The server that accepts outgoing emails and processes them.
    - **Email Transmission Process**:
        - “When you hit send, your email client contacts its SMTP server.”
        - “The SMTP server then uses DNS to locate the recipient’s MX record.”
        - “Based on the MX record, the server routes your email to the correct recipient mail server.”
    - **Introduction to Email Authentication**:
        - Briefly introduce **SPF (Sender Policy Framework)** and **DKIM (DomainKeys Identified Mail)**.
        - Explain that these protocols help verify the authenticity of the email, reducing spoofing and phishing.
        - Note that while these methods are not explored in-depth today, they are essential components of email security and will be covered in future sessions.
- **Hands-On Demo**:
    - **MX Record Lookup**:
        - Open a terminal or command prompt.
        - Run the command:
            
            ```bash
            nslookup -type=MX gmail.com
            ```
            
        - Walk through the output to illustrate how the MX records are listed and explain their significance.
    - **Optional Email Authentication Preview**:
        - Optionally demonstrate checking an SPF record by running:
            
            ```bash
            dig TXT example.com
            ```
            
        - Briefly discuss how these TXT records (which include SPF information) help validate email sources.

---

### 6. CPU & RAM Basics (65–80 minutes)

**Purpose**: Explain the basics of computer hardware and how processing and memory impact performance.

- **Slides to Create**:
    - **Slide 9**: “CPU Basics” – Introduce the fetch-decode-execute cycle in simple terms, mention clock speed and cores.
    - **Slide 10**: “RAM Basics” – Explain volatile memory versus storage and why sufficient RAM is important for performance.
- **Demonstration**:
    - Open Task Manager (Windows) or use `top`/`htop` (Linux/Mac) to show real-time CPU and RAM usage.
    - Open several applications or browser tabs and observe how resource usage changes.
- **Talking Points**:
    - “When your CPU is overloaded, your computer slows down because it can’t process instructions quickly enough.”
    - “RAM holds active processes—if you run out, your system may start swapping data to disk, which slows everything down.”

---

### 7. Mini Troubleshooting Activity (80–95 minutes)

**Purpose**: Reinforce concepts by walking through troubleshooting both network and email issues.

- **Scenario**:
    - “Your computer isn’t connecting to the internet and your emails aren’t sending. What steps would you take?”
- **Steps to Practice**:
    - **For Network Issues**:
        - Check IP address using `ipconfig /all` or `ifconfig`.
        - If you see a “169.x.x.x” address, suspect a DHCP problem; try releasing/renewing the IP (e.g., `ipconfig /release` & `ipconfig /renew`).
        - Use `nslookup google.com` to ensure DNS is resolving correctly.
    - **For Email Issues**:
        - Verify the email server’s MX record (e.g., using `nslookup -type=MX domain.com`).
        - Discuss potential causes like misconfigured SPF records or DNS issues.
- **Debrief**:
    - Summarize how each troubleshooting step ties back to DHCP, DNS, CPU/RAM, and email processing.
- **Teacher Note**:
    - Encourage teamwork if multiple devices are available. If only one machine is present, perform the steps as a group exercise.

---

### 8. Q&A, Feedback, and Wrap-Up (95–110 minutes)

**Purpose**: Address student questions, gather feedback, and highlight next steps for further learning.

- **Q&A**:
    - Invite questions covering all topics: internet basics, hardware, and email operations.
- **Feedback**:
    - Conduct a round-robin asking, “What’s one thing you learned today?” or “What would you like to explore further?”
- **Next Steps**:
    - Mention potential follow-up sessions on advanced topics (like deeper email security or networking protocols).
    - Provide links or resources (such as Khan Academy or Cisco Networking Academy) for further exploration.
- **Closing Slide**:
    - **Slide 11**: “Thanks for Participating!” with contact info, additional resources, and encouragement to experiment with commands and tools at home.

---

## 4. SLIDES SUMMARY

1. **Slide 1**: Class Title & Objectives
2. **Slide 2**: “What is the Internet?” – Overview
3. **Slide 3**: Internet Diagram (*Client → Router → Internet → Server*)
4. **Slide 4**: Intro to Computer Hardware (CPU & RAM basics)
5. **Slide 5**: DNS Overview (Phonebook analogy)
6. **Slide 6**: DHCP Overview (4-step handshake)
7. **Slide 7**: “What Happens When You Send an Email?”
8. **Slide 8**: Email Journey Diagram (SMTP, DNS lookup, MX records)
9. **Slide 9**: CPU Basics (Fetch-decode-execute)
10. **Slide 10**: RAM Basics (Volatile memory vs. storage)
11. **Slide 11**: Thank You / Next Steps / Resources

---

## 5. TEACHER’S “CHECKLIST” FOR THE CLASS

### Equipment & Software

- At least one computer with internet access.
- A projector or TV for displaying slides.
- Command Prompt/Terminal ready for demos (e.g., `ping`, `nslookup`, `ipconfig`/`ifconfig`).
- Optionally, a physical PC to show internal hardware (CPU/RAM).

### Materials

- Printouts or digital cheat sheets for IP addresses, DNS flow diagrams, and troubleshooting steps.
- Pre-loaded slides on a laptop or USB.
- A backup plan for demos if the real-world environment acts up.

### Preparation

- Test all demos (ping, nslookup, ipconfig/ifconfig, Task Manager) beforehand.
- Ensure all slides are organized and ready for display.
- Review basic troubleshooting steps so you can guide students if issues arise.

### During Class

- Maintain a friendly and engaging tone.
- Encourage participation by asking prompting questions.
- Keep track of time to ensure all segments are covered.

### Follow-Up

- Collect feedback through a quick round-robin or written notes.
- Note which topics resonated or needed further explanation.
- Adjust future sessions based on student input.

---

## 6. OPTIONAL IDEAS & EXTENSIONS

- **Packet Tracer Demo**:
    
    If available, use Cisco Packet Tracer to visually demonstrate how DHCP and DNS work within a network.
    
- **Interactive Quiz**:
    
    Use tools like Kahoot to create a mini quiz with questions such as “What does DHCP stand for?” or “Which command checks DNS resolution?”
    
- **Hands-On Hardware Session**:
    
    If feasible, open a PC case to show students the physical CPU, RAM, and motherboard connections. Ensure proper safety and guidance during this demo.