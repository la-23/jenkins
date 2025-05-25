pipeline{
    agent any 
    stages{
        stage("build"){
            steps{
                cleanWs()
                echo "building laptop ..."
                sh ''' 
                    mkdir -p buildP
                    touch build/computer.txt
                    echo "mainboard" >> build/computer.txt
                    echo "display" >> build/computer.txt
                    echo "keyboard" >> build/computer.txt
                    cat build/computer.txt
                '''
            }
        }
        stage("Test"){
            steps{
                echo "testing laptop"
                sh ''' 
                    test -f build/computer.txt
                    grep "mainboard" build/computer.txt
                
                '''
            }
        }
    }
}