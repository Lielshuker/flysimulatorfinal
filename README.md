# flySimulator1.0
link to git hub: 
git@github.com:Lielshuker/flysimulatorfinal.git
## Installation
to start the simulator ypu need to install flightgear simulator from the link: https://www.flightgear.org/
or do the following command at the terminal:
* sudo add-apt-repository ppa:saiarcot895/flightgear
* sudo apt-get update
* sudo apt-get install flightgear
after getting the simulator, there're several change at the setting:
--generic=socket,out,10,127.0.0.1,5400,tcp,generic_small   
--telnet=socket,in,10,127.0.0.1,5402,tcp
then, download the file generic_small to the protocol folder under data of the simulator code.
in addintion, add to the project file that give the simultor Instructions how to fly the airplane.
## Usage
compile the main.cpp with argument that contains the name file that the simulator will read the information from.
g++ -std=c++14 *.cpp -Wall -Wextra -Wshadow -Wnon-virtual-dtor -pedantic -o a.out -pthread
## Documentation 
this project get fly Instructions txt file, the file being read by lexar function and than parser funcation that open commands.
each command have the responsibility to do something with the simulator:
  * ### openDataServer:
    responsible for open thread that run sever and listing on the given port and
    and reading from generic_small. the information from genric_small get insert into map and like this     we can get them in o(1).
  * ### ConnectControlClient:
    responsible for creating theard that create client that will listen to the givan port and ip and         will sent information from the client to the server.
  * ### var:
    responsible on the variables of the airplane. get into the var info from the simulator (by           the server) and send from the var info for the simulator (by the client).
    the var responsible for the infromation from and to the simulator.
  * ### while:
    responsible for while loop.
  * ### if:
    responsible for if condition.
  * ### print:
    responsible for print the string / varible in after the print.
## Credits
* adi ungar
* liel shuker
