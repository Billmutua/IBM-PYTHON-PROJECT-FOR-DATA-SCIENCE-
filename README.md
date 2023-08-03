# IBM-PYTHON-PROJECT-FOR-DATA-SCIENCE-
Skills Network Logo

Extracting and Visualizing Stock Data
Description
Extracting essential data from a dataset and displaying it is a necessary part of data science; therefore individuals can make correct decisions based on the data. In this assignment, you will extract some stock data, you will then display this data in a graph.

Table of Contents
Define a Function that Makes a Graph
Question 1: Use yfinance to Extract Stock Data
Question 2: Use Webscraping to Extract Tesla Revenue Data
Question 3: Use yfinance to Extract Stock Data
Question 4: Use Webscraping to Extract GME Revenue Data
Question 5: Plot Tesla Stock Graph
Question 6: Plot GameStop Stock Graph
Estimated Time Needed: 30 min

Note:- If you are working in IBM Cloud Watson Studio, please replace the command for installing nbformat from !pip install nbformat==4.2.0 to simply !pip install nbformat

!pip install yfinance==0.1.67
!mamba install bs4==4.10.0 -y
!pip install nbformat==4.2.0
Collecting yfinance==0.1.67
  Downloading yfinance-0.1.67-py2.py3-none-any.whl (25 kB)
Requirement already satisfied: pandas>=0.24 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance==0.1.67) (1.3.5)
Requirement already satisfied: numpy>=1.15 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance==0.1.67) (1.21.6)
Requirement already satisfied: requests>=2.20 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance==0.1.67) (2.29.0)
Collecting multitasking>=0.0.7 (from yfinance==0.1.67)
  Downloading multitasking-0.0.11-py3-none-any.whl (8.5 kB)
Requirement already satisfied: lxml>=4.5.1 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance==0.1.67) (4.9.2)
Requirement already satisfied: python-dateutil>=2.7.3 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from pandas>=0.24->yfinance==0.1.67) (2.8.2)
Requirement already satisfied: pytz>=2017.3 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from pandas>=0.24->yfinance==0.1.67) (2023.3)
Requirement already satisfied: charset-normalizer<4,>=2 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.20->yfinance==0.1.67) (3.1.0)
Requirement already satisfied: idna<4,>=2.5 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.20->yfinance==0.1.67) (3.4)
Requirement already satisfied: urllib3<1.27,>=1.21.1 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.20->yfinance==0.1.67) (1.26.15)
Requirement already satisfied: certifi>=2017.4.17 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.20->yfinance==0.1.67) (2023.5.7)
Requirement already satisfied: six>=1.5 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from python-dateutil>=2.7.3->pandas>=0.24->yfinance==0.1.67) (1.16.0)
Installing collected packages: multitasking, yfinance
Successfully installed multitasking-0.0.11 yfinance-0.1.67

                  __    __    __    __
                 /  \  /  \  /  \  /  \
                /    \/    \/    \/    \
