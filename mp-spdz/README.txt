Suppose this folder is the application.
Client and MB's inputs are stored under /Player-Data/Input-Px-0, such that x is 0:client and 1:MB, respectively
Client needs to additionally set a key in /Player-Data/Input-P0-0
The number of test case can be set in /Programs/Public-Input/FIMB_AES

Note that the input is in biginteger format. For example, if we are testing for 8 items:
- Both entities set 8 into /Programs/Public-Input/FIMB_AES
- Client sets 8 IVs /Player-Data/Input-P0-0 and 9th-line with the key
- MB sets 8 IVs in /Player-Data/Input-P1-0

To run the program, open your bash at this directory, and 
execute: Scripts/semi.sh FIMB_AES

This will execute the interactive protocol using secret sharing with the compiled 'FIMB_AES' program.


To edit the program, navigate to /Programs/Source/FIMB_AES.mpc
After editing, navigate back to this directory, and
execute: ./compile.py FIMB_AES -l
