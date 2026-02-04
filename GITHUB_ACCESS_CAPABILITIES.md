# GitHub Access Capabilities

## Overview
This document explains what can be accessed within GitHub through the Copilot agent and available tools.

## What I CAN Access

### 1. Repository Content
✅ **Full access to repository files and structure**
- Read any file in the repository
- View directory structures
- Navigate the entire codebase
- Access file history through git

### 2. GitHub API via GitHub MCP Server
✅ **Comprehensive GitHub data access through specialized tools:**

#### Repository Information
- Search repositories across GitHub
- View repository metadata
- List branches, tags, and releases
- Access commit history and details

#### Issues
- List issues in repositories
- Read issue details, comments, and labels
- Search issues across repositories
- View issue sub-issues and metadata

#### Pull Requests
- List pull requests
- Read PR details, reviews, and comments
- View PR diffs and file changes
- Check PR status and checks
- Search pull requests

#### GitHub Actions
- List workflows in repositories
- View workflow runs and their status
- Get job logs (including failed jobs)
- Download workflow artifacts
- Check workflow run usage

#### Security
- List code scanning alerts
- View secret scanning alerts
- Get details of specific security alerts

#### Releases and Tags
- List releases in repositories
- Get latest release information
- View release details by tag
- Access git tag information

#### Commits
- List commits on branches
- View commit details with diffs
- Filter commits by author
- Access commit statistics

### 3. Web Access
✅ **Limited web browsing capabilities**
- Fetch content from web pages (converted to markdown or raw HTML)
- Access public documentation
- Retrieve information from allowed domains

### 4. Code Search
✅ **Powerful search capabilities**
- Search code across all GitHub repositories
- Use advanced GitHub search syntax
- Find specific functions, classes, or patterns
- Filter by language, organization, or repository

### 5. Local Repository Operations
✅ **Full git operations on cloned repository**
- Make commits
- Create branches
- View diffs and status
- Work with local files

## What I CANNOT Access

### GitHub Features I Cannot Use Directly

❌ **Cannot create or modify GitHub resources:**
- Cannot create new issues
- Cannot update existing issues (descriptions, assignees, labels)
- Cannot create pull requests
- Cannot update PR descriptions
- Cannot create releases
- Cannot modify repository settings
- Cannot manage GitHub Actions workflows

❌ **Cannot access:**
- Private repositories (unless specifically granted access)
- GitHub Codespaces (cannot launch or interact with them)
- GitHub Projects/Boards
- GitHub Discussions (no specialized tools available)
- GitHub Packages (limited access)
- Organization settings
- Team management features

❌ **Git limitations:**
- Cannot pull branches from GitHub (merge conflicts requiring branch pulling cannot be resolved)
- Cannot use `git push` directly (must use report_progress tool)
- Cannot use `git reset` or `git rebase` with force push
- Cannot clone additional repositories
- Cannot push to other repositories
- Note: Simple merge conflicts in already-pulled code can be resolved through local file editing

### Workarounds Available

While I cannot directly create/modify certain GitHub resources, I can:

1. **For Issues**: Create formatted content that you can copy-paste to create an issue
2. **For PRs**: Use `report_progress` tool to commit and push changes to the current PR
3. **For Documentation**: Create markdown files with all necessary information

## Available GitHub Tools

### GitHub MCP Server Tools

1. **Repository Search**: `search_repositories`
   - Find repositories by name, description, topics, etc.
   - Filter by stars, language, organization

2. **Code Search**: `search_code`
   - Search code across all GitHub repositories
   - Use GitHub's code search syntax

3. **Issue Management**: `list_issues`, `issue_read`, `search_issues`
   - List and read issues
   - Search with advanced filters
   - View comments and metadata

4. **Pull Request Operations**: `list_pull_requests`, `pull_request_read`, `search_pull_requests`
   - List PRs with filters
   - Read PR details, diffs, reviews
   - View PR status and checks

5. **Actions**: `actions_list`, `actions_get`, `get_job_logs`
   - Monitor workflow runs
   - Download logs
   - Check run status

6. **Security**: `list_code_scanning_alerts`, `list_secret_scanning_alerts`
   - View security alerts
   - Get alert details

7. **Releases**: `list_releases`, `get_latest_release`, `get_release_by_tag`
   - Access release information
   - View release assets

## Examples of What I Can Do

### Example 1: Analyze Repository Issues
```bash
# I can search for and analyze issues
- List all open issues in a repository
- Find issues with specific labels
- Read issue comments and discussions
- Identify patterns in issue reports
```

### Example 2: Review Pull Requests
```bash
# I can thoroughly review PRs
- Get PR diffs and file changes
- Read all comments and reviews
- Check CI/CD status
- Analyze code changes
```

### Example 3: Monitor CI/CD
```bash
# I can investigate build failures
- List recent workflow runs
- Get logs from failed jobs
- Identify failure patterns
- Suggest fixes based on logs
```

### Example 4: Search Across GitHub
```bash
# I can search for code patterns
- Find similar implementations
- Locate library usage examples
- Identify best practices
- Search by language or organization
```

## GitHub Codespaces

**Question**: Can I access GitHub Codespaces?

**Answer**: No, I cannot directly launch, access, or interact with GitHub Codespaces. However:
- I'm running in a sandboxed environment similar to Codespaces
- I have access to the cloned repository locally
- I can perform all development tasks within this environment
- I can read, edit, and test code
- I can run build tools, tests, and linters

## Best Practices

When working with GitHub resources:

1. **Use available tools** - Leverage GitHub MCP server tools for data retrieval
2. **Create templates** - For things I can't create directly (issues, etc.), I'll create formatted templates
3. **Provide instructions** - Include clear steps for manual actions needed
4. **Use report_progress** - For committing and pushing changes to PRs
5. **Search efficiently** - Use code/issue search tools before making assumptions

## Summary

I have extensive **read access** to GitHub resources through specialized tools, but limited **write access**. I can:
- ✅ Read and analyze any public GitHub content
- ✅ Search code, issues, PRs across GitHub
- ✅ Monitor CI/CD workflows and logs
- ✅ Work with repository files locally
- ✅ Commit changes via report_progress

I cannot:
- ❌ Create issues, PRs, or releases directly
- ❌ Access GitHub Codespaces
- ❌ Modify repository settings
- ❌ Manage organizations or teams

For any write operations I cannot perform, I'll create comprehensive templates and instructions for manual execution.
