# reproducibility-tutorial
reproducibility-tutorial FOSS2020
    1  cd /scratch
    2  git clone https://github.com/mgjust/reproducibility-tutorial.git
    3  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    4  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
    5  ln -s /opt/conda/pkgs/*/bin/* /bin
    6  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
    7  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
    8  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
    9  /opt/conda/bin/pip install bash_kernel
   10  /opt/conda/bin/pip install ipykernel
   11  /opt/conda/bin/python3 -m bash_kernel.install
   12  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   13  /opt/conda/bin/conda search -c bioconda snakemake
   14  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   15  ln -s /opt/conda/bin/* /bin
   16  ln -s /opt/conda/lib/* /usr/lib
   17  snakemake --version
   18  clear
   19  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   20  apt-get update
   21  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   22  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   23  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   24  sudo apt-get update
   25  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   26  docker run hello-world
   27  cd /scratch/reproducibility-tutorial/
   28  history >>README.md
