To convert and C01 images to tiff or png format (with and without normalization)

# 1. Download and install bftools:
cd ~/bin

wget http://downloads.openmicroscopy.org/latest/bio-formats/artifacts/bftools.zip

unzip bftools.zip

rm bftools.zip

export PATH=$PATH:~/bin/bftools

# 2. Install required python packages:
pip install argparse

pip install os

pip install subprocess

pip install tqdm

pip install pathlib

pip install numpy

pip install scikit-image

# 3. Perform .C01 to .tiff conversion and subsequent normalization and .png conversion with C01_to_png.py script:
python3 C01_to_png.py -i INDIR -o OUTDIR -ift C01 -oft tiff

the images can also first be converted to unnormalized png instead of tiff by changing the command to

python3 C01_to_png.py -i INDIR -o OUTDIR -ift C01 -oft png

