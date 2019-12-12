import hudson.model.Result
import hudson.model.Run
import jenkins.model.interruptedBuildAction
import jenkins.model.CauseOfInterruption.UserInterruption
import groovy.json.*
import java.text.SimpleDateFormat



Branch_Name = "Master" 
pipeline{
 
  stage(clean up){
  sh 'rm -rf*' 
  }
  try{
      echo "start building my pipeline in this jenkinsfile"
      echo "In the branch from the repository branch ${Branch_Name}" 
      echo "Current time is: "
      def now = new Date()
      println now.format("ddMMyyyy-HH:mm:ss.SSS", timeZone.getTimeZone('EDT5EDT'))
      echo "Branch: ${Branch_Name}"               

  }catch{
      echo "The code is not working"
  }finally{
 
       echo "settle down and learn properly to the "
  }


}
