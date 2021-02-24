# Special instructions for Windows

**NB**: Your copy of Windows will need to be the 64-bit version (if you
don't know how to check that you can [find out
here](https://support.microsoft.com/en-us/windows/which-version-of-windows-operating-system-am-i-running-628bec99-476a-2c13-5296-9dd081cdd808))

1. Start by installing miniconda. You can download it from
[https://docs.conda.io/latest/miniconda.html](https://docs.conda.io/latest/miniconda.html),
make sure you download the **python 3** version (not python 2) for 64-bit
Windows.

2. Once miniconda is installed you will find `Anaconda prompt
(miniconda3)` in the start menu. Click this to open up a terminal where
`conda` will be available

3. To "check out" (get a local copy of) the course notes and the
`convml_tt` software you will need `git`. In the command prompt type the
following and press enter to install `git`:

```bash
$> conda install -y -c conda-forge git
```

4. Move to a suitable folder where you want to store the course material
and the `convml_tt` software. For example your desktop

```bash
$> cd %homepath%\Desktop
```

5. Check out a copy of the course material

```bash
$> git clone https://github.com/leifdenby/SENSE_convml_tt
```

6. Enter the folder with the exercises and in there download and unpack a copy
   of the dataset you will be working with

```bash
$> cd SENSE_convml_tt
$> curl http://homepages.see.leeds.ac.uk/~earlcd/ml-datasets/Nx256_s200000.0_N500study_pretrained.tgz --output Nx256_s200000.0_N500study_pretrained.tgz
$> tar zxvf Nx256_s200000.0_N500study_pretrained.tgz
```

7. Return to the parent folder and check out a copy of the `convml_tt` software

```bash
$> cd ..
$> git clone https://github.com/leifdenby/convml_tt
```

8. Move into the `convml_tt` folder and create a conda environment from
the *environment file* in there

```bash
$> cd convml_tt
$> conda env create -f environment-cpu.yml
```

9. Activate your newly created conda environment

```bash
$> conda activate convml_tt
```

10. and install `convml_tt` into it:

```bash
$> pip install .
```

11. Now you can change back to the folder where you cheched out the course
material and open up the jupyter notebooks

```bash
$> cd ..
$> cd SENSE_convml_tt
$> jupyter notebook
```
