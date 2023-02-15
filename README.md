# Emineux
This script is designed to perform a port scan on a specified IP address and then use Hydra to attempt password recovery for an SSH server (if one is found). It prompts the user for additional options such as the wordlist to use, the SSH port number, and the number of retries.

The script first sets some constants for the directory of wordlists, the number of Hydra threads, and the Hydra timeout. It then displays a banner and prompts the user for a target IP address. If the IP address is invalid, the script will exit.

Next, the script runs an Nmap scan to find open ports on the target IP address and stores the output in a variable. It then displays the open ports in a user-friendly format.

If an SSH server is found, the script will prompt the user to run Hydra for password recovery. It will then prompt the user to select a wordlist to use, either "rockyou.txt", "cewl.txt" (which creates a wordlist from a specified URL using the cewl tool), or a custom wordlist. The user can also enter additional Hydra options such as exit on the first valid password.

The script will prompt the user for the SSH port number, the number of retries, the delay between retries, the Hydra username format, and the Hydra password format. It will then run Hydra with the specified options and store the output in a file.

If any credentials are found, the script will display them to the user.

*This is still under construction*
