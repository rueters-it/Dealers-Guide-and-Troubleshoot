# Keystone Printers Troubleshoot

## Understanding the Issue 

There are a number of reason why the printer may not be printing. See below for troubleshooting information and guide. If none of these work, or if you want to ensure the fix is done correctly, email <support@discrp.com> for assistance.

## Common Causes
1. Printer may just neeed a reboot in Keystone.
2. Printer writer issue and needs reset.

## Troubleshoot 
1. Reset printer in Keystone.
2. Reset printer's writer in an AS/400 Command Line in the Keystone/Quantum system.
3. "Load Forms" message in system operator message.
4. Contact DIS Support

### Reset Printer in Keystone 

1. Sign in to Keystone
2. In the top menu bar, click **System** > **System Operator Only** > **Start/End Printers**
   
   ![image](https://github.com/user-attachments/assets/96356bb0-d246-499a-a719-767ca428f847)

3. Select the pritner that is having issues > hit "End" then "Start" to reset that printer. 
   
   ![image](https://github.com/user-attachments/assets/c8ee1691-cf23-4322-898a-b2a4e34e1a9c)

### Reset printer's writer (Turn off/on)

#### To turn a writer off: 
1. Use `ENDWTR` + `Printer #` command in an AS/400 Command Line in Keystone/Quantum
2. Printer specific command: `ENDWTR P#`
3. If you're ending the writer for Printer P1, command is: `ENDWTR P1`

#### To turn the writer back up: 
1. If the printer is a LAN printer: use `STRPRTWTR P#`
2. If the printer is a LPR printer: use `STRRMTWTR P#`
3. Sometimes, the writer is already off, so you'd just need to run one of the above commands to start it to fix the issue. 

#### Check if writer is On or Off
1. You can check to see if the writer is on or off, enter the command `WRKOUTQ` to se the list of printers
2. You can specify further by typing in `WRKOUTQ P*` (wildcard) to see all pritners that start with "P" in the ID (or whatever letter you specifiy)
3. Writers are **OFF** if the "Writer" field is blank.
4. Writers are **ON** if you see the printer ID in the Writer field.  

### Load Forms message in System Operator Message  

Printers may not print if they have a Load Forms message appearing in System Operator Message. Those messages are the system making sure the right paper is in the printer before it lets the printer job go through. Sometimes, printe jobs don't print because the operator doesn't know to look out for those messages. This issue, however, is more complicated since there are several load form messages. In most cases, if the right paper is already in the printer and the user wants the print job to come out now, then the right response to those messages is a "G". 

#### To see Load Forms message: 
1. Log in to Keystone.
2. Navigate to **System** > **System Operator Only** > **Display Operator Messages**

   ![image](https://github.com/user-attachments/assets/a44cffff-17a4-4d43-80aa-87e651d11131)

4. Rendered output is the Display Messages window:
   
   ![image](https://github.com/user-attachments/assets/22145006-be6e-4176-86e3-d03eca28a569)

### Contact DIS Support 
1. Email <support@discrp.com> for assistance.
2. Try the new DIS Support Portal for help request
3. Email <DISLearn@discorp.com> (possible new support system/email)

## Resources 
1. [DIS Support Portal](https://perseus.my.site.com/DISSupportPortal/s/login/)
