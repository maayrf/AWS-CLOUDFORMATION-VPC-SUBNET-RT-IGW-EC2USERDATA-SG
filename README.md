# AWS-CLOUDFORMATION-VPC-SUBNET-RT-IGW-EC2USERDATA-SG
Subir instância com script de userdata já configurado com httpd básico (você instala e configura seus serviços de acordo com suas necessidades).

Faça download deste template "ec2-sg-vpc.yaml"; 
Entre na console AWS; 
CloudFormation; 
Stacks; Create stack; 
emplate is ready; 
Upload a template file; 
Selecione o template que foi feito download; 
E configure com o nome que deseja para sua Stack;
Você pode colocar dois ips /32 ou assim: adm-ip-publico/32, seu-ip-publico/32. Ou no código tire a opção de dois IPs e libere tudo 0.0.0.0/0;
O tipo da instância esta por padrão a t2.miro, mas se quiser pode alterar no "InstanceType" do .yaml; 
No código yaml você consegue liberar o Security Group para mais outras porta (acrescente um "XSecurityGroup" acrescente Ref no "GroupSet");
Você precisa ao subir sua stack para o Cloudformation:
    Definir nome da stack;
    Ter uma keypair já existente e selecioná-la;
    Colocar Description da EC2, SG, VPC, etc;
    Definir Subnet Privada (esta com uns "X" no lugar do número). Exemplo: 100.0.2.0/24, 100.0.4.0/24, 100.0.6.0/24;
    Definir Subnet Pública (esta com uns "X" no lugar do número). Exemplo: 100.0.1.0/24, 100.0.3.0/24, 100.0.5.0/24;
    Liberar redes de acessos ao SG;
    E por fim defina sua rede VPC. Exemplo: 100.0.0.0/16;
    OBS: Lembrando que as subnets devem caber no range da Rede VPC.
