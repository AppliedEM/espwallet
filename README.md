# espwallet
An open-source esp-12 arduino-based bitcoin hardware wallet

This set of programs is a tool designed to allow anyone with a few extra units of dumb paper money store all their valuable bitcoin in a secure location. It consists of two parts:

1.) The firmware that runs on the espressif esp-12 chip.
2.) The python frontend that runs all the tasty networking and crypto algos.

FLASHING THE BOARD:
1.) Install python 3
  a.) Download and open the installer. Navigate to advanced options. Check the box that says "add python to environment variable."
  a.) Optional: Make sure the "python" command executes python3 and not python2
2.) Connect the esp-12 D1 chip to your computer via usb. Make sure there are no other USB-Serial converters connected to your computer.
3.) In the ./barebones/esptool/ directory there will be an "upload.py" program. Double-click it or execute it with the "python" command and follow the directions.

INSTALLATION:
WINDOWS
1.) In the ./complete/dist/bitboard directory there will be a file called "bitboard.exe" you should be able to execute it and run the program!


USAGE:
This is a very basic program. As such, there are only three functions.

1.) Send
  Allows you to send bitcoin to another address. Enter the public key of the address you want to send it to, how much you want to send, and the fee (usually 300-5000 satoshi) and hit the button!
2.) Import
  Allows you to import bitcoin from a WIF (Wallet Import Format) key, that can be generated using a number of tools. As an example, here is one such tool:
  https://www.bitaddress.org/
3.) Receive
  Allows you to request bitcoin from another wallet or client. Hitting this button will copy your bitcoin address to your clipboard, which you can paste wherever you choose.

When conducting a transaction, the output will be displayed at the bottom of the screen. If it begins with "Success: True", your transaction was successful. If not, you might need to try again, and maybe consider increasing the fee.

The checkbox to the side of the balance switches the client to testnet mode, and is primarily for development purposes.

*Note: This wallet might not work with some bitcoin services. Coinbase is a notable example of this. As a general rul of thumb, if the transactions occur on the actual bitcoin blockchain, they should be recognized by the wallet. Coinbase sometimes does not conduct transactions on the blockchain, and will therefore sometimes not work. Conversely, Mycelium is a wallet known to work with this wallet.
