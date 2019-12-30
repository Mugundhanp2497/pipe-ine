node {
      def server = Artifactory.server "SERVER_ID"

    // Create an Artifactory Gradle instance.

    def rtGradle = Artifactory.newGradleBuild()

    def buildInfo
    stage('Clone sources') {

        git url: 'https://github.com/Mugundhanp2497/pipe-ine.git'

    }

    stage('Gradle build') {

        buildInfo = rtGradle.run rootDir: "gradle-examples/4/gradle-example-ci-server/", buildFile: 'build.gradle', tasks: 'clean artifactoryPublish'

    }

    stage('Publish build info') {

        server.publishBuildInfo buildInfo

    }

}
