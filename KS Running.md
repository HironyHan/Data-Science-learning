\documentclass[9pt]{osa-supplemental-document}
\setboolean{shortarticle}{false}

\title{Key steps for running a AIFeynman project}
\author{} %leave this blank
%% DO NOT ADD AUTHOR INFORMATION HERE; IT WILL BE ADDED DURING PRODUCTION

\begin{abstract}
This is a notebook about how to start from 0 to build a AIFeynman project. Including how to start the program and the potential obstacles. Follow the guideline and start building AIFeynman project.
\end{abstract}

\setboolean{displaycopyright}{false} %copyright statement should not display in the  supplemental document

\begin{document}

\maketitle

\section{Installation}

The first step is to install AIFeynman library on the computer. AIFeynman only support Linux or MacOS System.
\begin{enumerate}
    \item \textbf{Bulid a virtual environment. }
    Installing the library "virtualenv" and build a environment.
    
    \begin{verbatim}
    pip install virtualenv
    virtualenv -p python3 feyn
    source feyn/bin/activate
    \end{verbatim}
    
    \item \textbf{Installing the required compiler "gfortran".}

    \begin{verbatim}
    sudo apt-get update
    sudo apt-get install gfortran
    \end{verbatim}
    
    Open the ~/.bashrc file.

    \begin{verbatim}
    nano ~/.bashrc
    \end{verbatim}
    
    Add the following lines to your ~/.bashrc file to set environment variables related to.
    
    \begin{verbatim}
    export FC=gfortran
    export F77=gfortran
    \end{verbatim}
    
    Press Control+X to exit, press Y to save and press enter to exit.

    Run the following code to refresh the setting.
    
    \begin{verbatim}
    source ~/.bashrc
    \end{verbatim}
    
    \item \textbf{Installing the required library "numpy" and ipykernel.}
    
    \begin{verbatim}
    pip install numpy
    pip install ipykernel
    python -m ipykernel install --user --name=feyn
    \end{verbatim}

    \item \textbf{Installing the library "AIFeynman".} It is better to get a python version before 3.12.

    \begin{verbatim}
    pip install aifeynman
    \end{verbatim}

    \item \textbf{Opening jupyter notebook to build a python file.}

    \begin{verbatim}
    jupyter notebook
    \end{verbatim}

    After entering jupyter notebook, when choosing the new file's type, new a \textbf{feyn} type file. The installation steps are finished.
    
\end{enumerate}



% Bibliography
%\bibliography{sample}

%Manual citation list
%\begin{thebibliography}{1}
%\bibitem{Zhang:14}
%Y.~Zhang, S.~Qiao, L.~Sun, Q.~W. Shi, W.~Huang, %L.~Li, and Z.~Yang,
 % \enquote{Photoinduced active terahertz metamaterials with nanostructured
  %vanadium dioxide film deposited by sol-gel method,} Opt. Express \textbf{22},
  %11070--11078 (2014).
%\end{thebibliography}

\end{document}
