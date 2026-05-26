pipeline { 
 agent any 
 stages { 
 stage('Project 1: Create Folder') { 
 steps { 
 echo "Project 1: Creating a folder 'myProjectFolder'" 
 // For Linux/Unix agents: 
 // sh 'mkdir -p myProjectFolder' 
 // For Windows agents, uncomment the line below: 
 bat 'mkdir Folder1Jenkins' 
 } 
 } 
 stage('Project 2: Create File') { 
 steps { 
 echo "Project 2: Creating a file 'myProjectFolder2/myFile.txt'" 
 // For Linux/Unix agents: 
 //sh 'touch Folder1Jenkins/myFile.txt' 
 // For Windows agents, uncomment the line below: 
 bat 'type nul > Folder1Jenkins\\myFile.txt' 
 } 
 } 
 stage('Project 3: Write Contents to File') { 
 steps {
 echo "Project 3: Writing contents into 'myProjectFolder2/myFile.txt'"  // For Linux/Unix agents: 
 //sh 'echo "Hello, this is the content added by Project 3" > myProjectFolder/myFile.txt'  // For Windows agents, uncomment the line below: 
 bat 'echo Hello, this is the content added by Project 3 > Folder1Jenkins\\myFile.txt'  } 
 } 
 } 
 post { 
 always { 
 echo "Displaying the contents of the file:" 
 // For Linux/Unix agents: 
 //sh 'cat myProjectFolder/myFile.txt' 
 // For Windows agents, uncomment the line below: 
 bat 'type Folder1Jenkins\\myFile.txt' 
 } 
 } 
}
