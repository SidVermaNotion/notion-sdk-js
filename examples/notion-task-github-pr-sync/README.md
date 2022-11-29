# Sample Integration: GitHub PRs to Notion

<img src="https://dev.notion.so/front-static/external/readme/images/github-notion-example@2x.png" alt="drawing" width="500"/>

## About the Integration

This Notion integration updates Notion tasks when a linked Github PR is closed/merged. This integration requires the Notion task link be mentioned in the PR description. This integration was built using  [GitHub's Octokit Library](https://github.com/octokit).

## Running Locally

### 1. Setup your local project

```zsh
# Clone this repository locally
git clone https://github.com/makenotion/notion-sdk-js.git

# Switch into this project
cd notion-sdk-js/examples/notion-task-github-pr-sync

# Install the dependencies
npm install
```

### 2. Set your environment variables in a `.env` file

```zsh
GITHUB_KEY=<your-github-personal-access-token>
NOTION_KEY=<your-notion-api-key>
NOTION_DATABASE_ID=<notion-database-id>
GITHUB_REPO_OWNER=<github-owner-username>
GITHUB_REPO_NAME=<github-repo-name>
```

You can create your Notion API key [here](https://www.notion.com/my-integrations).

You can create your GitHub Personal Access token by following the guide [here](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).

To create a Notion database that will work with this example, duplicate [this empty database template](https://www.notion.com/367cd67cfe8f49bfaf0ac21305ebb9bf?v=bc79ca62b36e4c54b655ceed4ef06ebd).

### 3. Run code

```zsh
node index.js
```