<<<<<<< HEAD
<<<<<<< HEAD
## Step 1: Hello Copilot

Welcome to your **"Getting Started with GitHub Copilot"** exercise! :robot:

In this exercise, you will be using different GitHub Copilot features to work on a website that allows students of Mergington High School to sign up for extracurricular activities. 🎻 ⚽️ ♟️

<img width="600" alt="screenshot of Mergington High School WebApp" src="https://github.com/user-attachments/assets/472398fd-1aa1-4084-b443-4e242deb30d9" />

### What is GitHub Copilot?

<img width="150" align="right" alt="copilot logo" src="https://github.com/user-attachments/assets/4d22496d-850b-4785-aafe-11cba03cd5f2" />

GitHub Copilot is an AI coding assistant that helps you write code faster and with less effort, allowing you to focus more energy on problem solving and collaboration.

GitHub Copilot has been proven to increase developer productivity and accelerate the pace of software development. For more information, see [Research: quantifying GitHub Copilot’s impact on developer productivity and happiness in the GitHub blog.](https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/)

Your most common interactions will likely be:

- **Inline suggestions**: As you type, Copilot uses the nearby context to suggest code directly in your editor. This will be a familiar interaction if you have used code completion tools like [Intellisense](https://code.visualstudio.com/docs/editor/intellisense), except that the completions may be entire functions.
- **Copilot Chat**: A dedicated chat panel that lets you ask coding related questions. This will feel familiar if you have used online AI assistant chats. The big difference however, is that your project files will provide automatic context to provide tailored responses.
- **Copilot Edits**: Similar to Copilot Chat, but less conversational and more big picture or goal oriented.

> [!TIP]
> You can learn more about current and upcoming features in the [GitHub Copilot Features](https://docs.github.com/en/copilot/about-github-copilot/github-copilot-features) documentation. You can also select different [models](https://docs.github.com/en/github-models) and make your own [extensions](https://github.com/features/copilot/extensions), but that's for a different lesson!

### How can I use GitHub Copilot?

As you work, you'll find GitHub Copilot can help out in several places across the website and in your favorite coding environments such as VS Code, Jet Brains, and Xcode! For today's coding though, we will practice with VS Code in a preconfigured development environment known as [Codespace](https://github.com/features/codespaces).

### :keyboard: Activity: Get a project intro from Copilot Chat

Let's start up our development environment, use copilot to learn a bit about the project, and then give it a test run.

1. Right-click the below button to open the **Create Codespace** page in a new tab. Use the default configuration.

   [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/{{full_repo_name}}?quickstart=1)

1. Confirm the **Repository** field is your copy of the exercise, not the original, then click the green **Create Codespace** button.

   - ✅ Your copy: `/{{{full_repo_name}}}`
   - ❌ Original: `/skills/getting-started-with-github-copilot`

1. Wait a moment for Visual Studio Code to load in your browser.

1. In the left sidebar, click the extensions tab and verify that the `GitHub Copilot` and `Python` extensions are installed and enabled.

   <img width="350" alt="copilot extension for VS Code" src="https://github.com/user-attachments/assets/ef1ef984-17fc-4b20-a9a6-65a866def468" />

   <img width="350" alt="python extension for VS Code" src="https://github.com/user-attachments/assets/3040c0f5-1658-47e2-a439-20504a384f77" />

1. At the top of VS Code, locate and click the **Copilot icon** to open a Copilot Chat panel.

   <img width="150" alt="image" src="https://github.com/user-attachments/assets/5e64db46-95cb-415d-badc-b6b8677f10c1" />

1. If this is your first, time using GitHub Copilot, you will have to accept the usage terms to continue.

1. Enter the below prompt to ask Copilot to introduce you to the project.

   > <img width="13px" src="https://github.com/user-attachments/assets/98fd5d2e-ea29-4a4a-9212-c7050e177a69" /> **Prompt**
   >
   > ```prompt
   > @workspace Please briefly explain the structure of this project.
   > What should I do to run it?
   > ```

   > **Note**: It is not necesesary to follow Copilot's recommended instructions. We have already prepared the environment for you.

1. Now that we know a bit more about the project, let's actually try running it! In the left sidebar, select the `Run and Debug` tab and then press the **Start Debugging** icon.

   <img width="300" alt="image" src="https://github.com/user-attachments/assets/50b27f2a-5eab-4827-9343-ab5bce62357e" />

1. We want to see our webpage running in a browser, so let's find the url and port. If it isn't visible, expand the lower panel and select the **Ports** tab.

1. In the list, find port `8000` and the related link. Hover over the link and select the **Open in browser** icon.

   ![image](https://github.com/user-attachments/assets/92d5642e-ce99-4a66-850c-2d311a673596)

### :keyboard: Activity: Use Copilot to help remember a terminal command 🙋

Great work! Now that we are familiar with the app and we know it works, let's ask copilot for help starting a branch so we can do some customizing.

1. If not already there, return to VS Code.

1. In the bottom panel, select the **Terminal** tab. On the right side, click the plus `+` sign to create a new terminal window.

   > **Note:** This will avoid stopping the existing debug session that is hosting our web application service.

1. Within the new terminal window, `right click` and select `Copilot` then `Terminal Inline Chat`. Alternately, you can use the keyboard shortcut `Ctrl + I` (windows) or `Cmd + I` (mac).

1. Let's ask Copilot to help us remember a command we have forgotten: creating a branch and publishing it

   > <img width="13px" src="https://github.com/user-attachments/assets/98fd5d2e-ea29-4a4a-9212-c7050e177a69" /> **Prompt**
   >
   > ```prompt
   > Hey copilot, how can I create and publish a new Git branch?
   > ```

   > **Tip:** This is a simple example, but Copilot is great at providing more tailored commands that might involve loops, pattern matching, file modification, and more! Don't be afraid to ask Copilot for a suggestion. Just remember it is a suggestion and you should always verify it first to be safe.

1. Copilot probably gave us a command like the following. Rather than manually modify it, let's respond back to tell Copilot to use a particular name.

   ```bash
   git checkout -b {new_branch_name}
   git push -u origin {new_branch_name}
   ```

   > <img width="13px" src="https://github.com/user-attachments/assets/98fd5d2e-ea29-4a4a-9212-c7050e177a69" /> **Prompt**
   >
   > ```prompt
   > Awesome! Thanks, Copilot! Let's use the
   > branch name "accelerate-with-copilot".
   > ```

   > **Tip:** If Copilot doesn't give you quite what you want, you can always continue explaining what you need. Copilot will remember the conversation history for follow-up responses.

1. Now that we are happy with the command, press the `Run` button to let Copilot run it for us. No need to copy and paste!

1. After a moment, look in the VS Code lower status bar, on the left, to see the active branch. It should now say `accelerate-with-copilot`. If so, you are all done with this step!

1. Now that your branch is pushed to GitHub, Mona should already be busy checking your work. Give her a moment and keep watch in the comments. You will see her respond with progress info and the next lesson.

<details>
<summary>Having trouble? 🤷</summary><br/>

If you don't get feedback, here are some things to check:

- Make sure your created the branch with the exact name `accelerate-with-copilot`. No prefixes or suffixes.
- Make sure the branch was indeed published to your repository.
=======
=======
>>>>>>> main

## Passo 1: Olá, Piloto !

Neste exercício, você utilizará diferentes recursos do GitHub Copilot para trabalhar em um site que permite aos estudantes da Escola Secundária Mergington se inscreverem em atividades extracurriculares. 🎻 ⚽️ ♟️


<img width="600" alt="captura de tela do aplicativo da Escola Secundária Mergington" src="https://github.com/user-attachments/assets/472398fd-1aa1-4084-b443-4e242deb30d9" />

### Atividade: Conheça o projeto usando o Copilot Chat
Para o exercício de hoje, vamos praticar com VS Code em um ambiente de desenvolvimento pré-configurado conhecido como [Codespaces](https://github.com/features/codespaces).

Vamos iniciar nosso ambiente de desenvolvimento, utilizar o Copilot para aprender um pouco sobre o projeto e depois testá-lo.

1. Clique com o botão direito no botão abaixo para abrir a página **Criar Codespace** em uma nova guia. Use a configuração padrão.

   [![Abrir no GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/{{full_repo_name}}?quickstart=1)

2. Confirme que o campo **Repositório** seja sua cópia do exercício, não o original, e clique no botão verde **Create Codespace**.

   - ✅ Sua cópia: `/{{{full_repo_name}}}`
   - ❌ Original: `/Copilot-Workshop-Invillia/skills-getting-started-with-github-copilot`

3. Aguarde um momento enquanto o Visual Studio Code carrega no seu navegador.

4. Na barra lateral esquerda, clique na aba extensões e verifique se as extensões `GitHub Copilot` , `GitHub Actions` e `Python` estão instaladas e habilitadas.

5. No topo do VS Code, clique no **ícone do Copilot** para abrir o painel Copilot Chat.

6. Caso seja sua primeira vez usando GitHub Copilot, você precisará aceitar os termos de uso.

7. Insira o seguinte prompt para pedir ao Copilot que apresente o projeto:

   ```prompt
   @workspace Por favor, explique brevemente a estrutura deste projeto.
   O que devo fazer para executá-lo?
   ```

   > **Nota**: Não é necessário seguir as instruções recomendadas pelo Copilot. Nós já preparamos o ambiente para você.

8. Agora, vamos executar o projeto. Na barra lateral esquerda, selecione a aba `Run and Debug` e clique no ícone **Start Debugging**.

9. Para visualizar a página rodando no navegador, encontre a porta `8000` no painel inferior, guia **Ports**, passe o cursor sobre o link e clique no ícone **Open in browser**.

### Atividade: Peça ajuda ao Copilot para lembrar um comando do terminal 🙋

Agora que estamos familiarizados com o app e sabemos que funciona, vamos pedir ao Copilot ajuda para criar uma nova branch.

1. Retorne ao VS Code.
2. No painel inferior, selecione a guia **Terminal** e clique no sinal de `+` para criar uma nova janela do terminal.
3. Na nova janela do terminal, clique com o botão direito, selecione `Copilot` e depois `Terminal Inline Chat` (ou use o atalho `Ctrl + I` no Windows ou `Cmd + I` no Mac).

4. Pergunte ao Copilot como criar e publicar uma nova branch:

   ```prompt
   Ei, Copilot, como posso criar e publicar uma nova branch do Git?
   ```

5. O Copilot fornecerá algo semelhante ao seguinte comando:

   ```bash
   git checkout -b {nome_da_nova_branch}
   git push -u origin {nome_da_nova_branch}
   ```

   Em seguida, solicite ao Copilot para usar um nome específico:

   ```prompt
   Ótimo! Obrigado, Copilot! Vamos usar o nome da branch "accelerate-with-copilot".
   ```

6. Aperte o botão `Run` para executar o comando diretamente com a ajuda do Copilot.

7. Verifique na barra de status inferior esquerda do VS Code se a branch ativa é `accelerate-with-copilot`. Se sim, você concluiu esta etapa!

8. Com sua branch publicada no GitHub, aguarde que Mona verifique seu trabalho nos comentários e siga para a próxima lição.

<details>
<summary>Encontrando problemas? 🤷</summary><br/>

Se você não recebeu feedback, confira:
- O nome exato da branch criada: `accelerate-with-copilot`.
- Se a branch foi realmente publicada em seu repositório.
<<<<<<< HEAD
>>>>>>> dd563bf (Initial commit)
=======
>>>>>>> main

</details>
