# tweet-graph

****About this project:

This project analyse the social netwok of a user by: 

    # Plot conections:
        Plot a map with all the conections of user 
            (acording to certain level)

                [1]
                / \
            [2]     [3]
           / \      / \
        [4]  [5]  [6] [7]

    # Most Valuable conection: 
        Find the friends with more conections
    
    # Balance network
        Propouse a solution of conections to add in order to
        balance the three of user`

    # Shortest path <user a> <user b>
        Find the shortest path between 2 users ( if exist )

****INSTRUCTIONS:

---First of all, this project was proved on Ubuntu 16.04 OS---
    ---Run this instructions on terminal of linux---
    
------------------------------------------------------------------
----------------Programs that have to be installed----------------
------------------------------------------------------------------

   -Pip:
        sudo apt-get install python-pip python-dev build-essential 
        sudo pip install --upgrade pip 
        sudo pip install --upgrade virtualenv
   -Tweepy:
        sudo pip install tweepy
   -Npm:
        sudo apt-get update
        sudo apt-get install nodejs
        sudo apt-get install npm
   -Firebase-import:
         npm install firebase-import
         export PATH=$PATH:`npm bin`
         
   

1) Gather user information from tweeter API

    Givies as parameter the first and second user:
        python main.py --user 20_Vlad 
        python main.py --user BillGates
     
    To upload your results to a firebase database
        make upload
        
    On Makefile you can edit the upload line to your own firebase link database (https://basesdedatos-b5c80.firebaseio.com)
    Remember to disable the security on your firebase:
        On your project go to Database -> Rules and edit as following:
            {
              "rules": {
                ".read": false,
                ".write": false
              }
            }
   To open the graph just run the command line:
        evince graph.pdf
        
2) Generate a graph newtwork: 

    python graph_generator.py
    

    ( Take into consideration that you need to have 
    just the csv that you want to plot )


    The DOT code will be plotted in: 

        graph.pdf
        

[BUDILING]

    You can build the C code that will analyse the information 

    $ make

Then you can execute the main as : 

    ./main -p : Print graph network 

    ./main -v : Verbose 

    ./main -s : Sort the users by number of friends




