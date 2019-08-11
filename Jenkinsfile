node()  //this is a pipeline ..remove comment when putting in the file
{
    stage "Checkout Code"  //these are stages..remove comment when putting in the file
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/nvn17git/nvnshoppingcart']]])
    
    stage "Build Code"
        sh "mvn clean package"
        
    stage "Deploy Application"
        //sh 'rm /var/lib/tomcat/webapps/nvnshoppingcart*'
        sh 'cp **/*.war /opt/devops'
}

