pipeline {
agent any

stages{
stage(‘Build){
steps{
     Sh "composer install"
}
}
stage("Test"){
steps {
sh 'vendor/bin/phpunit tests'
}
}
stage('Deploy'){

steps{

    Sh 'docker-compose up -d'
}
}
}
}
