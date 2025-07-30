Basic commands in Linux
lsb_release -a  ###to check the version of ubuntu
df -h    ##check the space
du -h /folder_name   ## check space of specific folder
du -sh *  ##to check the memory consumed by each folder (used mostly by me)
apt list --installed ## to check the list of installed applications
chmod 775 folder_name    ### to provide read, write and other permissions when the file creates
visudo           ##to add sudo usser for admin access""
cat /etc/passwd      ####path that shows the user app_name
cat /etc/shadow             ###########to know the shell and home folder

cat   ## to see the content int the file
cat auth.log | less   ##(to see page by page)
grep 'keyword" (to search a specific word in the file)
grep  userfile 'keyword' -> destination_file   ######collects all the lines containing 'keyword' from userfile and writes to destination file
grep -i '^R' cap_10pF_mim_mom.pex.netlist > capacitor.txt  ######collects all the lines starting with R from userfile and writes to destination file

cat file_name | grep 'search_word"
adduser User_name (to add a account)
sudo apt install app_name
sudo apt update
su -- user name ## to switch to sudoe user or to switch from root 
ls -a   ## to see the hidden files
find ~ -name "*your_filename*"  ### this will search for the fine_name in all paths


git branch  ( to check which branch you are)
git checkout -b branch_name
###access the ubuntu from windows (WSL install)
Windows + E and \\wsl$ to access linux

## access windows from ubuntu 
/mnt

If paths are not same python -m streamlit run

##################
Final Notes
Why Shift Targets by 1?
Language models predict the next token in the sequence. For input [tok1, tok2, tok3], the target is [tok2, tok3, tok4].

Dataset Compatibility:
With __len__ and __getitem__, you can now use DataLoader to batch and shuffle the data:

python
Copy
dataloader = DataLoader(dataset, batch_size=32, shuffle=True)
#############


#####lock file
#find . -name '*lck*' '*panic.log*'
#find . -name '*lck*' '*panic.log*' -exec rm {} +
find . \( -name '*lck*' -o -name '*panic.log*' \)
find . \( -name '*lck*' -o -name '*panic.log*' \) -exec rm {} +


####python related :
pip show torch (or package name)  ## this will show the deltails of the package where installed, which version etc....

##  this will show the path where the python is installed
import sys
print(sys.executable)
##

If the packages are installed but not in the path where the python is installed, then you have to append the path in your code like below :
##
import sys
sys.path.append('/path/where/the/package/installed')
##

#########################################
5. Visualizing Compatibility
Imagine your dataset as a bookshelf:
__len__ tells the DataLoader how many books (samples) are on the shelf.
__getitem__ lets the DataLoader grab a specific book by its position.
The DataLoader acts like a librarian:
Shuffles the order of books (if asked).
Groups books into stacks (batch_size).
Hands these stacks to the model for training.
##################################







###############pytorch###############
1. Why __len__ and __getitem__ Matter
PyTorch’s Dataset class requires two core methods to work seamlessly with DataLoader:

__len__: Returns the total number of samples in the dataset.

__getitem__: Fetches a single sample (e.g., input and target) by index.

By defining these, your custom dataset becomes a standardized interface that DataLoader understands. Think of it like a checklist:

The DataLoader uses __len__ to know how many batches to create.

It uses __getitem__ to fetch individual samples and collate them into batches.

#############################################


######################################################
data_iter = iter(dataloader)  # Creates an iterator object. The iterator data_iter knows how to fetch batches sequentially from the dataloader.
######################################################
first_batch = next(data_iter)  # Get the first batch
The next() function asks the iterator for the next batch. Since batch_size=2, the first batch contains the first 2 samples from the dataset.

########BATTERY########
You have to check how much energy the battery can hold : This can be deduced by checking the parameter mAh and voltage rating. If a certain battery claimns 3000mAh/3V means, it can supply 3000mA with stable 3V continuously for 3V or continuosu 3mA with stable 3V continuosly for 3000 hrs or what ever the current calcultation. From here, you can get energy the battery can store, de/de=p


COMMOM MODE FEEDBACK (FOR BIASING THE UNDEFINED NETS) + SELF BIASING OF THE DIFF PAIR

