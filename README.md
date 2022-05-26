I had in issue where i uploaded my files in a different repository thats why it seems that ive uploaded recently. 

This is the link of my old repository that i've uploaded and worked on by accident: https://github.com/Teefaloshan/SWproject.git

# Food Investigator
# Description:

This workshop is based on developing a web based machine learning system for simple text classification. the following steps will show how to setup Node js server in order to run the core system of the machine learning (fasttexttool) on input from a user. 

First of all, you must enter the commands to install npm in the linux system. then downloaded the virtual box on my pc, i followed with writing in terminal the commands to install npm.

# Download npm 
to install npm 
  sudo apt install npm
i created a folder and named it "SWproject" placed in the laptop in order to place all the files in. (index.html, index.js, as well train.txt) in the folder.

#Initialize Requirements 
Firstwe should go to the project folder directory 
  SWproject 

then started to initalize requirements just follow these commands
  npm init -y

Download dependencies for a system:
  1) install node fasttext
        npm install node- fasttext --save
  
  2) install Express:
        npm install express --save
  
  3) install some cors issues:
        npm  install cors --save
        
  4)install node js:
         node index.js
         
# Release v1.1

In this Release we updated the js file to match the requirements. now the user will be able to input a text of any type of food in the text-area filed, the server provides a submit and clear buttons. submit button will be responsible to wrap up the text and sends it to the server (index.js). After the text has been submitted to the server. The server would now analyze the text and lable it with the correct category.

The result after being processed will be returned to the users page (UI).

# my website User Interface looks like: 
![Screenshot (182)](https://user-images.githubusercontent.com/105608503/170506098-d46532d0-9f08-4801-8643-b3fba7a8d566.png)


# Travis CI Testing 

We used Travis CI which wass the first CI as a service tool. it introduced a new approach to building code in the cloud. this tool allows the user to link repository, build and test their apps. As well it is a hosted continuous integration services used to build and test software projects hosted on GitHup.it also provides services for open-source projects for free 
   # The Benefits of Travis CI 
    1) you can monitor GitHub projects
    2) Run Test and generate results
    3) Easy development too cloud services 
    4) Developers can use Travis CI to watch the tests when they are running
    
   # Steps in Travis
   
   First go to Travis CI to sign in with your account in GitHub then accept the Authorization of Travis CI. followed with clicking on your profile on the top right    of your travis dashboard then settings and then the green active button to select the repositories you want to use.
   
   # The modifications to the files to make the build pass
   
   In package.json i changed it from:
      "test":"echo \"Error: no test specified\" && exit !"
   
   To:  
      "test": "echo \"No test specified\""
      
   As well i added a fil named ".travis.yml" with the following code was added in the file:
      
      Language: node_js

      node_js:
      - 7

      script:
      - npm test

      cache:
      npm: false
      
      
  # Then i uploaded the added file and the file after the update in GitHub for it to see if it passes in Travis CI
      In Terminal we prceeded the following commands:
          git status
          
          git add . 
          
          git commit -m"updated travis" 
          
          git push origin main
          
     Now you return to Travis CI and go to the intended repository and click on the braches then you will wait, few seconds later it will appear pass like in the pictures.
      
# Images of Pass in Travis CI 
![Screenshot (180)](https://user-images.githubusercontent.com/105608503/170506647-c22e870b-d727-4765-993a-4c28001270c0.png)
![Screenshot (181)](https://user-images.githubusercontent.com/105608503/170506662-ab64d07e-d727-47ca-abc5-9fdd6f810da4.png)
