<<<<<<< HEAD
<<<<<<< HEAD
## Step 2: Getting work done with Copilot

In the previous step, GitHub Copilot was able to help us onboard to the project. That alone is a huge time saver, but now let's get some work done!

We recently learned there is a bug where students are registering for the same activities twice. That simply isn't acceptable, so let's get it fixed!

Unfortunately, we were given little information to solve this problem. So, let's enlist Copilot to help find the problem area and get a potential solution made.

But before we do that, let's learn a bit more about Copilot! 🧑‍🚀

### How does Copilot work?

In short, you can think of Copilot like a very focused coworker. To be effective with them, you need to provide them background (context) and clear direction (prompts). Additionally, different people are better at different things because of their unique experiences (models).

- **How do we provide context?:** In our coding environment, Copilot will automatically consider nearby code and open tabs. If you are using chat, you can also explicitly refer to files.

- **What model should we pick?:** For our exercise, it shouldn't matter too much. Experimenting with different models is part of the fun! That's another lesson! 🤖

- **How do I make prompts?:** Being explicit and clear helps Copilot do the best job. But unlike some traditional systems, you can always clarify your direction with followup prompts.

### :keyboard: Activity: Use Copilot to fix our registration bug :bug:

1. Let's ask Copilot to suggest where our bug might be coming from. Open the **Copilot Chat** panel and ask the following.

   > <img width="13px" src="https://github.com/user-attachments/assets/98fd5d2e-ea29-4a4a-9212-c7050e177a69" /> **Prompt**
   >
   > ```prompt
   > @workspace Students are able to register twice for an activity.
   > Where could this bug be coming from?
   > ```

1. Now that we know the issue is in the `src/appy.py` file and the `signup_for_activity` method, let's follow Copilot's recommendation and go fix it (semi-manually). We'll start with a comment and let Copilot finish the correction.

   1. In VS Code, select the file **Explorer tab** to show the project files and open the `src/app.py` file.

   1. Scroll near the bottom of the file and find the `signup_for_activity` method.

   1. Find the comment line that describes adding a student. Above this is where it seems logical to do our registration check.

   1. Enter the below comment and press enter to go to the next line. After a moment, temporary shadow text will appear with a suggestion from Copilot! Nice! :tada:

      ```python
      # Validate student is not already signed up
      ```

   1. Press `Tab` to accept Copilot's suggestion and convert the shadow text to code.

      > **Tip:** If you would like to see other suggestions, instead of pressing `Tab`, hover over the shadow text suggestion and a toolbar will appear. Use the arrows to select other suggestions or the three dots `...` and `Open Completions Panel` option to show all suggestions in a dedicated panel.

   <details>
   <summary>Example Results</summary><br/>

   Copilot is growing every day and may not always produce the same results. If you are unhappy with the suggestions, here is an example of a valid suggestion result we produced during the making of this exercise. You can use it to continue forward.

   ```python
   @app.post("/activities/{activity_name}/signup")
   def signup_for_activity(activity_name: str, email: str):
      """Sign up a student for an activity"""
      # Validate activity exists
      if activity_name not in activities:
         raise HTTPException(status_code=404, detail="Activity not found")

      # Get the activity
      activity = activities[activity_name]

      # Validate student is not already signed up
      if email in activity["participants"]:
        raise HTTPException(status_code=400, detail="Student is already signed up")

      # Add student
      activity["participants"].append(email)
      return {"message": f"Signed up {email} for {activity_name}"}
   ```

   </details>

### :keyboard: Activity: Let Copilot generate sample data 📋

In new project developments, it's often helpful to have some realistic looking fake data for testing. Copilot is excellent at this task, so let's add some more sample activities and introduce another way to interact with Copilot using **Inline Chat**

**Inline Chat** and the **Copilot Chat** panel are very similar tools, but with slightly different automatic context. As such, while Copilot Chat is good at explaining about the project, inline chat might feel more natural for asking about a particular line or function.

1. If not already open, open the `src/app.py` file.

1. Near the top (about line 23), find the `activities` variable, where our example extracurricular activies are configured.

1. Open Copilot inline chat by right-clicking on any of the related lines and selecting **Copilot** and **Editor Inline Chat**.

   > **Tip:** You can also use the keyboard command `Ctrl + I` (windows) or `Cmd + I` (mac).

