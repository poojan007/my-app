node{
    stage('SCM Checkout'){
        git 'https://github.com/poojan007/my-app'
    }
    stage('Compile and Package'){
        def mvnHome = tool name: 'maven-3', type: 'maven'
        sh "${mvnHome}/bin/mvn package" 
    }
}
