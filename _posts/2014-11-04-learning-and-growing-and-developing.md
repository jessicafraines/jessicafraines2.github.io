---
layout: post
title:  "Learning and Growing and Developing"
date:   2014-11-04 15:34:42
categories: jekyll update
---

We are slowly building up our portfolio. Learning new things every day and becoming real live developers. It is a slow process, I'm not going to lie. All the tutorials and self-teaching that we may have done ahead of time only scratched the surface. Now we are put to the test with projects like, build a chess game. Sounds simple enough, doesn't it? Well for a bunch of newbies, not so much. Do you know how many rules there are for each piece in a game of chess? Could you write them all out? Now try coding it. Well we are doing just that, but in teams of four. This works really well, because it has taken all four of the brains in my group to even get a board to display. It started off as a 24 hour project, beginning last Thursday. Then my teacher pushed it through end of day Monday. Now I think we will have most of today to finish it up. My group is almost done. On the edge of completion. We can see light at the end of the tunnel. All we are lacking are the click events to get the pieces to move. The repo is currently on one of my classmate's Github account, but as soon as it is complete I will fork it to mine and share the link here.

We have also touched on a few new things in the past week. [JQuery](http://jquery.com/) was introduced and we are now trying to figure out how to work it into our code. It seems daunting at this point, but from what I hear it will make things much easier. 

We also talked about testing today. An extremely necessary function, but equally painful. Our focus was on [Qunit](http://qunitjs.com/), pronounced Q Unit. Qunit is a JavaScript unit testing framework. You start by adding the appropriate links in the HTML document.

    <!DOCTYPE html>
    <html>
      <head>
        <meta charset="utf-8">
        <title>Title here</title>
        <link rel="stylesheet" href="//code.jquery.com/qunit/qunit-1.15.0.css"> <==== HERE
      </head>
      <body>
        <div id="qunit"></div>  <==== HERE
        <div id="qunit-fixture"></div>  <====HERE
        <script src=//code.jquery.com/qunit/qunit-1.15.0.js"></script>  <==== HERE
        <script src="js/tests.js"></script>  <==== AND HERE
      </body>
    </html>

Then you open a test.js file in the your scripts folder. This is where you write all your tests. The examples that we worked on today were testing various [Lodash](https://lodash.com/) functions. The example that I am providing below was testing an array for the number 6, string "6" or string "six".

    QUnit.test("filter numbers with sixes", function(assert){
      var array = [1, 6, 8, 13, 16, 'three', 'six', '75', '76'];
      var arrayWithOnlySixes = [6, 16, 666, 'six', '76'];

      assert.deepEqual( onlySixes(array), arrayWithOnlySixes);
    });
    
The first line just states what we are testing. The second and third lines are the arrays that we will be using for our tests. The last line says that we will use an "onlySixes" function with the argument "array" and the result should be an array with only sixes. You will notice we used "deepEqual" instead of just "equal". The reason for this is that we are actually testing what is inside of the array. If we were testing the arrays in general, we would just use "equal".
    
Next you open a main.js file in your scripts folder. This is where you write the actual functions that you are testing. Here is the function for the test that we wrote above. 
    
    function onlySixes(array){
      return _.filter(array, function(item){
        return item.toString().indexOf('6') !== -1 ||
               item.toString().indexOf('six') !== -1
      });
    }

The first line is the function that we are testing. The second line is a "JQuery" method which returns elements that match a certain criteria. The third and fourth line use the method ".toString()" to convert the items to strings and returns the results that we are looking for.

Sound confusing? I hope so, because I don't want to be the only one confused. I'm told once I get this down, it will really help with writing code so I am all for it.

Well this turned out much longer than I intended, so I will call it here. I hope it helps!
