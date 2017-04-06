# CSS specificity & point model
CSS specificity rules help the browser determine what CSS specifications to honor when there are conflicts.

Inheritance does work from a top to bottom priority setting.


In this example, the lowest set CSS settings will be interpreted.

'''
.favorite {
   color: red;
}
.favorite {
   color: black;
}
'''

What often confuses is when expected inheritance does not work as excepted. CSS specificity could be the culprit at work.

'''
.favorite#cool {
   color: red;
}
.favorite {
   color: black;
}

'''

In the above example ".favorite#cool" has a higher specificity value. CSS applies different specificity wights to classes and ID's. An ID considered extremely specific.


Here is how specificity is calculated.

IMAGE HERE.


Here are sample calculations.

https://specificity.keegan.st/

ul#nav li.active a



