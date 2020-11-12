# authorized_keys
A list of authorized keys that are registered to my droplets on DO

Steps to get these onto a droplet:
1. Log into digital ocean dashboard
2. Go to droplet and open the browser-based console
3. Log in
4. Backup the current `.ssh/authorized_keys` file
    ```sh
    cp .ssh/authorized_keys .ssh/authorized_keys.backup
    ```
5. Download the `keys` file on this repo in raw mode
    ```sh
    wget https://raw.githubusercontent.com/morphatic/authorized_keys/main/keys?token=AADSIDBXK7WKGSC2V3PNO227VV36M > temp1
    ```
6. Append the downloaded key onto the end of the `authorized_keys` file:
    ```sh
    cat temp1 >> .ssh/authorized_keys
    ```
7. Test access from terminal on machine being added
8. Logout
