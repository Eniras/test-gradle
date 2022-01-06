pipeline {
  agent any
  stages {
    stage('stage 1') {
      steps {
        sh 'grep user /etc/passwd'
      }
    }

    stage('stage 2') {
      steps {
        sh '''if test \'grep -c orsys /etc/passwd\' -ne 0 
then 
find / -user orsys > /tmp/orsys
fi'''
      }
    }

    stage('Stage 3') {
      steps {
        sh '''for i in "cat /tmp/orsys"
do
ls -il $i
done'''
      }
    }

  }
}