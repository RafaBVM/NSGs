# NSG’s & Inpecting Network Protocols

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


