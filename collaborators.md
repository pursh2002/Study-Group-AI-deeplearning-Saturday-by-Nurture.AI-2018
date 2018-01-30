!wget --header="Host: nlp.stanford.edu" --header="User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/63.0.3239.132 Safari/537.36" --header="Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8" --header="Accept-Language: en-US,en;q=0.9" --header="Cookie: _ga=GA1.2.873806258.1516337648; _gid=GA1.2.1139333875.1517031430" --header="Connection: keep-alive" "https://nlp.stanford.edu/software/GloVe-1.2.zip" -O "GloVe-1.2.zip" -c

[2:42 PM]
!ls
!unzip GloVe-1.2.zip
!ls
!pip install keras
!pip install fastai
import pandas as pd
test = pd.DataFrame()
test.to_csv('test.csv')

[2:43 PM]
from google.colab import files
files.download(filename='test.csv')
!ls
!ls datalab
!pip install gensim

[http://forums.fast.ai/t/colaboratory-and-fastai/10122
[https://colab.research.google.com/notebook#fileId=1Yhmmws6eelhXs2WQHJ7BUMQO9Wu5MoQj&scrollTo=FJPKhur_wFwc
