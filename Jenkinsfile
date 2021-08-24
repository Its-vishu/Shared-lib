@Library('Shared-lib@main')_
pipeline {
agent any
stages{
stage('Demo') {
steps
{
echo 'Hello world'
sayHello 'Vishwajeet '
}
}
stage("build")
{
steps
{
script{
def filePath = readFile "Hello.csv"
def lines = filePath.readLines()
def linesbyline = filePath.readLines()
for (line in linesbyline) {
println "$line"}
}
}
}
}
post {
always {
// emailext body: '${env.BUILD_URL} has result ${currentBuild.result}', subject: 'test email', to: 'vishwajeet751srs@gmail.com'
mail to: 'Vishwajeet751srs@gmail.com',
subject: "Status of pipeline: ${currentBuild.fullDisplayName}",
body: "${env.BUILD_URL} has result ${currentBuild.result}"
}
}
}
