Nautilus-actions configuration tool, which was needed in order to have context menu actions in Nautilus doesn't seem available in the Software center in 18.04 LTS.

Update 2018-05-31.

Launchpad user Daniel Marynicz has created PPA for Ubuntu 18.04 LTS with Nautilus, Caja and Nemo-enabled packages. You can install them as usual:

sudo add-apt-repository ppa:daniel-marynicz/filemanager-actions

sudo apt-get install filemanager-actions-nautilus-extension # Nautilus
sudo apt-get install filemanager-actions-caja-extension # Caja
sudo apt-get install filemanager-actions-nemo-extension # Nemo

sudo apt-get install filemanager-actions* # simply all filemanagers

After installation you can launch fma-config-tool.

