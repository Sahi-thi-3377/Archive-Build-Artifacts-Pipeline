pipeline {
agent any
stages {
stage('Checkout') {
steps {
git branch: 'main', url: 'https://github.com/Sahi-thi-3377/Archive-Build-Artifacts-Pipeline.git'
}
}
stage('Generate Report') {
steps {
bat 'python app.py'
}
}
stage('Archive Report') {
steps {
archiveArtifacts artifacts: 'report.txt', followSymlinks: false
}
}
}
}