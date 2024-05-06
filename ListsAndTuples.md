Compound Data Types: Lists and Tuples
Tuples - an ordered sequence    Ratings = (10,9,6,5,10,8,9,6,2) **enclosed in parenthesis**
  strings, ints and floats can all be contained in a tuple   tuple1 = ('disco',10,1.2)
  type(tuple1) = tuple
  each element can be accessed by an index (0,1,2) 
  tuple1[0]: "disco"
  can also use a negative index beginning with -1 for the last element and going backward. 
  can also concatinate tuples
  slicing works like strings where a tuple equals ("disco",10,1.2,"hard rock",10)
    tuple2[0:3]:  ('disco',10,1.2)
    (the last index is one larger than the last element you want)
  tuples are immutable
  we must created a new tuple for example in a sort RatingsSorted = sorted(Ratings)
  a tuple can contain other tuples as well. 
  get the type with   type(tuple1)
  get the length with len(tuple1)
  Ratings = (0,9,6,5,10,8,9,6,2)
  RatingsSorted = sorted(Ratings)
  genres_tuple.index("disco")    :7
  or "disco" in genres_tuple   :True

Lists - an order sequece represented by an ordered list enclosed in **square brackets** 
  L - ["Michael Jackes",10.1,1982,"MJ",1]
   strings, ints and floats can all be contained in a List
   Lists are mutable and can be extended using L.extend(["pop",10])
   To change element 0 of the list use:  L[0]: "Michael Jackson"
   a negative index can also be used. 
   Lists can be sliced  L[3:5]: ["MJ",1]    the last index is 1 higher than the last element 
   Lists can be concatenated by adding them L1 = L+["pop",10]
    A = [1, 'a']
    B = [2. 1. 'd']
    C = A + B
   append adds a single item to the end of the list - this could also be a list - making it a nested list.
   extend adds multiple elements to the end of a list.
   delete an element with the index of the element in the list     del(L[0])
   split to convert a string to a list "A,B,C,D".split(",")
   when we set B = L both variables are referencing the same list 
      if we change the first element of B we also change the first element of L
   use help(L)  to fhid our what other things can be done with a list.
   A list can be cloned using the following syntax  -   B = A[:]
      B references a new copy of the original list
  Slicing a tuple will result in new tuples with the corresponding elements
  
  
