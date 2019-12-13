#!/usr/bin/env groovy

import hudson.model.*
import hudson.EnvVars
import hudson.model.Result
import hudson.model.Run
import jenkins.model.InterruptedBuildAction
import jenkins.model.CauseOfInterruption.UserInterruption
import groovy.json.*
import java.text.SimpleDateFormat



Branch_Name = "Master"
SOURCE_CODE_ROOT = "/var/lib/jenkins/workspace/firstPipelineWithShell" 
 
node{
    
    stage('clean up'){
      sh 'rm -rf *'
      echo "Now the repository is empty" 
    }
     try{
      echo "start building my pipeline in this jenkinsfile"
      echo "In the branch from the repository branch ${Branch_Name}" 
      def name = "raghuram"
      echo "My name is ${name}"

      echo "Branch: ${Branch_Name}"
      stage('first stage on my own'){
           dir("${SOURCE_CODE_ROOT}"){
                
               //git branch: "${Branch_Name}", changelog: true, poll : true 
               //GIT_COMMIT_HASH = sh (script : "git log -n 1 --pretty=format:'%H'", returnStdout: true)
               //echo "GIT_COMMIT_HASH: ${GIT_COMMIT_HASH}"
               //Short_Commit_Hash = GIT_COMMIT_HASH.substring(0,7)
               //env.committer = sh(returnStdout: true, script: "git log -n 1 --pretty=format:'%cn'").trim()
                 
             echo "The stage if working accordinglu try modifiying the next job"

           }
              
      }
      stage('stage 2'){
            
            build job: "${SOURCE_CODE_ROOT}", propogate: true, wait: true, parameters: [string(name: "${Branch_Name}", value: "This is test to learn" )] 
      }                

     }catch(Exception e){
      echo "The code is not working"
     }finally{
 
       echo "settle down and learn properly to the "
     }


}

