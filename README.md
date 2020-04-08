
# Learn Python for Data science

`Video` : <https://www.youtube.com/watch?v=T5pRlIbr6gg&list=PL2-dafEMk2A6QKz1mrk1uIGfHkC1zZ6UU>
#### Video 1.  
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



           
