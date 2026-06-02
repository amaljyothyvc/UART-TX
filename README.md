# UART-TX
This is a small UART TX code written by me.It makes use of baudtick for transitioning between states, baudtick is made True when the baudcounter matches the baudclk hence FSM transiton starts occuring.
UART is a serial communication protocoal.it will be having a transmitter and a reciever, the communication happens one bit per baudtick.
10 bits are available, start bit=0, stop bit=1, then 8 bits of actual data.
baudrate is the number of times symbol changes occur per second.
if systemclk=50_000_000
baudrate=9600
then systemclk/baudrate = number of sysetm clock needed for 1 baudrate to succcesfully occur.
when the internal counter reaches systemclk/baudrate we make the baudtick==1, transition occurs
