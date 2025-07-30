# CC Duplication error 

## Errors: "Authorization was interrupted, check for duplicate transaction." 

### Understanding the Issue

The ticket is sitting in the _Manual Authorized Transaction_ menu. This means that the system is unsure if the card was actually charged or not so the system keeps it open until that is determined. 

### Troubleshoot 

  <img width="1163" height="549" alt="image" src="https://github.com/user-attachments/assets/6be210fc-6c45-4e4f-a70a-0f206b939ca9" />

1. Go to POS > POST POS DOCUMENTS > TRANSMIT EDC CREDIT CARD TRANSACTION
2. Select the card type that was used on this ticket
3. On the following screen, click on the button for Manually Auth Trans (upper left corner)
4. On the next screen, you should see the associated invoice sitting in the table
5. **If the card was CHARGED:** Click on the invoice to highlight it > Click on ALLOW BYPASS > This will let you go back into POS Invoicing and close the ticket without charging the card again.
6. **If the card was NOT charged:** Click the RESET button and this will allow you to go to POS Invoicing and close the ticket and charge the card correctly. 
