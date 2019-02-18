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


# Appendix

## example download log 

~~~
Downloading: 100%|██████████████████████████████████| 330M/330M [01:22<00:00, 4.03MB/s]
MD5 checksumming: 100%|██████████████████████████████| 330M/330M [00:00<00:00, 432MB/s]
Skipping file S2A_MSIL1C_20181111T103241_N0207_R108_T32UMV_20181111T110239.SAFE, as it has already been downloaded and extracted in the directory. If you want to re-download it, delete it and run again.
Downloading S2B_MSIL1C_20171015T104009_N0205_R008_T32UMV_20171015T104525.SAFE...
Downloading: 100%|██████████████████████████████████| 121M/121M [00:26<00:00, 1.55MB/s]
MD5 checksumming: 100%|██████████████████████████████| 121M/121M [00:00<00:00, 386MB/s]
~~~


