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
1. Clique no menu hambúrguer;
   
2. Passe o mouse em cima do item "Kubernetes" e clique em "Clusters";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/29f9cf02-0366-4e9f-baba-96860fc29678)

3. Clique em "Criar Cluster"

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/a47e826f-f6b3-401b-b4a2-7572014eb385)

4. Selecione Infraestrutura VPC;
   
5. Selecione a VPC que foi criada no passo anterior;

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/f72db2c7-3ef2-44c0-abd8-9979649f7f2b)

6. Deixe habilitado apenas a subnet em que foi atachado o Public Gateway, e desabilite as demais subnets;

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/ca75bec2-c7d1-4707-982b-e6e3a3b2dfb5)

7. Defina um nome para o conjunto de workers;
   
8. Defina "1" na quantidade de worker por zona, garantindo que haja apenas 1 worker node no total;
   
9. Clique em "Mudar o tipo";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/a34ca60f-71db-4353-9a2f-7879e31cda71)

10. Selecione o perfil com 2 vCPUs e 4GB RAM;

11. Clique em "Salvar o tipo de conjunto de trabalhadores";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/69b1c6ae-dda1-47af-bd81-59afebb29865)

12. Defina um nome para o Cluster IKS e selecione o grupo de recursos (se houver);

13. Por fim, clique em "Criar" para criar o cluster.

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/34e8775d-02af-4583-a5c6-1e14a69dec41)

### 3. Criação do namespace do Container Registry
1. Clique no menu hambúrguer;
   
2. Passe o mouse em cima do item "Container Registry" e clique em "Namespaces";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/7b019bd6-e6b7-4b85-8a48-d1e0eda0fdde)

3. Selecione a região de São Paulo;
   
4. Clique em "Criar";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/bcd17861-2272-4392-a469-e9bdf62a1146)

5. Selecione o grupo de recursos (se houver);

6. Defina um nome para o namespace;

7. Clique em "Criar".

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/ff722a96-9d74-4a3f-877a-bacca73a2444)

### 4. Criação da Toolchain
1. Dentro do cluster IKS, clique em "DevOps" na barra lateral da esquerda;

2. Em seguida clique em "Criar uma cadeia de ferramentas";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/92036686-392a-4a93-a273-ef1659218ac6)

3. Clique no item "Desenvolva um app Kubernetes";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/3b6d751e-28fa-4409-ad4a-1ff11b2e0c27)

4. Defina um nome para a toolchain;

5. Selecione a região de São Paulo;

6. Selecione o grupo de recursos (se houver);

7. Selecione o tipo de pipeline Tekton;

8. Clique em Delivery Pipeline;

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/e227b983-5ae1-437f-a907-2866f3df3591)

9. Defina um nome para a aplicação;

10. Para criar uma chave de API da IBM Cloud, clique em "Novo";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/cdf0147c-d03f-432f-b66a-924e2b229f82)

11. Defina o nome para a sua API Key;

12. Defina uma breve descrição (opcional);

13. Clique em "OK" para criar;

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/15543763-2665-4f2f-8cef-a7cb5e6e9c2b)

