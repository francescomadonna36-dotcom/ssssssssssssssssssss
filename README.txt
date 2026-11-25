CHEEKOS  -  ROB RUN overlay
===========================

BEFORE THE FIRST START
  Install the Microsoft Edge WebView2 Runtime (Evergreen, x64) if this PC does
  not have it. Without it the menu window stays blank:
  https://developer.microsoft.com/microsoft-edge/webview2/

HOW TO START
  1. Make sure ROB RUN is closed.
  2. Double-click START.bat and accept the UAC prompt (the overlay runs as admin).
  3. Start ROB RUN. The overlay waits for the game and attaches on its own.
  4. Press F1 for the CHEEKOS menu.

  If START.bat says the driver is not mapped, run MAP-DRIVER.bat once per
  Windows session (also elevated), then START.bat again. Memory Integrity /
  Core Isolation must be off or the mapper cannot load the driver.

KEYS
  F1      open / close the CHEEKOS menu
  Insert  show / hide the overlay
  End     quit the overlay

FILES
  START.bat        normal launcher - uses RobRunPort.exe from this folder
  RobRunAIO.exe    single-file launcher: unpacks the payload and supervises it
  START-MASQ.bat   runs the overlay renamed as dllhost.exe from %TEMP%
  MAP-DRIVER.bat   maps driver.sys through kd2.exe (once per boot)
  RobRunAIO.ini    launcher timing and masquerade options
  CoreRR.cfg       settings saved by the menu (delete to reset to defaults)
  menu.html        settings page - keep it next to the exe
  OFFSETS.bat      diagnostic: dumps live class/field offsets

NOTES
  Run from a folder the account can write to - the overlay writes its logs,
  CoreRR.cfg and its runtime cache beside itself.
  The overlay is hidden from Task Manager by default and exits when ROB RUN
  exits. Delete *.log any time; they are diagnostics only.
