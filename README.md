Stage  Job ID             Job name           Workflow name       Workflow file              Events                
0      teste-basico       teste-basico       Hello Local         01-hello-local.yml         workflow_dispatch,push
0      setup-e-lint       setup-e-lint       Pipeline Principal  02-pipeline-principal.yml  push                  
1      testes-unitarios   testes-unitarios   Pipeline Principal  02-pipeline-principal.yml  push                  
1      scan-de-seguranca  scan-de-seguranca  Pipeline Principal  02-pipeline-principal.yml  push                  
2      build-e-deploy     build-e-deploy     Pipeline Principal  02-pipeline-principal.yml  push

Os Jobs 2 (testes-unitarios) e 3 (scan-de-seguranca) rodaram em paralelo porque ambos aparecem no mesmo Stage (Stage 1) na
 saída do comando act -l.
