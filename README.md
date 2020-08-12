#########################################################

 Description: Simple pifmrds testing script            
 Author: Tsali // James Washington - Network Engineer  
 Date: 2020/08/11                                      
 Twitter: @tsali                                       
 Instagram: red_hens                                   
 OnlyFans: Tsali                                       
 Facebook: TsaliJames                                  
 Website: cultofjames.org                              
                                                       
 ToDo: Make similar scripts for other RF technologies  

#########################################################

This is a simple script that will allow you to quickly enter info to test broadcasting with PIFMRDS

ASSUMPTIONS:
1. You already have pifmrds installed and available as a global command
2. You are using a shielded directly connected cable between your transmitter and receiver to ensure no illegal transmissions on public airwaves

To install
1. Log into the bash capable server you're installing it in
2. git clone https://github.com/tsali/broadcast
3. cd into the broadcast directory
4. chmod +x broadcast
5. use from within the broadcast directory (IE ./broadcast or bash broadcast,) or copy to /bin or /usr/bin as necessary

For the copy/paste inclined:                                                                                      

```
git clone https://github.com/tsali/broadcast.git && cd broadcast && chmod +x broadcast
```

Example usage:

```
pi@retropi3:~$ broadcast

Available Audio Sources:

1)Microphone (Default is plughw:1,0)
2)Local Music Directory (default is ~/music/*.mp3)
3)Website/Stream/Specific file
4)Cancel/Exit 

Audio Source: 2
Enter Frequency: 89.9
Enter station ID#: 1234
Enter station name: PiFM
Enter additional radio text (replace spaces with _ or -): Test_Pi_FM_transmission

Starting broadcast on 89.9, press CTRL+C to stop it

Using stdin for audio input.
Input: 44100 Hz, upsampling factor: 5.17
2 channels, generating stereo multiplex.
Created low-pass FIR filter for audio channels, with cutoff at 15700.0 Hz
PI: 1234, PS: "PiFM".
RT: "Test_Pi_FM_transmission"
Starting to transmit on 89.9 MHz.
```
