#Add a an AirPrint Printer via CLI

Replace "printerHostName" with the hostname of the printer you'd like to add. I use this with the Execute Command option in the Files and Processes pane in Jamf to create Self Service printer policies for my Mac relevant printers.

Running the command does require the user to confirm adding the printer:

![Confirm printer](<./ConfirmPrinter.png>)

This has not been tested with users that are not part of the printer admin group as part of my provisioning workflow is to run `sudo /usr/sbin/dseditgroup -o edit -n /Local/Default -a everyone -t group lpadmin` on all my devices to allow all users to manage printers.