```markdown
# Git Repository Manager

This Streamlit application provides a simple interface for managing Git repositories. It allows users to clone, checkout branches, add, commit, and push changes to a remote Git repository directly from a web browser.

## Features

*   **Clone Repository:** Clones a public Git repository to a local directory.
*   **Branch Management:** Fetches and lists branches from the remote repository, allows selecting an existing branch or creating a new one.
*   **File Selection:** Lists files and folders in the local repository and allows selecting files to be added to the commit.
*   **Commit and Push:** Commits the selected files with a user-provided message and pushes the changes to the remote repository.
*   **Git Configuration:** Allows setting Git username and email for commits.
*   **Error Handling:** Provides error messages for common Git operations failures.
*   **Force Push:** Attempts a force push if a normal push fails.
*   **Branch Creation:** Creates a new branch if it doesn't exist on the remote.

## File Structure

```
├── app.py
└── requirements.txt
```

*   `app.py`: The main Streamlit application script.
*   `requirements.txt`: Lists the Python dependencies required to run the application.

## Dependencies

*   streamlit
*   gitpython
*   pandas
*   matplotlib
*   numpy

## Usage Instructions

1.  **Install Dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

2.  **Run the Application:**

    ```bash
    streamlit run app.py
    ```

3.  **Access the Application:**

    Open your web browser and navigate to the URL provided by Streamlit (usually `http://localhost:8501`).

4.  **Configure the Repository:**

    *   In the sidebar, enter the public Git repository URL.
    *   Click "Fetch Branches" to retrieve the available branches.
    *   Select an existing branch or create a new one by checking the "Create new branch" checkbox and entering a name.
    *   Enter the local folder path where the repository will be cloned.
    *   Click "Set up repository" to clone the repository and checkout the selected branch.

5.  **Perform Git Operations:**

    *   In the main area, select the files to add to the commit by checking the corresponding checkboxes.
    *   Enter a commit message in the text area.
    *   Click "Commit and Push Changes" to commit the selected files and push the changes to the remote repository.

6.  **Git User Configuration:**

    *   In the sidebar, enter your Git username and email address. These will be used for the commits.

## Notes

*   The application requires a public Git repository URL.
*   The local folder path should be an existing directory or a new directory that the application can create.
*   The application uses the GitPython library to perform Git operations.
*   The application uses Streamlit's session state to persist variables across reruns.
*   Force push is attempted only when a normal push fails. Use with caution.
```