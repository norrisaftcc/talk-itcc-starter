# Printer Fix: Clear a Stuck Print Queue (Windows)

Purpose: steps to clear a print job that will not print or delete on a Windows PC.

Tested on: [Windows version], [date]

1. Ask the user which printer and which document. Write it in the ticket.
2. Open **Settings > Bluetooth & devices > Printers & scanners**. Select the printer. Select **Open print queue**.
3. Right-click the stuck job. Select **Cancel**. Wait 30 seconds.
4. If the job stays, open **Command Prompt** as administrator.
5. Stop the print service: `net stop spooler`
6. Delete the stuck job files: `del /Q /F %systemroot%\System32\spool\PRINTERS\*`
7. Start the print service again: `net start spooler`
8. Print a test page. Confirm with the user that it printed.
9. If the problem comes back, check the printer driver and escalate.

Note: Step 6 deletes **all** waiting jobs on this PC, not only the stuck one. Tell the user first.