1. Enter the following prompt text and press enter or the **Send and Dispatch** button.

   > <img width="13px" src="https://github.com/user-attachments/assets/98fd5d2e-ea29-4a4a-9212-c7050e177a69" /> **Prompt**
   >
   > ```prompt
   > Add 2 more sports related activities, 2 more artistic
   > activities, and 2 more intellectual activities.
   > ```

1. After a moment, Copilot will directly start making changes to the code. The changes will be stylized differently to make any additions and removals easy to identify. Take a moment to inspect and then press the **Accept** button.

<details>
<summary>Example Results</summary><br/>

Copilot is growing every day and may not always produce the same results. If you are unhappy with the suggestions, here is an example result we produced during the making of this exercise. You can use it to continue forward, if having trouble.

```python
# In-memory activity database
activities = {
   "Chess Club": {
      "description": "Learn strategies and compete in chess tournaments",
      "schedule": "Fridays, 3:30 PM - 5:00 PM",
      "max_participants": 12,
      "participants": ["michael@mergington.edu", "daniel@mergington.edu"]
   },
   "Programming Class": {
      "description": "Learn programming fundamentals and build software projects",
      "schedule": "Tuesdays and Thursdays, 3:30 PM - 4:30 PM",
      "max_participants": 20,
      "participants": ["emma@mergington.edu", "sophia@mergington.edu"]
   },
   "Gym Class": {
      "description": "Physical education and sports activities",
      "schedule": "Mondays, Wednesdays, Fridays, 2:00 PM - 3:00 PM",
      "max_participants": 30,
      "participants": ["john@mergington.edu", "olivia@mergington.edu"]
   },
   "Basketball Team": {
      "description": "Competitive basketball training and games",
      "schedule": "Tuesdays and Thursdays, 4:00 PM - 6:00 PM",
      "max_participants": 15,
      "participants": []
   },
   "Swimming Club": {
      "description": "Swimming training and water sports",
      "schedule": "Mondays and Wednesdays, 3:30 PM - 5:00 PM",
      "max_participants": 20,
      "participants": []
   },
   "Art Studio": {
      "description": "Express creativity through painting and drawing",
      "schedule": "Wednesdays, 3:30 PM - 5:00 PM",
      "max_participants": 15,
      "participants": []
   },
   "Drama Club": {
      "description": "Theater arts and performance training",
      "schedule": "Tuesdays, 4:00 PM - 6:00 PM",
      "max_participants": 25,
      "participants": []
   },
   "Debate Team": {
      "description": "Learn public speaking and argumentation skills",
      "schedule": "Thursdays, 3:30 PM - 5:00 PM",
      "max_participants": 16,
      "participants": []
   },
   "Science Club": {
      "description": "Hands-on experiments and scientific exploration",
      "schedule": "Fridays, 3:30 PM - 5:00 PM",
      "max_participants": 20,
      "participants": []
   }
}
```

</details>

### :keyboard: Activity: Use Copilot to describe our work 💬

Nice work fixing that bug and expanding the example activities! Now let's get our work committed and pushed to GitHub, again with the help of Copilot!

1. In the left sidebar, select the `Source Control` tab.

   > **Tip:** Opening a file from the source control area will show the differences to the original rather than simply opening it.

