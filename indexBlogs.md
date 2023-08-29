---
layout: blogs
permalink: /blogs
title: Sri's Blog
---
<html>
<head>
    <title>Search Terms</title>
    <script>
        var terms = []; // Global array to store terms

        function loadTerms() {
            var xhr = new XMLHttpRequest();
            xhr.open("GET", "terms.txt", true);
            xhr.onreadystatechange = function() {
                if (xhr.readyState === 4 && xhr.status === 200) {
                    var rawData = xhr.responseText;
                    var lines = rawData.split("\n");
                    for (var i = 0; i < lines.length; i++) {
                        var termData = lines[i].split("=");
                        terms.push(termData);
                    }
                }
            };
            xhr.send();
        }

        function searchTerms() {
            var searchInput = document.getElementById("searchInput").value;
            var resultOutput = document.getElementById("resultOutput");
            var found = false;

            for (var i = 0; i < terms.length; i++) {
                if (searchInput === terms[i][0]) {
                    found = true;
                    resultOutput.innerText = "Definition:\n" + terms[i][1];
                    break; // No need to continue searching if term is found
                }
            }

            if (!found) {
                resultOutput.innerText = "Sorry, we can't find that term. Make sure you have spelled your query correctly.";
            }
        }
    </script>
</head>
<body onload="loadTerms()">
    <h1>Search Terms</h1>
    <input type="text" id="searchInput" placeholder="Enter your search">
    <button onclick="searchTerms()">Search</button>
    <div id="resultOutput"></div>
</body>
</html>
<table>
  <tr>
    <th>Week</th>
    <th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Plans</th>
    <th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                &nbsp;&nbsp;&nbsp;&nbsp;Notes/Hacks</th>
    <th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tangibles</th>
  </tr>
  <tr>
    <td><font size="+2">0</font></td>
    <td>
      <ul>
        <li>Download VSCode, get coding tools set up</li>
        <li>Get accustomed to VScode, download and follow instructions on week 0 blog</li>
        <li>Download Jupyter, Python, Homebrew, all other necessary tools</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Listened to Mr. Mortenson talk about the class, online notebooks are important</li>
        <li>Installed VSCode, homebrew, and made an account for Github</li>
        <li>Was playing around with the terminal by opening directories</li>
        <li>Installed python and Jupyter on VSCode</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Code editor installed</li>
        <li>Requirements document</li>
        <li>Ideas list</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td><font size="+2">1</font></td>
    <td>
      <ul>
        <li>Download remaining tooks, get a local website running</li>
        <li>Experiment on modifying the website with images, videos, minigames</li>
        <li>Edit blogs to create notebook</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Opened a new terminal, created a vscode directory with mkdir vscode and then cd vscode</li>
        <li>Cloned a teacher repository by using git clone</li>
        <li>After learning how do clone a teacher repository I cloned a student repository and forked it onto my Github account</li>
        <li>Opened my student repository in VSCode</li>
        <li>Followed install steps to install gems, pip, ruby, and more</li>
        <li>Once done installing all the necessary tools, I opened terminal in vscode and wrote bundle install and then typed make</li>
        <li>Once the server ran and provided with the link, I opened the website</li>
        <li>I linked the website to my Github Account</li>
        <li>Played around with the website, opened index.md and then changed the heading text to Sri’s Page</li>
        <li>Pressed command save and then went to my website again to see the change</li>
        <li>Repeated the 2 steps above and added more info about me</li>
        <li>Wanted to add free form picture, tried dragging and linking image to my index.md but it didn’t work</li>
        <li>Fixed the problem by copying the relative path of the image and pasting it in and using ![](imageurl)</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Functional code</li>
        <li>Debugged issues</li>
      </ul>
    </td>
  </tr>
</table>

## Terms (How We Used Them)
 - make - command that helps run your local server 
 - make convert - checks and ensures Jupyter notebooks are up to date
 - make clean - stops the local server and cleans the files
 - make stop - stops the local server
 - cd ~ allows you to move through directories
 - cd vscode - allows you to go to VSCode directory
 - python –version - shows you your current python version
 - jupyter –version - shows all your jupyter files and their current versions
 - git clone - clones a repository 
 - rbenv versions - shows your current ruby versions
 - ruby -v - shows your current ruby version
 - bundle install - this command installs the dependencies in your Gemfile
 - ![]() - adds an image  
 - ls - lists files in the respository
 - pwd - Print working directory command
 - mkdir - Command used to create directories
 - echo - Print any text that follows the command
 - clear - Clear the terminal display
 - mv - Move or rename files
 - useradd - adds a new user
 - sudo - command to create privileges