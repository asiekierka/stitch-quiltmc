node {
   stage 'Checkout'

   checkout scm

   stage 'Build'

   sh "rm -rf build/libs/"
   sh "chmod +x gradlew"
   sh "./gradlew clean"
   sh "./gradlew build --stacktrace"

   stage "Archive artifacts"

   sh "./gradlew publish --stacktrace"
}
