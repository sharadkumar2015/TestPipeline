node {
    stage('Build') {
        echo 'Building Feature1....'
    }
    stage('Test') {
        echo 'Testing....'
    }
    stage('Deploy') {
       withCredentials([azureServicePrincipal('AzureServicePrincipal')]) {
        
       bat """ 
           az login --service-principal -u 78ac8c0f-77b0-4ebd-8896-de6b534b4eb7 -p st]jxgT3P@HZ2N@1N0@0hkKy_0JXbNgt -t 2e33e36d-8e9b-463e-a757-47e336e44a80 --subscription 32fcb35b-33ff-4600-ad9f-7ac2b7247d79
           az group create -l westus -n MyResourceGroup
       """
       }
        echo 'Deploying....'
    }
}
