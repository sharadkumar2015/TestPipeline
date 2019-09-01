node {
    stage('Build') {
        echo 'Building Feature1....'
    }
    stage('Test') {
        echo 'Testing....'
    }
    stage('Deploy') {
        withCredentials([azureServicePrincipal(credentialsId: 'credentials_id',
                                    subscriptionIdVariable: 'SUBS_ID',
                                    clientIdVariable: 'CLIENT_ID',
                                    clientSecretVariable: 'CLIENT_SECRET',
                                    tenantIdVariable: 'TENANT_ID')]) {
        sh 'az login --service-principal -u $CLIENT_ID -p $CLIENT_SECRET -t $TENANT_ID'
}
        echo 'Deploying....'
    }
}
