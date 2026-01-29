# Burp Suite

## What It Is

Burp Suite is a web application testing tool used to inspect and modify HTTP/HTTPS traffic between a browser and a web server.

It acts as an intercepting proxy to help analyze web requests and responses.

---

## What I Use It For

- Inspecting web traffic  
- Understanding how web apps communicate  
- Analyzing requests and responses  
- Practicing web security testing in labs  
- Learning how web attacks appear in traffic  

Burp Suite is one of the most valuable tools for web application visibility in a SOC and security testing environment.

---

## Basic Setup

1. Install Burp Suite  
2. Launch Burp and enable proxy listener  
3. Configure browser proxy settings  
4. Install Burp CA certificate (for HTTPS)  
5. Start intercepting traffic

---

## Core Concepts

Burp works around **intercepting and analyzing web traffic**.

Key concepts:

- Proxy interception  
- Requests and responses  
- Repeater for manual testing  
- Intruder for automated testing  

Understanding request structure is critical.

---

## Common Workflow

### Basic Investigation Flow

1. Enable proxy interception  
2. Browse target web app (lab only)  
3. Inspect captured requests  
4. Send interesting requests to Repeater  
5. Analyze server responses

---

## Troubleshooting

No traffic captured:
- Verify browser proxy settings  
- Confirm Burp listener is running  

HTTPS issues:
- Install Burp CA certificate  
- Trust certificate in browser

---

# Commands

---

## Proxy Control

Toggle intercept on/off:

Proxy → Intercept → Toggle

---

## Repeater

Send request to Repeater:

Right-click request → Send to Repeater

---

## Intruder

Send request to Intruder:

Right-click request → Send to Intruder

Start attack:

Intruder → Start Attack

---

## Logging

View HTTP history:

Proxy → HTTP History

---

## Lessons Learned

- Small request changes can matter  
- Headers often reveal useful details  
- Web apps expose a lot through traffic  
- Understanding web traffic helps detection work
