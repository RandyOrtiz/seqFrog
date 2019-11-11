# seqFrog
A bioinformatics pipeline for transcriptomic work in non-model organisms
 
Introducing a modified pipeline from seqFrog 2019 by:
 
`Rivera, Christopher, seqFrog, (2019), GitHub repository, https://github.com/c94rivera/seqFrog`
 
 
### Getting Started
 
1. Download seqFrog repository.
 
 
2. Install Python (v3).
 
 
3. Install the following dependencies:
  *One by one...make sure that no errors appear, and if they do following the prompt to correct it.
 
 ```
$ sudo apt install python3-pip
$ sudo apt install gcc
$ sudo apt install make
$ sudo apt install cmake
$ sudo apt install libbz2-dev
$ sudo apt install libncurses5-dev
$ sudo apt install zlib1g-dev
$ sudo apt install libncursesw5-dev
$ sudo apt install liblzma-dev
$ sudo apt install libcurl4-openssl-dev
$ sudo apt install libssl-dev
$ sudo apt install libsparsehash-dev
$ sudo apt install bowtie2
$ sudo apt install samtools
$ pip3 install pandas
$ pip3 install biopython
$ pip3 install tqdm
$ sudo apt install sra-toolkit
$ sudo apt-get update
$ sudo apt install default-jre
$ sudo apt install git
$ sudo apt install velvet
$ sudo apt install dos2unix
$ sudo apt install ncbi-blast+
$ sudo apt install cd-hit
 ```
 
 
4. Install [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)
     
