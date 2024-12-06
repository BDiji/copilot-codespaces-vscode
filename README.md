<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Master AI-Powered Coding with GitHub Copilot and VS Code</title>
    <link rel="stylesheet" href="style.css">
    <script src="script.js"></script>
</head>
<body>
    <header id="header">
        <img src="images/banner.jpg" alt="Course Banner">
        <h1>Level Up Your Development: Code with GitHub Copilot</h1>
        <p>Unleash the power of AI to write code faster and smarter.</p>
    </header>

    <main id="main">
        <section class="section">
            <h2>Introduction to AI-Driven Development</h2>
            <p>
                Welcome to "Master AI-Powered Coding with GitHub Copilot and VS Code"!  In this comprehensive course, you'll embark on a journey to transform your coding workflow by leveraging the innovative capabilities of GitHub Copilot. This powerful AI tool acts as your intelligent coding companion, suggesting real-time code completions and full lines to streamline your development process.
            </p>
            <p>
                GitHub Copilot is fueled by OpenAI Codex, a state-of-the-art generative pre-trained language model developed by OpenAI. It boasts support for a vast array of programming languages and seamlessly integrates with popular code editors like VS Code, Visual Studio, JetBrains IDEs, and Neovim. Get ready to experience a whole new level of coding efficiency and productivity!
            </p>
        </section>

        <section class="section">
            <h2>Step 1: Leverage Codespaces with VS Code for Copilot Power</h2>
            <p>
                Harness the incredible power of GitHub Codespaces, a cloud-based development environment, to unlock the full potential of GitHub Copilot. By combining these revolutionary tools, you'll establish a highly collaborative and efficient development workflow.
            </p>
            <p>
                Before we delve into the exciting world of Codespaces and Copilot, it's highly recommended that you complete the essential GitHub skill, "Codespaces" (https://github.com/skills/code-with-codespaces). This will equip you with the fundamental knowledge required to navigate Codespaces effectively.
            </p>
            <h3>Activity: Activate Copilot within a Codespace</h3>
            <p>
                We recommend opening a separate browser tab to follow these activities for easy reference.
            </p>
            <ol class="instructions">
                <li>
                    Navigate back to the **Code** tab of your repository. Click the **Add file** button (three dots) and select **Create new file**.
                </li>
                <li>
                    In the new file prompt, type or paste the following to name your file:
                    <pre>.devcontainer/devcontainer.json</pre>
                </li>
                <li>
                    Within the newly created `.devcontainer/devcontainer.json` file, add the following content:
                    <pre>
                    {
                        "name": "Codespace for Advanced Development",
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
                    Choose the option to **Commit directly to the `main` branch**, then click the **Commit new file** button.
                </li>
                <li>
                    Head back to your repository's home page by clicking the **Code** tab located in the top left corner of your screen.
                </li>
                <li>
                    Click the prominent **Code** button in the middle of the page.
                </li>
                <li>
                    Select the **Codespaces** tab on the pop-up window.
                </li>
                <li>
                    Click the **Create codespace on main** button.
                </li>
                <li>
                    **Allow approximately 2 minutes for the codespace to spin up completely.**
                </li>
                <li>
                    Verify that your codespace is up and running. Your browser should display a VS Code web-based editor alongside a terminal, similar to the image below:
                    <img src="images/codespace_screenshot.png" alt="Codespace Screenshot">
                </li>
                <li>
                    The **Copilot** extension should appear in the VS Code extension list. Click the extensions sidebar tab to view it.
                </li>
            </ol>
            <p>
                **Wait for about 60 seconds, then refresh your repository's landing page to proceed to the next step.**
            </p>
        </section>

        <section class="section">
            <h2>Step 6: Troubleshooting and Support</h2>
            <p>
                If you encounter any challenges while using GitHub Copilot, here are some steps you can take to troubleshoot and seek assistance:
            </p>
            <ul>
                <li>
                    **Consult the Official Documentation:** Refer to the comprehensive GitHub Copilot documentation for detailed information and troubleshooting tips.
                </li>
                <li>
                    **Leverage Search Engines:** Utilize search engines to find solutions to common issues. Many developers have encountered and resolved similar problems.
                </li>
                <li>
                    **Engage with the Community:** Post your query on the GitHub Copilot discussion board (https://github.com/orgs/skills/discussions/categories/code-with-copilot). The community can provide valuable insights and assistance.
                </li>
                <li>
                    **Contact GitHub Support:** If you require further support, reach out to GitHub's dedicated support team.
                </li>
            </ul>
        </section>

        <section class="section">
            <h2>Conclusion</h2>
            <p>
                Congratulations on completing the "Master AI-Powered Coding with GitHub Copilot and VS Code" course! You have now acquired the knowledge and skills to effectively leverage GitHub Copilot to enhance your coding efficiency and productivity.
            </p>
            <p>
                Continue to explore the vast capabilities of GitHub Copilot and seamlessly integrate it into your development workflow to achieve new heights in your coding endeavors.
            </p>
        </section>
    </main>

    <footer id="footer">
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
