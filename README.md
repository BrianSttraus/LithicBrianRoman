# LithicBrianRoman
Technical Support Lead Application Puzzle

* **How I found the hidden challenge:** Suspecting a hidden element, I used the browser's Developer Tools to inspect the page source. I noticed a couple of red flags, including a broken problem-solving link and a link leading to a non-existent job posting. Upon closer inspection, I discovered a long, unusual string embedded within the URL. I used Perplexity AI to help identify it as a Base64 encoded string.
* **How I decoded the original string:** I copied the isolated Base64 string from the URL and used an online Base64 decoder to extract the raw text, which revealed the hidden Python script.
* **What this script does:** The script checks for a specific environment variable (`DONT_PANIC=1`), decrypts a hardcoded string using a XOR, and then generates a unique 12-character verification linking my name to the decrypted answer.
* **The command I ran:** Because the provided example command was specific to Linux/macOS, running it directly in Windows Command Prompt failed. I resolved this by manually setting the environment variable in `cmd` before running the file:
  ```cmd
  set DONT_PANIC=1
  python puzzle.py --candidate "Brian Román Cepeda"
  ```
* **The exact output I received:**
  ```text
  Decrypted password: 42
  Candidate: Brian Román Cepeda
  Proof code: 95cd45c26b89
  ```
* **The final decrypted answer:** The answer to Life, the Universe, and Everything = 42
* **Tools used:** Browser Developer Tools, Perplexity AI, Base64 Decoder, Windows Command Prompt (CMD).
  
