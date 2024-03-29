# OpenSSH - Readme

## What is OpenSSH
>OpenSSH is a remote management tool, that gives you access to run commands on another machine.

- [ ] Standard for remote access
- [ ] A suite of utilities, most imp are the server and client components.
- [ ] ``` sudo apt install openssh-client openssh-server ```


## Prereqs
- [ ] Remote server must be on, connected, accessible.
- [ ] Obtain IP or name of the remote machine. 
- [ ] Ensure you've necessary permissions to access the remote machine. Have a valid username and password for the remote server. 
- [ ] Check firewall settings on both your local machine and remote server. Ensure - port 22 - is allowed by your firewall. Adjustment may be required to permit secure communication.  


## Connecting to a server via OpenSSH

- [ ] ```which ssh```
- [ ] You should have SSH client already installed locally on your machine. ###Check if pre-installed###: 
    - [ ] ``` which ssh```
                 /usr/bin/ssh




## Check the status of running server
- [ ] ```systemctl status sshd```
    - [ ] if service not running:
            - [ ] ```sudo systemctl start sshd```  - This prints no output.
    - [ ] starting service on boot:
            - [ ] ```sudo systemctl enable sshd```  -  Gets started during the boot process.



## How to connect to a Remote Server:
  ```ssh user_name@ip```
    - [ ] user_name: account that being accessed on the host
    - [ ] ip: machine that is being accessed. Can be an  IP address (192.168.1.24) or domain (www.domainname.com)

- [ ] Note: After logging into the host computer, commands work work as if they are written directly to the host terminal. Use a public-privaye key pair or SSH key pair to login into the remote host is more secure than using passwords. 



## How to create public-private keys?
- [ ] For generating public-private keys: 
    - [ ]  ```ssh-keygen ```
           
        - [ ] Your identification saved in:  /home/dfk/.ssh/id_rsa
        - [ ] Your public key saved in:  /home/dfk/.ssh/id_rsa.pub
        - [ ] fingerprint:  SHA256:9sXzb46rQkXVPyCU0ILwF5LYq97Bc10rHaHyFW4vTfI dfk@gallium

- [ ]  Public key must be copied to the remote host. Private key must remain hidden. After copying the public key to the remote host, the connection is established using SSH keys and not the password. 



<details>
<summary>Frequently asked questions about `ssh`</summary>

<ol>
<li>What is SSH used for?</li><p>SSH is used to securely connect to a remote system or server. It can be used to transfer data between two connected systems.</p>
<li>What port does SSH run on?</li><p>22</p>
<li>How can we access a Linux Machine via the Windows command prompt using SSH?</li><pre>ssh user_name@host(IP/Domaimn_name)</pre>

<li>How can we create public-private keys using SSH?</li><pre>ssh-keygen</pre>
<li>What are the three major encryption techniques used by SSH?
<li>Symmetrical encryption</li><li>Asymmetrical encryption</li><li>Hashing</li>
</li>
<li>How do I use SSH to connect to a remote server in Linux?</li>
<p>Replace `username` with your actual username and `remote_server_ip` with the IP address or domain of the remote server.</p>
<pre>ssh username@remote_server_ip</pre>

<li>What is the SSH command for connecting to a server with a specific port?</li>
<pre>ssh -p 2222 username@remote_server_ip</pre>

</li>How can I use SSH to transfer files between my local machine and a remote server?</li>
<pre>scp local_file.txt username@remote_server_ip:/path/to/destination/</pre>
<p>Using SCP for file transfer. This command securely copies the local file to the specified destination on the remote server. Adjust the file paths and names accordingly.</p>

</ol>
<pre>$ This dropdown contains<br>a code block!</pre>
</details>
