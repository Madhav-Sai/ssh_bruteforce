Certainly! Here's the updated section in the README file:

## Usage

1. Clone the repository:

```
git clone https://github.com/Madhav-Sai/ssh_bruteforce.git
```

2. Navigate to the project directory:

```
cd ssh-password-cracker
```

3. Install the required libraries:

```
pip install -r requirements.txt
```

4. Prepare the password list:

If you are looking for a wordlist to use (such as a similar file to the top-100 text file used in the lesson), you can download similar lists from [here](https://github.com/danielmiessler/SecLists/tree/master/Passwords/Common-Credentials). Save the wordlist file in the project directory.

5. Modify the script:

Open the script file `ssh_password_cracker.py` and update the following variables according to your target SSH server:

- `host`: Set the IP or hostname of the target SSH server.
- `username`: Set the SSH username you want to use for authentication.

6. Run the script:

```
python ssh_password_cracker.py
```

The script will iterate through each password in the wordlist file and attempt to authenticate with the SSH server. If a valid password is found, it will be displayed, and the script will exit. If none of the passwords work, the script will indicate that no valid password was found.

Please note that you must have a running SSH service that you are authorized to test, such as on your localhost. Additionally, if your SSH service has a default Kali configuration, it may block authentication attempts after 10 tries. If you want to test more than 10 connections with the wordlist, you will need to edit your `sshd_config` file (for example, by setting `MaxStartups 101`) and restart the SSH service. Alternatively, you can use a wordlist with less than 10 invalid passwords to stay within the limit.


