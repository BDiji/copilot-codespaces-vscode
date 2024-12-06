<!--
  <<< Author notes: Step 1 >>>
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
-->

## Step 1: Leverage Codespaces with VS Code for Copilot

_Welcome to "Develop With AI Powered Code Suggestions Using GitHub Copilot and VS Code"! :wave:_

GitHub Copilot is an AI pair programmer that helps you write code faster and with less work. It draws context from comments and code to suggest individual lines and whole functions instantly. GitHub Copilot is powered by OpenAI Codex, a generative pretrained language model created by OpenAI.

**Copilot works with many code editors including VS Code, Visual Studio, JetBrains IDE, and Neovim.**

Additionally, GitHub Copilot is trained on all languages that appear in public repositories. For each language, the quality of suggestions you receive may depend on the volume and diversity of training data for that language.

Using Copilot inside a Codespace shows just how easy it is to get up and running with GitHub's suite of [Collaborative Coding](https://github.com/features#features-collaboration) tools.

> **Note**
> This skills exercise will focus on leveraging GitHub Codespace. It is recommended that you complete the GitHub skill, [Codespaces](https://github.com/skills/code-with-codespaces), before moving forward with this exercise.

### :keyboard: Activity: Enable Copilot inside a Codespace

**We recommend opening another browser tab to work through the following activities so you can keep these instructions open for reference.**

Before you open up a codespace on a repository, you can create a development container and define specific extensions or configurations that will be used or installed in your codespace. Let's create this development container and add copilot to the list of extensions.

1. Navigating back to your **Code** tab of your repository, click the **Add file** drop-down button, and then click `Create new file`.
1. Type or paste the following in the empty text field prompt to name your file.
   ```
   .devcontainer/devcontainer.json
   ```
1. In the body of the new **.devcontainer/devcontainer.json** file, add the following content:
   ```
   {
       // Name this configuration
       "name": "Codespace for Skills!",
       "customizations": {
           "vscode": {
               "extensions": [
                   "GitHub.copilot"
               ]
           }
       }
   }
   ```
1. Select the option to **Commit directly to the `main` branch**, and then click the **Commit new file** button.
1. Navigate back to the home page of your repository by clicking the **Code** tab located at the top left of the screen.
1. Click the **Code** button located in the middle of the page.
1. Click the **Codespaces** tab on the box that pops up.
1. Click the **Create codespace on main** button.

   **Wait about 2 minutes for the codespace to spin itself up.**

1. Verify your codespace is running. The browser should contain a VS Code web-based editor and a terminal should be present such as the below:
   ![Screen Shot 2023-03-09 at 9 09 07 AM](https://user-images.githubusercontent.com/26442605/224102962-d0222578-3f10-4566-856d-8d59f28fcf2e.png)
1. The `copilot` extension should show up in the VS Code extension list. Click the extensions sidebar tab. You should see the following:
   ![Screen Shot 2023-03-09 at 9 04 13 AM](https://user-images.githubusercontent.com/26442605/224102514-7d6d2f51-f435-401d-a529-7bae3ae3e511.png)

**Wait about 60 seconds then refresh your repository landing page for the next step.**


<!--
  <<< Author notes: Step 2 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## Step 2: Seeing AI code suggestions in a Javascript file!

_Nice work! :tada: You created a Codespace using a devcontainer file that installed Copilot!_

GitHub Copilot provides suggestions for numerous languages and a wide variety of frameworks, but works especially well for Python, JavaScript, TypeScript, Ruby, Go, C# and C++. The following samples are in JavaScript, but other languages will work similarly.

Let's try this out utilizing Javascript for Copilot.

### :keyboard: Activity: Add a Javascript file and start writing code

1. From inside the codespace in the VS Code explorer window, create a new file.

> **Note**:
> If you closed the Codespace from above, please open it back up or create a new Codespace.

2. Name the file `skills.js`
3. Verify your new file looks like:
   ![Screen Shot 2023-03-09 at 9 21 34 AM](https://user-images.githubusercontent.com/26442605/224105906-d1beb531-b747-4c7a-85ba-a12526488422.png)
4. In the `skills.js` file, type the following function header.

   ```
   function calculateNumbers(var1, var2)
   ```

   GitHub Copilot will automatically suggest an entire function body in grayed text. Below is an example of what you'll most likely see, but the exact suggestion may vary.
   ![Screen Shot 2023-04-27 at 10 23 06 AM](https://user-images.githubusercontent.com/26442605/234941079-b4bf3e9d-fc70-4b20-b74c-0ee753ba344e.png)

5. Press `Tab` to accept the suggestion.

### :keyboard: Activity: Push code to your repository from the codespace

1. Use the VS Code terminal to add the `skills.js` file to the repository:

   ```
   git add skills.js
   ```

2. Next from the VS Code terminal stage and commit the changes to the repository:

   ```
   git commit -m "Copilot first commit"
   ```

3. Finally from the VS Code terminal push to code to the repository:

   ```
   git push
   ```

**Wait about 60 seconds then refresh your repository landing page for the next step.**


<!--
  <<< Author notes: Step 3 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## Step 3: View the GitHub Copilot tab with multiple suggestions

_Nice work! You just used AI code suggestions within a Javascript file by using GitHub Copilot :sparkles:_

Keep in mind that as you continue to use copilot, you may not want some of the suggestions GitHub Copilot offers. GitHub Copilot will show you multiple suggestions in a new tab.

### :keyboard: Activity: Pull the latest code to the Codespace repo.

> **Note**
> Pull MUST be done prior to the next activity.

1. Use the VS Code terminal to pull the latest code:

   ```
   git pull
   ```

### :keyboard: Activity: Add another Javascript method and view all suggestions

1. From inside the codespace in the VS Code explorer window, create a new file. Note: If you closed the Codespace from above please open it back up or create a new Codespace.
2. Name the file `member.js`
3. In the `member.js` file, type the following function header.
   ```
   function skillsMember()
   ```
4. Stop typing and view the Copilot suggestion by hovering over the red squiggly and select the `...`
5. Click `Open Completions Panel`. Copilot will synthesize around 10 different code suggestions. You should see something like this:
   ![Screen Shot 2023-04-27 at 10 06 55 AM](https://user-images.githubusercontent.com/26442605/234937592-d196bd5e-8ac2-4d9a-87f4-94e8a9b6a417.png)
6. Find a solution you like and click `Accept Solution`.
7. Your `member.js` file will be updated with your solution.

### :keyboard: Activity: Push code to your repository from the codespace

1. Use the VS Code terminal to add the `member.js` file to the repository:

   ```
   git add member.js
   ```

2. Next from the VS Code terminal stage and commit the changes to the repository:

   ```
   git commit -m "Copilot second commit"
   ```

3. Finally from the VS Code terminal push to code to the repository:

   ```
   git push
   ```

**Wait about 60 seconds then refresh your repository landing page for the next step.**


<!--
  <<< Author notes: Step 4 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## Step 4: Using comments to generate code with Copilot

_Nicely done utilizing the Copilot tab!_ :partying_face:

You now have leveraged the Copilot quick tab auto-suggest as well as the Copilot hub to accept AI generated suggestions.

Now lets see how you can leverage comments to generate Copilot suggestions!

### :keyboard: Activity: Pull the latest code to the Codespace repo.

> **Note**
> Pull MUST be done prior to the next activity.

1. Use the VS Code terminal to pull the latest code:

   ```
   git pull
   ```

### :keyboard: Activity: Generate Copilot suggested code from comments.

1. From inside the codespace in the VS Code explorer window, create a new file. (If you closed the Codespace from above, please open it back up or create a new Codespace.)
2. Name the file `comments.js`.
3. Type the following comment into the file:
   ```
   // Create web server
   ```
4. Press `enter` to go to a new line.
5. Copilot will suggest a code block.
6. Hover over the red squiggly and select the `...`

   > **Note**
   > If you don't see the copilot code block suggestion or the red squiggly and the three dots `...`, you can type `control + enter` to bring up the GitHub Copilot completions panel.

7. Click `Open Completions Panel`. Copilot will synthesise around 10 different code suggestions. You should see something like this:
   ![Screen Shot 2023-04-25 at 3 59 42 PM](https://user-images.githubusercontent.com/26442605/234425509-74ea96e0-bbd6-417b-84c5-73546ac7b2cd.png)
8. Find a solution you like and click `Accept Solution`.
9. Your `comments.js` file will be updated with your solution.

### :keyboard: Activity: Push code to your repository from the codespace

1. Use the VS Code terminal to add the `comments.js` file to the repository:

   ```
   git add comments.js
   ```

2. Next from the VS Code terminal stage and commit the changes to the repository:

   ```
   git commit -m "Copilot third commit"
   ```

3. Finally from the VS Code terminal push to code to the repository:

   ```
   git push
   ```

**Wait about 60 seconds then refresh your repository landing page for the next step.**


<!--
  <<< Author notes: Finish >>>
  Review what we learned, ask for feedback, provide next steps.
-->

## Finish

_Congratulations friend, you've completed this course!_

<img src="https://octodex.github.com/images/welcometocat.png" alt=celebrate width=300 align=right>

Here's a recap of all the tasks you completed:

- Set up Copilot inside a Codespace.
- Use Copilot to accept suggested code.
- Use Copilot's hub for alternate suggestions.
- Leverage comments to have Copilot auto-suggest code.

### Additional learning and resources

- [Copilot for Individuals](https://docs.github.com/en/copilot/overview-of-github-copilot/about-github-copilot-for-individuals)
- [Copilot for Business](https://docs.github.com/en/copilot/overview-of-github-copilot/about-github-copilot-for-business)
- [Getting started with Copilot](https://docs.github.com/en/copilot/getting-started-with-github-copilot/getting-started-with-github-copilot-in-visual-studio-code)
- [Configure Copilot settings](https://docs.github.com/en/copilot/configuring-github-copilot/configuring-github-copilot-settings-on-githubcom)

### What's next?

- [We'd love to hear what you thought of this course](https://github.com/orgs/skills/discussions/categories/code-with-copilot).
- [Learn another GitHub skill](https://github.com/skills).
- [Read the Get started with GitHub docs](https://docs.github.com/en/get-started).
- To find projects to contribute to, check out [GitHub Explore](https://github.com/explore).
