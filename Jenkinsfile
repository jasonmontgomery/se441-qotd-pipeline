stage "DEV-QA"

node {
git 'https://github.com/jasonmontgomery/se441-qotd-pipeline.git'

def gradleHome = tool 'Gradle 2.11'
bat "${gradleHome}\\bin\\gradle.bat assemble uploadArchives"

step([$class: 'ArtifactArchiver', artifacts: '**/*.war', fingerprint: true])
}