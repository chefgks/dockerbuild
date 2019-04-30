pipeline{
    agent any
    stages{
        stage("Build Image")
        {
            steps
            {
                bash 
                '''
                    #!/bin/bash                
                    echo "Hello I am Going to build your first Docker image"
                    cd /var/lib/jenkins/workspace/first-jenkins-job
                    echo "Building Image"
                    echo "Getting login to Docker hub repo"
                    sudo docker login -u gauravmca23 -p Redmi123
                    sudo docker build . -t ubuntu:myubuntu
                    if [ $? == 0 ] 
                    then 
                    echo "Pushing my new image"
                    sudo docker tag ubuntu:myubuntu gauravmca23/ubuntu:myubuntu1
                    sudo docker push gauravmca23/ubuntu:myubuntu1
                    else 
                    echo "I am exiting now"
                    fi
                '''
                
            }
    }   }    
}
