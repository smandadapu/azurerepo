#!/usr/bin/env groovy

loadLibraries()

def organizationName = getOrganizationName(scm)
def repositoryName = getRepositoryName(scm)

buildRetention('builds')

node {
        try {
            setupBuildEnvironment()

            stage('npm install') {
                echo "statge1"
            }

            stage('lint') {
                echo "lint"
            }
        }
        catch (e) {
            handleException(e, currentBuild, organizationName, repositoryName,
                              env.BRANCH_NAME, env.BUILD_NUMBER, env.BUILD_URL)
        }
        finally {
            cleanWorkspace()
    }
}
