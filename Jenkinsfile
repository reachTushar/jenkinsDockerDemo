node{
    stage ('SCM Checkout'){
    git 'https://github.com/reachTushar/jenkinsDockerDemo'
    }
    
    stage ('Compile-Package'){
        def mvnHome = tool name: 'maven3', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
     }
    stage ('Email Notification'){
    slackSend baseUrl: 'https://hooks.slack.com/services/', 
        channel: '#channel1', 
        color: 'good', 
        message: 'Welcome to Slack - this is Tushar ', 
        teamDomain: 'javahomecloud', 
        tokenCredentialId: 'slack-demo'
       }
    

}
