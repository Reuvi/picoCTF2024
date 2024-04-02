<h2>WinAntiDbg0x100</h2>
<ul>
  <li><strong>Author:</strong> IssacSasson</li>
  <li><strong>Category:</strong> Reverse Engineering</li>
  <li><strong>Points:</strong> 200</li>
  <li><strong>Description:</strong> This challenge will introduce you to 'Anti-Debugging.' Malware developers don't like it when you attempt to debug their executable files because debugging these files reveals many of their secrets! That's why, they include a lot of code logic specifically designed to interfere with your debugging process. Now that you've understood the context, go ahead and debug this Windows executable! This challenge binary file is a Windows console application and you can start with running it using cmd on Windows. Challenge can be downloaded here.</li>
  <li><strong>Approach:</strong> Use IDAFreeware for static analysis of what is even happening, which tells you that it is simply calling IsDebuggerPresent and if not you will get the flag. Use WinDbg for stepping through, and x64dbg for finding the address of IsDebuggerPresent. Set a breakpoint in WinDbg and step through until it returns, then set eax to 0 in order to patch the call so that it thinks there is no debugger present. WinDbg is used because it is easier to understand what is happening (from my experience).</li>
</ul>
