# Ambiente DevOps - Ferramentas IaC

* Sistema Operacional: Ubuntu:20.04

* Ferramentas instaladas

```
# Editor de texto
vi

# Estrutura de diretórios
tree

# Terraform
Versão: '1.1.3'

# Packer
Versão: '1.7.8'

# Ansible
Versão: '2.12.1'
```

* Comando para utilizar o container 

docker container run -it -v $PWD:/iac -w /iac --entrypoint "" lucascarmo/iac:latest bash