* Download and Extract contents.
* In 'seqFrog_conf.py' list path to 'trimmomatic_folder'
  
  
5. Install [Megahit](https://github.com/voutcn/megahit/releases)
 
* Download and Extract contents
* In 'seqFrog_conf.py' list path to megahit script in 'megahit_folder'


6. Install [ABySS](https://github.com/bcgsc/abyss/releases)

* Download and Extract contents
* Install Boost, run 
```
$ wget http://downloads.sourceforge.net/project/boost/boost/1.56.0/boost_1_56_0.tar.bz2
$ tar jxf boost_1_56_0.tar.bz2
```
* In abyss folder, run
```
$ ./configure
$ make
$ sudo make install
```
* In 'seqFrog_conf.py' list path to abyss script in 'abyss_folder'
* If issues with latest release, download v2.1.5


7. Install [SPAdes](http://cab.spbu.ru/software/spades/)
* Download and Extract contents
* In 'seqFrog_conf.py' list path to abyss script in 'abyss_folder'


8. Install Oases
```
$ git clone --recursive https://github.com/dzerbino/oases
$ make
```
* In 'seqFrog_conf.py' list path to oases script in 'oases_folder'
* If system fails to locate oases then add oases to the last line of your .bashrc file `export PATH="path/to/oases:$PATH"`
*	If system fails to locate velvet then add velvet to the last line of your .bashrc  `export PATH="/path/to/velveth:$PATH"`


9. Install [BBMap](https://sourceforge.net/projects/bbmap/)
* Download and Extract contents
* In 'seqFrog_conf.py' list path to tadpole script in 'tadpole_folder'

10. Install [Trinity](https://github.com/trinityrnaseq/trinityrnaseq/releases)
* Download and Extract contents
* Install [Jellyfish](https://github.com/gmarcais/Jellyfish/releases)
* Download and Extract contents
* In main jellyfish folder, run
```
$ ./configure
$ make
$ sudo make install
```
* Install [Salmon](https://github.com/COMBINE-lab/salmon/releases/tag/v1.0.0)
* Download and Extract contents
* Add path to salmon to .bashrc file `export PATH="/path/to/salmon/bin:$PATH"`
* In main trinity folder, run
```
$ make
$ make plugins
$ sudo make install
```
* Add path to trinity to .bashrc file `export TRINITY_HOME="/path/to/trinity/installation/dir"`
* In 'seqFrog_conf.py' list path to trinity script in 'trinity_folder'
* In 'seqFrog_conf.py' list path to salmon script in 'salmon_folder'


11. Install [Transrate](http://hibberdlab.com/transrate/installation.html)
* Download and Extract contents
* In 'seqFrog_conf.py' list path to transrate script in 'transrate_folder'


12. Install [Blast](ftp://ftp.ncbi.nlm.nih.gov/blast/executables/LATEST/)
* Download and Extract contents
* In main blast folder, run
```
$ ./configure
$ make
$ export PATH=$PATH:$HOME/ncbi-blast-2.9.0+/bin
```
* In 'seqFrog_conf.py' list path to blast bin in 'blast_folder'
* In 'seqFrog_conf' list location of 'custom_blast_library' (in test case the uniprot folder)
* (locate 'uniprot' folder in annotation_libraries directory test library)


13. Install [MIRA](https://sourceforge.net/projects/mira-assembler/files/MIRA/)
* Download and Extract contents
* In 'seqFrog_conf.py' list path to mirabait script in 'mirabait_folder'


14. Install [RSEM](https://deweylab.github.io/RSEM/)
* Download and Extract latest version
* In main RSEM folder, run
```
$ make
$ sudo make install
```


15. Install [Kallisto](https://pachterlab.github.io/kallisto/download)
* Download and Extract latest version
* In 'seqFrog_conf.py' list path to kallisto script in 'kallisto_folder'


16. Shannon Installation in this order:
* Install metis, numpy, and cvxopt
```
$ sudo apt-get install metis
$ pip install numpy
$ pip install cvxopt
```
* Install [Quorum](https://github.com/gmarcais/Quorum/releases)
* In main quorum folder, run
```
$ ./configure
$ make
$ sudo make install
```
* Install [Shannon](https://github.com/sreeramkannan/Shannon/releases)
* Download and Extract latest version
* If using a linux system as assumed until this point, open terminal and run
```
$ dos2unix 'shannon.py' #drag shannon script into terminal
```
* Open shannon.py and add shebang (top line of script, must be python2): `#!/usr/bin/env python2`
* Add locations of required directories in shannon.py
* Make sure shannon.py is an executable file, right click and check permissions
* In 'seqFrog_conf.py' list path to shannon script in 'shannon_folder'


17. Install [Mitobim](https://github.com/chrishah/MITObim/releases/tag/v1.9.1)
* Download and Extract latest version
* In 'seqFrog_conf.py' list path to mitobim.pl script in 'mitobim_folder'
* In 'seqFrog_conf.py' list path to mira script in 'mira_path'


18. Install [BUSCO](https://gitlab.com/ezlab/busco)
* Download and Extract latest version
* In main busco folder, run
```
$ python setup.py install --user
```
* Install HMMER
```
$ wget http://eddylab.org/software/hmmer/hmmer.tar.gz
$ tar zxf hmmer.tar.gz
$ cd hmmer-3.2.1
$ ./configure
$ make
$ sudo make install
```
* Install [Augustus](https://github.com/Gaius-Augustus/Augustus)
* Download and Extract latest version
* Open terminal and run the following
```
$ sudo apt install libboost-iostreams-dev
$ sudo apt install zlib1g-dev (previously installed)
$ sudo apt install libgsl-dev
$ sudo apt install libboost-graph-dev
$ sudo apt install libboost-all-dev
$ sudo apt install libsuitesparse-dev
$ sudo apt install liblpsolve55-dev
$ sudo apt install libsqlite3-dev (previously installed)
$ sudo apt install libmysql++-dev
$ sudo apt install libbamtools-dev
```
* In main augustus folder, run
```
$ make
$ sudo make install
```
* In .bashrc file add
```
export PATH="/path/to/augustus/bin:$PATH"
export PATH="/path/to/augustus/scripts:$PATH"
export AUGUSTUS_CONFIG_PATH="/path/to/augustus/config/"
```
* ...back to BUSCO...
* In the config subfolder copy config.ini.default and paste as config.ini
* In the config.ini folder state all dependencies...DO NOT USE QUOTES!!!
* In 'seqFrog_conf.py' list path to run_BUSCO.py script in 'busco_folder'
* [Install Lineages for BUSCO](https://busco.ezlab.org/)
* Download and Extract relevent lineage dataset (Eukaryota odb9 in our case)
* In 'seqFrog_conf' list path to lineage directory in 'busco_lin'


> Congrats! If everything is installed correctly seqFrog should work!







