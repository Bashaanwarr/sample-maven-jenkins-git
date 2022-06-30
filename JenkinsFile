pipeline
{
    agent
    {
        label 'Node-2'
    }
        stages
        {
            stage('Git-Checkout')
            {
                steps
                {
                    echo "Accessing bat files from github repo"
                    git 'https://github.com/Bashaanwarr/sample-maven-jenkins-git.git'
                }
            }
            stage ('MAVEN-VALIDATE')
            {
                steps
                {
                    echo "Validatingmaven repository"
                    bat 'mvn validate'
                }
            }
            stage ('MAVEN-COMPILE')
            {
                steps
                {
                     echo "Compling maven project"
                     bat 'mvn compile'
                }
            }
            stage ('MAVEN-PACKAGING')
            {
                steps 
                {
                    echo "packaging to war file"
                    bat 'mvn package'
                }
            }
            stage ('MAVEN-INSTALL')
            {
                steps
                {
                    echo "INSTALLING TO LOCAL .M2 REPOSITORY"
                    bat 'mvn install'
                }
            }
                
        }
}
