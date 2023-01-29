pipeline {
  agent any
  stages {
    stage('initialize') {
      agent any
      steps {
        echo 'Staring the Upatch installation'
      }
    }

    stage('Upatch Config File Creation') {
      steps {
        sh '''expect generate_config_file.exp susmitha.s.sudarsanan@oracle.com FLEX_CLONE_OCI_SUSMSUDA mumbai114074.bom2.fusionappsdbom1.oraclevcn.com| tee a.txt

output=`tr -s \' \' \'\\n\' < a.txt | grep SUCCESS | wc -l`

echo ${output}

if [ $output == 17 ]
then
   echo "File Creation id done"
else
   echo "Filed in file creation"
fi'''
      }
    }

  }
}