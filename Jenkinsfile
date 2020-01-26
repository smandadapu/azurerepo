#!/usr/bin/env groovy

def organizationName = getOrganizationName(scm)
def repositoryName = getRepositoryName(scm)

node {
        try {
            setupBuildEnvironment()

            stage('npm install') {
                echo "env.BRANCH_NAME"
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
