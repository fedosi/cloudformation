# cloudformation

### STACK DO LAB:

![STACK](picture/stack.png)

### APLICAR O CF:

**Validar o YAML:**
```Shell
aws --profile AWS-FEDOSI cloudformation validate-template --template-body file://./lab-fedosi.yaml
```

**Criar a stack:**
```Shell
aws --profile AWS-FEDOSI cloudformation create-stack --stack-name LAB-FEDOSI --template-body file://./lab-fedosi.yml
```

**Deletar a stack:**
```Shell
aws --profile AWS-FEDOSI cloudformation delete-stack --stack-name LAB-FEDOSI
```

**A EC2 utilizada como bastion não é criada juntamente com o LAB, para cria-la é necessario rodar o CLI abaixo:**

```Shell
aws --profile AWS-FEDOSI cloudformation create-stack --stacl-name EC2-BASTION --template-body file://.bastion.yaml
```