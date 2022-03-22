# Special instructions for Windows

**NB**: Your copy of Windows will need to be the 64-bit version (if you
don't know how to check that you can [find out
here](https://support.microsoft.com/en-us/windows/which-version-of-windows-operating-system-am-i-running-628bec99-476a-2c13-5296-9dd081cdd808))

1. Start by installing miniconda. You can download it from
   [https://docs.conda.io/latest/miniconda.html](https://docs.conda.io/latest/miniconda.html),
   make sure you download the **python 3** version (not python 2) for 64-bit
   Windows.

2. Once miniconda is installed you will find `Anaconda prompt (miniconda3)` in
   the start menu. Click this to open up a terminal where `conda` will be
   available

3. Create a conda environment for the course

```bash
$> conda env create -n convml-tt -y
```

4. Activate your newly created conda environment. You will noticed your prompt
   change and now any package you install (with conda or pip) will be installed
   into this enviroment

```bash
$> conda activate convml-tt
```

5. To "check out" (get a local copy of) the course notes you will need `git`.
   In the command prompt type the following and press enter to install `git`:

```bash
$> conda install -y -c conda-forge git
```

6. convml-tt is built on the [pytorch](https://pytorch.org) deep learning
   package which you can install with conda:

```bash
$> conda install pytorch "torchvision>=0.4.0" cpuonly -c pytorch
```

7. With pytorch installed you can now install the `convml-tt` package that you
   will be working with:

```bash
$> python -m pip install convml-tt
```

8. The very last thing you need is a copy of the course material. Move to a
   suitable folder where you want to store the course material. For example
   your desktop

```bash
$> cd %homepath%\Desktop
```

9. Check out a copy of the course material with git

```bash
$> git clone https://github.com/leifdenby/SENSE_convml_tt
```

10. Now you can change back to the folder where you cheched out the course
material and open up the jupyter notebooks

```bash
$> cd SENSE_convml_tt
$> jupyter notebook
```