ANALOG - OP-AMP 
Virtual short is valid until which point - Virtual short of the op-amp is valid until the output of the op-amp saturates (It doesnt follow the virtual ground once the output of the opamp saturates)
The virtual short condition is valid as long as the op-amp operates within its linear region. When the op-amp's output reaches its saturation point (i.e., it can no longer increase or decrease its output voltage), the virtual short condition no longer holds. In essence, the virtual short is dependent on the op-amp's ability to adjust its output to maintain the near-zero voltage difference between its inputs. Once it saturates, it loses this ability.

UGB is critical for analyzing the stability of negative feedback systems. As far as the closed-loop gain is considered, UGB doesnt make any sense. As the closed loop gain will become 0.5 at UGB, so as far as the negative feedback to be stronger, we have to think about the frequencies until where the oper-loop gain is atleast 10 times higher than 1, that meanse Ab > 10, then A/(1+Ab) will be 1/b. So,the phase margin at the UGB frequency is a key indicator of how stable the feedback system will be. Hence, as far as the UGB is concerned, stability is the key indicator we get from UGB.

Quality factor explains how good the resonance or how low/high are the looses in the RLC circuit or any filter. If there are any loses means, the oscillations will die eventually. However, if the Q is high means, the oscillations dies slower than that of the oscillations that die in lower Q. Ideally if Q is infinite means, oscillations keep on sustain. If it is series RLC circuit, we will have to see the current, and if R = 0 means high current will flow (ideally Q will be infite and R appears in denominator of Q). On the other hand, if it is parallel RLC circuit, for sure we have to read voltage and hence, if R = infinite, we see more voltage (ideally Q will be infite and R appears in numerator of Q)

Miller capacitance :
Any impedance connected connected between two nodes (say p and q) in a circuit can always be resolved into two impedences : one between p and GND, other between q and GND as long as there is a stringant relation between p and q at low frequences irrespective of the presence of the impedance between p and q. This means even though the impedance between p and q is absent, the relation between p and q still exists
Any impedance connected between two nodes (say p and q) in a circuit can always be resolved into two impedances: one between p and GND, and the other between q and GND, provided there is a strong relationship between the voltages at p and q at low frequencies, regardless of the presence of a direct impedance between p and q. This implies that even if the direct impedance between p and q is absent, the relationship between their voltages still exists.

#######SOURCE DEGENERATION NOTES######
We can generate a stable current even if VGS and VDS (not PV) is varied, How can we do that? Take an NMOS (or PMOS) and connect a very big resistor at the dource, this resistor introduces feedback and, if the resistor is so large, it will prevent changes in Vgs. This means, if the device follows square law, even thogh the vgs is flucating, the source resistor makes sure that the (vgs-Vt) always constant and the current will not change even the gate voltage is changing. VDS any-way will not have effect (atleast ideal case)
######################################


#############MOSFET Notes#####################
Mobility (un) will decrease kind of exponentially with temperature. Threshold voltage (Vt) decreases linearly with temperature. If an NMOS is connected in a diode connected fashion and a constant current is forced, then under these coniderations, the gm varies largely with temperature than the VDS due to the fact that the mobility decreases exponentially

VELOCITY SATURATION: The saturation velocity or the maximum velocity the charge carriers can attain in the MOSFET is roughly at 100k m/sec. This means, eventhough the VDS is kept on increased, after reaching the maximum velocity, the charge carriers cannot attain any higher velocity than 100k m/sec and device may break. On the other hand, this VDS value is different for different technological nodes. For longer channel length devices, the VDS may be very large may be well above VDD. Generally we do not operate at that higher voltages. Hence we do not see velocity saturation effect in long length devices. However, this saturation voltage decreases as the channel length shrinks. For more aggressive technological nodes, it may have as smaller as 0.3V-0.5V (may be smaller than Vt). Hence, before reaching the normal current saturation region, the devices hit the velocity saturation and the current changes linearly rather than qadratically wrt VGS  

SECOND ORDER EFFECTS OF MOSFET:
1. CHANNEL LENGTH MODULATION (due to the VDS, the channel gets affected.Long channel devices means negligible. Short channel devices means channel significantly reduces w.r.t VDS, which will also alter the threshold another second order)
2. DIBL : The channel will be controlled by the drain-source voltage, so the Vth gets altered w.r.t VDS is calledd DIBL
3. Velocity Saturation : Current varies linearly instead of quadratic in saturation region w.r.t VGS 
Gist: Because of VDS : channel gets modulated, threshold voltage gets modulated, and velocity gets saturated)

