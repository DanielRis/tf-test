pipeline {
  agent any
  
  stages {
    stage("Generate") {
      steps {
        echo "hello"
      }
    }
    stage("World") {
      steps {
        script {
          terraforge = readYaml(
            file: ".terraforge.yaml"
          )
        }
        echo terraforge.namespace
        configFileProvider([configFile(fileId: 'c3f8d8a5-ed85-4fe0-9bbc-feaaa85337e2', variable: 'MAVEN_SETTINGS')]) {
            echo "world"
        }
      }
    }
  }
}
