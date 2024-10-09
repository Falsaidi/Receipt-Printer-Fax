# Receipt-Printer-Fax
Website which sends a text message through a Raspberry Pi to a connected receipt printer.

# Usage
All associated program files control a website which prompts the user to input a message, which is then received by the Raspberry Pi hosting the website and sent via Serial USB to a receipt printer which formats and prints the message. Ideally, the receipt printer should be a laser printer and support POS1 coreless paper and a direct USB connection.

`receipt.js` sets a character limit for the form defined in `index.html`, enforcing the character limit before sending the message.

The form in `index.html` sends a POST request to `receive-text.php` when successfully submitted, which displays a success screen and sends the message to the receipt printer. The default directory for the printer is the Linux directory `/dev/usb/lp0`.
