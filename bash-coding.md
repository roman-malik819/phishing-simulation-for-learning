## Step 1: Switch to Root User

To begin the setup process, switch to the root user by entering the following command in your terminal:

```bash
sudo su
```

This will grant you root-level access, which is required for certain administrative actions during the setup of the phishing simulation environment. Use root privileges responsibly.
## Step 2: Update the System (If Not Already Updated)

Before installing any necessary packages or tools, ensure your system is up to date. This helps avoid compatibility issues during the setup.

Run the following command:

```bash
sudo apt update
```

This command updates the package index so your system can access the latest versions of available packages. It is recommended to run this before installing any dependencies.
## Step 3: Install cURL

Next, install **cURL**, a command-line tool used for transferring data. It is essential for downloading tools or scripts required in this phishing simulation project.

Run the following command:

```bash
sudo apt install curl
```

If `curl` is already installed, this command will confirm the latest version is present. If not, it will install it.
## Step 4: Install OpenSSL

Install **OpenSSL**, a powerful toolkit for Secure Sockets Layer (SSL) and Transport Layer Security (TLS) protocols, which is often used in encryption and security testing.

Run the following command:

```bash
sudo apt install openssl
```

This will install the OpenSSL library and command-line tools, which may be useful for simulating secure communications or understanding certificate handling during phishing simulations.
## Step 5: Install Required Packages

Install all the essential packages needed for this phishing simulation, including Git, Python, pip, PHP, and the OpenSSH client.

Run the following command:

```bash
sudo apt install git python3 python3-pip php openssh-client -y
```

### Package Breakdown:
- `git` – version control system for managing code
- `python3` – required for running Python scripts
- `python3-pip` – Python package manager
- `php` – used to simulate dynamic pages in phishing scenarios
- `openssh-client` – enables secure connections to remote systems

The `-y` flag automatically confirms installation prompts.
## Step 6: Clone the PyPhisher Tool

Now, clone the **PyPhisher** tool from GitHub. This tool will be used to simulate phishing attacks in a controlled, educational environment.

Run the following command:

```bash
git clone https://github.com/SACHINSIROHI47/PyPhisher
```

This command will download the `PyPhisher` repository into your current directory. Make sure you have an active internet connection before running it.
## Step 7: View Downloaded Files and Navigate to PyPhisher Directory

After cloning the repository, list all files and directories in your current location to confirm the `PyPhisher` folder has been downloaded successfully.

Run the following command:

```bash
ls
```

You should see a directory named `PyPhisher`. To move into that directory, run:

```bash
cd PyPhisher
```

Once inside the folder, list its contents to view all files, scripts, and directories included in the tool:

```bash
ls
```

You will now see all the files related to the `PyPhisher` project. From here, you can begin setup or run the simulation as per the tool’s instructions.
## Step 8: Install Python Dependencies

To ensure all necessary Python packages are available for the PyPhisher tool, install the dependencies listed in the `requirements.txt` file.

Run the following command:

```bash
pip3 install -r files/requirements.txt
```

If you encounter the following error:

```
error: externally managed environment
```

It means your Python environment is being controlled by the system package manager. To bypass this and proceed with installation, use the following command instead:

```bash
pip3 install -r files/requirements.txt --break-system-packages
```

This command will force the installation of required packages even in a managed environment. Use this option only if you understand the implications, especially on system-wide Python configurations.

## Step 9: Launch the PyPhisher Tool

To begin using PyPhisher, execute the main script by running the following command:

```bash
python3 pyphisher.py
```

After launching, you will be prompted with the question:

```
Do you have a LocalXpose authtoken? (y/n):
```

Since we are not using a LocalXpose token for this simulation, type:

```bash
n
```

Once you respond, the PyPhisher interface will display a menu containing a list of social media platforms and popular websites that can be simulated.

It will then ask you to select an option. For this demonstration, it is recommended to choose:

```bash
1
```

This option corresponds to **Facebook (Traditional Login Page)**. You may choose any option based on your interest, but for learning and consistency, it is best to follow the recommended instruction.

## Step 10: Configure Phishing Page Options and Launch the Simulation

After selecting your desired platform (e.g., Facebook Traditional), PyPhisher will prompt you with a few setup questions:

1. **Do you want to enable OTP (One-Time Password) pages?**  
   Type:

   ```bash
   n
   ```

2. **Do you want to enter a custom shadow URL?**  
   Press `Enter` to skip.

3. **Enter redirection URL (leave empty for default):**  
   Press `Enter` again to skip.

### Generating the Phishing Link

Once configuration is complete, PyPhisher will initialize and generate a **Cloudflared phishing URL**. Two types of links will appear:

- The first is a raw Cloudflared URL.
- The **second is a masked URL**, commonly used to make phishing links appear legitimate.

**Copy the masked URL** and **paste it into your browser**.

This will launch a **cloned Facebook login page**.

### Simulating a Credential Capture

Enter **fake credentials** into the login form for testing purposes only.

After submission:

- You will see the captured **username** and **password** displayed directly in your **Kali Linux terminal**.
- The terminal will actively monitor for and display any further credential submissions in real time.

This simulation demonstrates how phishing pages operate and how sensitive information can be collected when users are not cautious.

> ⚠️ **Disclaimer:** This project is strictly for ethical hacking education. It must only be used in controlled environments like Kali Linux, cybersecurity labs, or academic settings. Any misuse for malicious intent is illegal and strongly discouraged.
## Conclusion

This project successfully demonstrates the structure and flow of a simulated phishing attack using a cloned Facebook login interface within a controlled ethical hacking environment. By walking through each step — from installation to execution — learners gain hands-on insight into how phishing attacks are carried out and how credentials can be intercepted if users are not vigilant.

The purpose of this simulation is to build **awareness**, **defensive skills**, and **ethical understanding** of phishing techniques. It is not intended for real-world deployment or exploitation.

### ⚠️ Final Reminder:
> This project is for **educational purposes only**. Running or sharing phishing simulations outside of authorized, ethical environments is strictly prohibited and illegal.

By responsibly studying such simulations, ethical hackers, students, and cybersecurity professionals can better understand and defend against real phishing threats in the digital world.

---

Thank you for exploring this project.

