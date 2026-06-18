pipeline {
agent any
stages {
stage ('Install dependencies') {
steps {
sh 'pip install -r requirements.txt'
}
}
stage ('Tests') {
steps {
sh 'pytest'
}
}
stages {
stage ('Build Docker Image') {
steps {
sh 'docker build -t myapp .'
}
}
stage ('Run Docker Container') {
steps {
sh 'docker run myapp'
}
}
}
}
}