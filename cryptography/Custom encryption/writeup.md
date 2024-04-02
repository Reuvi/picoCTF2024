<h2>Custom encryption</h2>
<ul>
  <li><strong>Author:</strong> IssacSasson</li>
  <li><strong>Category:</strong> Cryptography</li>
  <li><strong>Points:</strong> 100</li>
  <li><strong>Description:</strong> Can you get sense of this code file and write the function that will decode the given encrypted file content. Find the encrypted file here flag_info and code file might be good to analyze and get the flag.</li>
  <li><strong>Approach:</strong> What’s happening: Generation of a shared key using a Diffie-Hellman-like mechanism. Application of a dynamic XOR operation on the plaintext with a given text key. Multiplication of each character's ASCII value by the shared key and a constant (311) to produce the cipher. To decrypt, you must: Recompute the shared key using the same parameters (a, b, g, p). Invert the multiplication for each cipher element to retrieve the XOR-encrypted characters. Reverse the XOR operation using the same text key to get the original plaintext.</li>
</ul>
