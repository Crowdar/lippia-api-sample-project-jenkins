#           steps {
  #              echo "Realizando Pruebas"
   #             sh 'mvn test -P$TESTTYPE -Dcrowdar.cucumber.filter="'$TAG'" -Dcrowdar.cucumber.filter.language="'$LANG'"' 
    #            junit 'target/extent-reports/' 
     #       }
 #           steps {
  #          if (env.CI_COMMIT_BRANCH == "master") || (env.CI_COMMIT_BRANCH == "main"){
   #         variables:
    #            TAG: "@Success"
    #            TESTTYPE: "Secuencial"
      #          LANG: "@EN"
       #     }    
    #        if (env.CI_COMMIT_BRANCH != "master") || (env.CI_COMMIT_BRANCH != "main"){ 
     #       when: manual   
      #      }    
       #     }
        }
