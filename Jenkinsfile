pipeline {
    agent any
    
    environment {
        PYTHON_VERSION = '3.8'  
    }

    stages { 
    

 stage('Install Dependencies') {
            steps {
                script {
                    // Install required Python packages using pip
                    sh "pip install -r requirements.txt"
                }
            }
        }
        stage('Set Up Environment') {
            steps {
                script {
                    // Set up a virtual environment
                    sh "python${PYTHON_VERSION} -m venv venv"
                    sh "source venv/bin/activate"
                }
            }
        }
}
}