LEVEL-1 SPICE MODEL PARAMETERS : mu, lambda, threhsold_voltage, Vdsat(velocity saturation), and gamma. These 5 parameters uniquely characterize transistor in a particular technology. GIDL is w.r.t gate tosource voltage
################################################

###################Square-law deviation notes###################
HOW TO CALCULATE THE GM OF THE MOSFET : Find an operating point for VGS, IDS for a given VDS, then find the differentiation of the IDS wrt to VGS around that operating point. This is called the gm. In general we can fit the IDS vs VGS data to the nearest sqaure law equation and compare the simulated values with the nearest square-law equation. We can clearly see the IDS is changing slow or fast w.r.t square law equation as kind of sens the gm is underestimated or over-estimated.
We often approximate the IDS−VGS relationship with a square law, but in reality, the current scales with VGS to an exponent typically ranging from 1 to 2. This non-ideal behavior means that relying on the simple square law equation will result in significant deviation in the calculated transconductance gm.
#############################################################

###################
For a given MOS size, if I keep decreasing the current from max to min or increasing the current from min to max, the transconductance will match to ideal squared law at certain amount of current. And the error/ deviation increases as the current is moved father from that point
###################



#######SRAM Notes##########
Vt variations will be ther as the SRAM cell is scaled down aggressively and operated at very low voltages. So make sure that the cells falling in the tails of the gaussian curve are working fine (lets say around 5 sigma to 6 sigma). If they are operating ok ok, then the yield will automatically improves.
How to enhance SNM in SRAM cell: 8T-SRAM, we can decouple the internal node separately for reading purpose by adding two extra NMOS devices and make 6T SRAM as an 8T SRAM cell to increase the static noise margin (SNM)
If I still have to worry about area, and  reduce tha rea, istead of decoupling the bumping node by adding 2 device, add a device in the other side of inverter and deactivate that side by opening. This way, even if there is a bump voltage, it wont trip and the SNM would be good
whichever memory architecture it is (whether SRAM, DRAM, or NVM), the architecture will have row-decoder (for address accessing), column mux, I/O, and control.

MEMORY CUT - ARCHITECTURE (HOW TO DECODE) - EXAMPLE IS BELOW
Let's say the memory has labelled as "512words*74bits with mux8" what it actually meets: This means there are 512 words with each word having 74 bits (so the memory capacity is 512*74). Now these 512 words are rearranged with mux8. What this mean? This means 512 rows are folded such that it aligns with mux8 or in other words these 512 words are organized with 8-input multiplex. This means, rows will be 512/8 = 64, number of word columns will be 8 (each with 74 bits). So the address will be like, 6-bits for the row decoding (since 64 rows) and 3 bit for the column-decoding.  

SELF TIMED SRAM : FEEDBACK IS MADE INBUILT

############################

Open_source Simulators I am using :

Xschem for the schematic
ngspice for the netlist generation, simulation, and then viewing the results
magic layout for the layout
save the netlist before running the simulator. Then the waveform reloader will reload
Command for plotting gain and phase plot in ngspice : plot db(v(node)) 180*cph(v(node))/pi
analoglibin xschem:
vsource.sym
cap
res
gnd.sym --- ground

#####################Procedure to invoke magic layout in the terminal################
magic  -rcfile /usr/local/share/pdk/sky130A/libs.tech/magic/sky130A.magicrc
-rcfile will intantiates or makes sure the the layouts of the SKY130A library is called.
makesure that the sky130A.magicrc file do exist at the path "usr/local/share/pdk/sky130A/libs.tech/magic/"  Otherwise check for the file in the pdk folder and copy in side the magic or just copy where you want (not sure this)


#################### Procedure for invoking the xschem and setting up the environment for simulations################
1. copy the xschemrc file from "/usr/local/share/pdk/sky130B/libs.tech/xschem/" to the working directory
     The pdk is copied/saved to the path "/usr/local/share/pdk/sky130B/libs.tech/xschem/"
2. Once you copied xschem to your working directory, you can invode xschem :  How to invoke the xschem?
     xschem &
3. the default extension of the file_name is .sch (example : user_file_name.sch)
    xschem user_file_name.sch &
#####################################################################################################################

##############################temperature variations - DC characteritcs of inverter ngspice #############################
name=s1 only_toplevel=false value= "
.dc Vinp 0 2 0.1 TEMP 1 100 10
.save all
.control
 write inv_tran.raw
.endc"





