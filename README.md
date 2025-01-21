# Tutorial_Github

Este tutorial tem como objetivo introduzir os principais comandos utilizados no Git, a ferramenta de controle de versão por trás do GitHub. Ao longo deste guia, você aprenderá desde operações básicas, como criar um repositório e fazer commits, até comandos mais avançados, como gerenciar branches e resolver conflitos.

---

## **1. Criar um repositório**

No perfil existe uma sessão chamada **Repositories**, e nela é possível clicar no botão **New** para ser direcionado à página de criação de repositórios. 

![image](https://github.com/user-attachments/assets/c084065d-50cc-4ca7-bfd7-a32dda7e3951)

Onde deve ser inserido o nome do repositório, e outras informações opcionais, caso deseje.

![image](https://github.com/user-attachments/assets/12aeae8c-a67f-430e-8f20-20c2b402528c)

Para finalizar a criação basta selecionar **Create Repositorie** no final da página.

## **2. Utilizar repositório de maneira remota**

Na página do repositório, selecionar o botão **< > Code** e copiar a URL mostrada.

![image](https://github.com/user-attachments/assets/e8ce60c4-ec3d-4f34-a3f3-af37ec35f0e2)

No VS Code, utilizar o comando `git remote add origin "URL do repositório"`, por exemplo `git remote add origin https://github.com/MarianaXBDias/Tutorial_Github.git`

* Sincronizar com repositório remoto: `git pull`
* Criar uma cópia de repositório remoto: `git clone "URL do repositório"` (Exemplo: `git clone https://github.com/MarianaXBDias/Tutorial_Github.git`)
  
## **3. Editar Branch**

* Verificar as branches do repositório: `git branch`
* Alterar nome da branch atual: `git branch -M "novo nome"` (Exemplo: `git branch -M main`)
* Adicionar conteúdo da branch no repositório: `git push -u "branch remota" "branch local"` (Exemplo: `git push -u origin main`)
* Sair da branch atual: `git checkout`
* Sair da branch atual e criar uma nova: `git checkout -b "nova branch"` (Exemplo: `git checkout -b teste`)
* Enviar nova branch ao repositório: `git push --set--upstream "branch remota" "nova branch"` (Exemplo: `git push --set--upstream origin teste`)

## **4. Realizar commits**

No VS Code, verificar a instalação do Git a partir do comando `git --version`. Em seguida, no diretório da pasta que deseja adicionar ao repositório, utilizar o comando `git init` para criar uma pasta **.git**.

Para verificar o status dos arquivos na pasta basta usar o comando `git status`.

![image](https://github.com/user-attachments/assets/b7cc1405-881d-4aa2-bf35-dbb2c4881f04)

No exemplo acima, nenhum dos arquivos foi adicionado ao repositório ainda.

Para adicionar um arquivo específico, utilizar o comando `git add "nome do arquivo"`. Por exemplo, para adicionar o arquivo "exemplo_github.py" foi utilizado `git add exemplo_github.py`, e após o comando `git status` temos a seguinte resposta:

![image](https://github.com/user-attachments/assets/3451b231-50d2-40dd-adde-2bb34412032b)

Pode ser usado também o comando `git add .`, que traz mais praticidade adicionando os arquivos alterados, além dos que foram criados e excluídos da pasta.

Para confirmar as mudanças deve ser feito o commit a partir do comando `git commit`. Que também pode ser feito como `git commit -a -m "mensagem personalizada"`, onde `-a` adiciona ao commit todos os arquivos que foram modificados e excluídos, e `-m` permite adicionar uma mensagem personalizada que pode ser usada para explicar o conteúdo ou finalidade do commit, por exemplo.

Ao utilizar o comando `git satatus`, esta será a resposta recebida:

![image](https://github.com/user-attachments/assets/b2e1b0d0-6f1e-4726-ac8d-d1cbf291b660)

Pois todas as alterações foram confirmadas.

* Verificar histórico de commits realizados: `git log`

## 5. Realizar merge

Para combinar as mudanças de uma branch com a branch atual, atilizar `git merge "nova branch"` (Exemplo: `git merge teste`)

## 6. Remover arquivos

* Remover arquivos não rastreados: `git clean -f`













