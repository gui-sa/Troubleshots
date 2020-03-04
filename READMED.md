**TROUBLESHOT**




**Formatando** **o** **ubuntu** **:**


1 - Download Ubuntu LTS

2 - Download RUFUS

3 - Criar um USB bootavel

4 - Reiniciar

5 - Repetidamente clicar f2 na tela inicial para entrar na bios

6 - Na aba EXIT, escolher o usb bootavel

7 - instalar o ubunut

8 - conectar `a rede

9 - Instalar drives e softwares de terceiros  (essa parte vai demorar)


10 - No tipo de instalacao escolher opcoes avancadas e criar um particao para ele de no minimo 30 gb, colocar no formato ext4 e inicializacao /

11 - instalar o ubunut

12 - entrando no ubuntu, no terminal:

	sudo -H gedit /etc/default/grub

		NA LINHA QUE ESTA:

		GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"

		MUDAR PARA:

		GRUB_CMDLINE_LINUX_DEFAULT="acpi=force"

		SALVAR

------------------------------------------------------



**Instalando** **o** **GIT**


Sudo apt-get update 

Sudo apt-get install git

git config --global user.name "Guilherme Salomao" 

git config --global user.email "guime.sa9@gmail.com"
-------------------------------------------------------


**Arrumando** **o** **INPUT**


1 - Settings

2 - Region & Language

3 - +

4 - English United states

5 - English(US, intl., with dead keys)

6 - choice option

7 - erase older option

--------------------------------------------------------


**Instalando** **CUDA:**


https://www.pugetsystems.com/labs/hpc/How-To-Install-CUDA-10-1-on-Ubuntu-19-04-1405/
segue o tutorial


0 - Rode :
		sudo apt-get update

		sudo add-apt-repository ppa:graphics-drivers/ppa

		sudo apt-get install dkms build-essential

		sudo apt-get install nvidia-driver-440
		
		nvidia-smi

		sudo apt-get install freeglut3 freeglut3-dev libxi-dev libxmu-dev

1 -  Entra no cuda site e baixe o run file

2 -  Instala o .run sem os drivers

3 - em um arquivo novo de nome preferencial digite:



		export PATH=$PATH:/usr/local/cuda-10.2/bin

		export CUDADIR=/usr/local/cuda-10.2

		export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda-10.2/lib64


4- Desta forma o cuda so se ativa qndo voce entrar no path do arquivo e digitar:

		source <nome do arquivo>


Com o terminal aberto é possivel ver que o cuda esta sendo executado:

		nvcc --version

		nvidia-smi

Quando for usar algo que necessita do cuda, execute os comandos na janela em que o cuda foi aberto como source.


-----------------------------------------------------------



