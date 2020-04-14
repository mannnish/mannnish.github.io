
# Learn Python for Data science

`Video` : <https://www.youtube.com/watch?v=T5pRlIbr6gg&list=PL2-dafEMk2A6QKz1mrk1uIGfHkC1zZ6UU>
#### Video 1.  Basic ML Classifier
install python
  
setup pip by typing  `py -m pip install -U pip`
  
add scikit package by writing `py -m pip install -U scikit-learn`
  
after this done you can code your first project to tell the gender with just few details like height, weight and shoe size
          
          from sklearn import tree

          # [height, weight, shoe_size]
          X = [[181, 80, 44], [177, 70, 43], [160, 60, 38], [154, 54, 37], [166, 65, 40],
               [190, 90, 47], [175, 64, 39],
               [177, 70, 40], [159, 55, 37], [171, 75, 42], [181, 85, 43]]

          Y = ['male', 'male', 'female', 'female', 'male', 'male', 'female', 'female',
               'female', 'male', 'male']

          clf = tree.DecisionTreeClassifier()
          clf = clf.fit(X,Y)

          pred = clf.predict([[155,63,37]])
          print(pred)

#### Video 2.  Find Emotions from Text(Tweet)
register yourself on twitter dev. website, from there get your consumer API keys 

install the dependency 

    py -m pip install tweepy
    py -m pip install textblob
    py
    >>> import nltk
    >>> nltk.download('punkt')
    >>> nltk.download('averaged_perceptron_tagger')

and run this code to get the tags and word and check if the dependencies have been installed properly

    from textblob import TextBlob
    wiki = TextBlob("Manish is happy, and not angry")
    print(wiki.words)
    # -1(sad) to 1(happy)
    print(wiki.sentiment.polarity)
    
this is the code to generate things

    import tweepy
    from textblob import TextBlob

    consumer_key= ' PASTE HERE '
    consumer_secret= ' PASTE HERE '
    access_token=' PASTE HERE '
    access_token_secret=' PASTE HERE '

    auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
    auth.set_access_token(access_token, access_token_secret)
    api = tweepy.API(auth)
    public_tweets = api.search('Trump')

    for tweet in public_tweets:
        #print(tweet.text)
        analysis = TextBlob(tweet.text)
        # this is just experiment but you get the idea right
        if analysis.sentiment.polarity < 0:
            print(tweet.text)
            print(analysis.sentiment)
            
#### Video 3.
