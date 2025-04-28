<<<<<<< HEAD
## Step 3: Getting work done even _faster_ with Copilot Edits

In our previous steps, we used features of Copilot that require more hands-on guidance and they produced mostly localized results. Now, we will explore Copilot Edits, a feature that allows working more holistically on our repo.

[Copilot Edits](https://code.visualstudio.com/docs/copilot/copilot-edits) is an AI-powered code editing session to make changes across **multiple files** using **natural language**, and applies the edits directly in the editor, where you can review them in-place, with the full context of the surrounding code.

#### Key features

- **Multi-file Editing**: Copilot Edits can make changes across multiple files in your workspace.
- **Iterative Workflow**: Designed for fast iteration, allowing you to review, accept, or discard AI-generated code.
- **In-place Edits**: Shows generated code directly in your editor, providing a code review-like flow.
- **Working Set**: Allows you to define which files the edits should be applied to.

#### How it works

1. **Set Context**: Select files to be in the working set.
1. **Provide Instructions**: Use natural language to describe the required changes.
1. **Review Changes**: See proposed changes in-place in your code.
1. **Accept or Discard**: Review each suggested edit and choose which to keep.
1. **Iterate**: If needed, provide follow-up instructions to refine the changes.

### :keyboard: Activity: Use Copilot to add a new feature! :rocket:

1. If the Copilot Chat panel is not visible, please reopen it.

1. In the top left part of Copilot Chat window, click the **Copilot Edits** icon to switch modes.

   <img width="200" alt="image" src="https://github.com/user-attachments/assets/0b17c5bd-d03b-41b1-b97d-624fcbf8ccd1" />

1. Open the files related to our webpage then drag each editor window (or file) to the chat panel, informing Copilot to use them as context.
=======
## Passo 3: Trabalhando ainda _mais rápido_ com o Copilot Edits

Nas etapas anteriores, utilizamos recursos do Copilot que exigem uma orientação mais próxima e produziram resultados mais localizados. Agora vamos explorar o Copilot Edits, um recurso que permite trabalhar de forma mais abrangente em nosso repositório.

[Copilot Edits](https://code.visualstudio.com/docs/copilot/copilot-edits) é uma sessão de edição de código baseada em IA que realiza alterações em **vários arquivos** utilizando **linguagem natural**, aplicando as edições diretamente no editor, onde você pode revisá-las com o contexto completo do código ao redor.

#### Recursos principais

- **Edição em múltiplos arquivos**: Copilot Edits pode fazer alterações em vários arquivos no seu espaço de trabalho.
- **Fluxo iterativo**: Projetado para rápida iteração, permitindo revisar, aceitar ou descartar código gerado pela IA.
- **Edições diretas**: Exibe o código gerado diretamente no seu editor, proporcionando uma experiência semelhante à revisão de código.
- **Conjunto de trabalho**: Permite definir em quais arquivos as edições serão aplicadas.

#### Como funciona

1. **Definir Contexto**: Selecione arquivos para incluir no conjunto de trabalho.
2. **Fornecer Instruções**: Use linguagem natural para descrever as alterações necessárias.
3. **Revisar Alterações**: Veja as mudanças propostas diretamente no código.
4. **Aceitar ou Descartar**: Revise cada edição sugerida e escolha quais manter.
5. **Iterar**: Se necessário, forneça instruções adicionais para refinar as mudanças.

### :keyboard: Atividade: Use o Copilot para adicionar um novo recurso! :rocket:

1. Se o painel Copilot Chat não estiver visível, reabra-o.

2. Na parte superior esquerda da janela do Copilot Chat, clique no ícone **Copilot Edits** para mudar de modo.

   <img width="200" alt="imagem" src="https://github.com/user-attachments/assets/0b17c5bd-d03b-41b1-b97d-624fcbf8ccd1" />

3. Abra os arquivos relacionados à página web e arraste cada janela do editor (ou arquivo) para o painel de chat, informando ao Copilot para usá-los como contexto:
>>>>>>> dd563bf (Initial commit)

   - `src/static/app.js`
   - `src/static/index.html`
   - `src/static/styles.css`

<<<<<<< HEAD
   > **Tip:** You can also use the **Attach files...** button to provide other sources of context items, like a GitHub issue, the entire codebase, or the results of a terminal window.

1. Ask Copilot to update our project to display the current participants of activities. Wait a moment for the edit suggestions to arrive and be applied.

   > <img width="13px" src="https://github.com/user-attachments/assets/98fd5d2e-ea29-4a4a-9212-c7050e177a69" /> **Prompt**
   >
   > ```prompt
   > Hey Copilot, can you please edit the area where activities are
   > listed on the website to show what participants are already signed up for that activity.
   > ```

   - An extra icon has appeared next to the file names and open editor windows indicating they have suggested edits.
   - A suggested edits panel has appeared in the bottom right of the editor window providing controls to jump to the recommended changes.

      <img width="200" alt="files with icons indicating they have been edited" src="https://github.com/user-attachments/assets/9c7c2e10-cd18-43c5-9947-cffd6dde0473" />

      <img width="250" alt="edit navigation panel" src="https://github.com/user-attachments/assets/a84965a5-2f43-4c93-a814-0fdeb3a06494" />

   <details>
   <summary>Need help? 🤷</summary><br/>

   Remember, to add the relevant files to the working set.

   ![image](https://github.com/user-attachments/assets/bdd7318b-50e3-46d0-88ce-7615f45ce334)

   </details>

1. Before we simply accept the changes, please check our website again and verify everything is updated as expected. Here is an example of an updated activity card. You may need to restart the app or refresh the page.

   <img width="350" alt="Activity card with participant info" src="https://github.com/user-attachments/assets/59fe792e-d587-487d-8525-2548ac0a7adf" />

   > **Note:** Your activity card may look different. Copilot won't always produce the same results.

   <details>
   <summary>Need help? 🤷</summary><br/>
   If the website is not loading, here are some things to check.

   - Restart the VS Code Debugger to make sure the latest version of the website is served.
   - If you forgot the url, or closed the window, please review step 1.
   - Try hard refreshing the webpage or opening in a private window so it downloads a fresh copy.

   </details>

1. Now that we have confirmed our changes are good, use the panel to cycle through each suggested edit and press **Keep** to apply the change.

   > **Tip:** You can accept the changes directly, modify them, or provide additional instruction to refine them using the chat interface.

1. With our new feature complete, please **commit** and **push** the changes to GitHub.

1. Wait a moment for Mona to check your work, provide feedback, and share the the final lesson. Almost done!

<details>
<summary>Having trouble? 🤷</summary><br/>

If you don't get feedback, here are some things to check:

- Make sure your commite the changes in the `src/static/` directory to the branch `accelerate-with-copilot` and pushed/synchronized to GitHub.
- If Mona found a mistake, simply make a correction and push your changes again. Mona will check your work as many times as needed.

</details>
=======
   > **Dica:** Você também pode usar o botão **Attach files...** para fornecer outras fontes de contexto, como uma issue do GitHub, a base de código completa ou os resultados de uma janela de terminal.

4. Solicite ao Copilot atualizar o projeto para exibir os participantes atuais das atividades. Aguarde um momento para as sugestões aparecerem e serem aplicadas:

   ```prompt
   Olá Copilot, você poderia editar a área onde as atividades são listadas no site para mostrar quais participantes já estão inscritos naquela atividade?
   ```

   - Um ícone extra aparecerá ao lado dos nomes dos arquivos e das janelas do editor indicando edições sugeridas.
   - Um painel de edições sugeridas surgirá no canto inferior direito da janela do editor, oferecendo controles para navegar pelas alterações recomendadas.

5. Antes de aceitar as mudanças, confira novamente o site e verifique se tudo foi atualizado corretamente. Aqui está um exemplo de um cartão de atividade atualizado. Você pode precisar reiniciar o aplicativo ou atualizar a página.

   > **Nota:** Seu cartão de atividade pode estar diferente. O Copilot nem sempre produz resultados idênticos.

   <details>
   <summary>Precisando de ajuda? 🤷</summary><br/>
   Se o site não carregar, confira:

   - Reinicie o depurador do VS Code para garantir que a última versão do site esteja sendo exibida.
   - Se esqueceu a URL ou fechou a janela, revise o passo 1.
   - Tente atualizar a página com força ou abrir em uma janela privada para baixar uma cópia nova.

   </details>

6. Agora que as mudanças estão confirmadas, use o painel para percorrer cada edição sugerida e clique em **Keep** para aplicá-las.

   > **Dica:** Você pode aceitar as mudanças diretamente, modificá-las ou fornecer instruções adicionais usando a interface do chat.

7. Com nosso novo recurso concluído, faça o **commit** e envie (**push**) as alterações para o GitHub.

8. Aguarde um momento para Mona verificar seu trabalho, fornecer feedback e compartilhar a lição final. Está quase lá!

<details>
<summary>Encontrando problemas? 🤷</summary><br/>

Se não receber feedback, verifique:

- Se você enviou corretamente as mudanças na pasta `src/static/` para a branch `accelerate-with-copilot` e sincronizou com o GitHub.
- Caso Mona identifique um erro, faça a correção e envie novamente as alterações. Mona verificará quantas vezes forem necessárias.

</details>

>>>>>>> dd563bf (Initial commit)
