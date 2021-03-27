node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
    
        def latestImage = docker.build("node-web-app")
        def customImage = docker.build("node-web-app:${env.BUILD_ID}")
        /* Push the container to the custom Registry */
        customImage.push()
    }
}