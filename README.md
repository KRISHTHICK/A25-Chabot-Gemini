# A25-Chabot-Gemini
Gen AI

1. Create a GitHub RepositoryGo to https://github.com/ and log in to your account.Click the "+" button in the top right corner and select "New repository".Give your repository a name (e.g., "streamlit-ollama-chatbot").You can add a description if you like.Choose whether you want the repository to be public or private.Click "Create repository".Follow the instructions on the screen to connect your local repository to the remote repository.2. Set up a Local Git RepositoryOpen VS Code.Open the folder where you want to store your project.Open the terminal in VS Code (View -> Terminal).Initialize a Git repository:git init
Create a virtual environment (recommended):python3 -m venv venv
Activate the virtual environment:On Windows: venv\Scripts\activateOn macOS/Linux: source venv/bin/activateInstall the required packages:pip install streamlit requests
Save the code from the previous step (the "chatbot_streamlit_ollama" code) into a file named app.py in your project folder.3. Connect to the Remote RepositoryAdd the remote repository as an origin:git remote add origin <your_repository_url>
(Replace <your_repository_url> with the URL of your repository from GitHub)Check the remote:git remote -v
4. Commit and Push Your CodeAdd the files to the staging area:git add app.py
Commit the changes:git commit -m "Initial commit of chatbot code"
Push the changes to the remote repository:git push -u origin main
(The -u flag sets the upstream branch, so you only need to use git push next time)5. Run the ApplicationMake sure your virtual environment is activated.Run the Streamlit app:streamlit run app.py
Additional Notes.gitignore:  Create a .gitignore file in your repository to exclude files that should not be tracked by Git (e.g., venv/, __pycache__/).  Here's an example:venv/
__pycache__/
*.pyc
.DS_Store
VS Code Git Integration: VS Code has excellent Git integration.  You can use the Source Control view to commit, push, pull, and manage your repository without using the terminal.Ollama:  Make sure you have Ollama installed and running, with the model you selected (e.g., "mistral") available.  You'll need to download the model within Ollama itself.