1. Find the `app.py` file and press the `+` sign to collect your changes together in the staging area.

   ![image](https://github.com/user-attachments/assets/7d3daf4e-4125-4775-88a7-33251cd7293e)

1. Above the list of staged changes, find the **Message** text box, but **don't enter anything** for now.

   - Typically, you would write a short description of the changes here, but now we have Copilot to help out!

1. To the right of the **Message** text box, find and click the **Generate Commit Message with Copilot** button (sparkles icon).

1. Press the **Commit** button and **Sync Changes** button to push your changes to GitHub.

1. Wait a moment for Mona to check your work, provide feedback, and share the next lesson.

<details>
<summary>Having trouble? 🤷</summary><br/>

If you don't get feedback, here are some things to check:

- Make sure your pushed the `src/app.py` file changes to the branch `accelerate-with-copilot`.

</details>
=======
=======
>>>>>>> main
## Passo 2: Trabalhando com o Copilot

Na etapa anterior, o GitHub Copilot nos ajudou a entender o projeto. Só isso já economiza muito tempo, mas agora vamos colocar a mão na massa!

Recentemente descobrimos um bug onde estudantes estão se cadastrando duas vezes na mesma atividade. Isso não é aceitável, então vamos consertar isso!

Infelizmente, recebemos poucas informações sobre esse problema. Portanto, vamos usar o Copilot para encontrar o problema e criar uma solução potencial.

Mas antes, vamos aprender mais sobre o Copilot! 🧑‍🚀

### Como o Copilot funciona?

Você pode pensar no Copilot como um colega de trabalho muito focado. Para que ele seja eficaz, você precisa fornecer contexto e instruções claras (prompts). Além disso, pessoas diferentes são boas em coisas diferentes por causa de suas experiências únicas (modelos).

- **Como fornecer contexto?** No nosso ambiente de programação, o Copilot considera automaticamente o código próximo e as abas abertas. Se estiver usando o chat, você também pode se referir explicitamente a arquivos.

- **Qual modelo escolher?** Para nosso exercício, isso não importa muito. Experimentar modelos diferentes faz parte da diversão! 🤖

- **Como criar prompts?** Ser [explícito e claro](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/2-prompt-engineering-foundations-best-practices) ajuda o Copilot a trabalhar melhor. Diferentemente de sistemas tradicionais, você sempre pode esclarecer seu pedido com prompts adicionais.

### Atividade: Use o Copilot para corrigir o bug de registro

1. Peça ao Copilot sugestões sobre a possível origem do bug. Abra o painel **Copilot Chat** e pergunte:

   ```prompt
   @workspace Os alunos conseguem se inscrever duas vezes em uma atividade. De onde pode estar vindo esse bug?
   ```

2. Sabendo que o problema está no arquivo `src/app.py` e no método `signup_for_activity`, siga a recomendação do Copilot e corrija o problema (semi-manualmente):

   1. No VS Code, abra a aba **Explorer** e o arquivo `src/app.py`.
   2. Role até o método `signup_for_activity`.
   3. Localize o comentário que descreve a adição do estudante. Acima dele parece lógico fazer nossa validação.
   4. Insira o comentário abaixo e pressione enter. O Copilot sugerirá automaticamente uma solução!

      ```python
      # Validar se o aluno já está inscrito
      ```

   5. Pressione `Tab` para aceitar a sugestão do Copilot.

### :keyboard: Atividade: Gere dados de exemplo usando o Copilot 📋

Em novos projetos, é útil ter dados fictícios realistas para testes. O Copilot é excelente nisso, então vamos adicionar atividades adicionais usando o **Inline Chat**.

**Inline Chat** é parecido com o painel **Copilot Chat**, mas com contexto mais específico para linhas ou funções individuais.

1. Abra o arquivo `src/app.py`.
2. Próximo à linha 23, encontre a variável `activities`.
3. Clique com o botão direito sobre as linhas relacionadas e selecione **Copilot → Editor Inline Chat**.
4. Insira o prompt abaixo e envie:

   ```prompt
   Adicione mais 2 atividades esportivas, 2 artísticas e 2 intelectuais.
   ```

5. Após o Copilot sugerir mudanças diretamente no código, revise e clique em **Accept**.

### :keyboard: Atividade: Use o Copilot para descrever nosso trabalho 💬

Ótimo trabalho corrigindo o bug e expandindo as atividades! Vamos agora enviar nosso trabalho para o GitHub novamente com ajuda do Copilot!

1. Na barra lateral esquerda, selecione a aba `Source Control`.
2. Localize o arquivo `app.py` e pressione o sinal `+` para preparar suas alterações.
3. Acima das alterações, encontre o campo **Message**, mas não escreva nada ainda.
4. Clique no botão **Generate Commit Message with Copilot** (ícone com brilhos).
5. Clique em **Commit** e depois em **Sync Changes** para enviar ao GitHub.
6. Aguarde Mona verificar seu trabalho, fornecer feedback e compartilhar a próxima lição.

<details>
<summary>Encontrando problemas? 🤷</summary><br/>

Se não houver feedback, verifique:
- Se você enviou corretamente as alterações no arquivo `src/app.py` para a branch `accelerate-with-copilot`.

</details>

<<<<<<< HEAD
>>>>>>> dd563bf (Initial commit)
=======
>>>>>>> main
