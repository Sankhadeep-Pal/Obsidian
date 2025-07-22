# Personal Access Token

If we use our system terminal to upload local repository to remote repository on GitHub via HTTPS, we need a PAT.
## Process to create Personal Access Token
#### 1. **Log In to GitHub**

- Go to [GitHub](https://github.com) 

- Sign in to your GitHub account.

#### 2. **Navigate to Developer Settings**

- Click on your profile picture (top right) → **Settings**

- Scroll down the left sidebar and click **Developer settings**

#### 3. **Go to Personal Access Tokens**

- Under **Developer settings**, click **Personal access tokens**

- Choose one of the following:
    - **Tokens (classic)** – Older method (still available but being phased out)
	 
	- **Fine-grained tokens** – Recommended (more secure and flexible)        

---

#### If You Choose **Fine-grained Token** (Recommended):

a. **Token name**: Enter a name to identify the token

b. **Expiration**: Choose how long the token will be valid

c. **Resource owner**: Usually your account

d. **Repository access**: Choose repositories the token can access

e. **Permissions**: Select required permissions (e.g., `repo`, `workflow`, `admin:org`, etc.)

Click **Generate token** at the bottom.

---

### 🔑 **Copy Your Token**

Once generated, **copy it immediately**. You won’t be able to see it again.

---

### 💡 **Using the Token**

Use the token in place of your GitHub password when accessing:

- Git operations via HTTPS (e.g., `git push`)

- GitHub API

- Third-party apps