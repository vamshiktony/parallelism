# parallelism
Task: Run teo different jobs simul in two different slaves,code must be written in single pipeline Job using groovy script

CODE:
        parallel (
                "stream 1" : { 
                     node ("jen-slv") { 
                           sh 'pwd'
                          } 
                        },
                 "stream 2" : { 
                     node ("jen-slv2") { 
                           sh 'mkdir vamshi98'
                           sh 'cd vamshi98'
                       } 
                   }
                )
     
