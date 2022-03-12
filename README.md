## <h2 align="center"> <hr/>Stock Prices Prediction Based on Social Influence & Historic Data<hr/> </h2>

<h2 align= "center">Abstract</h2>
                                         
> <p align="justify"> Stock market price prediction is a challenging issue as it is impacted by a range of elements including political statements, economic circumstances, business market value, historical stock price, and so on. Hence study exhibit that many prebuild models like: ARIMA or deep learning model like:LSTM but their efficiency is not up to mark for stock price prediction . In this paper, we build hybrid model which is blended with CNN and LSTM to improve the performance. We used historical data (prior stock price) in the form of numerical information from of the NIFTY50 from 2015 to 2020, as well as news data in textual form from the @NDTVProfit twitter account. In addition, we used a variety of prebuild models and deep learning models to forecast the next 10 days’ values. We initiated with numerals / historical dataset and applied ARIMA, SARIMAX, Facebook prophet and LSTM on historical datasts and we got error score 1062, 964, 709 and 285 respectively . In addition we applied all model like: ARIMA, SARIMAX, Facebook prophet and LSTM on combined dataset (historical datasts+news datasets) and obtained error score 789,655,380 and 170. The new hybrid model which is blended with CNN and LSTM deep learning models is applied on combined dataset and 89 error score was obtained which is better as compared to all previous models.</p>
 
> **Keywords :- Deep Learning, Stock Price, Lstm, Arima, Sarimax, Facebook Prophet, Rmse.**

 <h2 align= "center">Introduction</h2>
 
> <p align="justify"> From past many years, analysts and scholars have been interested in predicting stock market values. Stock prices are difficult to anticipate because of their significant volatility, which is influenced by a variety of political and economic issues, as well as changes in leadership, investor attitude, and a variety of other factors. Stock price forecasting based only on historical data and textual information has shown to be ineffective. Investor views and mood about the overall financial markets, particularly specific sectors and assets, are measured by market sentiment. Hence Stock market price is a challenging issue and needs to be resolved in optimized way.</p>

> <p align="justify"> For active traders and long-term investors, positive and negative emotion enhances price behaviour and generates trading and investing possibilities. According to existing sentiment research studies there is a high association between stock price swings and the release of news stories. Using machine learning and deep learning methods likes SVM, Naive Bayesian and LSTM, Sentiments analysis research have been done. The quantity of training data given determines the accuracy of the deep learning algorithm.</p>

> <p align="justify"> In this work, two types of data has been collected data. First one is Textual or news data which was collected from twitter username @NDTVprofit and second one was numeric data or stock price data which was collected from NIFTY50 from 2015 to 2020. In addition, we cleaned and preprocessed our data then applied some prebuild model like: ARIMA,SARIMAX,Facebook Prophet on only numerical data and we got 1062,964 and 709 error score respectively then we applied deep learning model LSTM and we got 285 error score then we applied all the models on combined dataset (numerical + textual) and we got 789,655,380 and 170 respectively. Since the error score is not upto the mark, we build a new hybrid model which is combination of LSTM and CNN.The hybrid model is applied on combined dataset and 89 error score was obtained which is better as compared to all previous models. Contribution of this paper is improvement of the stock market prediction. We combined deep learning models LSTM and CNN as well as taking multiples learning rate , various activation and loss function to improve our model .The hybrid model exhibit good performance to the as compare to the previous models. </p>

<h2 align= "center"> Proposed Model </h2>

> <p align="justify"> Predict stock prices using social history news data and a shared platform that comprises the five stages below and refer our model in figure 1: In the first stage, the dataset is scraped. The stock data comes from investing.com, while the news data comes from @NDTVProfit on Twitter. The data is then scrubbed and preprocessed. During the second stage Word tokenization, stopword deletion, text segmentation, word vectorization, and word segmentation are all applied to Twitter data.The data is normalised using inventory data.</p>

> #### The procedure for cleaning data is as follows:

