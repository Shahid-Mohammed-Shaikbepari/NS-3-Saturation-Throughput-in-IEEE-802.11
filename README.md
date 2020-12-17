# Saturation-throughput
#### Pre-Requisites:
Please pre install NS-3 from NS-3 website in a VM by following the instructions.

### NS-3 simulations
In total four cases have been simulated as follows:
#### Case   Minimum Backoff window size   Minimum Backoff window size    Date Rate    Number of nodes
      A E1             1                            1023                  constant       change
      A E2             1                            1023                  change         constant
      B E1             63                           127                   constant       change
      B E2             1                            127                   change         constant
      

The following instructions to run the NS-3 simulations:

1. In terminal navigate to the NS-3 home directory and run the following command
./waf configure -d optimized
2. In total 2 files have been modified viz. regular-wifi-mac.cc, mywifi-pcf.cc and have been placed in sperate folder with each case name.
Case A E1:
3. For the Case A E1, copy mywifi-pcf.cc file present in the folder AE1 and paste in /ns-3-dev/scratch/ and replace regular-wifi-mac.cc in 
path /src/wifi/model/regular-wifi-mac.cc
4. From the terminal run the following command, 
./waf --run "mywifi-pcf enablePcf=0 --nWifi=10 --M=1"
5. You can see the output printed in the output screen. For the plots we have used Matlab by copying this data over there

Case A E2:
 
3. For the Case A E2, copy mywifi-pcf.cc file present in the folder AE2 and replace in /ns-3-dev/scratch and replace regular-wifi-mac.cc in 
path /src/wifi/model/regular-wifi-mac.cc
4. From the terminal run the following command, 
./waf --run "mywifi-pcf enablePcf=0 --nWifi=5 --M=1"
5. You can see the output printed in the output screen. For the plots we have used Matlab by copying this data over there

Case B E1:

3. For the Case B E1, copy mywifi-pcf.cc file present in the folder AE2 and replace in /ns-3-dev/scratch and replace regular-wifi-mac.cc in 
path /src/wifi/model/regular-wifi-mac.cc
4. From the terminal run the following command, 
./waf --run "mywifi-pcf enablePcf=0 --nWifi=10 --M=1"
5. You can see the output printed in the output screen. For the plots we have used Matlab by copying this data over there

Case B E2:

3. For the Case B E2, copy mywifi-pcf.cc file present in the folder AE2 and replace in /ns-3-dev/scratch and replace regular-wifi-mac.cc in 
path /src/wifi/model/regular-wifi-mac.cc
4. From the terminal run the following command, 
./waf --run "mywifi-pcf enablePcf=0 --nWifi=10 --M=1"
5. You can see the output printed in the output screen. For the plots we have used Matlab by copying this data over there

6. The matlab scripts are also attached in the codes section which have the data for every simulation corresponding to its name, just by running the scripts 
we get plots


### Theorotical analysis of Binachi's model 
In this section theorotical analysis of Binachi's model has been performed and ananlyzed with the simulation results
* File 1 : Case A :  bianchi_analysisCaseA.m
    * To run this function :
    * [Throughput,Throughput_perNode] = bianchi_analysisCaseA(cwMin,N) 
    * enter cwMin = 1 and N = any number of nodes, cwMax in the function is taken as 1023 ( m = 10).
* File 2 : Case B :  bianchi_analysisCaseB.m
     * To run this function :
     * [Throughput,Throughput_perNode] = bianchi_analysisCaseB(cwMin,N) 
     * enter cwMin = 63 and N = any number of nodes, cwMax in the function is taken as 1023 ( m = 10).
     
### Results
The results have been described in detail in the 'NS-3 Saturation Throughput.pdf' file with images and explanation

