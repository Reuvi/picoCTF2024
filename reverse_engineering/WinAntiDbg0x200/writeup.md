<h2>WinAntiDbg0x200</h2>
<ul>
  <li><strong>Author:</strong> IssacSasson</li>
  <li><strong>Category:</strong> Reverse Engineering</li>
  <li><strong>Points:</strong> 300</li>
  <li><strong>Description:</strong> If you have solved WinAntiDbg0x100, you'll discover something new in this one. Debug the executable and find the flag! This challenge executable is a Windows console application, and you can start by running it using Command Prompt on Windows. This executable requires admin privileges. You might want to start Command Prompt or your debugger using the 'Run as administrator' option. Challenge can be downloaded here.</li>
  <li><strong>Approach:</strong> Similar to the last one, where you need to patch IsDebuggerPresent, however you also need to fork it to actually send you to IsDebuggerPresent, since the “straight forward” path leads you to the debugger breaking. Fork, then patch, and you get the flag. Use IDA Freeware for static analysis, WinDbg for stepping through until you find where it ruins itself, and use x64dbg for finding addresses of functions. In this case, I found the address of the output string, which is where they print the start of the challenge, and manually stepped through until I found where it is forking.</li>
</ul>
