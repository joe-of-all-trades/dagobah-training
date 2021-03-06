layout: true
class: inverse, middle, large

---
class: special
# Advanced tool definiton

slides by @martenson

.footnote[\#usegalaxy / @galaxyproject]

---
class: larger

## Please Interrupt!
We answer to you.

---
# Planemo

[Command-line utilities](http://planemo.readthedocs.io/) to ease the development of tools.

```shell
$ planemo lint
$ planemo test
$ planemo serve
```
[Full list of commands](http://planemo.readthedocs.io/en/latest/commands.html)

---
# Port forwarding

Planemo runs disposable Galaxy on port 9090 by default.

Please make sure you ssh to VM with port forwarding.

```shell
$ ssh -L 9090:localhost:9090 galaxyguest@YOUR_VM
```

---
# Bringing up to speed

- Is seqtk present? If not run:

```shell
$ sudo apt-get install seqtk
```

- Obtain the necessary files.

```shell
$ mkdir -p ~/tools/seqtk/test-data
$ cd ~/tools/seqtk/test-data
$ wget https://raw.githubusercontent.com/galaxyproject/galaxy-test-data/master/2.fastq
$ seqtk seq -A 2.fastq > 2.fasta
$ cd ..
$ wget https://raw.githubusercontent.com/martenson/dagobah-training/master/advanced/003-tools-advanced/seqtk_seq.xml
```

---
# Make sure

```
$ planemo l
$ planemo t
$ planemo s
```

Check at http://localhost:9090 (with port forwarding)

---
# Advanced tool building

[Planemo advanced tool wrapping](http://planemo.readthedocs.io/en/latest/writing_standalone.html#simple-parameters)
- let's continue with the planemo-based tool wrapping!
