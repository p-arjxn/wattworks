# Secure Boot with Microwatt

## Project Description

The objective of this project is to demonstrate a simple secure boot mechanism using the open-source Microwatt CPU core and an open-source SHA-256 hashing engine.  

The design works as follows:
1. When Microwatt starts, it runs a small firmware program.  
2. The firmware sends a boot payload to the SHA-256 core through the Wishbone bus.  
3. The SHA-256 core calculates the hash of the payload.  
4. Microwatt compares the calculated hash with an expected value stored in firmware.  
5. If both values match, the system reports **BOOT OK**. If they do not match, it reports **BOOT FAIL**.  

This setup shows how a processor can check the integrity of its code before execution. It is a minimal and practical example of secure boot, built entirely with open-source hardware blocks.


## Proposal

This project will be implemented by:
- Integrating Microwatt and the SHA-256 core inside the OpenFrame harness.  
- Writing firmware to perform the secure boot check.  
- Running simulations to show the results for both valid and invalid payloads.  

The expected outcome is a reproducible example of secure boot that is simple, clear, and easy for others to extend. It highlights the importance of trusted execution while remaining fully open-source and beginner-friendly.
