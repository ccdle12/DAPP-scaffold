# DAPP-scaffold
Scaffold for ethereum solidity dapp

Setup

Git clone:
``` cd DAPP-scaffold/webapp ```

Make the scripts we need to be executable:
``` chmod +x npmscript.sh ```


Run the script to install all the dependencies:
``` ./npmscript.sh ```


After installation you will be prompted with Yeoman web app generator,
Deselect all the options,
Type "n" when prompted to include jQuery,
Choose TDD when prompted with DSL style



Move to the truffle folder:
``` cd ../ | cd truffle ```



Make the script executable:
``` chmod +x initnewaccount.sh ```



Run the script to init the geth console with a new account:
``` ./initnewaccount.sh ```


You will be prompted in the terminal to create a password to create an account.
Enter a password and then an address will be returned. Copy the address.


Move to the data folder:
``` cd ../ | cd data ```


Paste the new account address into the genesis.json:
``` vi genesis.json ```
Paste the address and replace "<enter new account address here>"



Make the script executable:
``` chmod +x initgenesis.sh ```



Run the script to initialize the genesis block for this private chain:
``` ./initgenesis.sh ```



Move to the truffle folder:
``` cd ../cd truffle ```


Edit truffle.js and add the copied address to truffle.js "<add account address here>"
``` vi truffle.js ```


Make the script executable:
``` chmod +x gethconsole.sh ```



Execute the script to setup the geth console:
``` ./gethconsole.sh ```



Make the script executable:
``` chmod +x vi tcmt.sh ```



Execute the script to compile, migrate and test the contracts:
``` ./tcmt.sh ```


