# FeynGKZ
FeynGKZ : a Mathematica package for solving **Feyn**man Integrals using **GKZ** Hypergeometric systems.

## Installation of dependencies

FeynGKZ needs the following dependencies:

<details>
  <summary> AMBRE </summary>
  
  1. Software site: [here](https://jgluza.us.edu.pl/ambre/)
  2. Version used: 2.1.1 
  3. Installation instructions:  
	Move this package to the directory containing FeynGKZ.wl. In Mathematica, this directory is specified by the global variable `FeynGKZPath`.
</details>

<details>
  <summary> Olsson.wl </summary>
  
  1. Software site: available as ancillary files from [here](https://arxiv.org/abs/2201.01189)
  2. Version used: N/A
  3. Installation instructions:  
	Move this package to the directory containing FeynGKZ.wl. In Mathematica, this directory is specified by the global variable `FeynGKZPath`.
</details>
 
<details>
  <summary> polymake </summary>
  
  1. Software site: [here](https://polymake.org/doku.php)
  2. Version used: 4.6
  3. Installation instructions:  
    On a Linux system, it is usually sufficient to do the following:  
    <pre>
    $ sudo apt-get install polymake
    </pre>
    Further installation instructions have been provided on the polymake website. 
</details>

<details>
  <summary> TOPCOM </summary>
  
  1. Software site: [here](https://www.wm.uni-bayreuth.de/de/team/rambau_joerg/TOPCOM/index.html)
  2. Version used: 0.17.8
  3. Installation instructions:
	
  * On Linux:  
	<pre>
	$ sudo apt-get install -y build-essential wget libgmp-dev libcdd-dev m4
	$ mkdir topcom && cd topcom && mkdir source && mkdir install
	$ cd install && export topcompath=$PWD && cd ..
	$ cd source && wget https://www.wm.uni-bayreuth.de/de/team/rambau_joerg/TOPCOM-Downloads/TOPCOM-0_17_8.tgz
	$ tar -xzf TOPCOM-0_17_8.tgz && cd topcom-0.17.8
	$ ./configure --prefix=$topcompath && make -j4 && make install
	</pre>
	After this, the `bin`, `lib` and `include` folders for TOPCOM could be found under `topcompath`. The paths to these folders could be prepended to the environment variables `PATH`, `LD_LIBRARY_PATH` and `CPATH` in the `~/.bashrc` file, so as to ensure that TOPCOM executables such as `points2triangs` or `points2ntriangs` could be called from any directory using the login-shell, as long as a single-user installation is concerned. 
	
  * On MacOS:  
	  First, install `brew` from [homebrew](https://brew.sh/). After that, one can follow the same set of steps as given for Linux, with the difference being     only in the very first step:
  	<pre>
  	% brew install gcc cddlib gmp m4
  	</pre>
    The rest of the steps are again similar to those for Linux, including the names of the environment variables, with the difference being that in most modern Macs, the default login-shell is not `bash` but rather `zsh`. So the paths need to be set in the `~/.zshrc` file, accordingly.

4. Further comments:  
In case one faces complications regarding installing TOPCOM on their system, they may use a minimal docker build of the same. The image is available [here](https://hub.docker.com/r/sudeepan/topcom), with the corresponding dockerfile being accessible from [here](https://github.com/sudeepan/topcom). One may follow the set of instructions provided in the latter to run this image in a container, and to subsequently rename this container.

</details>

<details>
  <summary> Macaulay2 </summary>
  
  1. Software site: [here](http://www2.macaulay2.com/Macaulay2/)
  2. Version used: 1.20
  3. Installation instructions:  
    On a Linux system, it is usually sufficient to do the following:  
    <pre>
    $ sudo apt install macaulay2
    </pre>
    Further installation instructions have been provided on the Macaulay2 website. 
</details>
