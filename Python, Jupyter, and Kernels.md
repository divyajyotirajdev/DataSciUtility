## Python, Jupyter, and Kernels
**Citations:**
- [Python Docs: Python vs IPython](https://plot.ly/python/ipython-vs-python/)
- [Datacamp: IPython or Jupyter](https://www.datacamp.com/community/blog/ipython-jupyter)
- [Medium: sh vs bash](https://medium.com/@varunkumar_53845/sh-vs-bash-a-summary-50f92a719e0d)
- [Jupyter Docs: How IPython and Jupyter work](https://jupyter.readthedocs.io/en/latest/architecture/how_jupyter_ipython_work.html)

User interacts with -> shell which calls -> kernel which invokes -> system / hardware. 
Shell is the command line interpreter. It interprets the command either in interactive mode or scripts. 
Kernel is where stuff happens - it interacts with hardware, spawns processes, does IO etc.

![Fig shows shell - kernel interaction](https://cdn-images-1.medium.com/max/800/1*OwJKhKiNr5OUhmsR_qOyLg.png)  

In Jupyter notebooks at the core is the language execution engine which interacts with terminal (shell interface) and language kernels.

![Jupyter high level view](https://jupyter.readthedocs.io/en/latest/_images/ipy_kernel_and_terminal.png)

Defaults for Jupyter -- execution happens in python, shell interface is Ipython, language kernels can be python 2.x, 3.x, conda distributions. 

*python Vs Ipython* - Python is the programming language. Ipython is the REPL (read eval print loop) environment with niceties like tab autocomplete, syntax highlight etc. It is a interface to python and isn't the only one. Ipython is python version agnostic and Jupyter project was a spinoff from the non python dependent parts like notebook server.

It is possible to create different language kernels by either creating a wrapper that still uses the python environment for execution or in languages where that would be infeasible or suboptimal - writing native language kernels with their own messaging machinery and outputs. 

**Why have notebook servers?**

![Jupyter end to end](https://jupyter.readthedocs.io/en/latest/_images/notebook_components.png)

1. Notebooks are the front end that along with running the code - save the input and output cells
2. If you don't have a kernel installed you can still open the file but not run it
3. Therefore, isolating the NB from the different (language / version) kernels becomes essential

