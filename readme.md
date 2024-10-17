# MAC Flooding (macof attack) and Port Security Prevention

## Steps to Reproduce

1. **Set up the network topology on EVE-NG** with:
   - Kali VM
   - Cisco Switch
   - Optional: Additional end devices

2. **Verify initial setup**:
   - run the following on in switch terminal:
        show mac address-table
        show port-security

3. **Execute macof attack on Kali**:
    -run in terminal
        macof -n <number of frames>

4. **After the attack**:
    - run the following commands in the Switch's terminal to verify
        show mac address-table
        show port-security

5. **Configure port security on switch**
        interface [range] [interface-id]
        switchport mode access
        switchport port-security
        switchport port-security maximum 1
        switchport port-security violation shutdown
        end
        write memory

6.  **Re-run macoff attack**

7.  **execute same instructions in step 4 to verify**

8.  **