> - Remove all of the numbers.
> - Make all of the letters lowercase.
> - In your manuscript, remove all hashtags and @ symbols.
> - Remove any links from your website that begin with http, pic.twitter.com, or https.
> - Remove ETMarkets, ndtv, moneycontrol, market update, biznews, NewsAlert, and other similar phrases from the list.

> <p align="justify"> In the third step, features are extracted from the preprocessed text. A statistical model of text representation was used to extract features.In the fourth phase, VADER was used to do sentiment analysis on Twitter data. VADER is a wonderful choice since it performs well in this situation, particularly for social media messages.Phase 5 entails transmitting the processed data to several machine learning models as input. </p>

<img src="./Image/Flowchart.jpg" alt="Proposed model" width="100%" height="auto"/>

_<h4 align= "center">Flow Chart</h2>_

<br/>

<h2 align= "center">Hybrid Model (LSTM+CNN)</h2>

> Implementation of
> Hybrid Model:

<img src="./Image/Structure of LSTM_CNN.jpg" alt="Proposed model" width="100%" height="550px"/>

_<h4 align= "center">Structure of Hybrid model</h2>_

> <p align="justify"> We may deduce that the particular model is developed as present in the sample on the CNN LSTM show’s variable choices: The learning set’s input data is a tri information vector (Zero, 10, 8), where 10 specifies the temporal step size and 8 denotes the input planet eight attributes.The input is first processed through a one-dimensional convolution layer, which extracts further information and provides a three- dimensional output sequence (None, 10, 32), with 32 becoming the size of the convolution layer filters. In the pooling layer, the vector is then converted into a three- dimensional output vector (None, 10, 32). The output vector is sent to the LSTM layer after training, and the output data (None, 64) is fed into a complete means of communication with the output value; the current hidden units in the Hidden layers is 64.</p>

<br/>

<h2 align= "center"> Result Table</h2>

<h4 align= "center">

|          Model Name        |      RMSE   |
| -------------------------- | ------------|
|  LSTM                      |      285    |
|  ARIMA                     |      1062   |
|  SARIMAX                   |      964    |
|  FB Prophet                |      709    |
|  LSTM on New Data          |      170    |
|  Arima on New Data         |      789    |
|  SARIMA on New Data        |      655    |
|  FB Prophet on New Data    |      380    |
|  Hybrid Model(LSTM + CNN)  |      89     |
</h4>


> <p align="justify"> This Table consist of results of various prebuild and deep learning models.we got results from Facebook prophet, SARIMAX, ARIMA, LSTM is 709, 964, 1062 and 285 respectively on numerical data or historical data and also we got results from Facebook prophet, SARIMAX, ARIMA, LSTM is 380, 655, 789 and 170 respectively on combined datasets. We got improved results in hybrid model which is 89 error score on combined dataset and ARIMA model gave us worst results which is 1062 error score on combined dataset. Which is shown in table. </p>

 <h2 align= "center"> Conclusion </h2>
 
 > <p align="justify"> We discuss how to analyse time data and develop Deep learning models from a development standpoint in this paper. The most difficult time series to anticipate is stock prices, and we can do it with great accuracy for the Nifty Index Data. Because our RMSE value was the lowest compared to the other models’ RMSE values, our Hybrid model (LSTM+CNN) predicted the best result out of all the pre-build models we investigated, as shown in the Result table. </p>

> #### However, the following suggestions might help you boost your performance even more:

> - Gather news data for a longer period of time in order to have more data points.
> - Quantization of the model to int8 may be employed for even quicker prediction, but it will degrade the accuracy significantly.
> - According to recent study, reinforcement learning,also known as GAN, can be used to better correctly anticipate the stock market
> - Anomalies may be better addressed by retraining the data with the appropriate sentiment ratings using a customized trained sentiment analyzer.
> - Machine Learning When dealing with large volumes of data, models are quite useful. Because we only have a limited quantity of data on stock prices.

---

 <h2 align="center"> ** Thank YOU ** </h2> 
 
 ***
