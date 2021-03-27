node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
    
        def latestImage = docker.build("dhikrahouissa/node-web-app")
        def customImage = docker.build("dhikrahouissa/node-web-app:${env.BUILD_ID}")
        /* Push the container to the custom Registry */
        customImage.push()
    }
}