pipeline {
  agent any
  parameters {
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'master', name: 'BRANCH', type: 'PT_BRANCH'
  }
  stages {
    stage('Example') {
      steps {
        git branch: "${params.BRANCH}", url: 'https://github.com/smandadapu/azurerepo.git'
        echo '${BRANCH}'
        echo 'env.${BRANCH_NAME}'
      }
    }
  }
}
