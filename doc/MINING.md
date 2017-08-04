TODO: Finish shitty mining guide

# Mining Shit
Shitcoin can be mined in the same ways as any other bitcoin based scrypt coin. If you know how to mine Litecoin, than you know how to shit. If you don't know, than hold onto your ass because you're gonna learn today. 

## CPU Mining
Because of the truly ass shattering hash rates present on the networks of non-shitcoins, CPU mining won't get you very far with them. With Shitcoin, however, CPU mining can yield new blocks just fine. The version of Litecoin that Shitcoin is cloned from actually has a built it CPU miner. It can be used by going to the debug console (accessable via the help tab) and using the command `setgenerate true [threads]`, where threads is the amount of CPU cores you'd like to use. If you'd like to use a third party miner however, the most efficient miner is pooler's [cpuminer](https://sourceforge.net/projects/cpuminer/files/). As a heads up, many antivirus programs will think that mining programs are trojan viruses. This is probably due to the fact that in the age of cryptocurrency many viruses have been created to use the host computer as a miner. Any way, cpuminer is used via the command line. To use it, navigate to the directory where the program is stored in the terminal/command prompt. For a list of options, you can use `miner -h`, where miner is the name of the program. On linux this will probably just be "minerd" whereas on windows it will be "something.exe".

## GPU Mining
In the very early days of Bitcoin and up until just recently with most scrypt coins, mining with a rig made of gaming GPUs was the way to do it. Thanks to the development of machines specifically built to mine however, it has been impractical to mine Bitcoin at home for quite some time even with your own ASIC, and lately ASICs built for scrypt have been bringing the same bullshit to Litecoin. However, given the Shitcoin network difficulty as of this writing GPUs essentially function as mining laxatives. You will need to find mining software that is compatable with your GPU. In the case of NVIDIA GPUs, I recommend this incarnation of [ccminer](https://github.com/tpruvot/ccminer/releases). It is almost identical to cpuminer in terms of use, and as a matter of fact you can follow the below example down to the command line arguments to get started. 

### Example: Solo mining with cpuminer
In order to solo mine, you will first need to configure your client correctly. In order to do this, you will need to create a file name "shitcoin.conf" in the application data directory. On Ubuntu, this is a hidden folder called .shitcoin in your home directory. On windows, this is a folder called Shitcoin located in the %appdata% directory. Create shitcoin.conf and add the following:

```
server=1
rpcuser=shituser
rpcpassword=yourshitpass
rpcport=14300
rpcallowip=127.0.0.1
```
Remember those login credentials, as you will need them for the miner. After you've done that and restarted your shit wallet, you're ready to mine. Navigate to the cpuminer directory in your terminal and enter the following:

`miner -a scrypt -o 127.0.0.1:14300 -O shituser:yourshitpass`

Executing that command will fire up the miner and starting using all available cpu threads to mine. If you like, you can specificy the amount of threads you'd like to use by appending `-t <threads>` to the command. When you've had enough shit, simply use control-C while in the terminal window to terminate the program. 
