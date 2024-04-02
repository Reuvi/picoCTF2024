<h2>WinAntiDbg0x300</h2>
<ul>
  <li><strong>Author:</strong> IssacSasson</li>
  <li><strong>Category:</strong> Reverse Engineering</li>
  <li><strong>Points:</strong> 400</li>
  <li><strong>Description:</strong> This challenge is a little bit invasive. It will try to fight your debugger. With that in mind, debug the binary and get the flag! This challenge executable is a GUI application and it requires admin privileges. And remember, the flag might get corrupted if you mess up the process's state.</li>
  <li><strong>Approach:</strong> Taking what is learned from the last two WinAntiDbg challenges, you simply need to utilize the forking and patching techniques multiple times to avoid the debugger from crashing. Use IDA Freeware to navigate through the many sub directories, until you find one that belongs to WinMain, and you can break at the address of any function inside the sub directory by finding it in x64dbg. Use WinDbg to manually step through, and follow the code both dynamically and statically to keep track of where you are, which allows you to know where each jump will lead. If a jump leads somewhere undesirable, simply patch it, and continue until you reach the flag.</li>
</ul>
