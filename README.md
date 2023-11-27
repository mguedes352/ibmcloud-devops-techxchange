# IBM Cloud DevOps - TechXchange
IBM Cloud DevOps na prática para o TechXchange: Step by Step

### 1. Criação da VPC (Virtual Private Cloud)
1. Clique no menu hambúrguer;

2. Passe o mouse em cima do item "Infraestrutura VPC" e clique em "VPCs";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/bb935046-7d66-4df5-a273-777fdfb24fdb)

3. Clique em "Criar";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/e5d4467e-cc8d-4515-a43a-bd829f5960e5)

4. Selecione a geografia da América do Sul e a região de São Paulo;

5. Defina um nome para a VPC e selecione o grupo de recursos (se houver);

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/950548b7-fcc8-447d-9af4-6a0d9aa3ab55)

6. Para atachar um Public Gateway, desça a tela até a sessão das Sub-redes, escolha uma subnet e clique em "editar";
   
7. Com a aba de edição aberta, desça a tela até encontrar Gateway público (ou Public Gateway) e habilite;

8. Clique em "Salvar";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/6cb90a5c-91ab-4d88-8f92-d7b4a60ae9ea)

9. Por fim, clique em "Criar nuvem privada virtual".

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/6582f46d-8e83-42ab-95d0-028bdaaa5178)


### 2. Criação do Cluster IKS
1. Clique no menu hambúrguer novamente;
   
2. Passe o mouse em cima do item "Kubernetes" e clique em "Clusters";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/29f9cf02-0366-4e9f-baba-96860fc29678)

3. Clique em "Criar Cluster"

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/a47e826f-f6b3-401b-b4a2-7572014eb385)

4. Selecione Infraestrutura VPC;
   
5. Selecione a VPC que foi criada no passo anterior;

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/f72db2c7-3ef2-44c0-abd8-9979649f7f2b)

6. Deixe habilitado apenas a subnet em que foi atachado o Public Gateway, e desabilitar as demais subnets;

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/ca75bec2-c7d1-4707-982b-e6e3a3b2dfb5)

7. Defina um nome para o conjunto de workers;
   
8. Defina "1" na quantidade de worker por zona, garantindo que haja apenas 1 worker node no total;
   
9. Clique em "Mudar o tipo";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/a34ca60f-71db-4353-9a2f-7879e31cda71)

