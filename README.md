<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Develop With AI-Powered Code Suggestions Using GitHub Copilot and VS Code</title>
    <style>
        body {
            background-color: black;
            color: white;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header, main, footer {
            padding: 20px;
        }
        header {
            background-color: black;
            color: red;
            text-align: center;
        }
        header img {
            width: 100%;
            max-width: 1280px;
            height: auto;
        }
        header h1 {
            font-size: 36px;
            margin: 20px 0;
        }
        header p {
            font-size: 20px;
            font-weight: bold;
            margin: 10px 0;
        }
        main {
            background-color: black;
            color: white;
        }
        main h2 {
            font-size: 28px;
            margin: 20px 0;
            border-bottom: 2px solid red;
            padding-bottom: 10px;
        }
        main h3 {
            font-size: 24px;
            margin: 20px 0;
            border-bottom: 1px solid red;
            padding-bottom: 5px;
        }
        main p {
            font-size: 18px;
            line-height: 1.6;
        }
        main ol, main ul {
            font-size: 18px;
            line-height: 1.6;
            margin-left: 20px;
        }
        main li {
            margin-bottom: 10px;
        }
        main pre {
            background-color: #333;
            color: red;
            padding: 10px;
            border-radius: 5px;
            overflow-x: auto;
        }
        main img {
            max-width: 100%;
            height: auto;
            margin: 20px 0;
        }
        main a {
            color: red;
            text-decoration: none;
        }
        main a:hover {
            text-decoration: underline;
        }
        footer {
            background-color: black;
            color: red;
            text-align: center;
        }
        footer hr {
            border: 1px solid red;
            margin: 20px 0;
        }
        footer p {
            font-size: 16px;
            margin: 10px 0;
        }
    </style>
</head>
<body>

<header>
    <img src="https://example.com/1280x640-image.png" alt="Course Banner">
    <h1>Code with GitHub Copilot</h1>
    <p>
        GitHub Copilot can help you code by offering autocomplete-style suggestions right in VS Code and Codespaces.
    </p>
</header>

<main>

    <section>
        <h2>Introduction</h2>
        <p>
            Welcome to "Develop With AI-Powered Code Suggestions Using GitHub Copilot and VS Code"! :wave: In this course, you will learn how to leverage GitHub Copilot to enhance your coding efficiency and productivity. GitHub Copilot is an AI pair programmer that provides real-time code suggestions, helping you write code faster and with less effort.
        </p>
        <p>
            GitHub Copilot is powered by OpenAI Codex, a generative pretrained language model created by OpenAI. It supports a wide range of programming languages and integrates seamlessly with popular code editors like VS Code, Visual Studio, JetBrains IDE, and Neovim.
        </p>
    </section>

    <section>
        <h2>Step 1: Leverage Codespaces with VS Code for Copilot</h2>
        <p>
            GitHub Codespaces is a powerful tool that allows you to develop in a cloud-based environment. By combining Codespaces with GitHub Copilot, you can create a highly efficient and collaborative development workflow.
        </p>
        <p>
            Before you begin, it is recommended that you complete the GitHub skill, <a href="https://github.com/skills/code-with-codespaces">Codespaces</a>, to familiarize yourself with the basics of using Codespaces.
        </p>
        <h3>Activity: Enable Copilot inside a Codespace</h3>
        <p>
            We recommend opening another browser tab to work through the following activities so you can keep these instructions open for reference.
        </p>
        <ol>
            <li>
                Navigate back to your <strong>Code</strong> tab of your repository, click the <strong>Add file</strong> drop-down button, and then click <strong>Create new file</strong>.
            </li>
            <li>
                Type or paste the following in the empty text field prompt to name your file:
                <pre>
                    .devcontainer/devcontainer.json
                </pre>
            </li>
            <li>
                In the body of the new <strong>.devcontainer/devcontainer.json</strong> file, add the following content:
                <pre>
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
                </pre>
            </li>
            <li>
                Select the option to <strong>Commit directly to the `main` branch</strong>, and then click the <strong>Commit new file</strong> button.
            </li>
            <li>
                Navigate back to the home page of your repository by clicking the <strong>Code</strong> tab located at the top left of the screen.
            </li>
            <li>
                Click the <strong>Code</strong> button located in the middle of the page.
            </li>
            <li>
                Click the <strong>Codespaces</strong> tab on the box that pops up.
            </li>
            <li>
                Click the <strong>Create codespace on main</strong> button.
            </li>
            <li>
                <strong>Wait about 2 minutes for the codespace to spin itself up.</strong>
            </li>
            <li>
                Verify your codespace is running. The browser should contain a VS Code web-based editor and a terminal should be present, similar to the following:
                <img src="https://user-images.githubusercontent.com/26442605/224102962-d0222578-3f10-4566-856d-8d59f28fcf2e.png" alt="Codespace Screenshot">
            </li>
            <li>
                The <strong>copilot</strong> extension should show up in the VS Code extension list. Click the extensions sidebar tab. You should see the following:
                <img src="https://user-images.githubusercontent.com/26442605/224102514-7d6d2f51-f435-401d-a529-7bae3ae3e511.png" alt="Copilot Extension">
            </li>
        </ol>
        <p>
            <strong>Wait about 60 seconds then refresh your repository landing page for the next step.</strong>
        </p>
    </section>

    <section>
        <h2>Step 2: Configure Advanced Settings for Copilot</h2>
        <p>
            GitHub Copilot offers several advanced settings that can be configured to tailor its behavior to your specific needs. These settings can be managed through the VS Code settings editor.
        </p>
        <h3>Activity: Configure Copilot Settings</h3>
        <ol>
            <li>
                Open the VS Code settings editor by clicking on the gear icon in the lower-left corner of the Codespace and selecting <strong>Settings</strong>.
            </li>
            <li>
                In the settings editor, search for <strong>Copilot</strong> to find the relevant settings.
            </li>
            <li>
                Configure the following settings as needed:
                <ul>
                    <li>
                        <strong>Copilot: Enable</strong> - Enable or disable Copilot globally.
                    </li>
                    <li>
                        <strong>Copilot: Suggest Snippets</strong> - Enable or disable snippet suggestions.
                    </li>
                    <li>
                        <strong>Copilot: Suggest Full Lines</strong> - Enable or disable full line suggestions.
                    </li>
                    <li>
                        <strong>Copilot: Suggest Inline</strong> - Enable or disable inline suggestions.
                    </li>
                    <li>
                        <strong>Copilot: Suggest On Commit</strong> - Enable or disable suggestions on commit.
                    </li>
                </ul>
            </li>
            <li>
                Save your settings by clicking the <strong>Apply</strong> button or simply closing the settings editor.
            </li>
        </ol>
    </section>

    <section>
        <h2>Step 3: Collaborate with Copilot in Real-Time</h2>
        <p>
            GitHub Copilot can be used in a collaborative environment to enhance team productivity. By sharing your Codespace with team members, you can work together on the same project while leveraging Copilot's AI-powered suggestions.
        </p>
        <h3>Activity: Share Your Codespace</h3>
        <ol>
            <li>
                Open your Codespace in VS Code.
            </li>
            <li>
                Click on the <strong>Codespaces</strong> icon in the left sidebar.
            </li>
            <li>
                Click on the <strong>Share</strong> button to generate a shareable link.
            </li>
            <li>
                Share the link with your team members.
            </li>
            <li>
                Team members can open the shared Codespace and start collaborating with you in real-time.
            </li>
        </ol>
    </section>

    <section>
        <h2>Step 4: Advanced Use Cases and Tips</h2>
        <p>
            GitHub Copilot can be used for a variety of advanced use cases, from generating complex algorithms to writing documentation. Here are some tips to help you get the most out of Copilot:
        </p>
        <ul>
            <li>
                <strong>Use Comments for Context</strong> - Write clear and descriptive comments to provide context for Copilot. This will help it generate more accurate and relevant suggestions.
            </li>
            <li>
                <strong>Experiment with Different Languages</strong> - Copilot supports a wide range of programming languages. Try using it with different languages to see how it performs.
            </li>
            <li>
                <strong>Customize Your Development Container</strong> - Customize your development container to include specific tools and dependencies that are relevant to your project.
            </li>
            <li>
                <strong>Use Copilot with Git</strong> - Use Copilot to generate commit messages, pull request descriptions, and other Git-related tasks.
            </li>
            <li>
                <strong>Integrate with CI/CD Pipelines</strong> - Integrate Copilot with your CI/CD pipelines to automate code generation and testing.
            </li>
        </ul>
    </section>

    <section>
        <h2>Step 5: Best Practices and Common Pitfalls</h2>
        <p>
            To ensure you get the most out of GitHub Copilot, it's important to follow best practices and be aware of common pitfalls. Here are some tips to help you:
        </p>
        <ul>
            <li>
                <strong>Regularly Update Copilot</strong> - Ensure that you are using the latest version of Copilot to benefit from the latest features and improvements.
            </li>
            <li>
                <strong>Review Suggestions</strong> - Always review the suggestions provided by Copilot before accepting them. While Copilot is highly accurate, it's important to verify the code for correctness and security.
            </li>
            <li>
                <strong>Use Version Control</strong> - Use version control systems like Git to track changes and revert to previous versions if needed.
            </li>
            <li>
                <strong>Document Your Code</strong> - Even with Copilot's assistance, it's important to write clear and concise documentation for your code. This helps other developers understand your code and maintain it more effectively.
            </li>
            <li>
                <strong>Test Thoroughly</strong> - Always test your code thoroughly, especially when using AI-generated suggestions. Automated testing can help catch issues early in the development process.
            </li>
        </ul>
    </section>

    <section>
        <h2>Step 6: Troubleshooting and Support</h2>
        <p>
            If you encounter any issues while using GitHub Copilot, here are some steps you can take to troubleshoot and get support:
        </p>
        <ul>
            <li>
                <strong>Check the Documentation</strong> - Refer to the official GitHub Copilot documentation for detailed information and troubleshooting tips.
            </li>
            <li>
                <strong>Search for Solutions</strong> - Use search engines to find solutions to common issues. Many developers have encountered and solved similar problems.
            </li>
            <li>
                <strong>Post in the Discussion Board</strong> - If you can't find a solution, post your issue in the <a href="https://github.com/orgs/skills/discussions/categories/code-with-copilot">GitHub Copilot discussion board</a>. The community can provide valuable insights and help.
            </li>
            <li>
                <strong>Contact Support</strong> - If you need further assistance, you can contact GitHub support for help.
            </li>
        </ul>
    </section>

    <section>
        <h2>Conclusion</h2>
        <p>
            Congratulations on completing the "Develop With AI-Powered Code Suggestions Using GitHub Copilot and VS Code" course! You have learned how to set up and use GitHub Copilot in a Codespace, configure advanced settings, collaborate with team members, and explore advanced use cases.
        </p>
        <p>
            Continue to explore the capabilities of GitHub Copilot and integrate it into your development workflow to enhance your productivity and code quality.
        </p>
    </section>

</main>

<footer>
    <hr>
    <p>
        Get help: <a href="https://github.com/orgs/skills/discussions/categories/code-with-copilot">Post in our discussion board</a> &bull; <a href="https://www.githubstatus.com/">Review the GitHub status page</a>
    </p>
    <p>
        &copy; 2023 GitHub &bull; <a href="https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md">Code of Conduct</a> &bull; <a href="https://gh.io/mit">MIT License</a>
    </p>
</footer>

</body>
</html>