███████████████/  /██/  /██/  /██/  /████████████████████████
              /  / \   / \   / \   / \  \____
             /  /   \_/   \_/   \_/   \    o \__,
            / _/                       \_____/  `
            |/
        ███╗   ███╗ █████╗ ███╗   ███╗██████╗  █████╗
        ████╗ ████║██╔══██╗████╗ ████║██╔══██╗██╔══██╗
        ██╔████╔██║███████║██╔████╔██║██████╔╝███████║
        ██║╚██╔╝██║██╔══██║██║╚██╔╝██║██╔══██╗██╔══██║
        ██║ ╚═╝ ██║██║  ██║██║ ╚═╝ ██║██████╔╝██║  ██║
        ╚═╝     ╚═╝╚═╝  ╚═╝╚═╝     ╚═╝╚═════╝ ╚═╝  ╚═╝

        mamba (1.4.2) supported by @QuantStack

        GitHub:  https://github.com/mamba-org/mamba
        Twitter: https://twitter.com/QuantStack

█████████████████████████████████████████████████████████████


Looking for: ['bs4==4.10.0']

[+] 0.0s
[+] 0.1s
pkgs/main/linux-64 ━━━━━━━━━━━━━━╸━━━━━━━━━━   0.0 B /  ??.?MB @  ??.?MB/s  0.1s
pkgs/main/noarch   ━━━━━━━━╸━━━━━━━━━━━━━━━━   0.0 B /  ??.?MB @  ??.?MB/s  0.1s
pkgs/r/linux-64    ━━╸━━━━━━━━━━━━━━━╸━━━━━━   0.0 B /  ??.?MB @  ??.?MB/s  0.1s
pkgs/r/noarch      ━━━━━━━━━━╸━━━━━━━━━━━━━━   0.0 B /  ??.?MB @  ??.?MB/s  0.1s[+] 0.2s
pkgs/main/linux-64 ━━━━━━━━━╸━━━━━━━━━━━━━━━  28.7kB /  ??.?MB @ 186.4kB/s  0.2s
pkgs/main/noarch   ━━━━━━━━━━╸━━━━━━━━━━━━━━  12.3kB /  ??.?MB @  79.7kB/s  0.2s
pkgs/r/linux-64    ━━━━╸━━━━━━━━━━━━━━━╸━━━━   0.0 B /  ??.?MB @  ??.?MB/s  0.2s
pkgs/r/noarch      ━━━━━━━━━━━━╸━━━━━━━━━━━━  86.0kB /  ??.?MB @ 528.5kB/s  0.2s[+] 0.3s
pkgs/main/linux-64 ━━━━━━━━━━━╸━━━━━━━━━━━━━ 540.7kB /  ??.?MB @   2.1MB/s  0.3s
pkgs/main/noarch   ━━━━━━━━━━━━━╸━━━━━━━━━━━ 507.9kB /  ??.?MB @   2.0MB/s  0.3s
pkgs/r/linux-64    ━━━━━━╸━━━━━━━━━━━━━━━╸━━ 520.2kB /  ??.?MB @   2.0MB/s  0.3s
pkgs/r/noarch      ━━━━━━━━━━━━━━╸━━━━━━━━━━ 606.2kB /  ??.?MB @   2.3MB/s  0.3spkgs/main/noarch                                   852.1kB @   2.6MB/s  0.3s
[+] 0.4s
pkgs/main/linux-64 ━━━━━━━━━━━━━╸━━━━━━━━━━━   1.3MB /  ??.?MB @   3.4MB/s  0.4s
pkgs/r/linux-64    ━━━━━━━━╸━━━━━━━━━━━━━━━━ 774.2kB /  ??.?MB @   2.5MB/s  0.4s
pkgs/r/noarch      ╸━━━━━━━━━━━━━━━╸━━━━━━━━ 860.2kB /  ??.?MB @   2.7MB/s  0.4spkgs/r/noarch                                        1.3MB @   3.2MB/s  0.4s
[+] 0.5s
pkgs/main/linux-64 ━━━━━━━━━━━━━━╸━━━━━━━━━   1.9MB @   3.8MB/s             0.5s
pkgs/r/linux-64    ━━━━━━━━━━━━━━━━━━━━━━━━   1.4MB @   2.9MB/s Finalizing  0.5s[+] 0.6s
pkgs/main/linux-64 ━━━━━━━━━━━━━━━╸━━━━━━━━━   1.9MB /  ??.?MB @   3.8MB/s  0.6spkgs/r/linux-64                                    @   2.9MB/s  0.5s
[+] 0.7s
pkgs/main/linux-64 ━╸━━━━━━━━━━━━━━━╸━━━━━━━   2.9MB /  ??.?MB @   4.3MB/s  0.7s[+] 0.8s
pkgs/main/linux-64 ━━━╸━━━━━━━━━━━━━━━╸━━━━━   3.4MB /  ??.?MB @   4.4MB/s  0.8s[+] 0.9s
pkgs/main/linux-64 ━━━━━━╸━━━━━━━━━━━━━━━╸━━   4.0MB /  ??.?MB @   4.5MB/s  0.9s[+] 1.0s
pkgs/main/linux-64 ━━━━━━━━╸━━━━━━━━━━━━━━━━   4.6MB /  ??.?MB @   4.6MB/s  1.0s[+] 1.1s
pkgs/main/linux-64 ━━━━━━━━━━━╸━━━━━━━━━━━━━   5.2MB /  ??.?MB @   4.8MB/s  1.1s[+] 1.2s
pkgs/main/linux-64 ━━━━━━━━━━━━━╸━━━━━━━━━━━   5.7MB /  ??.?MB @   4.8MB/s  1.2s[+] 1.3s
pkgs/main/linux-64 ━━━━━━━━━━━━━━━━━━━━━━━━   6.0MB @   4.8MB/s Finalizing  1.3s[+] 1.4s
pkgs/main/linux-64                                 @   4.8MB/s  1.4s

Pinned packages:
  - python 3.7.*


Transaction

  Prefix: /home/jupyterlab/conda/envs/python

  Updating specs:

   - bs4==4.10.0
   - ca-certificates
   - certifi
   - openssl


  Package               Version  Build         Channel                 Size
─────────────────────────────────────────────────────────────────────────────
  Install:
─────────────────────────────────────────────────────────────────────────────

  + bs4                  4.10.0  hd3eb1b0_0    pkgs/main/noarch        10kB

  Upgrade:
─────────────────────────────────────────────────────────────────────────────

  - ca-certificates    2023.5.7  hbcca054_0    conda-forge                 
  + ca-certificates  2023.05.30  h06a4308_0    pkgs/main/linux-64     123kB
  - openssl              1.1.1t  h0b41bf4_0    conda-forge                 
  + openssl              1.1.1u  h7f8727e_0    pkgs/main/linux-64       4MB

  Downgrade:
─────────────────────────────────────────────────────────────────────────────

  - beautifulsoup4       4.11.1  pyha770c72_0  conda-forge                 
  + beautifulsoup4       4.10.0  pyh06a4308_0  pkgs/main/noarch        87kB

  Summary:

  Install: 1 packages
  Upgrade: 2 packages
  Downgrade: 1 packages

  Total download: 4MB

─────────────────────────────────────────────────────────────────────────────


[+] 0.0s
Downloading  (1) ━━━━━━━━━━━━━━━━━━━━━━━   0.0 B beautifulsoup4             0.0s
Extracting       ━━━━━━━━━━━━━━━━━━━━━━━       0                            0.0s[+] 0.1s
Downloading  (4) ━━━━━━━━━━━━━━━━━━━━━━━   0.0 B beautifulsoup4             0.1s
Extracting       ━━━━━━━━━━━━━━━━━━━━━━━       0                            0.0sbs4                                                 10.2kB @  67.5kB/s  0.2s
ca-certificates                                    122.6kB @ 778.4kB/s  0.2s
beautifulsoup4                                      86.6kB @ 527.0kB/s  0.2s
[+] 0.2s
Downloading  (1) ━━━━━━━━━╸━━━━━━━━━━━━━   1.9MB openssl                    0.2s
Extracting   (3) ━━━━━━━━━━╸━━━━━━━━━━━━       0 beautifulsoup4             0.0sopenssl                                              3.9MB @  16.1MB/s  0.2s
[+] 0.3s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━━━━━╸━━━━━━━━━━━       0 beautifulsoup4             0.1s[+] 0.4s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━━━━━━╸━━━━━━━━━━       0 beautifulsoup4             0.2s[+] 0.5s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━╸━━━━━━━━━━━━━━━       0 beautifulsoup4             0.3s[+] 0.6s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━━╸━━━━━━━━━━━━━━       0 bs4                        0.4s[+] 0.7s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━━━╸━━━━━━━━━━━━━       0 bs4                        0.5s[+] 0.8s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━━━━╸━━━━━━━━━━━━       0 bs4                        0.6s[+] 0.9s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━━━━━╸━━━━━━━━━━━       0 bs4                        0.7s[+] 1.0s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━━━━━━━╸━━━━━━━━━       0 ca-certificates            0.8s[+] 1.1s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━━━━━━━━╸━━━━━━━━       0 ca-certificates            0.9s[+] 1.2s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━━━━━━━━━╸━━━━━━━       0 ca-certificates            1.0s[+] 1.3s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ╸━━━━━━━━━━━━━━━╸━━━━━━       0 ca-certificates            1.1s[+] 1.4s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━╸━━━━━━━━━━━━━━━╸━━━━━       0 openssl                    1.2s[+] 1.5s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━╸━━━━━━━━━━━━━━━╸━━━━       0 openssl                    1.3s[+] 1.6s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━╸━━━━━━━━━━━━━━━╸━━━       0 openssl                    1.4s[+] 1.7s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━╸━━━━━━━━━━━━━━━╸━━       0 openssl                    1.5s[+] 1.8s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━╸━━━━━━━━━━━━━━━╸━       0 beautifulsoup4             1.6s[+] 1.9s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━╸━━━━━━━━━━━━━━━━       0 beautifulsoup4             1.7s[+] 2.0s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (4) ━━━━━━━━╸━━━━━━━━━━━━━━       0 beautifulsoup4             1.8s[+] 2.1s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (3) ━━━━╸━━━━━━━━━━━━━━━━━━       1 beautifulsoup4             1.9s[+] 2.2s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (2) ━━━━━━━━━━╸━━━━━━━━━━━━       2 ca-certificates            2.0s[+] 2.3s
Downloading      ━━━━━━━━━━━━━━━━━━━━━━━   4.1MB                            0.3s
Extracting   (1) ━━━━━━━━━━━━━━━━╸━━━━━━       3 openssl                    2.1s
Downloading and Extracting Packages

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
Collecting nbformat==4.2.0
  Downloading nbformat-4.2.0-py2.py3-none-any.whl (153 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 153.3/153.3 kB 20.2 MB/s eta 0:00:00
Requirement already satisfied: ipython-genutils in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from nbformat==4.2.0) (0.2.0)
Requirement already satisfied: jsonschema!=2.5.0,>=2.4 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from nbformat==4.2.0) (4.17.3)
Requirement already satisfied: jupyter-core in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from nbformat==4.2.0) (4.12.0)
Requirement already satisfied: traitlets>=4.1 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from nbformat==4.2.0) (5.9.0)
Requirement already satisfied: attrs>=17.4.0 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from jsonschema!=2.5.0,>=2.4->nbformat==4.2.0) (23.1.0)
Requirement already satisfied: importlib-metadata in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from jsonschema!=2.5.0,>=2.4->nbformat==4.2.0) (4.11.4)
Requirement already satisfied: importlib-resources>=1.4.0 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from jsonschema!=2.5.0,>=2.4->nbformat==4.2.0) (5.12.0)
Requirement already satisfied: pkgutil-resolve-name>=1.3.10 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from jsonschema!=2.5.0,>=2.4->nbformat==4.2.0) (1.3.10)
Requirement already satisfied: pyrsistent!=0.17.0,!=0.17.1,!=0.17.2,>=0.14.0 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from jsonschema!=2.5.0,>=2.4->nbformat==4.2.0) (0.19.3)
Requirement already satisfied: typing-extensions in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from jsonschema!=2.5.0,>=2.4->nbformat==4.2.0) (4.5.0)
Requirement already satisfied: zipp>=3.1.0 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from importlib-resources>=1.4.0->jsonschema!=2.5.0,>=2.4->nbformat==4.2.0) (3.15.0)
Installing collected packages: nbformat
  Attempting uninstall: nbformat
    Found existing installation: nbformat 5.8.0
    Uninstalling nbformat-5.8.0:
      Successfully uninstalled nbformat-5.8.0
ERROR: pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.
jupyter-server 1.24.0 requires nbformat>=5.2.0, but you have nbformat 4.2.0 which is incompatible.
nbclient 0.7.4 requires nbformat>=5.1, but you have nbformat 4.2.0 which is incompatible.
nbconvert 7.4.0 requires nbformat>=5.1, but you have nbformat 4.2.0 which is incompatible.
Successfully installed nbformat-4.2.0
import yfinance as yf
import pandas as pd
import requests
from bs4 import BeautifulSoup
import plotly.graph_objects as go
from plotly.subplots import make_subplots
Define Graphing Function
In this section, we define the function make_graph. You don't have to know how the function works, you should only care about the inputs. It takes a dataframe with stock data (dataframe must contain Date and Close columns), a dataframe with revenue data (dataframe must contain Date and Revenue columns), and the name of the stock.

def make_graph(stock_data, revenue_data, stock):
    fig = make_subplots(rows=2, cols=1, shared_xaxes=True, subplot_titles=("Historical Share Price", "Historical Revenue"), vertical_spacing = .3)
    stock_data_specific = stock_data[stock_data.Date <= '2021--06-14']
    revenue_data_specific = revenue_data[revenue_data.Date <= '2021-04-30']
    fig.add_trace(go.Scatter(x=pd.to_datetime(stock_data_specific.Date, infer_datetime_format=True), y=stock_data_specific.Close.astype("float"), name="Share Price"), row=1, col=1)
    fig.add_trace(go.Scatter(x=pd.to_datetime(revenue_data_specific.Date, infer_datetime_format=True), y=revenue_data_specific.Revenue.astype("float"), name="Revenue"), row=2, col=1)
    fig.update_xaxes(title_text="Date", row=1, col=1)
    fig.update_xaxes(title_text="Date", row=2, col=1)
    fig.update_yaxes(title_text="Price ($US)", row=1, col=1)
    fig.update_yaxes(title_text="Revenue ($US Millions)", row=2, col=1)
    fig.update_layout(showlegend=False,
    height=900,
    title=stock,
    xaxis_rangeslider_visible=True)
    fig.show()
Question 1: Use yfinance to Extract Stock Data
Using the Ticker function enter the ticker symbol of the stock we want to extract data on to create a ticker object. The stock is Tesla and its ticker symbol is TSLA.

tesla = yf.Ticker('TSLA')
Using the ticker object and the function history extract stock information and save it in a dataframe named tesla_data. Set the period parameter to max so we get information for the maximum amount of time.

tesla_data = tesla.history(period="max")
Reset the index using the reset_index(inplace=True) function on the tesla_data DataFrame and display the first five rows of the tesla_data dataframe using the head function. Take a screenshot of the results and code from the beginning of Question 1 to the results below.

tesla_data.reset_index(inplace=True)
tesla_data.head(5)
Date	Open	High	Low	Close	Volume	Dividends	Stock Splits
0	2010-06-29	1.266667	1.666667	1.169333	1.592667	281494500	0	0.0
1	2010-06-30	1.719333	2.028000	1.553333	1.588667	257806500	0	0.0
2	2010-07-01	1.666667	1.728000	1.351333	1.464000	123282000	0	0.0
3	2010-07-02	1.533333	1.540000	1.247333	1.280000	77097000	0	0.0
4	2010-07-06	1.333333	1.333333	1.055333	1.074000	103003500	0	0.0
Question 2: Use Webscraping to Extract Tesla Revenue Data
Use the requests library to download the webpage https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm Save the text of the response as a variable named html_data.

url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm"
html_data = requests.get(url).text
Parse the html data using beautiful_soup.

import requests
from bs4 import BeautifulSoup
​
url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm"
html_data = requests.get(url).text
​
# Parse the HTML data using BeautifulSoup with 'html.parser' (or 'lxml')
soup = BeautifulSoup(html_data, "html.parser")
​
# Print the prettified version of the HTML data
print(soup.prettify())
​
​
<!DOCTYPE html>
<!--[if lt IE 7]>      <html class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if IE 7]>         <html class="no-js lt-ie9 lt-ie8"> <![endif]-->
<!--[if IE 8]>         <html class="no-js lt-ie9"> <![endif]-->
<!--[if gt IE 8]><!-->
<html class="no-js">
 <!--<![endif]-->
 <head>
  <meta charset="utf-8"/>
  <meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible"/>
  <link href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue" rel="canonical"/>
  <title>
   Tesla Revenue 2010-2022 | TSLA | MacroTrends
  </title>
  <meta content="Tesla annual/quarterly revenue history and growth rate from 2010 to 2022. Revenue can be defined as the amount of money a company receives from its customers in exchange for the sales of goods or services.  Revenue is the top line item on an income statement from which all costs and expenses are subtracted to arrive at net income.    
				
				&lt;ul style='margin-top:10px;'&gt;
				&lt;li&gt;Tesla revenue for the quarter ending September 30, 2022 was &lt;strong&gt;$21.454B&lt;/strong&gt;, a &lt;strong&gt;55.95% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla revenue for the twelve months ending September 30, 2022 was &lt;strong&gt;$74.863B&lt;/strong&gt;, a &lt;strong&gt;59.8% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2021 was &lt;strong&gt;$53.823B&lt;/strong&gt;, a &lt;strong&gt;70.67% increase&lt;/strong&gt; from 2020.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2020 was &lt;strong&gt;$31.536B&lt;/strong&gt;, a &lt;strong&gt;28.31% increase&lt;/strong&gt; from 2019.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2019 was &lt;strong&gt;$24.578B&lt;/strong&gt;, a &lt;strong&gt;14.52% increase&lt;/strong&gt; from 2018.&lt;/li&gt;
				&lt;/ul&gt;" name="description">
   <meta content="" name="robots">
    <link href="/assets/images/icons/FAVICON/macro-trends_favicon.ico" rel="shortcut icon" type="image/x-icon"/>
    <meta content="1228954C688F5907894001CD8E5E624B" name="msvalidate.01"/>
    <meta content="6MnD_3iDtAP1ZyoGK1YMyVIVck4r5Ws80I9xD3ue4_A" name="google-site-verification"/>
    <!-- Load in Roboto Font -->
    <link href="https://fonts.googleapis.com/css?family=Roboto:400,600,700" rel="stylesheet"/>
    <!-- Bootstrap -->
    <link href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet"/>
    <!--for Bootstrap CDN version-->
    <link href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap-theme.min.css" rel="stylesheet"/>
    <!-- Font Awesome -->
    <link href="//stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet"/>
    <!--for Font Awesome CDN version-->
    <!-- Jquery, Bootstrap and Menu Javascript -->
    <script crossorigin="anonymous" integrity="sha256-ZosEbRLbNQzLpnKIkEdrPv7lOy9C27hHQ+Xp8a4MxAQ=" src="//code.jquery.com/jquery-1.12.4.min.js">
    </script>
    <script src="//maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js">
    </script>
    <!-- Modernizr for cross-browser support -->
    <script src="/assets/javascript/modernizr-2.6.2-respond-1.1.0.min.js" type="text/javascript">
    </script>
    <!-- Latest compiled and minified CSS -->
    <link href="//www.fuelcdn.com/fuelux/3.13.0/css/fuelux.min.css" rel="stylesheet"/>
    <!-- Latest compiled and minified JavaScript -->
    <script src="//www.fuelcdn.com/fuelux/3.13.0/js/fuelux.min.js">
    </script>
    <!-- Twitter Card data -->
    <meta content="summary_large_image" name="twitter:card"/>
    <meta content="@tmacrotrends" name="twitter:site"/>
    <meta content="Tesla Revenue 2010-2022 | TSLA" name="twitter:title"/>
    <meta content="Tesla annual/quarterly revenue history and growth rate from 2010 to 2022. Revenue can be defined as the amount of money a company receives from its customers in exchange for the sales of goods or services.  Revenue is the top line item on an income statement from which all costs and expenses are subtracted to arrive at net income.    
				
				&lt;ul style='margin-top:10px;'&gt;
				&lt;li&gt;Tesla revenue for the quarter ending September 30, 2022 was &lt;strong&gt;$21.454B&lt;/strong&gt;, a &lt;strong&gt;55.95% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla revenue for the twelve months ending September 30, 2022 was &lt;strong&gt;$74.863B&lt;/strong&gt;, a &lt;strong&gt;59.8% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2021 was &lt;strong&gt;$53.823B&lt;/strong&gt;, a &lt;strong&gt;70.67% increase&lt;/strong&gt; from 2020.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2020 was &lt;strong&gt;$31.536B&lt;/strong&gt;, a &lt;strong&gt;28.31% increase&lt;/strong&gt; from 2019.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2019 was &lt;strong&gt;$24.578B&lt;/strong&gt;, a &lt;strong&gt;14.52% increase&lt;/strong&gt; from 2018.&lt;/li&gt;
				&lt;/ul&gt;" name="twitter:description"/>
    <!-- Open Graph data -->
    <meta content="https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue" property="og:url">
     <meta content="Tesla Revenue 2010-2022 | TSLA" property="og:title">
      <meta content="Tesla annual/quarterly revenue history and growth rate from 2010 to 2022. Revenue can be defined as the amount of money a company receives from its customers in exchange for the sales of goods or services.  Revenue is the top line item on an income statement from which all costs and expenses are subtracted to arrive at net income.    
				
				&lt;ul style='margin-top:10px;'&gt;
				&lt;li&gt;Tesla revenue for the quarter ending September 30, 2022 was &lt;strong&gt;$21.454B&lt;/strong&gt;, a &lt;strong&gt;55.95% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla revenue for the twelve months ending September 30, 2022 was &lt;strong&gt;$74.863B&lt;/strong&gt;, a &lt;strong&gt;59.8% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2021 was &lt;strong&gt;$53.823B&lt;/strong&gt;, a &lt;strong&gt;70.67% increase&lt;/strong&gt; from 2020.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2020 was &lt;strong&gt;$31.536B&lt;/strong&gt;, a &lt;strong&gt;28.31% increase&lt;/strong&gt; from 2019.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2019 was &lt;strong&gt;$24.578B&lt;/strong&gt;, a &lt;strong&gt;14.52% increase&lt;/strong&gt; from 2018.&lt;/li&gt;
				&lt;/ul&gt;" property="og:description">
       <!-- JQXGRID STYLES AND JAVASCRIPT -->
       <link href="/assets/php/jqfiles/jqwidgets/styles/jqx.base.css" rel="stylesheet" type="text/css">
        <link href="/assets/php/jqfiles/jqwidgets/styles/jqx.bootstrap.css" rel="stylesheet" type="text/css">
         <!-- LOAD THESE SCRIPTS EARLY SO THE TICKER INPUT FIELD IS STYLED INSTANTLY -->
         <script src="/assets/php/jqfiles/jqwidgets/jqxcore.js" type="text/javascript">
         </script>
         <script src="/assets/php/jqfiles/jqwidgets/jqxdata.js" type="text/javascript">
         </script>
         <script src="/assets/php/jqfiles/jqwidgets/jqxinput.js" type="text/javascript">
         </script>
         <!-- Styling for search box -->
         <link href="/assets/php/jquery-typeahead/jquery.typeahead_pages.css" rel="stylesheet" type="text/css"/>
         <!-- Search box javascript -->
         <script src="/assets/php/jquery-typeahead/jquery.typeahead.min.js">
         </script>
         <link href="//cdnjs.cloudflare.com/ajax/libs/select2/4.0.3/css/select2.min.css" rel="stylesheet">
          <script src="//cdnjs.cloudflare.com/ajax/libs/select2/4.0.3/js/select2.min.js">
          </script>
          <!-- ToolTips -->
          <script src="/assets/php/tipped-4.6.1/js/tipped/tipped.js">
          </script>
          <link href="/assets/php/tipped-4.6.1/css/tipped/tipped.css" rel="stylesheet"/>
          <!-- START IC AD INSERT -->
          <script>
           InvestingChannelQueue = window.InvestingChannelQueue || [];
          </script>
          <script async="" src="https://u5.investingchannel.com/static/uat.js">
          </script>
          <script type="text/javascript">
           //Push Run command with the API-Key, so that UAT will start processing publishers request.
        InvestingChannelQueue.push(function() {
            ic_page = InvestingChannel.UAT.Run("df17ac1e-cc7f-11e8-82a5-0abbb61c4a6a");        
        });
		
		var tickerValue = 'TSLA';			
        var oopDivTag;
		var subLeaderboardTag;
		var rightSidebarTag1;
		var rightSidebarTag2;
		var searchButtonTag;
		var partner_center_tag;
		var videoTag;
		var ic_3x7_1;
 		//var IC_D_300x250_BCC;
		//var IC_D_3x7_BCC;
   
        //To define new tags/out of page tags.
        InvestingChannelQueue.push(function() {
			
			ic_page.setKval({'t': tickerValue});
			
            //videoTag = ic_page.defineNativeTag("Macrotrends/fundamentalanalysis","3x6, 728x90, Fluid","IC_D_3x6",35);
			
            oopDivTag = ic_page.defineOutOfPageTag("Macrotrends/fundamentalanalysis","oopDivTag_1");
			oopDivTag.setKval({"adslot":"IC_OOP_1"});
            
			
			LeaderboardTag = ic_page.defineTag("Macrotrends/fundamentalanalysis","970x250,728x90,970x90,fluid", "IC_D_970x250_1");
			LeaderboardTag.setKval({"adslot":"IC_D_970x250_1"});


			subLeaderboardTag = ic_page.defineTag("Macrotrends/fundamentalanalysis","728x90","ic_728x90_1");
			subLeaderboardTag.setKval({"adslot":"IC_728x90_1"});
			
			
			rightSidebarTag1 = ic_page.defineTag("Macrotrends/fundamentalanalysis","300x250,Fluid","ic_300x250_1");
			rightSidebarTag1.setKval({"adslot":"IC_300x250_1"});
			
			
			rightSidebarTag2 = ic_page.defineTag("Macrotrends/fundamentalanalysis","300x600,300x250,160x600,300x1050,Fluid","ic_300x600_1");
			rightSidebarTag2.setKval({"adslot":"IC_300x600_1"});
			
			
			searchButtonTag = ic_page.defineTag("Macrotrends/fundamentalanalysis","88x31","ic_88x31_1");
			searchButtonTag.setKval({"pc":"pc","adslot":"IC_88x31"});
			
			partner_center_tag = ic_page.defineTag("macrotrends/fundamentalanalysis","728x214, 728x90","IC_728x214_1");
			partner_center_tag.setKval({"pc":"pc","adslot":"d_728x90_2"});

			ic_3x7_1 = ic_page.defineNativeTag("macrotrends/fundamentalanalysis","3x7,728x90,Fluid","IC_3x7_1", 35);
			
			//IC_D_300x250_BCC = ic_page.defineTag(adCategory,"300x250,Fluid","IC_D_300x250_BCC");
			//IC_D_300x250_BCC.setKval({"adslot":"IC_D_300x250_BCC"});

			//IC_D_3x7_BCC = ic_page.defineTag(adCategory,"3x7, Fluid","IC_D_3x7_BCC");
			//IC_D_3x7_BCC.setKval({"adslot":"IC_D_3x7_BCC"});
			

        });
    
        //To render tags.
			InvestingChannelQueue.push(function() {
            ic_page.renderTags();
        });
          </script>
          <!-- END IC AD INSERT -->
          <!-- Global site tag (gtag.js) - Google Analytics -->
          <script async="" src="https://www.googletagmanager.com/gtag/js?id=UA-62099500-1">
          </script>
          <script>
           window.dataLayer = window.dataLayer || [];
		  function gtag(){dataLayer.push(arguments);}
		  gtag('js', new Date());

		  gtag('config', 'UA-62099500-1');
          </script>
          <!-- Google tag (gtag.js) -->
          <script async="" src="https://www.googletagmanager.com/gtag/js?id=G-3KL0LYERBH">
          </script>
          <script>
           window.dataLayer = window.dataLayer || [];
		  function gtag(){dataLayer.push(arguments);}
		  gtag('js', new Date());

		  gtag('config', 'G-3KL0LYERBH');
          </script>
          <!--<script>
			(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
			(i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
			m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
			})(window,document,'script','//www.google-analytics.com/analytics.js','ga');

			ga('create', 'UA-62099500-1', 'auto');
			ga('send', 'pageview');
			
			
			
		   
			//Send one event to GA at 30 seconds to control bounce rate
			setTimeout("ga('send','event','Engaged User','30 Second Engagement')",30000); 


		  //This code sends events to ga every 30 seconds when the window is in focus
			var count = 0;
			var myInterval;
					
			// Active
			window.addEventListener('load', startTimer);
			window.addEventListener('focus', startTimer);

			// Inactive
			window.addEventListener('blur', stopTimer);

			function timerHandler() {
				count++;
				
				if(count % 60 == 0 && count <= 1800) {
					
					var interval = (count/60);
					interval = interval.toFixed(0);
					
					var action = interval + " Minute Engagement";
					
					ga('send','event','Engaged User',action);

					
				}
			
			}

			// Start timer
			function startTimer() {
			myInterval = window.setInterval(timerHandler, 1000);
			}

			// Stop timer
			function stopTimer() {
			window.clearInterval(myInterval);
			}
			
			

		</script>-->
          <style>
           #style-1::-webkit-scrollbar-track
{
	-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3);
	border-radius: 3px;
	background-color: #F5F5F5;
}

#style-1::-webkit-scrollbar
{
	width: 18px;
	background-color: #F5F5F5;
}

#style-1::-webkit-scrollbar-thumb
{
	border-radius: 3px;
	-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3);
	background-color: #5B9BD5;
}

html {
	width:100%;
	position: relative;
	min-height: 100%;
}

body {
	
	width:100%;

	/* Margin bottom by footer height */
	  margin-bottom: 80px;
	  color: #444;
	  background-color:#fff;
	  font-family: 'Roboto', sans-serif;
	  font-size:14px;
}





.header_content_container {
	
	min-width: 1280px;
	padding: 0px;
}

.main_content_container {
	
	min-width: 1280px;
	max-width: 1280px;
	padding: 0px 30px 100px 30px;
	
}

.sub_main_content_container {
	
	
}



#main_content {
	
	padding:0px 20px 0px 0px;
	width:826px;
    float:left;
	
}

#right_sidebar {
	
  width: 300px;
  float:left;
  height:3200px;
	
}

#sticky_ad_left {
	
  position: -webkit-sticky;
  position: sticky;
  top: 30px;
	
	
}

#sticky_ad_right {
	
  position: -webkit-sticky;
  position: sticky;
  top: 30px;
	
	
}





.footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  /* Set the fixed height of the footer here */
  height: 100px;
  margin-top: 10px;	
  padding: 30px 20px 20px 20px;
  color:#fff !important;
  background-color:#444;
  text-align: center;
  font-size:16px;
}

.footer a {
  color:#fff !important;
}

.ticker_search_box {
	
	background-color:#F5F5F5;
	border: 1px solid #E0E0E0;
	border-bottom:none;
	padding:10px 30px 10px 10px;
	margin:0px 0px 0px 0px;
	text-align:center;
	
}

.related_tickers {
	
	width:100%;
	background-color:#F5F5F5;
	border: 1px solid #E0E0E0;
	border-top: 0px;
	padding:3px 30px 3px 10px;
	margin:0px 0px 0px 0px;
	text-align:center;
	
}

.statement_type_select {

	width:100%;
	height:28px;
	
}

.frequency_select {

	width:100%;
	height:28px;
	font-weight:600;
	
}


.select2 {
	
	text-align:left;
	font-weight:600;
	
	}
	
#jqxInput {

		width:100%;
		height:28px;
		
}



.header__parent_container {

	width:100%;
	height:50px;
	padding:15px 0px 10px -20px; 
	margin:0px 0px 0px 0px;
	background-color:#444;

}

.header_container {

	width:100%;
	height:50px;
	padding:15px 0px 10px -20px; 
	margin:0px 0px 0px 0px;
	background-color:#444;

}

.header_logo {
	
	padding-top:10px;
	margin-left:50px;
	
}

.menu_parent_container {
	
	width:100%;
	height:34px;
	font-size:16px;
	padding:15px 0px 10px -20px; 
	margin:0px 0px 0px 0px;
	background-color:#0089de;
}

.menu_container {
	
	width:1280px;
	height:34px;
	font-size:16px;
	padding:11px 0px 0px -20px; 
	margin: 0 auto;
	background-color:#0089de;
	z-index:1000;
}

.menu_item {

	height:34px;
	float:left;
	font-size:14px;
	font-weight:bold;
	color:#fff;
	text-align:center;
	padding:7px 16px 0px 16px;	

}

.menu_item:hover
{
	background-color:#32a0e4;
	cursor: pointer;
}

.menu_item a
{
	color:#fff;
	cursor: pointer;
}

.menu_item a:hover
{
	text-decoration:none;
	cursor: pointer;
}

.leaderboard_ad {

	margin-top:20px;
	margin-bottom:20px;
	text-align:center;
	min-height:100px;

}

#filter_result_count {
	
	width:100%;
	text-align:center;
	font-size:24px;
	font-weight:bold;
	padding:10px 15px;
	background-color:#efefef;
	border: 1px solid #dfdfdf;
	margin:20px;
	
}


select {
  color: #444;
  background-color: #FFF;
  border: 1px solid #AAA;
  border-radius: 4px;
  box-sizing: border-box;
  cursor: pointer;
  display: block;
  height:40px;
  line-height: 40px;
}

.historical_data_table  {
    table-layout: fixed;
	margin:20px;
}

.historical_data_table tbody tr td {
	
	padding:6px;
	vertical-align: middle !important;

}


.descriptors {
	
	text-align:center;
	font-size:14px;
	padding:15px;
	
}

.td_metric_name {
	
	width:110px;
	padding-top:17px;
	
}

.metric_link {
	
	font-size:14px;
	font-weight:bold;

}

.help_icon {
	
	width:15px;
	height:18px; 
	padding-bottom:3px;
	
}

.td_min_value {
	
	width:75px;
	text-align:center;
	font-size:13px;
	
}

.td_max_value {
	
	width:75px;
	text-align:center;
	font-size:13px;
	
}

#myCombobox .form-control {
	
	background-color: #99d5ff;

	
}

.dropdown-toggle {
	
	height:24px;
	padding-top:0px;
	padding-left:7px;
	width:24px;
	
}

.dropdown-menu-right {
	
	min-width:75px;
	font-size:13px;
	
}

.form-control {
	
	font-size:12px;	
	padding:5px 10px;
	height:24px;

	
}

#myPills1 {
	
	margin:0px 15px 10px 0px;
	
}

#jqxgrid {
	
	border-radius:0px;
	
}

.jqx-widget-header {
	
    font-family: 'Roboto', sans-serif;
	font-size:13px;	
	
}

.jqx-item {
	
    font-family: 'Roboto', sans-serif;
	font-size: 13px;
	
}

.jqx-widget-content {
	
	border-color: #E0E0E0;
	
}

#jqxgrid .jqx-grid-cell {
	
	border-color: #E0E0E0;
	
}

#jqxgrid .jqx-grid-cell-pinned {
	
	border-color: #E0E0E0;
	background-color: #F5F5F5;
	
}

#jqxgrid .jqx-grid-column-header {
	
	border-color: #E0E0E0;
	background-color: #F5F5F5;
	
}

.clear_zero {

	height:0px;

}



/* Styles for Popup Charts */

.tpd-size-large {
	
	margin:0px;	
	padding: 0px;
}

.popup_window_wrapper {
	
	margin:15px;
	
}

.popup_stock_name {

	font-size:16px;
	font-weight:bold;
	margin:5px;

}

.popup_stock_attributes {

	font-size:13px;
	font-weight:bold;
	margin:5px;

}

.popup_stock_description {

	font-size:12px;
	margin:5px;

}

.jqx-input {
	
	font-size:14px;
	
} 

.jqx-menu-item {
	
	font-size:14px;
	
}

.jqx-input {
	
	padding:5px 10px;
	
}

.nav-tabs {
    border: 1px solid #E0E0E0;
	background-color:#F5F5F5;
	padding: 3px 5px 0px 5px;
	margin: 0px 0px 10px 0px;
}

.nav-tabs>li>a {
	font-size:13px;
	padding:7px 11px;
	font-weight:600;
    margin-right: 0px;
    line-height: 1.42857143;
    border: 0px;
    border-radius: 0px 0px 0 0;
	background-color:#F5F5F5;

}

.nav-tabs>li>a .active {
    margin-right: 0px;
    line-height: 1.42857143;
    border: 1px solid #E0E0E0;
    border-radius: 0px 0px 0 0;
	background-color:#F5F5F5;

}

.nav-tabs>li>a:hover { 
    background-color: #F5F5F5;
	text-decoration: underline;

}

.donate_buttons {

	margin-left:20px;
	
	}

.modal-body {

	margin:10px 40px 20px 40px;
	text-align:left;
	font-size:18px;

}

.modal-body li {

	margin-top:20px;
	font-size:14px;

}


.modal_title {


	text-align:center;
	margin-bottom:30px;

}

.modal-body th{

	margin-left:10px;
	font-size:14px;
}

.modal-body td {

	color: #337ab7;
	margin-left:10px;
	font-size:14px;
}

.modal_button {

	margin-top:50px;
	text-align:center;
	font-size:16px;

}
          </style>
         </link>
        </link>
       </link>
      </meta>
     </meta>
    </meta>
   </meta>
  </meta>
 </head>
 <body class="fuelux">
  <!--[if lt IE 7]>
            <p class="browsehappy">You are using an <strong>outdated</strong> browser. Please <a href="https://browsehappy.com/">upgrade your browser</a> to improve your experience.</p>
        <![endif]-->
  <div class="header_content_container container-fluid">
   <div class="header_parent_container">
    <div class="header_container">
     <div class="header_logo col-xs-2">
      <a class="logo" href="https://www.macrotrends.net" title="MacroTrends Home Page">
       <img src="/assets/images/logo_bright1.png"/>
      </a>
     </div>
     <div class="col-xs-1 pull-right" style="padding-top:8px; margin-right:10px; margin-left:0px; padding-left:0px;">
      <div id="ic_88x31_1">
      </div>
     </div>
     <div class="col-xs-5 pull-right" style="padding-top:8px;">
      <form>
       <div class="typeahead__container">
        <div class="typeahead__field">
         <span class="typeahead__query">
          <input autocomplete="off" autofocus="" class="js-typeahead" name="q" placeholder="Search over 200,000 charts..." type="search"/>
         </span>
         <span class="typeahead__button">
          <button type="submit">
           <span class="typeahead__search-icon">
           </span>
          </button>
         </span>
        </div>
       </div>
      </form>
     </div>
    </div>
   </div>
   <div class="menu_parent_container">
    <div class="menu_container">
     <a href="/stocks/stock-screener">
      <div class="menu_item">
       Stock Screener
      </div>
     </a>
     <a href="/stocks/research">
      <div class="menu_item">
       Stock Research
      </div>
     </a>
     <a href="/charts/stock-indexes">
      <div class="menu_item">
       Market Indexes
      </div>
     </a>
     <a href="/charts/precious-metals">
      <div class="menu_item">
       Precious Metals
      </div>
     </a>
     <a href="/charts/energy">
      <div class="menu_item">
       Energy
      </div>
     </a>
     <a href="/charts/commodities">
      <div class="menu_item">
       Commodities
      </div>
     </a>
     <a href="/charts/exchange-rates">
      <div class="menu_item">
       Exchange Rates
      </div>
     </a>
     <a href="/charts/interest-rates">
      <div class="menu_item">
       Interest Rates
      </div>
     </a>
     <a href="/charts/economy">
      <div class="menu_item">
       Economy
      </div>
     </a>
     <a href="/countries/topic-overview">
      <div class="menu_item">
       Global Metrics
      </div>
     </a>
    </div>
   </div>
  </div>
  <div class="main_content_container container-fluid" id="main_content_container">
   <div class="adx_top_ad col-xs-12" id="ic_leaderboard" style="margin: 20px 20px 30px 20px; min-height:265px; text-align:center;">
    <div id="IC_D_970x250_1">
    </div>
    <!--Smartad # 4058: Macrotrends - 970x250 Image - Placement 2-->
    <!--<iframe id="dianomi_leaderboard" WIDTH="970" HEIGHT="250" SCROLLING="NO" src="//www.dianomi.com/smartads.epl?id=4058"  style="height: 250px; border: none; overflow: hidden;"></iframe>-->
   </div>
   <div style="margin:20px 20px 20px 5px;">
    <h2 style="margin-left:0px; font-weight:600; color:#444;">
     Tesla Revenue 2010-2022 | TSLA
    </h2>
   </div>
   <div class="sub_main_content_container">
    <div id="main_content">
     <div class="navigation_tabs" style="margin-bottom:20px;">
      <ul class="nav nav-tabs" id="myTabs" style="font-size:15px;">
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/stock-price-history">
         Prices
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/financial-statements">
         Financials
        </a>
       </li>
       <li class="active">
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue">
         Revenue &amp; Profit
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/total-assets">
         Assets &amp; Liabilities
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/profit-margins">
         Margins
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/pe-ratio">
         Price Ratios
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/current-ratio">
         Other Ratios
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/dividend-yield-history">
         Other Metrics
        </a>
       </li>
      </ul>
      <ul class="nav nav-tabs" id="myTabs" style="font-size:15px;">
       <li class="active">
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue">
         Revenue
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/gross-profit">
         Gross Profit
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/operating-income">
         Operating Income
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/ebitda">
         EBITDA
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/net-income">
         Net Income
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/eps-earnings-per-share-diluted">
         EPS
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/shares-outstanding">
         Shares Outstanding
        </a>
       </li>
      </ul>
     </div>
     <div style="background-color:#fff; margin: 0px 0px 20px 0px; padding:20px 30px; border:1px solid #dfdfdf;">
      <span style="color:#444; line-height: 1.8;">
       Tesla annual/quarterly revenue history and growth rate from 2010 to 2022. Revenue can be defined as the amount of money a company receives from its customers in exchange for the sales of goods or services.  Revenue is the top line item on an income statement from which all costs and expenses are subtracted to arrive at net income.
       <ul style="margin-top:10px;">
        <li>
         Tesla revenue for the quarter ending September 30, 2022 was
         <strong>
          $21.454B
         </strong>
         , a
         <strong>
          55.95% increase
         </strong>
         year-over-year.
        </li>
        <li>
         Tesla revenue for the twelve months ending September 30, 2022 was
         <strong>
          $74.863B
         </strong>
         , a
         <strong>
          59.8% increase
         </strong>
         year-over-year.
        </li>
        <li>
         Tesla annual revenue for 2021 was
         <strong>
          $53.823B
         </strong>
         , a
         <strong>
          70.67% increase
         </strong>
         from 2020.
        </li>
        <li>
         Tesla annual revenue for 2020 was
         <strong>
          $31.536B
         </strong>
         , a
         <strong>
          28.31% increase
         </strong>
         from 2019.
        </li>
        <li>
         Tesla annual revenue for 2019 was
         <strong>
          $24.578B
         </strong>
         , a
         <strong>
          14.52% increase
         </strong>
         from 2018.
        </li>
       </ul>
      </span>
     </div>
     <div style="background-color:#fff; margin: 30px 0px 30px 0px; text-align:center; min-height:90px;">
      <div id="ic_728x90_1" style="margin:10px 20px;">
      </div>
     </div>
     <div class="ticker_search_box" style="text-align:center;">
      <div style="width:400px; margin-left:20px; border-bottom:none;">
       <script type="text/javascript">
        $(document).ready(function () {
				                
					var url = "https://www.macrotrends.net/assets/php/ticker_search_list.php";
				
                // prepare the data
                var source =
                {
                    datatype: "json",
                    datafields: [
                        { name: 'n' },
						{ name: 's'}
                    ],
                    url: url
                };
                var dataAdapter = new $.jqx.dataAdapter(source);
                // Create a jqxInput
                $("#jqxInput").jqxInput({ source: dataAdapter, minLength: 1, placeHolder: "Search for ticker or company name...", items: 20, searchMode: 'containsignorecase', displayMember: "n", valueMember: "s", width: '100%', height: 22, theme: 'bootstrap'});
                $("#jqxInput").on('select', function (event) {
                    if (event.args) {
                        var item = event.args.item;
						
						//Have to split the ticker and slug back out since jqxinput only seems to allow one data value
						var itemArray = item.value.split("\/"); 
						var ticker = itemArray[0];
						var slug = itemArray[1];
                        if (item) {
							
														
								window.location = "https://www.macrotrends.net/stocks/charts/" + ticker + "/" + slug + "/revenue";
							
							                        }
                    }
                });
            });
       </script>
       <input autocomplete="off" id="jqxInput">
       </input>
      </div>
      <div style="width:280px; margin-top: -32px; margin-left:80px; border-bottom:none; float:right;">
       <button class="chart_buttons btn btn-success btn-sm" id="compareStocks" style="margin-right:15px;">
        <span class="glyphicon glyphicon-stats">
        </span>
        <strong>
         Compare TSLA With Other Stocks
        </strong>
       </button>
      </div>
     </div>
     <div style="height:690px; background-color:#fff; border:1px solid #dfdfdf;">
      <iframe frameborder="0" height="680" hspace="0" id="chart_iframe" margin="0px" marginheight="0" marginwidth="0" scrolling="NO" src="https://www.macrotrends.net/assets/php/fundamental_iframe.php?t=TSLA&amp;type=revenue&amp;statement=income-statement&amp;freq=Q" title="Interactive chart: Tesla Revenue 2010-2022 | TSLA" valign="middle" vspace="0" width="800">
      </iframe>
     </div>
     <div id="ic_video_ad" style="height:317px; margin:30px;">
      <div id="IC_D_3x6">
      </div>
     </div>
     <div style="background-color:#fff; margin: 30px 0px; padding:10px 30px; border:1px solid #dfdfdf;">
      <iframe frameborder="0" height="300" hspace="0" id="dianomi_below_chart" marginheight="0" marginwidth="0" scrolling="NO" src="//www.dianomi.com/smartads.epl?id=4057" valign="middle" vspace="0" width="100%">
      </iframe>
      <!--<div id="IC_D_3x7_BCC"></div>-->
     </div>
     <div id="style-1" style="background-color:#fff; height:510px; overflow:auto; margin: 30px 0px 30px 0px; padding:0px 30px 20px 0px; border:1px solid #dfdfdf;">
      <div class="col-xs-6">
       <table class="historical_data_table table">
        <thead>
         <tr>
          <th colspan="2" style="text-align:center">
           Tesla Annual Revenue
           <br/>
           <span style="font-size:14px;">
            (Millions of US $)
           </span>
          </th>
         </tr>
        </thead>
        <tbody>
         <tr>
          <td style="text-align:center">
           2021
          </td>
          <td style="text-align:center">
           $53,823
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2020
          </td>
          <td style="text-align:center">
           $31,536
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2019
          </td>
          <td style="text-align:center">
           $24,578
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2018
          </td>
          <td style="text-align:center">
           $21,461
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2017
          </td>
          <td style="text-align:center">
           $11,759
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2016
          </td>
          <td style="text-align:center">
           $7,000
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2015
          </td>
          <td style="text-align:center">
           $4,046
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2014
          </td>
          <td style="text-align:center">
           $3,198
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2013
          </td>
          <td style="text-align:center">
           $2,013
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2012
          </td>
          <td style="text-align:center">
           $413
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2011
          </td>
          <td style="text-align:center">
           $204
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2010
          </td>
          <td style="text-align:center">
           $117
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2009
          </td>
          <td style="text-align:center">
           $112
          </td>
         </tr>
        </tbody>
       </table>
      </div>
      <div class="col-xs-6">
       <table class="historical_data_table table">
        <thead>
         <tr>
          <th colspan="2" style="text-align:center">
           Tesla Quarterly Revenue
           <br/>
           <span style="font-size:14px;">
            (Millions of US $)
           </span>
          </th>
         </tr>
        </thead>
        <tbody>
         <tr>
          <td style="text-align:center">
           2022-09-30
          </td>
          <td style="text-align:center">
           $21,454
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2022-06-30
          </td>
          <td style="text-align:center">
           $16,934
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2022-03-31
          </td>
          <td style="text-align:center">
           $18,756
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2021-12-31
          </td>
          <td style="text-align:center">
           $17,719
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2021-09-30
          </td>
          <td style="text-align:center">
           $13,757
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2021-06-30
          </td>
          <td style="text-align:center">
           $11,958
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2021-03-31
          </td>
          <td style="text-align:center">
           $10,389
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2020-12-31
          </td>
          <td style="text-align:center">
           $10,744
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2020-09-30
          </td>
          <td style="text-align:center">
           $8,771
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2020-06-30
          </td>
          <td style="text-align:center">
           $6,036
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2020-03-31
          </td>
          <td style="text-align:center">
           $5,985
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2019-12-31
          </td>
          <td style="text-align:center">
           $7,384
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2019-09-30
          </td>
          <td style="text-align:center">
           $6,303
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2019-06-30
          </td>
          <td style="text-align:center">
           $6,350
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2019-03-31
          </td>
          <td style="text-align:center">
           $4,541
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2018-12-31
          </td>
          <td style="text-align:center">
           $7,226
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2018-09-30
          </td>
          <td style="text-align:center">
           $6,824
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2018-06-30
          </td>
          <td style="text-align:center">
           $4,002
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2018-03-31
          </td>
          <td style="text-align:center">
           $3,409
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2017-12-31
          </td>
          <td style="text-align:center">
           $3,288
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2017-09-30
          </td>
          <td style="text-align:center">
           $2,985
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2017-06-30
          </td>
          <td style="text-align:center">
           $2,790
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2017-03-31
          </td>
          <td style="text-align:center">
           $2,696
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2016-12-31
          </td>
          <td style="text-align:center">
           $2,285
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2016-09-30
          </td>
          <td style="text-align:center">
           $2,298
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2016-06-30
          </td>
          <td style="text-align:center">
           $1,270
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2016-03-31
          </td>
          <td style="text-align:center">
           $1,147
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2015-12-31
          </td>
          <td style="text-align:center">
           $1,214
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2015-09-30
          </td>
          <td style="text-align:center">
           $937
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2015-06-30
          </td>
          <td style="text-align:center">
           $955
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2015-03-31
          </td>
          <td style="text-align:center">
           $940
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2014-12-31
          </td>
          <td style="text-align:center">
           $957
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2014-09-30
          </td>
          <td style="text-align:center">
           $852
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2014-06-30
          </td>
          <td style="text-align:center">
           $769
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2014-03-31
          </td>
          <td style="text-align:center">
           $621
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2013-12-31
          </td>
          <td style="text-align:center">
           $615
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2013-09-30
          </td>
          <td style="text-align:center">
           $431
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2013-06-30
          </td>
          <td style="text-align:center">
           $405
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2013-03-31
          </td>
          <td style="text-align:center">
           $562
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2012-12-31
          </td>
          <td style="text-align:center">
           $306
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2012-09-30
          </td>
          <td style="text-align:center">
           $50
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2012-06-30
          </td>
          <td style="text-align:center">
           $27
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2012-03-31
          </td>
          <td style="text-align:center">
           $30
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2011-12-31
          </td>
          <td style="text-align:center">
           $39
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2011-09-30
          </td>
          <td style="text-align:center">
           $58
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2011-06-30
          </td>
          <td style="text-align:center">
           $58
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2011-03-31
          </td>
          <td style="text-align:center">
           $49
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2010-12-31
          </td>
          <td style="text-align:center">
           $36
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2010-09-30
          </td>
          <td style="text-align:center">
           $31
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2010-06-30
          </td>
          <td style="text-align:center">
           $28
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2010-03-31
          </td>
          <td style="text-align:center">
           $21
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2009-12-31
          </td>
          <td style="text-align:center">
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2009-09-30
          </td>
          <td style="text-align:center">
           $46
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2009-06-30
          </td>
          <td style="text-align:center">
           $27
          </td>
         </tr>
        </tbody>
       </table>
      </div>
     </div>
     <div style="background-color:#fff; margin: 0px 0px 20px 0px; padding:5px 50px 5px 10px; border:1px solid #dfdfdf;">
      <table class="historical_data_table table">
       <thead>
        <tr>
         <th style="text-align:center">
          Sector
         </th>
         <th style="text-align:center">
          Industry
         </th>
         <th style="text-align:center">
          Market Cap
         </th>
         <th style="text-align:center">
          Revenue
         </th>
        </tr>
       </thead>
       <tbody>
        <tr>
         <td style="text-align:center">
          <a href="https://www.macrotrends.net/stocks/sector/5/auto-tires-trucks">
           Auto/Tires/Trucks
          </a>
         </td>
         <td style="text-align:center">
          <a href="https://www.macrotrends.net/stocks/industry/7/">
           Auto Manufacturers - Domestic
          </a>
         </td>
         <td style="text-align:center">
          $549.575B
         </td>
         <td style="text-align:center">
          $53.823B
         </td>
        </tr>
        <tr>
         <td colspan="4" style="padding:15px;">
          <span>
           Tesla is the market leader in battery-powered electric car sales in the United States, with roughly 70% market share. The company's flagship Model 3 is the best-selling EV model in the United States. Tesla, which has managed to garner the reputation of a gold standard over the years, is now a far bigger entity that what it started off since its IPO in 2010, with its market cap crossing $1 trillion for the first time in October 2021.? The EV king's market capitalization is more than the combined value of legacy automakers including Toyota, Volkswagen, Daimler, General Motors and Ford.Over the years, Tesla has shifted from developing niche products for affluent buyers to making more affordable EVs for the masses. The firm's three-pronged business model approach of direct sales, servicing, and charging its EVs sets it apart from other carmakers. Tesla, which is touted as the clean energy revolutionary automaker, is much more than just a car manufacturer.
          </span>
         </td>
        </tr>
       </tbody>
      </table>
     </div>
     <div style="background-color:#fff; margin: 20px 0px 30px 0px; padding:5px 50px 5px 10px; border:1px solid #dfdfdf;">
      <table class="historical_data_table table">
       <thead>
        <tr>
         <th style="text-align:center; width:40%;">
          Stock Name
         </th>
         <th style="text-align:center; width:20%;">
          Country
         </th>
         <th style="text-align:center; width:20%;">
          Market Cap
         </th>
         <th style="text-align:center; width:20%;">
          PE Ratio
         </th>
        </tr>
       </thead>
       <tbody>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/GM/general-motors/revenue">
           General Motors (GM)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $53.930B
         </td>
         <td style="text-align:center">
          5.56
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/F/ford-motor/revenue">
           Ford Motor (F)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $52.668B
         </td>
         <td style="text-align:center">
          8.09
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/HOG/harley-davidson/revenue">
           Harley-Davidson (HOG)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $6.762B
         </td>
         <td style="text-align:center">
          9.56
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/PII/polaris/revenue">
           Polaris (PII)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $6.267B
         </td>
         <td style="text-align:center">
          11.86
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/IAA/iaa/revenue">
           IAA (IAA)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $5.134B
         </td>
         <td style="text-align:center">
          16.40
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/FSR/fisker/revenue">
           Fisker (FSR)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $2.261B
         </td>
         <td style="text-align:center">
          0.00
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/LEV/lion-electric/revenue">
           Lion Electric (LEV)
          </a>
         </td>
         <td style="text-align:center">
          Canada
         </td>
         <td style="text-align:center">
          $0.551B
         </td>
         <td style="text-align:center">
          0.00
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/VLTA/volta/revenue">
           Volta (VLTA)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $0.071B
         </td>
         <td style="text-align:center">
          0.00
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/BRDS/bird-global/revenue">
           Bird Global (BRDS)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $0.054B
         </td>
         <td style="text-align:center">
          0.00
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/ZEV/lightning-emotors/revenue">
           Lightning EMotors (ZEV)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $0.043B
         </td>
         <td style="text-align:center">
          0.00
         </td>
        </tr>
       </tbody>
      </table>
     </div>
     <div>
      <!-- Partner Center Ad Unit -->
      <div id="IC_728x214_1" style="width:728px; height:214px; margin-left:30px;">
      </div>
     </div>
    </div>
    <div "="" id="right_sidebar">
     <!--<a href="/stocks/stock-screener" style="text-decoration:none; color: #fff; ">
					<div style="margin:0px; padding: 20px; width:300px; background-color: #01579b; min-height:150px; text-align:center;">

						<h2 style="font-weight:600;">Try our new<br />stock screener!</h2></a>

					</div>
				</a>-->
     <!--<div style="margin-top:0px; min-height:250px;">

					<script src='//ads.investingchannel.com/adtags/Macrotrends/fundamentalanalysis/300x600.js?zhpos=300_2&multi_size=false' type='text/javascript' charset='utf-8'></script>

				</div>-->
     <div style="margin-top:0px; min-height:250px;">
      <div id="ic_300x250_1">
      </div>
     </div>
     <div id="sticky_ad_right" style="margin-top:30px; height:1000px;">
      <script id="dianomi_context_script" src="https://www.dianomi.com/js/contextfeed.js" type="text/javascript">
      </script>
      <div class="dianomi_context" data-dianomi-context-id="743">
      </div>
      <!-- <div id="IC_D_300x250_BCC"></div>-->
      <!--Smartad # 2981: Macrotrends - 300x670 Right Rail-->
      <iframe height="670" id="dianomi_sidebar" scrolling="NO" src="//www.dianomi.com/smartads.epl?id=4059" style="width: 300px; border: none; overflow: hidden;" width="300">
      </iframe>
      <div id="IC_D_300x250_BCC">
      </div>
     </div>
    </div>
   </div>
  </div>
  <!--This is the div for the IC OOP ad-->
  <div id="oopDivTag_1" style="width:1px;height:1px;">
  </div>
  <footer class="footer">
   <span>
    © 2010-2022 Macrotrends LLC
   </span>
   |
   <a href="/terms">
    Terms of Service
   </a>
   |
   <a href="/privacy">
    Privacy Policy
   </a>
   |
   <a href="mailto:%69n%66o@%6Dac%72otrends%2En%65t">
    Contact Us
   </a>
   |
   <a href="/ccpa">
    Do Not Sell My Personal Information
   </a>
   <br/>
   <span>
    Fundamental data from
   </span>
   <a href="https://www.zacksdata.com" rel="nofollow" target="_blank">
    Zacks Investment Research, Inc.
   </a>
  </footer>
  <div aria-hidden="true" aria-labelledby="exampleModalLabel" class="modal" id="smallWidthModal1" role="dialog" tabindex="-1">
   <div class="modal-dialog modal-lg">
    <div class="modal-content">
     <div class="modal-body">
      <div class="modal_title">
       <h2>
        <strong>
         We Need Your Support!
        </strong>
       </h2>
      </div>
      <p>
       Backlinks from other websites are the lifeblood of our site and a primary source of new traffic.
       <p>
        <p>
         If you use our chart images on your site or blog, we ask that you provide attribution via a "dofollow" link back to this page.  We have provided a few examples below that you can copy and paste to your site:
        </p>
        <br/>
        <table class="table">
         <thead>
          <tr>
           <th>
            Link Preview
           </th>
           <th>
            HTML Code (Click to Copy)
           </th>
          </tr>
         </thead>
         <tbody>
          <tr>
           <td>
            <a>
             Tesla Revenue 2010-2022 | TSLA
            </a>
           </td>
           <td>
            <input class="modal_link" size="60" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Tesla Revenue 2010-2022 | TSLA&lt;/a&gt;"/>
           </td>
          </tr>
          <tr>
           <td>
            <a>
             Macrotrends
            </a>
           </td>
           <td>
            <input class="modal_link" size="60" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Macrotrends&lt;/a&gt;"/>
           </td>
          </tr>
          <tr>
           <td>
            <a>
             Source
            </a>
           </td>
           <td>
            <input class="modal_link" size="60" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Source&lt;/a&gt;"/>
           </td>
          </tr>
         </tbody>
        </table>
        <br/>
        <p style="text-align:center">
         Your image export is now complete.  Please check your download folder.
        </p>
       </p>
      </p>
     </div>
     <div class="modal-footer">
      <button class="btn btn-primary" data-dismiss="modal" type="button">
       Close Window
      </button>
     </div>
    </div>
   </div>
  </div>
  <div aria-hidden="true" aria-labelledby="exampleModalLabel" class="modal" id="smallWidthModal2" role="dialog" tabindex="-1">
   <div class="modal-dialog modal-lg">
    <div class="modal-content">
     <div class="modal-body">
      <div class="modal_title">
       <h2>
        <strong>
         We Need Your Support!
        </strong>
       </h2>
      </div>
      <p>
       Backlinks from other websites are the lifeblood of our site and a primary source of new traffic.
       <p>
        <p>
         If you use our datasets on your site or blog, we ask that you provide attribution via a "dofollow" link back to this page.  We have provided a few examples below that you can copy and paste to your site:
        </p>
        <br/>
        <table class="table">
         <thead>
          <tr>
           <th>
            Link Preview
           </th>
           <th>
            HTML Code (Click to Copy)
           </th>
          </tr>
         </thead>
         <tbody>
          <tr>
           <td>
            <a>
             Tesla Revenue 2010-2022 | TSLA
            </a>
           </td>
           <td>
            <input class="modal_link" size="50" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Tesla Revenue 2010-2022 | TSLA&lt;/a&gt;"/>
           </td>
          </tr>
          <tr>
           <td>
            <a>
             Macrotrends
            </a>
           </td>
           <td>
            <input class="modal_link" size="50" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Macrotrends&lt;/a&gt;"/>
           </td>
          </tr>
          <tr>
           <td>
            <a>
             Source
            </a>
           </td>
           <td>
            <input class="modal_link" size="50" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Source&lt;/a&gt;"/>
           </td>
          </tr>
         </tbody>
        </table>
        <br/>
        <p style="text-align:center">
         Your data export is now complete.  Please check your download folder.
        </p>
       </p>
      </p>
     </div>
     <div class="modal-footer">
      <button class="btn btn-primary" data-dismiss="modal" type="button">
       Close Window
      </button>
     </div>
    </div>
   </div>
  </div>
  <script type="text/javascript">
   $.typeahead({
		input: '.js-typeahead',
		minLength: 1,
		filter: false,  //Disables typahead filter to just show everything in the results from the database
		debug: false,
		highlight: true,
		maxItem: 10,
		dynamic: true,
		delay: 200,
		searchOnFocus: true,
		backdrop: {
			"background-color": "#fff"
		},
		href: "{{url}}",
		emptyTemplate: "no result for {{query}}",
		display: ["name"],
		source: {
			users: {
				ajax: {
					url: '/assets/php/all_pages_query.php',
					data: {
						q: '{{query}}'
					}
				}
			}
		}
	});
  </script>
  <script>
   // /*! js-cookie v3.0.0-rc.1 | MIT */
	// !function(e,t){"object"==typeof exports&&"undefined"!=typeof module?module.exports=t():"function"==typeof define&&define.amd?define(t):(e=e||self,function(){var n=e.Cookies,r=e.Cookies=t();r.noConflict=function(){return e.Cookies=n,r}}())}(this,function(){"use strict";function e(e){for(var t=1;t<arguments.length;t++){var n=arguments[t];for(var r in n)e[r]=n[r]}return e}var t={read:function(e){return e.replace(/(%[\dA-F]{2})+/gi,decodeURIComponent)},write:function(e){return encodeURIComponent(e).replace(/%(2[346BF]|3[AC-F]|40|5[BDE]|60|7[BCD])/g,decodeURIComponent)}};return function n(r,o){function i(t,n,i){if("undefined"!=typeof document){"number"==typeof(i=e({},o,i)).expires&&(i.expires=new Date(Date.now()+864e5*i.expires)),i.expires&&(i.expires=i.expires.toUTCString()),t=encodeURIComponent(t).replace(/%(2[346B]|5E|60|7C)/g,decodeURIComponent).replace(/[()]/g,escape),n=r.write(n,t);var c="";for(var u in i)i[u]&&(c+="; "+u,!0!==i[u]&&(c+="="+i[u].split(";")[0]));return document.cookie=t+"="+n+c}}return Object.create({set:i,get:function(e){if("undefined"!=typeof document&&(!arguments.length||e)){for(var n=document.cookie?document.cookie.split("; "):[],o={},i=0;i<n.length;i++){var c=n[i].split("="),u=c.slice(1).join("=");'"'===u[0]&&(u=u.slice(1,-1));try{var f=t.read(c[0]);if(o[f]=r.read(u,f),e===f)break}catch(e){}}return e?o[e]:o}},remove:function(t,n){i(t,"",e({},n,{expires:-1}))},withAttributes:function(t){return n(this.converter,e({},this.attributes,t))},withConverter:function(t){return n(e({},this.converter,t),this.attributes)}},{attributes:{value:Object.freeze(o)},converter:{value:Object.freeze(r)}})}(t,{path:"/"})});

			
	// // Cookie Settings
	// var maxCookieValue = 4, initCookie = 1, expirationDays = 1;
	// var cookieName = "session_pageviews";
	// var getCookie = Cookies.get(cookieName);

	// // Under the Hood
	// if (getCookie == null) {
		// Cookies.set(cookieName, initCookie, { expires: expirationDays });
		// console.log('Cookie set to value 1');
		// $( "#ic_video_ad" ).append( "<div id=\"IC_D_3x6\" style=\"margin:30px;\"></div>" );
	// } else {
		// if (getCookie >= initCookie && getCookie < maxCookieValue) {
			// getCookie++;
			// Cookies.set(cookieName, getCookie, { expires: expirationDays });
			// console.log('Cookie incremented. New value is ' + getCookie);
			// $( "#ic_video_ad" ).append( "<div id=\"IC_D_3x6\" style=\"margin:30px;\"></div>" );
		// }
		// else if (getCookie >= maxCookieValue && getCookie < 7) {
			// getCookie++;
			// Cookies.set(cookieName, getCookie, { expires: expirationDays });
			// console.log('Cookie max allowed value reached. No video ads showing. New value is ' + getCookie);
			// //Cookies.remove(cookieName);
			// // if cookie is equal with the number you've set, then do something
			// // hide an element, delete the cookie etc...
		// }
		// else if (getCookie >= 7) {
			// Cookies.remove(cookieName);
			// // if cookie is equal with the number you've set, then do something
			// // hide an element, delete the cookie etc...
		// }	
	// }
  </script>
  <script>
   $(document).ready(function() {
	
	var user_data = '171.76.81.154';	var country_code = 'United States';
	$.post('https://www.macrotrends.net/assets/php/user_frequency_tracking.php', {user_ip: user_data, user_country: country_code}); 

	// Selects all of the text in the chart export window when clicked
	$(".modal_link").focus(function() {
		var $this = $(this);
		$this.select();

		// Work around Chrome's little problem
		$this.mouseup(function() {
			// Prevent further mouseup intervention
			$this.unbind("mouseup");
			return false;
		});
	});	
	
	
	$('[data-toggle="tooltip"]').tooltip();
	
    $('.statement_type_select').select2({
	
	theme: "classic",
	minimumResultsForSearch: 20
	
	});

    $('.frequency_select').select2({
	
	theme: "classic",
	minimumResultsForSearch: 20
	
	});
	
	
});

$( "#compareStocks" ).click(function() {
	
	
	window.location.href = '/stocks/stock-comparison?s=revenue&axis=single&comp=TSLA';
	
	
});

$( "#chartExport" ).click(function() {
	
		window.$('#smallWidthModal1').modal();

		//Turn off scroll bar for image export
		chart.chartScrollbarSettings.enabled = false;
		chart.validateNow(); 
		
		
		chart.export.capture({},function() {
			this.toPNG({},function(data) {
				// Download the image to the browser
				this.download( data, "image/png", "TSLA-revenue-2022-12-09-macrotrends.png" );
				
				});

		//Turn scroll bar back on again
		chart.chartScrollbarSettings.enabled = true;
		chart.validateNow(); 
				
	});

});

$( ".statement_type_select" ).change(function() {
  
  window.location.href = 'https://testing.macrotrends.net/assets/php/income_statement_testing.php?t=ZEV&type=' + this.value + '&freq=Q';

});

$( ".frequency_select" ).change(function() {
  
  window.location.href = '/assets/php/new_chart_page.php?t=ZEV&type=revenue&freq=' + this.value;

});
  </script>
  <!--<div class="modal" id="contribute_modal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="false">
  <div class="modal-dialog modal-lg">
    <div class="modal-content">
      <div class="modal-body" style="margin:20px 40px 20px 40px; text-align:left;font-size:18px;">
	  	  


<div class="row">

<div class="col-xs-6">

<script src="https://donorbox.org/widget.js" paypalExpress="true"></script><iframe src="https://donorbox.org/embed/macrotrends-donations?hide_donation_meter=true" height="685px" width="100%" style="max-width:500px; min-width:310px; max-height:none!important" seamless="seamless" name="donorbox" frameborder="0" scrolling="no" allowpaymentrequest></iframe>

</div>

<div class="col-xs-6">

		<div class="modal_title"><h1><strong>We Need Your Support!</strong></h1></div>

		<p><strong>Macrotrends has been subscription-free since 2010 and we want to keep it that way.</strong></p>

<p>Our goal has always been to serve as an easily accessible, high quality source of investment research for both professionals and amateurs alike.</p>

<p>Any amount that you can contribute will help ensure we can keep the site completely free for many years to come.</p>

<p style="margin-top:20px;">Regards,</p>
<p>The Macrotrends Team</p>

</div>

</div>

</div>

      <div class="modal-footer" style="text-align:center;">
        <button type="button" class="btn btn-success" data-dismiss="modal">Maybe Next Time...</button>
      </div>
    </div>
  </div>
</div>	


<script src="/ads.js" type="text/javascript"></script>

<script>

$(document).ready(function() {
	
	var botPattern = "(googlebot\/|Googlebot-Mobile|Googlebot-Image|Google favicon|Mediapartners-Google|bingbot|slurp|java|wget|curl|Commons-HttpClient|Python-urllib|libwww|httpunit|nutch|phpcrawl|msnbot|jyxobot|FAST-WebCrawler|FAST Enterprise Crawler|biglotron|teoma|convera|seekbot|gigablast|exabot|ngbot|ia_archiver|GingerCrawler|webmon |httrack|webcrawler|grub.org|UsineNouvelleCrawler|antibot|netresearchserver|speedy|fluffy|bibnum.bnf|findlink|msrbot|panscient|yacybot|AISearchBot|IOI|ips-agent|tagoobot|MJ12bot|dotbot|woriobot|yanga|buzzbot|mlbot|yandexbot|purebot|Linguee Bot|Voyager|CyberPatrol|voilabot|baiduspider|citeseerxbot|spbot|twengabot|postrank|turnitinbot|scribdbot|page2rss|sitebot|linkdex|Adidxbot|blekkobot|ezooms|dotbot|Mail.RU_Bot|discobot|heritrix|findthatfile|europarchive.org|NerdByNature.Bot|sistrix crawler|ahrefsbot|Aboundex|domaincrawler|wbsearchbot|summify|ccbot|edisterbot|seznambot|ec2linkfinder|gslfbot|aihitbot|intelium_bot|facebookexternalhit|yeti|RetrevoPageAnalyzer|lb-spider|sogou|lssbot|careerbot|wotbox|wocbot|ichiro|DuckDuckBot|lssrocketcrawler|drupact|webcompanycrawler|acoonbot|openindexspider|gnam gnam spider|web-archive-net.com.bot|backlinkcrawler|coccoc|integromedb|content crawler spider|toplistbot|seokicks-robot|it2media-domain-crawler|ip-web-crawler.com|siteexplorer.info|elisabot|proximic|changedetection|blexbot|arabot|WeSEE:Search|niki-bot|CrystalSemanticsBot|rogerbot|360Spider|psbot|InterfaxScanBot|Lipperhey SEO Service|CC Metadata Scaper|g00g1e.net|GrapeshotCrawler|urlappendbot|brainobot|fr-crawler|binlar|SimpleCrawler|Livelapbot|Twitterbot|cXensebot|smtbot|bnf.fr_bot|A6-Indexer|ADmantX|Facebot|Twitterbot|OrangeBot|memorybot|AdvBot|MegaIndex|SemanticScholarBot|ltx71|nerdybot|xovibot|BUbiNG|Qwantify|archive.org_bot|Applebot|TweetmemeBot|crawler4j|findxbot|SemrushBot|yoozBot|lipperhey|y!j-asr|Domain Re-Animator Bot|AddThis)";

	var re = new RegExp(botPattern, 'i');

	if (re.test(navigator.userAgent)) {
		
	} else {
		
		//Check to see whether they are running an ad blocker
		if(document.getElementById('12mORwMnaEkJXlxz')){
		  var ad_blocker = 'N';
		} else {
		  var ad_blocker = 'Y';
		}

		$.post('https://api.ipstack.com/check?access_key=14fe63e83d5cfefa0b3d4cec498479ba&output=json&fields=ip,continent_name,country_name,region_name,city', 
		function(ip_data){
			
			$.post('https://www.macrotrends.net/assets/php/page_view_tracking.php', {ip: ip_data.ip,continent: ip_data.continent_name, country: ip_data.country_name, state: ip_data.region_name, city: ip_data.city, screen_width: screen.width, ads: ad_blocker, page_type: 'stock'}, 
				function(data){
					/*					
					if(data % 20 === 0) {
						
						//$('#contribute_modal').modal();
						
					}
					*/
				});
		
		});


	}
	

});


$.post('https://api.ipstack.com/check?access_key=14fe63e83d5cfefa0b3d4cec498479ba&output=json&fields=ip,continent_name,country_name,region_name,city', 
function(ip_data){
	
	$(".contribute_user_id").val(ip_data.ip);
	
});

$( ".donate_buttons" ).click(function() {
  
	var payment = $(this).attr("value");

	$.post('https://api.ipstack.com/check?access_key=14fe63e83d5cfefa0b3d4cec498479ba&output=json&fields=ip,continent_name,country_name,region_name,city', 
		function(ip_data){
					
		$.post('https://www.macrotrends.net/assets/php/page_view_tracking.php', {ip: ip_data.ip, paid: payment}); 
	
	});
		 
});

</script>

-->
  <script type="text/javascript">
   var clicky_site_ids = clicky_site_ids || [];
clicky_site_ids.push(100827248);
(function() {
  var s = document.createElement('script');
  s.type = 'text/javascript';
  s.async = true;
  s.src = '//static.getclicky.com/js';
  ( document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0] ).appendChild( s );
})();
  </script>
  <noscript>
   <p>
    <img alt="Clicky" height="1" src="//in.getclicky.com/100827248ns.gif" width="1"/>
   </p>
  </noscript>
  <!-- This site is converting visitors into subscribers and customers with OptinMonster - https://optinmonster.com -->
  <!-- <script type="text/javascript" src="https://a.omappapi.com/app/js/api.min.js" data-account="6392" data-user="15772" async></script> -->
  <!-- / OptinMonster -->
 </body>
</html>

Using BeautifulSoup or the read_html function extract the table with Tesla Revenue and store it into a dataframe named tesla_revenue. The dataframe should have columns Date and Revenue.

Click here if you need help locating the table
tesla_revenue = pd.DataFrame(columns = ["Date","Revenue"])
​
for table in soup.find_all('table'):
    if table.find('th').getText().startswith("Tesla Quarterly Revenue"):
        for row in table.find("tbody").find_all("tr"):
            col = row.find_all("td")
            if len(col) != 2: continue
            Date = col[0].text
            Revenue = col[1].text.replace("$","").replace(",","")
               
            tesla_revenue = tesla_revenue.append({"Date":Date, "Revenue":Revenue}, ignore_index=True)
Execute the following line to remove the comma and dollar sign from the Revenue column.

tesla_revenue.dropna(axis=0, how='all', subset=['Revenue']) #drop NaN values
tesla_revenue = tesla_revenue[tesla_revenue['Revenue'] != ""] #drop empty string values
Execute the following lines to remove an null or empty strings in the Revenue column.

tesla_revenue.dropna(inplace=True)
​
tesla_revenue = tesla_revenue[tesla_revenue['Revenue'] != ""]
Display the last 5 row of the tesla_revenue dataframe using the tail function. Take a screenshot of the results.

tesla_revenue.tail(5)
Date	Revenue
48	2010-09-30	31
49	2010-06-30	28
50	2010-03-31	21
52	2009-09-30	46
53	2009-06-30	27
Question 3: Use yfinance to Extract Stock Data
Using the Ticker function enter the ticker symbol of the stock we want to extract data on to create a ticker object. The stock is GameStop and its ticker symbol is GME.

gme = yf.Ticker('GME')
Using the ticker object and the function history extract stock information and save it in a dataframe named gme_data. Set the period parameter to max so we get information for the maximum amount of time.

gme_data = gme.history(period = "max")
Reset the index using the reset_index(inplace=True) function on the gme_data DataFrame and display the first five rows of the gme_data dataframe using the head function. Take a screenshot of the results and code from the beginning of Question 3 to the results below.

gme_data.reset_index(inplace=True)
gme_data.head(5)
Date	Open	High	Low	Close	Volume	Dividends	Stock Splits
0	2002-02-13	1.620129	1.693350	1.603296	1.691667	76216000	0.0	0.0
1	2002-02-14	1.712707	1.716074	1.670626	1.683250	11021600	0.0	0.0
2	2002-02-15	1.683250	1.687458	1.658001	1.674834	8389600	0.0	0.0
3	2002-02-19	1.666418	1.666418	1.578047	1.607504	7410400	0.0	0.0
4	2002-02-20	1.615920	1.662210	1.603296	1.662210	6892800	0.0	0.0
Question 4: Use Webscraping to Extract GME Revenue Data
Use the requests library to download the webpage https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/stock.html. Save the text of the response as a variable named html_data.

url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/stock.html."
html_data = requests.get(url).text
Parse the html data using beautiful_soup.

import requests
from bs4 import BeautifulSoup
​
url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm"
html_data = requests.get(url).text
​
# Parse the HTML data using BeautifulSoup with 'html.parser' (or 'lxml')
soup = BeautifulSoup(html_data, "html.parser")
​
# Print the prettified version of the HTML data
print(soup.prettify())
​
<!DOCTYPE html>
<!--[if lt IE 7]>      <html class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if IE 7]>         <html class="no-js lt-ie9 lt-ie8"> <![endif]-->
<!--[if IE 8]>         <html class="no-js lt-ie9"> <![endif]-->
<!--[if gt IE 8]><!-->
<html class="no-js">
 <!--<![endif]-->
 <head>
  <meta charset="utf-8"/>
  <meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible"/>
  <link href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue" rel="canonical"/>
  <title>
   Tesla Revenue 2010-2022 | TSLA | MacroTrends
  </title>
  <meta content="Tesla annual/quarterly revenue history and growth rate from 2010 to 2022. Revenue can be defined as the amount of money a company receives from its customers in exchange for the sales of goods or services.  Revenue is the top line item on an income statement from which all costs and expenses are subtracted to arrive at net income.    
				
				&lt;ul style='margin-top:10px;'&gt;
				&lt;li&gt;Tesla revenue for the quarter ending September 30, 2022 was &lt;strong&gt;$21.454B&lt;/strong&gt;, a &lt;strong&gt;55.95% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla revenue for the twelve months ending September 30, 2022 was &lt;strong&gt;$74.863B&lt;/strong&gt;, a &lt;strong&gt;59.8% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2021 was &lt;strong&gt;$53.823B&lt;/strong&gt;, a &lt;strong&gt;70.67% increase&lt;/strong&gt; from 2020.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2020 was &lt;strong&gt;$31.536B&lt;/strong&gt;, a &lt;strong&gt;28.31% increase&lt;/strong&gt; from 2019.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2019 was &lt;strong&gt;$24.578B&lt;/strong&gt;, a &lt;strong&gt;14.52% increase&lt;/strong&gt; from 2018.&lt;/li&gt;
				&lt;/ul&gt;" name="description">
   <meta content="" name="robots">
    <link href="/assets/images/icons/FAVICON/macro-trends_favicon.ico" rel="shortcut icon" type="image/x-icon"/>
    <meta content="1228954C688F5907894001CD8E5E624B" name="msvalidate.01"/>
    <meta content="6MnD_3iDtAP1ZyoGK1YMyVIVck4r5Ws80I9xD3ue4_A" name="google-site-verification"/>
    <!-- Load in Roboto Font -->
    <link href="https://fonts.googleapis.com/css?family=Roboto:400,600,700" rel="stylesheet"/>
    <!-- Bootstrap -->
    <link href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet"/>
    <!--for Bootstrap CDN version-->
    <link href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap-theme.min.css" rel="stylesheet"/>
    <!-- Font Awesome -->
    <link href="//stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet"/>
    <!--for Font Awesome CDN version-->
    <!-- Jquery, Bootstrap and Menu Javascript -->
    <script crossorigin="anonymous" integrity="sha256-ZosEbRLbNQzLpnKIkEdrPv7lOy9C27hHQ+Xp8a4MxAQ=" src="//code.jquery.com/jquery-1.12.4.min.js">
    </script>
    <script src="//maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js">
    </script>
    <!-- Modernizr for cross-browser support -->
    <script src="/assets/javascript/modernizr-2.6.2-respond-1.1.0.min.js" type="text/javascript">
    </script>
    <!-- Latest compiled and minified CSS -->
    <link href="//www.fuelcdn.com/fuelux/3.13.0/css/fuelux.min.css" rel="stylesheet"/>
    <!-- Latest compiled and minified JavaScript -->
    <script src="//www.fuelcdn.com/fuelux/3.13.0/js/fuelux.min.js">
    </script>
    <!-- Twitter Card data -->
    <meta content="summary_large_image" name="twitter:card"/>
    <meta content="@tmacrotrends" name="twitter:site"/>
    <meta content="Tesla Revenue 2010-2022 | TSLA" name="twitter:title"/>
    <meta content="Tesla annual/quarterly revenue history and growth rate from 2010 to 2022. Revenue can be defined as the amount of money a company receives from its customers in exchange for the sales of goods or services.  Revenue is the top line item on an income statement from which all costs and expenses are subtracted to arrive at net income.    
				
				&lt;ul style='margin-top:10px;'&gt;
				&lt;li&gt;Tesla revenue for the quarter ending September 30, 2022 was &lt;strong&gt;$21.454B&lt;/strong&gt;, a &lt;strong&gt;55.95% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla revenue for the twelve months ending September 30, 2022 was &lt;strong&gt;$74.863B&lt;/strong&gt;, a &lt;strong&gt;59.8% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2021 was &lt;strong&gt;$53.823B&lt;/strong&gt;, a &lt;strong&gt;70.67% increase&lt;/strong&gt; from 2020.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2020 was &lt;strong&gt;$31.536B&lt;/strong&gt;, a &lt;strong&gt;28.31% increase&lt;/strong&gt; from 2019.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2019 was &lt;strong&gt;$24.578B&lt;/strong&gt;, a &lt;strong&gt;14.52% increase&lt;/strong&gt; from 2018.&lt;/li&gt;
				&lt;/ul&gt;" name="twitter:description"/>
    <!-- Open Graph data -->
    <meta content="https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue" property="og:url">
     <meta content="Tesla Revenue 2010-2022 | TSLA" property="og:title">
      <meta content="Tesla annual/quarterly revenue history and growth rate from 2010 to 2022. Revenue can be defined as the amount of money a company receives from its customers in exchange for the sales of goods or services.  Revenue is the top line item on an income statement from which all costs and expenses are subtracted to arrive at net income.    
				
				&lt;ul style='margin-top:10px;'&gt;
				&lt;li&gt;Tesla revenue for the quarter ending September 30, 2022 was &lt;strong&gt;$21.454B&lt;/strong&gt;, a &lt;strong&gt;55.95% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla revenue for the twelve months ending September 30, 2022 was &lt;strong&gt;$74.863B&lt;/strong&gt;, a &lt;strong&gt;59.8% increase&lt;/strong&gt; year-over-year.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2021 was &lt;strong&gt;$53.823B&lt;/strong&gt;, a &lt;strong&gt;70.67% increase&lt;/strong&gt; from 2020.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2020 was &lt;strong&gt;$31.536B&lt;/strong&gt;, a &lt;strong&gt;28.31% increase&lt;/strong&gt; from 2019.&lt;/li&gt;
				&lt;li&gt;Tesla annual revenue for 2019 was &lt;strong&gt;$24.578B&lt;/strong&gt;, a &lt;strong&gt;14.52% increase&lt;/strong&gt; from 2018.&lt;/li&gt;
				&lt;/ul&gt;" property="og:description">
       <!-- JQXGRID STYLES AND JAVASCRIPT -->
       <link href="/assets/php/jqfiles/jqwidgets/styles/jqx.base.css" rel="stylesheet" type="text/css">
        <link href="/assets/php/jqfiles/jqwidgets/styles/jqx.bootstrap.css" rel="stylesheet" type="text/css">
         <!-- LOAD THESE SCRIPTS EARLY SO THE TICKER INPUT FIELD IS STYLED INSTANTLY -->
         <script src="/assets/php/jqfiles/jqwidgets/jqxcore.js" type="text/javascript">
         </script>
         <script src="/assets/php/jqfiles/jqwidgets/jqxdata.js" type="text/javascript">
         </script>
         <script src="/assets/php/jqfiles/jqwidgets/jqxinput.js" type="text/javascript">
         </script>
         <!-- Styling for search box -->
         <link href="/assets/php/jquery-typeahead/jquery.typeahead_pages.css" rel="stylesheet" type="text/css"/>
         <!-- Search box javascript -->
         <script src="/assets/php/jquery-typeahead/jquery.typeahead.min.js">
         </script>
         <link href="//cdnjs.cloudflare.com/ajax/libs/select2/4.0.3/css/select2.min.css" rel="stylesheet">
          <script src="//cdnjs.cloudflare.com/ajax/libs/select2/4.0.3/js/select2.min.js">
          </script>
          <!-- ToolTips -->
          <script src="/assets/php/tipped-4.6.1/js/tipped/tipped.js">
          </script>
          <link href="/assets/php/tipped-4.6.1/css/tipped/tipped.css" rel="stylesheet"/>
          <!-- START IC AD INSERT -->
          <script>
           InvestingChannelQueue = window.InvestingChannelQueue || [];
          </script>
          <script async="" src="https://u5.investingchannel.com/static/uat.js">
          </script>
          <script type="text/javascript">
           //Push Run command with the API-Key, so that UAT will start processing publishers request.
        InvestingChannelQueue.push(function() {
            ic_page = InvestingChannel.UAT.Run("df17ac1e-cc7f-11e8-82a5-0abbb61c4a6a");        
        });
		
		var tickerValue = 'TSLA';			
        var oopDivTag;
		var subLeaderboardTag;
		var rightSidebarTag1;
		var rightSidebarTag2;
		var searchButtonTag;
		var partner_center_tag;
		var videoTag;
		var ic_3x7_1;
 		//var IC_D_300x250_BCC;
		//var IC_D_3x7_BCC;
   
        //To define new tags/out of page tags.
        InvestingChannelQueue.push(function() {
			
			ic_page.setKval({'t': tickerValue});
			
            //videoTag = ic_page.defineNativeTag("Macrotrends/fundamentalanalysis","3x6, 728x90, Fluid","IC_D_3x6",35);
			
            oopDivTag = ic_page.defineOutOfPageTag("Macrotrends/fundamentalanalysis","oopDivTag_1");
			oopDivTag.setKval({"adslot":"IC_OOP_1"});
            
			
			LeaderboardTag = ic_page.defineTag("Macrotrends/fundamentalanalysis","970x250,728x90,970x90,fluid", "IC_D_970x250_1");
			LeaderboardTag.setKval({"adslot":"IC_D_970x250_1"});


			subLeaderboardTag = ic_page.defineTag("Macrotrends/fundamentalanalysis","728x90","ic_728x90_1");
			subLeaderboardTag.setKval({"adslot":"IC_728x90_1"});
			
			
			rightSidebarTag1 = ic_page.defineTag("Macrotrends/fundamentalanalysis","300x250,Fluid","ic_300x250_1");
			rightSidebarTag1.setKval({"adslot":"IC_300x250_1"});
			
			
			rightSidebarTag2 = ic_page.defineTag("Macrotrends/fundamentalanalysis","300x600,300x250,160x600,300x1050,Fluid","ic_300x600_1");
			rightSidebarTag2.setKval({"adslot":"IC_300x600_1"});
			
			
			searchButtonTag = ic_page.defineTag("Macrotrends/fundamentalanalysis","88x31","ic_88x31_1");
			searchButtonTag.setKval({"pc":"pc","adslot":"IC_88x31"});
			
			partner_center_tag = ic_page.defineTag("macrotrends/fundamentalanalysis","728x214, 728x90","IC_728x214_1");
			partner_center_tag.setKval({"pc":"pc","adslot":"d_728x90_2"});

			ic_3x7_1 = ic_page.defineNativeTag("macrotrends/fundamentalanalysis","3x7,728x90,Fluid","IC_3x7_1", 35);
			
			//IC_D_300x250_BCC = ic_page.defineTag(adCategory,"300x250,Fluid","IC_D_300x250_BCC");
			//IC_D_300x250_BCC.setKval({"adslot":"IC_D_300x250_BCC"});

			//IC_D_3x7_BCC = ic_page.defineTag(adCategory,"3x7, Fluid","IC_D_3x7_BCC");
			//IC_D_3x7_BCC.setKval({"adslot":"IC_D_3x7_BCC"});
			

        });
    
        //To render tags.
			InvestingChannelQueue.push(function() {
            ic_page.renderTags();
        });
          </script>
          <!-- END IC AD INSERT -->
          <!-- Global site tag (gtag.js) - Google Analytics -->
          <script async="" src="https://www.googletagmanager.com/gtag/js?id=UA-62099500-1">
          </script>
          <script>
           window.dataLayer = window.dataLayer || [];
		  function gtag(){dataLayer.push(arguments);}
		  gtag('js', new Date());

		  gtag('config', 'UA-62099500-1');
          </script>
          <!-- Google tag (gtag.js) -->
          <script async="" src="https://www.googletagmanager.com/gtag/js?id=G-3KL0LYERBH">
          </script>
          <script>
           window.dataLayer = window.dataLayer || [];
		  function gtag(){dataLayer.push(arguments);}
		  gtag('js', new Date());

		  gtag('config', 'G-3KL0LYERBH');
          </script>
          <!--<script>
			(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
			(i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
			m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
			})(window,document,'script','//www.google-analytics.com/analytics.js','ga');

			ga('create', 'UA-62099500-1', 'auto');
			ga('send', 'pageview');
			
			
			
		   
			//Send one event to GA at 30 seconds to control bounce rate
			setTimeout("ga('send','event','Engaged User','30 Second Engagement')",30000); 


		  //This code sends events to ga every 30 seconds when the window is in focus
			var count = 0;
			var myInterval;
					
			// Active
			window.addEventListener('load', startTimer);
			window.addEventListener('focus', startTimer);

			// Inactive
			window.addEventListener('blur', stopTimer);

			function timerHandler() {
				count++;
				
				if(count % 60 == 0 && count <= 1800) {
					
					var interval = (count/60);
					interval = interval.toFixed(0);
					
					var action = interval + " Minute Engagement";
					
					ga('send','event','Engaged User',action);

					
				}
			
			}

			// Start timer
			function startTimer() {
			myInterval = window.setInterval(timerHandler, 1000);
			}

			// Stop timer
			function stopTimer() {
			window.clearInterval(myInterval);
			}
			
			

		</script>-->
          <style>
           #style-1::-webkit-scrollbar-track
{
	-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3);
	border-radius: 3px;
	background-color: #F5F5F5;
}

#style-1::-webkit-scrollbar
{
	width: 18px;
	background-color: #F5F5F5;
}

#style-1::-webkit-scrollbar-thumb
{
	border-radius: 3px;
	-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3);
	background-color: #5B9BD5;
}

html {
	width:100%;
	position: relative;
	min-height: 100%;
}

body {
	
	width:100%;

	/* Margin bottom by footer height */
	  margin-bottom: 80px;
	  color: #444;
	  background-color:#fff;
	  font-family: 'Roboto', sans-serif;
	  font-size:14px;
}





.header_content_container {
	
	min-width: 1280px;
	padding: 0px;
}

.main_content_container {
	
	min-width: 1280px;
	max-width: 1280px;
	padding: 0px 30px 100px 30px;
	
}

.sub_main_content_container {
	
	
}



#main_content {
	
	padding:0px 20px 0px 0px;
	width:826px;
    float:left;
	
}

#right_sidebar {
	
  width: 300px;
  float:left;
  height:3200px;
	
}

#sticky_ad_left {
	
  position: -webkit-sticky;
  position: sticky;
  top: 30px;
	
	
}

#sticky_ad_right {
	
  position: -webkit-sticky;
  position: sticky;
  top: 30px;
	
	
}





.footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  /* Set the fixed height of the footer here */
  height: 100px;
  margin-top: 10px;	
  padding: 30px 20px 20px 20px;
  color:#fff !important;
  background-color:#444;
  text-align: center;
  font-size:16px;
}

.footer a {
  color:#fff !important;
}

.ticker_search_box {
	
	background-color:#F5F5F5;
	border: 1px solid #E0E0E0;
	border-bottom:none;
	padding:10px 30px 10px 10px;
	margin:0px 0px 0px 0px;
	text-align:center;
	
}

.related_tickers {
	
	width:100%;
	background-color:#F5F5F5;
	border: 1px solid #E0E0E0;
	border-top: 0px;
	padding:3px 30px 3px 10px;
	margin:0px 0px 0px 0px;
	text-align:center;
	
}

.statement_type_select {

	width:100%;
	height:28px;
	
}

.frequency_select {

	width:100%;
	height:28px;
	font-weight:600;
	
}


.select2 {
	
	text-align:left;
	font-weight:600;
	
	}
	
#jqxInput {

		width:100%;
		height:28px;
		
}



.header__parent_container {

	width:100%;
	height:50px;
	padding:15px 0px 10px -20px; 
	margin:0px 0px 0px 0px;
	background-color:#444;

}

.header_container {

	width:100%;
	height:50px;
	padding:15px 0px 10px -20px; 
	margin:0px 0px 0px 0px;
	background-color:#444;

}

.header_logo {
	
	padding-top:10px;
	margin-left:50px;
	
}

.menu_parent_container {
	
	width:100%;
	height:34px;
	font-size:16px;
	padding:15px 0px 10px -20px; 
	margin:0px 0px 0px 0px;
	background-color:#0089de;
}

.menu_container {
	
	width:1280px;
	height:34px;
	font-size:16px;
	padding:11px 0px 0px -20px; 
	margin: 0 auto;
	background-color:#0089de;
	z-index:1000;
}

.menu_item {

	height:34px;
	float:left;
	font-size:14px;
	font-weight:bold;
	color:#fff;
	text-align:center;
	padding:7px 16px 0px 16px;	

}

.menu_item:hover
{
	background-color:#32a0e4;
	cursor: pointer;
}

.menu_item a
{
	color:#fff;
	cursor: pointer;
}

.menu_item a:hover
{
	text-decoration:none;
	cursor: pointer;
}

.leaderboard_ad {

	margin-top:20px;
	margin-bottom:20px;
	text-align:center;
	min-height:100px;

}

#filter_result_count {
	
	width:100%;
	text-align:center;
	font-size:24px;
	font-weight:bold;
	padding:10px 15px;
	background-color:#efefef;
	border: 1px solid #dfdfdf;
	margin:20px;
	
}


select {
  color: #444;
  background-color: #FFF;
  border: 1px solid #AAA;
  border-radius: 4px;
  box-sizing: border-box;
  cursor: pointer;
  display: block;
  height:40px;
  line-height: 40px;
}

.historical_data_table  {
    table-layout: fixed;
	margin:20px;
}

.historical_data_table tbody tr td {
	
	padding:6px;
	vertical-align: middle !important;

}


.descriptors {
	
	text-align:center;
	font-size:14px;
	padding:15px;
	
}

.td_metric_name {
	
	width:110px;
	padding-top:17px;
	
}

.metric_link {
	
	font-size:14px;
	font-weight:bold;

}

.help_icon {
	
	width:15px;
	height:18px; 
	padding-bottom:3px;
	
}

.td_min_value {
	
	width:75px;
	text-align:center;
	font-size:13px;
	
}

.td_max_value {
	
	width:75px;
	text-align:center;
	font-size:13px;
	
}

#myCombobox .form-control {
	
	background-color: #99d5ff;

	
}

.dropdown-toggle {
	
	height:24px;
	padding-top:0px;
	padding-left:7px;
	width:24px;
	
}

.dropdown-menu-right {
	
	min-width:75px;
	font-size:13px;
	
}

.form-control {
	
	font-size:12px;	
	padding:5px 10px;
	height:24px;

	
}

#myPills1 {
	
	margin:0px 15px 10px 0px;
	
}

#jqxgrid {
	
	border-radius:0px;
	
}

.jqx-widget-header {
	
    font-family: 'Roboto', sans-serif;
	font-size:13px;	
	
}

.jqx-item {
	
    font-family: 'Roboto', sans-serif;
	font-size: 13px;
	
}

.jqx-widget-content {
	
	border-color: #E0E0E0;
	
}

#jqxgrid .jqx-grid-cell {
	
	border-color: #E0E0E0;
	
}

#jqxgrid .jqx-grid-cell-pinned {
	
	border-color: #E0E0E0;
	background-color: #F5F5F5;
	
}

#jqxgrid .jqx-grid-column-header {
	
	border-color: #E0E0E0;
	background-color: #F5F5F5;
	
}

.clear_zero {

	height:0px;

}



/* Styles for Popup Charts */

.tpd-size-large {
	
	margin:0px;	
	padding: 0px;
}

.popup_window_wrapper {
	
	margin:15px;
	
}

.popup_stock_name {

	font-size:16px;
	font-weight:bold;
	margin:5px;

}

.popup_stock_attributes {

	font-size:13px;
	font-weight:bold;
	margin:5px;

}

.popup_stock_description {

	font-size:12px;
	margin:5px;

}

.jqx-input {
	
	font-size:14px;
	
} 

.jqx-menu-item {
	
	font-size:14px;
	
}

.jqx-input {
	
	padding:5px 10px;
	
}

.nav-tabs {
    border: 1px solid #E0E0E0;
	background-color:#F5F5F5;
	padding: 3px 5px 0px 5px;
	margin: 0px 0px 10px 0px;
}

.nav-tabs>li>a {
	font-size:13px;
	padding:7px 11px;
	font-weight:600;
    margin-right: 0px;
    line-height: 1.42857143;
    border: 0px;
    border-radius: 0px 0px 0 0;
	background-color:#F5F5F5;

}

.nav-tabs>li>a .active {
    margin-right: 0px;
    line-height: 1.42857143;
    border: 1px solid #E0E0E0;
    border-radius: 0px 0px 0 0;
	background-color:#F5F5F5;

}

.nav-tabs>li>a:hover { 
    background-color: #F5F5F5;
	text-decoration: underline;

}

.donate_buttons {

	margin-left:20px;
	
	}

.modal-body {

	margin:10px 40px 20px 40px;
	text-align:left;
	font-size:18px;

}

.modal-body li {

	margin-top:20px;
	font-size:14px;

}


.modal_title {


	text-align:center;
	margin-bottom:30px;

}

.modal-body th{

	margin-left:10px;
	font-size:14px;
}

.modal-body td {

	color: #337ab7;
	margin-left:10px;
	font-size:14px;
}

.modal_button {

	margin-top:50px;
	text-align:center;
	font-size:16px;

}
          </style>
         </link>
        </link>
       </link>
      </meta>
     </meta>
    </meta>
   </meta>
  </meta>
 </head>
 <body class="fuelux">
  <!--[if lt IE 7]>
            <p class="browsehappy">You are using an <strong>outdated</strong> browser. Please <a href="https://browsehappy.com/">upgrade your browser</a> to improve your experience.</p>
        <![endif]-->
  <div class="header_content_container container-fluid">
   <div class="header_parent_container">
    <div class="header_container">
     <div class="header_logo col-xs-2">
      <a class="logo" href="https://www.macrotrends.net" title="MacroTrends Home Page">
       <img src="/assets/images/logo_bright1.png"/>
      </a>
     </div>
     <div class="col-xs-1 pull-right" style="padding-top:8px; margin-right:10px; margin-left:0px; padding-left:0px;">
      <div id="ic_88x31_1">
      </div>
     </div>
     <div class="col-xs-5 pull-right" style="padding-top:8px;">
      <form>
       <div class="typeahead__container">
        <div class="typeahead__field">
         <span class="typeahead__query">
          <input autocomplete="off" autofocus="" class="js-typeahead" name="q" placeholder="Search over 200,000 charts..." type="search"/>
         </span>
         <span class="typeahead__button">
          <button type="submit">
           <span class="typeahead__search-icon">
           </span>
          </button>
         </span>
        </div>
       </div>
      </form>
     </div>
    </div>
   </div>
   <div class="menu_parent_container">
    <div class="menu_container">
     <a href="/stocks/stock-screener">
      <div class="menu_item">
       Stock Screener
      </div>
     </a>
     <a href="/stocks/research">
      <div class="menu_item">
       Stock Research
      </div>
     </a>
     <a href="/charts/stock-indexes">
      <div class="menu_item">
       Market Indexes
      </div>
     </a>
     <a href="/charts/precious-metals">
      <div class="menu_item">
       Precious Metals
      </div>
     </a>
     <a href="/charts/energy">
      <div class="menu_item">
       Energy
      </div>
     </a>
     <a href="/charts/commodities">
      <div class="menu_item">
       Commodities
      </div>
     </a>
     <a href="/charts/exchange-rates">
      <div class="menu_item">
       Exchange Rates
      </div>
     </a>
     <a href="/charts/interest-rates">
      <div class="menu_item">
       Interest Rates
      </div>
     </a>
     <a href="/charts/economy">
      <div class="menu_item">
       Economy
      </div>
     </a>
     <a href="/countries/topic-overview">
      <div class="menu_item">
       Global Metrics
      </div>
     </a>
    </div>
   </div>
  </div>
  <div class="main_content_container container-fluid" id="main_content_container">
   <div class="adx_top_ad col-xs-12" id="ic_leaderboard" style="margin: 20px 20px 30px 20px; min-height:265px; text-align:center;">
    <div id="IC_D_970x250_1">
    </div>
    <!--Smartad # 4058: Macrotrends - 970x250 Image - Placement 2-->
    <!--<iframe id="dianomi_leaderboard" WIDTH="970" HEIGHT="250" SCROLLING="NO" src="//www.dianomi.com/smartads.epl?id=4058"  style="height: 250px; border: none; overflow: hidden;"></iframe>-->
   </div>
   <div style="margin:20px 20px 20px 5px;">
    <h2 style="margin-left:0px; font-weight:600; color:#444;">
     Tesla Revenue 2010-2022 | TSLA
    </h2>
   </div>
   <div class="sub_main_content_container">
    <div id="main_content">
     <div class="navigation_tabs" style="margin-bottom:20px;">
      <ul class="nav nav-tabs" id="myTabs" style="font-size:15px;">
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/stock-price-history">
         Prices
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/financial-statements">
         Financials
        </a>
       </li>
       <li class="active">
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue">
         Revenue &amp; Profit
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/total-assets">
         Assets &amp; Liabilities
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/profit-margins">
         Margins
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/pe-ratio">
         Price Ratios
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/current-ratio">
         Other Ratios
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/dividend-yield-history">
         Other Metrics
        </a>
       </li>
      </ul>
      <ul class="nav nav-tabs" id="myTabs" style="font-size:15px;">
       <li class="active">
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue">
         Revenue
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/gross-profit">
         Gross Profit
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/operating-income">
         Operating Income
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/ebitda">
         EBITDA
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/net-income">
         Net Income
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/eps-earnings-per-share-diluted">
         EPS
        </a>
       </li>
       <li>
        <a href="https://www.macrotrends.net/stocks/charts/TSLA/tesla/shares-outstanding">
         Shares Outstanding
        </a>
       </li>
      </ul>
     </div>
     <div style="background-color:#fff; margin: 0px 0px 20px 0px; padding:20px 30px; border:1px solid #dfdfdf;">
      <span style="color:#444; line-height: 1.8;">
       Tesla annual/quarterly revenue history and growth rate from 2010 to 2022. Revenue can be defined as the amount of money a company receives from its customers in exchange for the sales of goods or services.  Revenue is the top line item on an income statement from which all costs and expenses are subtracted to arrive at net income.
       <ul style="margin-top:10px;">
        <li>
         Tesla revenue for the quarter ending September 30, 2022 was
         <strong>
          $21.454B
         </strong>
         , a
         <strong>
          55.95% increase
         </strong>
         year-over-year.
        </li>
        <li>
         Tesla revenue for the twelve months ending September 30, 2022 was
         <strong>
          $74.863B
         </strong>
         , a
         <strong>
          59.8% increase
         </strong>
         year-over-year.
        </li>
        <li>
         Tesla annual revenue for 2021 was
         <strong>
          $53.823B
         </strong>
         , a
         <strong>
          70.67% increase
         </strong>
         from 2020.
        </li>
        <li>
         Tesla annual revenue for 2020 was
         <strong>
          $31.536B
         </strong>
         , a
         <strong>
          28.31% increase
         </strong>
         from 2019.
        </li>
        <li>
         Tesla annual revenue for 2019 was
         <strong>
          $24.578B
         </strong>
         , a
         <strong>
          14.52% increase
         </strong>
         from 2018.
        </li>
       </ul>
      </span>
     </div>
     <div style="background-color:#fff; margin: 30px 0px 30px 0px; text-align:center; min-height:90px;">
      <div id="ic_728x90_1" style="margin:10px 20px;">
      </div>
     </div>
     <div class="ticker_search_box" style="text-align:center;">
      <div style="width:400px; margin-left:20px; border-bottom:none;">
       <script type="text/javascript">
        $(document).ready(function () {
				                
					var url = "https://www.macrotrends.net/assets/php/ticker_search_list.php";
				
                // prepare the data
                var source =
                {
                    datatype: "json",
                    datafields: [
                        { name: 'n' },
						{ name: 's'}
                    ],
                    url: url
                };
                var dataAdapter = new $.jqx.dataAdapter(source);
                // Create a jqxInput
                $("#jqxInput").jqxInput({ source: dataAdapter, minLength: 1, placeHolder: "Search for ticker or company name...", items: 20, searchMode: 'containsignorecase', displayMember: "n", valueMember: "s", width: '100%', height: 22, theme: 'bootstrap'});
                $("#jqxInput").on('select', function (event) {
                    if (event.args) {
                        var item = event.args.item;
						
						//Have to split the ticker and slug back out since jqxinput only seems to allow one data value
						var itemArray = item.value.split("\/"); 
						var ticker = itemArray[0];
						var slug = itemArray[1];
                        if (item) {
							
														
								window.location = "https://www.macrotrends.net/stocks/charts/" + ticker + "/" + slug + "/revenue";
							
							                        }
                    }
                });
            });
       </script>
       <input autocomplete="off" id="jqxInput">
       </input>
      </div>
      <div style="width:280px; margin-top: -32px; margin-left:80px; border-bottom:none; float:right;">
       <button class="chart_buttons btn btn-success btn-sm" id="compareStocks" style="margin-right:15px;">
        <span class="glyphicon glyphicon-stats">
        </span>
        <strong>
         Compare TSLA With Other Stocks
        </strong>
       </button>
      </div>
     </div>
     <div style="height:690px; background-color:#fff; border:1px solid #dfdfdf;">
      <iframe frameborder="0" height="680" hspace="0" id="chart_iframe" margin="0px" marginheight="0" marginwidth="0" scrolling="NO" src="https://www.macrotrends.net/assets/php/fundamental_iframe.php?t=TSLA&amp;type=revenue&amp;statement=income-statement&amp;freq=Q" title="Interactive chart: Tesla Revenue 2010-2022 | TSLA" valign="middle" vspace="0" width="800">
      </iframe>
     </div>
     <div id="ic_video_ad" style="height:317px; margin:30px;">
      <div id="IC_D_3x6">
      </div>
     </div>
     <div style="background-color:#fff; margin: 30px 0px; padding:10px 30px; border:1px solid #dfdfdf;">
      <iframe frameborder="0" height="300" hspace="0" id="dianomi_below_chart" marginheight="0" marginwidth="0" scrolling="NO" src="//www.dianomi.com/smartads.epl?id=4057" valign="middle" vspace="0" width="100%">
      </iframe>
      <!--<div id="IC_D_3x7_BCC"></div>-->
     </div>
     <div id="style-1" style="background-color:#fff; height:510px; overflow:auto; margin: 30px 0px 30px 0px; padding:0px 30px 20px 0px; border:1px solid #dfdfdf;">
      <div class="col-xs-6">
       <table class="historical_data_table table">
        <thead>
         <tr>
          <th colspan="2" style="text-align:center">
           Tesla Annual Revenue
           <br/>
           <span style="font-size:14px;">
            (Millions of US $)
           </span>
          </th>
         </tr>
        </thead>
        <tbody>
         <tr>
          <td style="text-align:center">
           2021
          </td>
          <td style="text-align:center">
           $53,823
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2020
          </td>
          <td style="text-align:center">
           $31,536
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2019
          </td>
          <td style="text-align:center">
           $24,578
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2018
          </td>
          <td style="text-align:center">
           $21,461
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2017
          </td>
          <td style="text-align:center">
           $11,759
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2016
          </td>
          <td style="text-align:center">
           $7,000
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2015
          </td>
          <td style="text-align:center">
           $4,046
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2014
          </td>
          <td style="text-align:center">
           $3,198
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2013
          </td>
          <td style="text-align:center">
           $2,013
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2012
          </td>
          <td style="text-align:center">
           $413
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2011
          </td>
          <td style="text-align:center">
           $204
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2010
          </td>
          <td style="text-align:center">
           $117
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2009
          </td>
          <td style="text-align:center">
           $112
          </td>
         </tr>
        </tbody>
       </table>
      </div>
      <div class="col-xs-6">
       <table class="historical_data_table table">
        <thead>
         <tr>
          <th colspan="2" style="text-align:center">
           Tesla Quarterly Revenue
           <br/>
           <span style="font-size:14px;">
            (Millions of US $)
           </span>
          </th>
         </tr>
        </thead>
        <tbody>
         <tr>
          <td style="text-align:center">
           2022-09-30
          </td>
          <td style="text-align:center">
           $21,454
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2022-06-30
          </td>
          <td style="text-align:center">
           $16,934
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2022-03-31
          </td>
          <td style="text-align:center">
           $18,756
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2021-12-31
          </td>
          <td style="text-align:center">
           $17,719
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2021-09-30
          </td>
          <td style="text-align:center">
           $13,757
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2021-06-30
          </td>
          <td style="text-align:center">
           $11,958
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2021-03-31
          </td>
          <td style="text-align:center">
           $10,389
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2020-12-31
          </td>
          <td style="text-align:center">
           $10,744
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2020-09-30
          </td>
          <td style="text-align:center">
           $8,771
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2020-06-30
          </td>
          <td style="text-align:center">
           $6,036
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2020-03-31
          </td>
          <td style="text-align:center">
           $5,985
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2019-12-31
          </td>
          <td style="text-align:center">
           $7,384
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2019-09-30
          </td>
          <td style="text-align:center">
           $6,303
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2019-06-30
          </td>
          <td style="text-align:center">
           $6,350
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2019-03-31
          </td>
          <td style="text-align:center">
           $4,541
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2018-12-31
          </td>
          <td style="text-align:center">
           $7,226
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2018-09-30
          </td>
          <td style="text-align:center">
           $6,824
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2018-06-30
          </td>
          <td style="text-align:center">
           $4,002
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2018-03-31
          </td>
          <td style="text-align:center">
           $3,409
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2017-12-31
          </td>
          <td style="text-align:center">
           $3,288
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2017-09-30
          </td>
          <td style="text-align:center">
           $2,985
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2017-06-30
          </td>
          <td style="text-align:center">
           $2,790
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2017-03-31
          </td>
          <td style="text-align:center">
           $2,696
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2016-12-31
          </td>
          <td style="text-align:center">
           $2,285
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2016-09-30
          </td>
          <td style="text-align:center">
           $2,298
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2016-06-30
          </td>
          <td style="text-align:center">
           $1,270
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2016-03-31
          </td>
          <td style="text-align:center">
           $1,147
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2015-12-31
          </td>
          <td style="text-align:center">
           $1,214
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2015-09-30
          </td>
          <td style="text-align:center">
           $937
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2015-06-30
          </td>
          <td style="text-align:center">
           $955
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2015-03-31
          </td>
          <td style="text-align:center">
           $940
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2014-12-31
          </td>
          <td style="text-align:center">
           $957
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2014-09-30
          </td>
          <td style="text-align:center">
           $852
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2014-06-30
          </td>
          <td style="text-align:center">
           $769
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2014-03-31
          </td>
          <td style="text-align:center">
           $621
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2013-12-31
          </td>
          <td style="text-align:center">
           $615
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2013-09-30
          </td>
          <td style="text-align:center">
           $431
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2013-06-30
          </td>
          <td style="text-align:center">
           $405
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2013-03-31
          </td>
          <td style="text-align:center">
           $562
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2012-12-31
          </td>
          <td style="text-align:center">
           $306
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2012-09-30
          </td>
          <td style="text-align:center">
           $50
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2012-06-30
          </td>
          <td style="text-align:center">
           $27
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2012-03-31
          </td>
          <td style="text-align:center">
           $30
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2011-12-31
          </td>
          <td style="text-align:center">
           $39
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2011-09-30
          </td>
          <td style="text-align:center">
           $58
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2011-06-30
          </td>
          <td style="text-align:center">
           $58
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2011-03-31
          </td>
          <td style="text-align:center">
           $49
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2010-12-31
          </td>
          <td style="text-align:center">
           $36
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2010-09-30
          </td>
          <td style="text-align:center">
           $31
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2010-06-30
          </td>
          <td style="text-align:center">
           $28
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2010-03-31
          </td>
          <td style="text-align:center">
           $21
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2009-12-31
          </td>
          <td style="text-align:center">
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2009-09-30
          </td>
          <td style="text-align:center">
           $46
          </td>
         </tr>
         <tr>
          <td style="text-align:center">
           2009-06-30
          </td>
          <td style="text-align:center">
           $27
          </td>
         </tr>
        </tbody>
       </table>
      </div>
     </div>
     <div style="background-color:#fff; margin: 0px 0px 20px 0px; padding:5px 50px 5px 10px; border:1px solid #dfdfdf;">
      <table class="historical_data_table table">
       <thead>
        <tr>
         <th style="text-align:center">
          Sector
         </th>
         <th style="text-align:center">
          Industry
         </th>
         <th style="text-align:center">
          Market Cap
         </th>
         <th style="text-align:center">
          Revenue
         </th>
        </tr>
       </thead>
       <tbody>
        <tr>
         <td style="text-align:center">
          <a href="https://www.macrotrends.net/stocks/sector/5/auto-tires-trucks">
           Auto/Tires/Trucks
          </a>
         </td>
         <td style="text-align:center">
          <a href="https://www.macrotrends.net/stocks/industry/7/">
           Auto Manufacturers - Domestic
          </a>
         </td>
         <td style="text-align:center">
          $549.575B
         </td>
         <td style="text-align:center">
          $53.823B
         </td>
        </tr>
        <tr>
         <td colspan="4" style="padding:15px;">
          <span>
           Tesla is the market leader in battery-powered electric car sales in the United States, with roughly 70% market share. The company's flagship Model 3 is the best-selling EV model in the United States. Tesla, which has managed to garner the reputation of a gold standard over the years, is now a far bigger entity that what it started off since its IPO in 2010, with its market cap crossing $1 trillion for the first time in October 2021.? The EV king's market capitalization is more than the combined value of legacy automakers including Toyota, Volkswagen, Daimler, General Motors and Ford.Over the years, Tesla has shifted from developing niche products for affluent buyers to making more affordable EVs for the masses. The firm's three-pronged business model approach of direct sales, servicing, and charging its EVs sets it apart from other carmakers. Tesla, which is touted as the clean energy revolutionary automaker, is much more than just a car manufacturer.
          </span>
         </td>
        </tr>
       </tbody>
      </table>
     </div>
     <div style="background-color:#fff; margin: 20px 0px 30px 0px; padding:5px 50px 5px 10px; border:1px solid #dfdfdf;">
      <table class="historical_data_table table">
       <thead>
        <tr>
         <th style="text-align:center; width:40%;">
          Stock Name
         </th>
         <th style="text-align:center; width:20%;">
          Country
         </th>
         <th style="text-align:center; width:20%;">
          Market Cap
         </th>
         <th style="text-align:center; width:20%;">
          PE Ratio
         </th>
        </tr>
       </thead>
       <tbody>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/GM/general-motors/revenue">
           General Motors (GM)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $53.930B
         </td>
         <td style="text-align:center">
          5.56
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/F/ford-motor/revenue">
           Ford Motor (F)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $52.668B
         </td>
         <td style="text-align:center">
          8.09
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/HOG/harley-davidson/revenue">
           Harley-Davidson (HOG)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $6.762B
         </td>
         <td style="text-align:center">
          9.56
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/PII/polaris/revenue">
           Polaris (PII)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $6.267B
         </td>
         <td style="text-align:center">
          11.86
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/IAA/iaa/revenue">
           IAA (IAA)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $5.134B
         </td>
         <td style="text-align:center">
          16.40
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/FSR/fisker/revenue">
           Fisker (FSR)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $2.261B
         </td>
         <td style="text-align:center">
          0.00
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/LEV/lion-electric/revenue">
           Lion Electric (LEV)
          </a>
         </td>
         <td style="text-align:center">
          Canada
         </td>
         <td style="text-align:center">
          $0.551B
         </td>
         <td style="text-align:center">
          0.00
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/VLTA/volta/revenue">
           Volta (VLTA)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $0.071B
         </td>
         <td style="text-align:center">
          0.00
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/BRDS/bird-global/revenue">
           Bird Global (BRDS)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $0.054B
         </td>
         <td style="text-align:center">
          0.00
         </td>
        </tr>
        <tr>
         <td style="text-align:left">
          <a href="/stocks/charts/ZEV/lightning-emotors/revenue">
           Lightning EMotors (ZEV)
          </a>
         </td>
         <td style="text-align:center">
          United States
         </td>
         <td style="text-align:center">
          $0.043B
         </td>
         <td style="text-align:center">
          0.00
         </td>
        </tr>
       </tbody>
      </table>
     </div>
     <div>
      <!-- Partner Center Ad Unit -->
      <div id="IC_728x214_1" style="width:728px; height:214px; margin-left:30px;">
      </div>
     </div>
    </div>
    <div "="" id="right_sidebar">
     <!--<a href="/stocks/stock-screener" style="text-decoration:none; color: #fff; ">
					<div style="margin:0px; padding: 20px; width:300px; background-color: #01579b; min-height:150px; text-align:center;">

						<h2 style="font-weight:600;">Try our new<br />stock screener!</h2></a>

					</div>
				</a>-->
     <!--<div style="margin-top:0px; min-height:250px;">

					<script src='//ads.investingchannel.com/adtags/Macrotrends/fundamentalanalysis/300x600.js?zhpos=300_2&multi_size=false' type='text/javascript' charset='utf-8'></script>

				</div>-->
     <div style="margin-top:0px; min-height:250px;">
      <div id="ic_300x250_1">
      </div>
     </div>
     <div id="sticky_ad_right" style="margin-top:30px; height:1000px;">
      <script id="dianomi_context_script" src="https://www.dianomi.com/js/contextfeed.js" type="text/javascript">
      </script>
      <div class="dianomi_context" data-dianomi-context-id="743">
      </div>
      <!-- <div id="IC_D_300x250_BCC"></div>-->
      <!--Smartad # 2981: Macrotrends - 300x670 Right Rail-->
      <iframe height="670" id="dianomi_sidebar" scrolling="NO" src="//www.dianomi.com/smartads.epl?id=4059" style="width: 300px; border: none; overflow: hidden;" width="300">
      </iframe>
      <div id="IC_D_300x250_BCC">
      </div>
     </div>
    </div>
   </div>
  </div>
  <!--This is the div for the IC OOP ad-->
  <div id="oopDivTag_1" style="width:1px;height:1px;">
  </div>
  <footer class="footer">
   <span>
    © 2010-2022 Macrotrends LLC
   </span>
   |
   <a href="/terms">
    Terms of Service
   </a>
   |
   <a href="/privacy">
    Privacy Policy
   </a>
   |
   <a href="mailto:%69n%66o@%6Dac%72otrends%2En%65t">
    Contact Us
   </a>
   |
   <a href="/ccpa">
    Do Not Sell My Personal Information
   </a>
   <br/>
   <span>
    Fundamental data from
   </span>
   <a href="https://www.zacksdata.com" rel="nofollow" target="_blank">
    Zacks Investment Research, Inc.
   </a>
  </footer>
  <div aria-hidden="true" aria-labelledby="exampleModalLabel" class="modal" id="smallWidthModal1" role="dialog" tabindex="-1">
   <div class="modal-dialog modal-lg">
    <div class="modal-content">
     <div class="modal-body">
      <div class="modal_title">
       <h2>
        <strong>
         We Need Your Support!
        </strong>
       </h2>
      </div>
      <p>
       Backlinks from other websites are the lifeblood of our site and a primary source of new traffic.
       <p>
        <p>
         If you use our chart images on your site or blog, we ask that you provide attribution via a "dofollow" link back to this page.  We have provided a few examples below that you can copy and paste to your site:
        </p>
        <br/>
        <table class="table">
         <thead>
          <tr>
           <th>
            Link Preview
           </th>
           <th>
            HTML Code (Click to Copy)
           </th>
          </tr>
         </thead>
         <tbody>
          <tr>
           <td>
            <a>
             Tesla Revenue 2010-2022 | TSLA
            </a>
           </td>
           <td>
            <input class="modal_link" size="60" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Tesla Revenue 2010-2022 | TSLA&lt;/a&gt;"/>
           </td>
          </tr>
          <tr>
           <td>
            <a>
             Macrotrends
            </a>
           </td>
           <td>
            <input class="modal_link" size="60" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Macrotrends&lt;/a&gt;"/>
           </td>
          </tr>
          <tr>
           <td>
            <a>
             Source
            </a>
           </td>
           <td>
            <input class="modal_link" size="60" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Source&lt;/a&gt;"/>
           </td>
          </tr>
         </tbody>
        </table>
        <br/>
        <p style="text-align:center">
         Your image export is now complete.  Please check your download folder.
        </p>
       </p>
      </p>
     </div>
     <div class="modal-footer">
      <button class="btn btn-primary" data-dismiss="modal" type="button">
       Close Window
      </button>
     </div>
    </div>
   </div>
  </div>
  <div aria-hidden="true" aria-labelledby="exampleModalLabel" class="modal" id="smallWidthModal2" role="dialog" tabindex="-1">
   <div class="modal-dialog modal-lg">
    <div class="modal-content">
     <div class="modal-body">
      <div class="modal_title">
       <h2>
        <strong>
         We Need Your Support!
        </strong>
       </h2>
      </div>
      <p>
       Backlinks from other websites are the lifeblood of our site and a primary source of new traffic.
       <p>
        <p>
         If you use our datasets on your site or blog, we ask that you provide attribution via a "dofollow" link back to this page.  We have provided a few examples below that you can copy and paste to your site:
        </p>
        <br/>
        <table class="table">
         <thead>
          <tr>
           <th>
            Link Preview
           </th>
           <th>
            HTML Code (Click to Copy)
           </th>
          </tr>
         </thead>
         <tbody>
          <tr>
           <td>
            <a>
             Tesla Revenue 2010-2022 | TSLA
            </a>
           </td>
           <td>
            <input class="modal_link" size="50" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Tesla Revenue 2010-2022 | TSLA&lt;/a&gt;"/>
           </td>
          </tr>
          <tr>
           <td>
            <a>
             Macrotrends
            </a>
           </td>
           <td>
            <input class="modal_link" size="50" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Macrotrends&lt;/a&gt;"/>
           </td>
          </tr>
          <tr>
           <td>
            <a>
             Source
            </a>
           </td>
           <td>
            <input class="modal_link" size="50" type="text" value="&lt;a href='https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'&gt;Source&lt;/a&gt;"/>
           </td>
          </tr>
         </tbody>
        </table>
        <br/>
        <p style="text-align:center">
         Your data export is now complete.  Please check your download folder.
        </p>
       </p>
      </p>
     </div>
     <div class="modal-footer">
      <button class="btn btn-primary" data-dismiss="modal" type="button">
       Close Window
      </button>
     </div>
    </div>
   </div>
  </div>
  <script type="text/javascript">
   $.typeahead({
		input: '.js-typeahead',
		minLength: 1,
		filter: false,  //Disables typahead filter to just show everything in the results from the database
		debug: false,
		highlight: true,
		maxItem: 10,
		dynamic: true,
		delay: 200,
		searchOnFocus: true,
		backdrop: {
			"background-color": "#fff"
		},
		href: "{{url}}",
		emptyTemplate: "no result for {{query}}",
		display: ["name"],
		source: {
			users: {
				ajax: {
					url: '/assets/php/all_pages_query.php',
					data: {
						q: '{{query}}'
					}
				}
			}
		}
	});
  </script>
  <script>
   // /*! js-cookie v3.0.0-rc.1 | MIT */
	// !function(e,t){"object"==typeof exports&&"undefined"!=typeof module?module.exports=t():"function"==typeof define&&define.amd?define(t):(e=e||self,function(){var n=e.Cookies,r=e.Cookies=t();r.noConflict=function(){return e.Cookies=n,r}}())}(this,function(){"use strict";function e(e){for(var t=1;t<arguments.length;t++){var n=arguments[t];for(var r in n)e[r]=n[r]}return e}var t={read:function(e){return e.replace(/(%[\dA-F]{2})+/gi,decodeURIComponent)},write:function(e){return encodeURIComponent(e).replace(/%(2[346BF]|3[AC-F]|40|5[BDE]|60|7[BCD])/g,decodeURIComponent)}};return function n(r,o){function i(t,n,i){if("undefined"!=typeof document){"number"==typeof(i=e({},o,i)).expires&&(i.expires=new Date(Date.now()+864e5*i.expires)),i.expires&&(i.expires=i.expires.toUTCString()),t=encodeURIComponent(t).replace(/%(2[346B]|5E|60|7C)/g,decodeURIComponent).replace(/[()]/g,escape),n=r.write(n,t);var c="";for(var u in i)i[u]&&(c+="; "+u,!0!==i[u]&&(c+="="+i[u].split(";")[0]));return document.cookie=t+"="+n+c}}return Object.create({set:i,get:function(e){if("undefined"!=typeof document&&(!arguments.length||e)){for(var n=document.cookie?document.cookie.split("; "):[],o={},i=0;i<n.length;i++){var c=n[i].split("="),u=c.slice(1).join("=");'"'===u[0]&&(u=u.slice(1,-1));try{var f=t.read(c[0]);if(o[f]=r.read(u,f),e===f)break}catch(e){}}return e?o[e]:o}},remove:function(t,n){i(t,"",e({},n,{expires:-1}))},withAttributes:function(t){return n(this.converter,e({},this.attributes,t))},withConverter:function(t){return n(e({},this.converter,t),this.attributes)}},{attributes:{value:Object.freeze(o)},converter:{value:Object.freeze(r)}})}(t,{path:"/"})});

			
	// // Cookie Settings
	// var maxCookieValue = 4, initCookie = 1, expirationDays = 1;
	// var cookieName = "session_pageviews";
	// var getCookie = Cookies.get(cookieName);

	// // Under the Hood
	// if (getCookie == null) {
		// Cookies.set(cookieName, initCookie, { expires: expirationDays });
		// console.log('Cookie set to value 1');
		// $( "#ic_video_ad" ).append( "<div id=\"IC_D_3x6\" style=\"margin:30px;\"></div>" );
	// } else {
		// if (getCookie >= initCookie && getCookie < maxCookieValue) {
			// getCookie++;
			// Cookies.set(cookieName, getCookie, { expires: expirationDays });
			// console.log('Cookie incremented. New value is ' + getCookie);
			// $( "#ic_video_ad" ).append( "<div id=\"IC_D_3x6\" style=\"margin:30px;\"></div>" );
		// }
		// else if (getCookie >= maxCookieValue && getCookie < 7) {
			// getCookie++;
			// Cookies.set(cookieName, getCookie, { expires: expirationDays });
			// console.log('Cookie max allowed value reached. No video ads showing. New value is ' + getCookie);
			// //Cookies.remove(cookieName);
			// // if cookie is equal with the number you've set, then do something
			// // hide an element, delete the cookie etc...
		// }
		// else if (getCookie >= 7) {
			// Cookies.remove(cookieName);
			// // if cookie is equal with the number you've set, then do something
			// // hide an element, delete the cookie etc...
		// }	
	// }
  </script>
  <script>
   $(document).ready(function() {
	
	var user_data = '171.76.81.154';	var country_code = 'United States';
	$.post('https://www.macrotrends.net/assets/php/user_frequency_tracking.php', {user_ip: user_data, user_country: country_code}); 

	// Selects all of the text in the chart export window when clicked
	$(".modal_link").focus(function() {
		var $this = $(this);
		$this.select();

		// Work around Chrome's little problem
		$this.mouseup(function() {
			// Prevent further mouseup intervention
			$this.unbind("mouseup");
			return false;
		});
	});	
	
	
	$('[data-toggle="tooltip"]').tooltip();
	
    $('.statement_type_select').select2({
	
	theme: "classic",
	minimumResultsForSearch: 20
	
	});

    $('.frequency_select').select2({
	
	theme: "classic",
	minimumResultsForSearch: 20
	
	});
	
	
});

$( "#compareStocks" ).click(function() {
	
	
	window.location.href = '/stocks/stock-comparison?s=revenue&axis=single&comp=TSLA';
	
	
});

$( "#chartExport" ).click(function() {
	
		window.$('#smallWidthModal1').modal();

		//Turn off scroll bar for image export
		chart.chartScrollbarSettings.enabled = false;
		chart.validateNow(); 
		
		
		chart.export.capture({},function() {
			this.toPNG({},function(data) {
				// Download the image to the browser
				this.download( data, "image/png", "TSLA-revenue-2022-12-09-macrotrends.png" );
				
				});

		//Turn scroll bar back on again
		chart.chartScrollbarSettings.enabled = true;
		chart.validateNow(); 
				
	});

});

$( ".statement_type_select" ).change(function() {
  
  window.location.href = 'https://testing.macrotrends.net/assets/php/income_statement_testing.php?t=ZEV&type=' + this.value + '&freq=Q';

});

$( ".frequency_select" ).change(function() {
  
  window.location.href = '/assets/php/new_chart_page.php?t=ZEV&type=revenue&freq=' + this.value;

});
  </script>
  <!--<div class="modal" id="contribute_modal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="false">
  <div class="modal-dialog modal-lg">
    <div class="modal-content">
      <div class="modal-body" style="margin:20px 40px 20px 40px; text-align:left;font-size:18px;">
	  	  


<div class="row">

<div class="col-xs-6">

<script src="https://donorbox.org/widget.js" paypalExpress="true"></script><iframe src="https://donorbox.org/embed/macrotrends-donations?hide_donation_meter=true" height="685px" width="100%" style="max-width:500px; min-width:310px; max-height:none!important" seamless="seamless" name="donorbox" frameborder="0" scrolling="no" allowpaymentrequest></iframe>

</div>

<div class="col-xs-6">

		<div class="modal_title"><h1><strong>We Need Your Support!</strong></h1></div>

		<p><strong>Macrotrends has been subscription-free since 2010 and we want to keep it that way.</strong></p>

<p>Our goal has always been to serve as an easily accessible, high quality source of investment research for both professionals and amateurs alike.</p>

<p>Any amount that you can contribute will help ensure we can keep the site completely free for many years to come.</p>

<p style="margin-top:20px;">Regards,</p>
<p>The Macrotrends Team</p>

</div>

</div>

</div>

      <div class="modal-footer" style="text-align:center;">
        <button type="button" class="btn btn-success" data-dismiss="modal">Maybe Next Time...</button>
      </div>
    </div>
  </div>
</div>	


<script src="/ads.js" type="text/javascript"></script>

<script>

$(document).ready(function() {
	
	var botPattern = "(googlebot\/|Googlebot-Mobile|Googlebot-Image|Google favicon|Mediapartners-Google|bingbot|slurp|java|wget|curl|Commons-HttpClient|Python-urllib|libwww|httpunit|nutch|phpcrawl|msnbot|jyxobot|FAST-WebCrawler|FAST Enterprise Crawler|biglotron|teoma|convera|seekbot|gigablast|exabot|ngbot|ia_archiver|GingerCrawler|webmon |httrack|webcrawler|grub.org|UsineNouvelleCrawler|antibot|netresearchserver|speedy|fluffy|bibnum.bnf|findlink|msrbot|panscient|yacybot|AISearchBot|IOI|ips-agent|tagoobot|MJ12bot|dotbot|woriobot|yanga|buzzbot|mlbot|yandexbot|purebot|Linguee Bot|Voyager|CyberPatrol|voilabot|baiduspider|citeseerxbot|spbot|twengabot|postrank|turnitinbot|scribdbot|page2rss|sitebot|linkdex|Adidxbot|blekkobot|ezooms|dotbot|Mail.RU_Bot|discobot|heritrix|findthatfile|europarchive.org|NerdByNature.Bot|sistrix crawler|ahrefsbot|Aboundex|domaincrawler|wbsearchbot|summify|ccbot|edisterbot|seznambot|ec2linkfinder|gslfbot|aihitbot|intelium_bot|facebookexternalhit|yeti|RetrevoPageAnalyzer|lb-spider|sogou|lssbot|careerbot|wotbox|wocbot|ichiro|DuckDuckBot|lssrocketcrawler|drupact|webcompanycrawler|acoonbot|openindexspider|gnam gnam spider|web-archive-net.com.bot|backlinkcrawler|coccoc|integromedb|content crawler spider|toplistbot|seokicks-robot|it2media-domain-crawler|ip-web-crawler.com|siteexplorer.info|elisabot|proximic|changedetection|blexbot|arabot|WeSEE:Search|niki-bot|CrystalSemanticsBot|rogerbot|360Spider|psbot|InterfaxScanBot|Lipperhey SEO Service|CC Metadata Scaper|g00g1e.net|GrapeshotCrawler|urlappendbot|brainobot|fr-crawler|binlar|SimpleCrawler|Livelapbot|Twitterbot|cXensebot|smtbot|bnf.fr_bot|A6-Indexer|ADmantX|Facebot|Twitterbot|OrangeBot|memorybot|AdvBot|MegaIndex|SemanticScholarBot|ltx71|nerdybot|xovibot|BUbiNG|Qwantify|archive.org_bot|Applebot|TweetmemeBot|crawler4j|findxbot|SemrushBot|yoozBot|lipperhey|y!j-asr|Domain Re-Animator Bot|AddThis)";

	var re = new RegExp(botPattern, 'i');

	if (re.test(navigator.userAgent)) {
		
	} else {
		
		//Check to see whether they are running an ad blocker
		if(document.getElementById('12mORwMnaEkJXlxz')){
		  var ad_blocker = 'N';
		} else {
		  var ad_blocker = 'Y';
		}

		$.post('https://api.ipstack.com/check?access_key=14fe63e83d5cfefa0b3d4cec498479ba&output=json&fields=ip,continent_name,country_name,region_name,city', 
		function(ip_data){
			
			$.post('https://www.macrotrends.net/assets/php/page_view_tracking.php', {ip: ip_data.ip,continent: ip_data.continent_name, country: ip_data.country_name, state: ip_data.region_name, city: ip_data.city, screen_width: screen.width, ads: ad_blocker, page_type: 'stock'}, 
				function(data){
					/*					
					if(data % 20 === 0) {
						
						//$('#contribute_modal').modal();
						
					}
					*/
				});
		
		});


	}
	

});


$.post('https://api.ipstack.com/check?access_key=14fe63e83d5cfefa0b3d4cec498479ba&output=json&fields=ip,continent_name,country_name,region_name,city', 
function(ip_data){
	
	$(".contribute_user_id").val(ip_data.ip);
	
});

$( ".donate_buttons" ).click(function() {
  
	var payment = $(this).attr("value");

	$.post('https://api.ipstack.com/check?access_key=14fe63e83d5cfefa0b3d4cec498479ba&output=json&fields=ip,continent_name,country_name,region_name,city', 
		function(ip_data){
					
		$.post('https://www.macrotrends.net/assets/php/page_view_tracking.php', {ip: ip_data.ip, paid: payment}); 
	
	});
		 
});

</script>

-->
  <script type="text/javascript">
   var clicky_site_ids = clicky_site_ids || [];
clicky_site_ids.push(100827248);
(function() {
  var s = document.createElement('script');
  s.type = 'text/javascript';
  s.async = true;
  s.src = '//static.getclicky.com/js';
  ( document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0] ).appendChild( s );
})();
  </script>
  <noscript>
   <p>
    <img alt="Clicky" height="1" src="//in.getclicky.com/100827248ns.gif" width="1"/>
   </p>
  </noscript>
  <!-- This site is converting visitors into subscribers and customers with OptinMonster - https://optinmonster.com -->
  <!-- <script type="text/javascript" src="https://a.omappapi.com/app/js/api.min.js" data-account="6392" data-user="15772" async></script> -->
  <!-- / OptinMonster -->
 </body>
</html>

Using BeautifulSoup or the read_html function extract the table with GameStop Revenue and store it into a dataframe named gme_revenue. The dataframe should have columns Date and Revenue. Make sure the comma and dollar sign is removed from the Revenue column using a method similar to what you did in Question 2.

Click here if you need help locating the table
gme_revenue = pd.DataFrame(columns = ["Date","Revenue"])
​
for table in soup.find_all('table'):
    if table.find('th').getText().startswith("GameStop Quarterly Revenue"):
        for row in table.find("tbody").find_all("tr"):
            col = row.find_all("td")
            if len(col) != 2: continue
            Date = col[0].text
            Revenue = col[1].text.replace("$","").replace(",","")
               
            gme_revenue = gme_revenue.append({"Date":Date, "Revenue":Revenue}, ignore_index=True)
Display the last five rows of the gme_revenue dataframe using the tail function. Take a screenshot of the results.

gme_revenue.tail(5)
Date	Revenue
Question 5: Plot Tesla Stock Graph
Use the make_graph function to graph the Tesla Stock Data, also provide a title for the graph. The structure to call the make_graph function is make_graph(tesla_data, tesla_revenue, 'Tesla'). Note the graph will only show data upto June 2021.

make_graph(tesla_data, tesla_revenue, 'Tesla')
Question 6: Plot GameStop Stock Graph
Use the make_graph function to graph the GameStop Stock Data, also provide a title for the graph. The structure to call the make_graph function is make_graph(gme_data, gme_revenue, 'GameStop'). Note the graph will only show data upto June 2021.

​
make_graph(gme_data, gme_revenue, 'GameStop')






About the Authors:
Joseph Santarcangelo has a PhD in Electrical Engineering, his research focused on using machine learning, signal processing, and computer vision to determine how videos impact human cognition. Joseph has been working for IBM since he completed his PhD.

Azim Hirjani
