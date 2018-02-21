Curl Widget-[http://Builds%20a%20command%20line%20for%20%27curl/wget%27%20tools%20to%20enable%20the%20download%20of%20data%20on%20a%20console%20only%20session.]

!wget --header="Host: nlp.stanford.edu" --header="User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/63.0.3239.132 Safari/537.36" --header="Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,/;q=0.8" --header="Accept-Language: en-US,en;q=0.9" --header="Cookie: _ga=GA1.2.873806258.1516337648; _gid=GA1.2.1139333875.1517031430" --header="Connection: keep-alive" "https://nlp.stanford.edu/software/GloVe-1.2.zip" -O "GloVe-1.2.zip" -c

[2:42 PM] !ls !unzip GloVe-1.2.zip !ls !pip install keras !pip install fastai import pandas as pd test = pd.DataFrame() test.to_csv('test.csv')

[2:43 PM] from google.colab import files files.download(filename='test.csv') !ls !ls datalab !pip install gensim

[http://forums.fast.ai/t/colaboratory-and-fastai/10122 [https://colab.research.google.com/notebook#fileId=1aolUxkEYWiz_ofKhy_AZNRJKLrCMeOZx&scrollTo=xc0L0mK_Ye7T [https://colab.research.google.com/notebook#fileId=1Yhmmws6eelhXs2WQHJ7BUMQO9Wu5MoQj&scrollTo=FJPKhur_wFwc [https://towardsdatascience.com/fast-ai-lesson-1-on-google-colab-free-gpu-d2af89f53604 [https://colab.research.google.com/notebook#fileId=1v-yZk-W4YXOxLTLi7bekDw2ZWZXWW216&scrollTo=mKaIFIz17_bY ---xlrd

[https://medium.com/ai-saturdays/kaggle-planet-competition-how-to-land-in-top-4-a679ff0013ba---Kaggle Planet Competition: How to land in top ---kaggle-cli

[https://github.com/floydwch/kaggle-cli

#To extract .7z files 7z x -so <file_name>.7z | tar xf - #To extract.zip files unzip <file_name>.zip
