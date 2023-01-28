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


# File Shares & Permissions

<p>
<img src="https://i.imgur.com/OXy1zTC.png" alt="Disk Sanitization Steps"/>
</p>
<p>
I log off and log back on DC-1 as an admin.
</p>
<br />

<p>
<img src="https://i.imgur.com/cLdZtkl.png" alt="Disk Sanitization Steps"/>
</p>
<p>
Went to Active Directory Users & Computers, went to my domain and clicked on _EMPLOYEES
</p>
<br />

<p>
<img src="https://i.imgur.com/d07k2V0.png" alt="Disk Sanitization Steps"/>
</p>
<p>
Selected random user and logged into Client-1 using the user I've selected.
</p>
<br />

<p>
<img src="https://i.imgur.com/O15UDBE.png" alt="Disk Sanitization Steps"/>
</p>
<p>
I go back to DC-1 to create some new folders on the C: drive named read-access, write access, no access, and accounting.
</p>
<br />

<p>
<img src="https://i.imgur.com/sPQN2O4.png" alt="Disk Sanitization Steps"/>
</p>
<p>
As you can tell I gave each folder their designated access, copied the link of the write access folder in the midst of this process. Also gave access to the access folder only to domain admins. I skipped on accounting.
</p>
<br />

<p>
<img src="https://i.imgur.com/6ALCIrA.png" alt="Disk Sanitization Steps"/>
</p>
<p>
I go to Client-1 and typed \\dc-1 on file explorer.
</p>
<br />

<p>
<img src="https://i.imgur.com/FOIE6J5.png" alt="Disk Sanitization Steps"/>
</p>
<p>
Went back to DC-1 and put in a text document in the read-access folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/reEWkpr.png" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/UuvI4mc.png" alt="Disk Sanitization Steps"/>
</p>
<p>
I go to Client-1’s desktop and notice how I can’t create a new document, but I can still access the created documents I made from DC-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/VMBarmi.png" alt="Disk Sanitization Steps"/>
</p>
<p>
Back in DC-1, I create a new organizational unit under the name _SECURITY_GROUPS.
</p>
<br />

<p>
<img src="https://i.imgur.com/FwG7eFK.png" alt="Disk Sanitization Steps"/>
</p>
<p>
I make a new group under _SECURITY_GROUPS called ACCOUNTANTS.
</p>
<br />

<p>
<img src="https://i.imgur.com/zxpBfnt.png" alt="Disk Sanitization Steps"/>
</p>
<p>
Now I go to the file explorer and I right click the accounting folder I had made earlier, and I give it read and write access to the ACCOUNTANTS.
</p>
<br />

<p>
<img src="https://i.imgur.com/lYzcFt9.png" alt="Disk Sanitization Steps"/>
</p>
<p>
I go to Client-1 to see if I have access to the accounting in which I do not.
</p>
<br />

<p>
<img src="https://i.imgur.com/F9fPGAj.png" alt="Disk Sanitization Steps"/>
</p>
<p>
I go to DC-1 to Active Directory->_SECURITY_GROUPS->go to members->and paste random name from Client_1’s login account.
</p>
<br />

<p>
<img src="https://i.imgur.com/v4S77Mb.png" alt="Disk Sanitization Steps"/>
</p>
<p>
I logoff and log back in on Client-1 using the name I had put in the accountant group to essentially gain full access of the accounting folder.
</p>
<br />











