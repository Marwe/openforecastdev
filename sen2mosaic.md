# sen2mosaic


https://sen2mosaic.readthedocs.io/en/latest/setup.html

wget https://repo.anaconda.com/archive/Anaconda2-5.1.0-Linux-x86_64.sh

## Install sen2mosaic

### create a python virtualenv

    mkvirtualenv sen2mosaic
    workon sen2mosaic
    pip install -r requirements.txt
    deactivate # to finally leave


#### download data

    source ./.hub_credentials # read credentials for sentinel hub
    sen2mosaic/sen2mosaic/download.py -u "$hubuser" -p "$hubpass" -t 32UMV -c 20 -s 20180801 


## mosaic

    ipython # run from ipython shell
    %run sen2mosaic/sen2mosaic/mosaic.py -te 456000 5428000 476000 5448000 -e 25832 -res 20 -n worked_example -b AGGRESSIVE ./


## sentinelsat

* https://sentinelsat.readthedocs.io/en/stable/
* https://github.com/sentinelsat/sentinelsat/


