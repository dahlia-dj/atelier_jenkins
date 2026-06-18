pipeline {
agent any
stages {
stage ('Clone') {
steps {
    echo 'Repository cloned '
}
}
stage ('Run Python') {
steps {
sh 'py app.py'
}
}
}
}