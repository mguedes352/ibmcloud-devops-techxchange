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

14. Selecione a região do namespace do container registry criado (São Paulo);

15. Insira ou selecione o nome do namespace do container registry criado anteriormente;

16. Selecione o grupo de recursos (se houver);

17. Escolha o cluster IKS criado e, por fim, clique em "Criar" ao final da página para finalizar a criação da pipeline;

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/68a2fbdf-88b7-4b60-82c2-f0d5921e41ed)

18. Clique em "ci-pipeline";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/c26b9cbc-ab83-419d-9ac1-8670aa4ed4c2)

19. Clique em "manual-run";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/233ff820-4c4e-4fdd-820d-aa9b570a3142)

20. Clique no seu #1 manual-run;

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/f0d4782e-c7cd-4110-ab9d-7783ab58f168)

21. Clique na etapa "deploy-to-kubernetes";

22. Clique na aba de "Resultados";

23. Copie a URL da aplicação;

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/ce3025b8-9039-4f4b-836a-09de826a7809)

24. Por fim, abra uma aba em seu navegador e cole a URL para visualizar a aplicação.

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/3baf360a-3f64-4c47-8a28-ed95c8b98d3f)

### 5. Executando um trigger automático
1. Clique na etapa "extract-repository-url";

2. Clique na aba de "Resultados";

3. Copie a URL do repositório;

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/9519287c-6b1f-40f1-b699-fe8b7c5974e9)

4. Abra uma nova aba no navegador e cole a URL do repositório;

5. Clique no arquivo "util.js";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/183d1323-729d-4363-8faa-0fcbc41bddef)

6. Clique em "Edit";

7. Clique em "Edit single file";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/73ed5c21-d5ed-40af-8f07-967ff0387863)

8. Faça uma pequena alteração no texto da variável "welcomeMessage";

![image](https://github.com/mguedes352/ibmcloud-devops-techxchange/assets/79527238/31e89e9b-7c66-41e5-a7e3-0091ce4a71ec)


