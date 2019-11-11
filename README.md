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
 ```
 
4. Install [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)
     
* Download and Extract contents.
* In 'seqFrog_conf.py' list path to 'trimmomatic_folder'
     
5. Install [Megahit](https://github.com/voutcn/megahit/releases)
 
* Download and Extract contents
* In 'seqFrog_conf.py' list path to megahit script in 'megahit_folder'

6. Install [ABySS](https://github.com/bcgsc/abyss/releases)

> Download and Extract contents
* Install Boost, run 
```
$ wget http://downloads.sourceforge.net/project/boost/boost/1.56.0/boost_1_56_0.tar.bz2
$ tar jxf boost_1_56_0.tar.bz2
```
* In abyss folder, run `$ ./configure`
* 
* In 'seqFrog_conf.py' list path to abyss script in 'abyss_folder'

7.
