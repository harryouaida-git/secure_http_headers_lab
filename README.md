# Secure HTTP Headers Lab

## Overview
This lab guides you through understanding, testing, and implementing secure HTTP headers to improve web application security using OWASP resources.

---

## Part 1: Understanding Security Headers (Theory + Exploration)

### Step 1: Research and List Security Headers

1. Visit the OWASP Secure Headers Project page:  
   https://owasp.org/www-project-secure-headers/  
2. Write down these headers and in one sentence explain their purpose:

- Content-Security-Policy (CSP): Controls allowed content sources to prevent XSS attacks.
- Strict-Transport-Security (HSTS): Enforces HTTPS to secure communication.
- X-Content-Type-Options: Prevents MIME sniffing attacks.
- X-Frame-Options: Prevents clickjacking by disallowing iframe embeds.
- Referrer-Policy: Controls referrer information sent to other sites.
- Permissions-Policy: Restricts use of powerful browser features.

---

### Step 2: Identify Headers on Popular Websites

1. Open Developer Tools in your browser (`F12` or `Ctrl+Shift+I` / `Cmd+Option+I`).  
2. Go to the Network tab.  
3. Visit https://www.google.com and https://www.mozilla.org.  
4. Select the main document request and check Response Headers.  
5. Note which security headers are present or missing.

---

## Part 2: Analyzing Headers Using OWASP Tools (Hands-on)

### Step 3: Use Mozilla Observatory

1. Go to https://observatory.mozilla.org/  
2. Enter a website URL from Step 2.  
3. Click Scan and review the report.  
4. Identify missing or misconfigured headers.  
5. Take screenshots.

### Step 4: (Optional) Use Browser Extensions

1. Install a Security Headers extension (Chrome/Firefox).  
2. Visit websites and inspect their security headers quickly.

---

## Part 3: Implementing Security Headers Locally

### Apache Setup

1. Ensure Apache is installed.  
2. Create or edit the .htaccess file in your web root.  
3. Add the provided security headers (see .htaccess file).  
4. Restart Apache: `sudo systemctl restart apache2`

### Node.js (Express) Setup

1. Create or open a Node.js project.  
2. Install helmet: `npm install helmet`  
3. Add helmet middleware to your app.js (see app.js sample).  
4. Run the server: `node app.js`

---

## Part 4: Verifying Your Implementation

### Step 6: Check Headers in Browser

1. Open your local site (http://localhost or http://localhost:3000).  
2. Open Developer Tools → Network tab.  
3. Select the main document request.  
4. Confirm security headers are present.

### Step 7: Analyze Using Tools

- Use Mozilla Observatory if public.  
- Or use curl: `curl -I http://localhost:3000`  

---

## Part 5: Reflection and Improvement

Answer these questions:

- Which headers were easiest and hardest to implement?  
- Did any headers cause issues or conflicts?  
- How do these headers improve security?  
- What would you try next?

Try modifying CSP or Permissions-Policy and observe changes.

---

## Deliverables

- List of headers and purposes  
- Screenshots from Parts 2 & 4  
- Reflection answers  
- Optional experiments notes

---

Good luck and have fun securing your web apps!
