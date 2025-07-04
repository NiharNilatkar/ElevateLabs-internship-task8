# Task 8: Working with VPNs

## Objective
Understand the role of VPNs in protecting privacy and secure communication.

---

## Tools Used
- Wireshark
- Opera GX browser
- Proton VPN
- https://whatismyipaddress.com
- https://www.speedtest.net

---

## Step-by-Step Breakdown

### Step 1: Install a VPN
Installed Proton VPN, and made my account

### Step 2: Connect to the VPN
Connected to Netherlands server.

### Step 3: Open Wireshark
Launched Wireshark and started capturing packets on the active network interface(Wi-Fi).

### Step 4: Analyze VPN Traffic
Checked `https://whatismyipaddress.com` to verify that my IP address was changed.

### Step 5: Browse a Website
- Browsed `https://wikipedia.org/`
- Used Wireshark to confirm there was no plaintext `http` traffic visible
- Verified all traffic was encrypted while VPN was active
- Verified the lock icon in browser,confirming that connection was private and secure.

### Step 6: Disconnect VPN and Compare
- Compared IP address before and after VPN
  - With VPN: IP changed to VPN server location(Netherlands)
  - Without VPN: IP reverted to original ISP address
- Compared internet speed using `speedtest.net`
  - VPN reduced speed slightly due to encryption overhead
  - Latency (ping) was higher while on VPN.

---

### Step 7: Research VPN encryption and privacy features

I learned about how VPNs provide secure and private connections via encryption and tunneling protocols. Here is what I found out:

#### VPN Encryption
Encryption in VPNs
- VPNs employ robust encryption (e.g., **AES-256**) for safeguarding data in transit.
- This ensures data cannot be intercepted or eavesdropped.
- This guarantees that even when traffic is intercepted, it cannot be read unless with the key.

| Criteria         | With VPN           | Without VPN        |
|------------------|--------------------|--------------------|
| IP Address       | Masked (VPN exit)  | Real ISP IP        |
| Wireshark Data   | Encrypted HTTP     | May show HTTP pcket|
| Speed Test       | Slower             | Faster             |
| DNS Requests     | Secured            | ISP-resolved       |

#### Privacy Features Provided by VPNs
- **IP masking**: conceals your original IP address and displays the VPN server IP
- **No-logs policy**: reliable VPNs don't save your web history
- **Kill switch**: prevents internet if VPN unexpectedly disconnects
- **DNS leak protection**: makes sure DNS requests pass through the VPN tunnel

---

## Conclusion

Using Wireshark and browser inspection, I confirmed that:
- VPN effectively masked my IP address
- All traffic was encrypted (no HTTP/plaintext visible)
- There was a noticeable performance drop, which is a fair trade for enhanced privacy

---

## Deliverables
- This README.md file
- Screenshots from speed test, and Broswer
- Wireshark captures
