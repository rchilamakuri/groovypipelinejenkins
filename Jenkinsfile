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
           mkdir raghuram
           dir(./raghuram){
          echo "Directory raghuram is created"
          touch firstfile.groovy
              
           }
              
      }               

     }catch(Exception e){
      echo "The code is not working"
     }finally{
 
       echo "settle down and learn properly to the "
     }


}

