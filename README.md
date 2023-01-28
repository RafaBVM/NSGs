# NSG’s & Inspecting Network Protocols

<p>
<img src="https://i.imgur.com/JINu0s3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I login to Client-1 using my domain address and password.
</p>
<br />

<p>
<img src="https://i.imgur.com/YElWWlJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now I logged back in DC-1 under an admin account.
</p>
<br />

<p>
<img src="https://i.imgur.com/uPVC3Hn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I go to the Server Manager Panel->Tools->Select DNS->Expand DC-1->select my domain
</p>
<br />

<p>
<img src="https://i.imgur.com/Lzoi9aB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I then right click within the blank space and create a new host under DC-1’s IP Address.
</p>
<br />

<p>
<img src="https://i.imgur.com/avBirzR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I go back to Client-1’s desktop and ping my host name I just created. You can see DC-1’s IP address above.
</p>
<br />

<p>
<img src="https://i.imgur.com/8BpHbUG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then I ipconfig /dns to see my local DNS cache record.
</p>
<br />

<p>
<img src="https://i.imgur.com/zSqcRhJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I go back to DC-1 and change the IP address to 8.8.8.8 on the host I had created.
</p>
<br />

<p>
<img src="https://i.imgur.com/eTU2b3o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now I’m back on Client-1 on the command prompt as an admin and here I ipconfig /flushdns.
</p>
<br />

<p>
<img src="https://i.imgur.com/8MMlR3v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now I ping my host name in which resulted in getting resolved under 8.8.8.8 since everything got flushed out the cache.
</p>
<br />

<p>
<img src="https://i.imgur.com/7Fitc18.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once again I go back to DC-1 and create a new CNAME.
</p>
<br />

<p>
<img src="https://i.imgur.com/8KhT8ID.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I call the record search and associate it with www.google.com
</p>
<br />

<p>
<img src="https://i.imgur.com/FsVLOMX.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I return to Client-1 and ping search, in which it resolves to www.google.com
</p>
<br />

<p>
<img src="https://i.imgur.com/UayPASV.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I ipconfig /display dns in which  shows that everything resolves towards one another.
</p>
<br />




