# Automatic LeetCode Submission

This project automates the daily submission of LeetCode problems using GitHub Actions and Selenium. The submissions are scheduled using cron syntax, making it easy to manage and automate your LeetCode streak.

## Introduction

This repository hosts a script that automates the process of solving and submitting a LeetCode problem daily. The automation is set up using GitHub Actions and Selenium. The submission is triggered daily by a scheduled cron job, ensuring that you maintain your streak and practice regularly. The script runs Chrome in headless mode, and wait times have been optimized to work within the 1-minute limit for GitHub Actions in the free tier😅.

## How to Set It Up

### 1. Fork the Repository

Start by forking this repository to your GitHub account. This will create a copy of the project under your account, which you can easily configure and use.

1. Navigate to the top-right corner of this page and click on the "Fork" button.
2. Choose your account as the destination for the fork.

### 2. Set Up GitHub Secrets

You'll need to store your LeetCode credentials as secrets in your forked GitHub repository.

1. Go to your forked repository on GitHub.
2. Click on "Settings".
3. Navigate to "Secrets and variables" > "Actions".
4. Add the following secrets:
   - `LEETCODE_USERNAME`: Your LeetCode username.
   - `LEETCODE_PASSWORD`: Your LeetCode password.

### 2.1 Alternate Way (Not Recommended)

- If you want to avoid the hassle of setting up secrets, you can replace the credentials locally and make the repo <span style="color:red"> **private**</span>. However, this method is not recommended for security reasons.

```python
# Log in (replace 'username' and 'password' with your credentials)
username = "<username>"
password = "<password>"
```

### 3. Update the Cron Schedule

The script is currently scheduled to run daily at 9:00 PM IST (3:30 PM UTC). You can modify the cron schedule in the `.github/workflows/leetcode_submission.yml` file if needed.

### 4. Run the Workflow

Once everything is set up, the workflow will automatically run daily at the scheduled time. You can also trigger it manually from the GitHub Actions tab in your forked repository.

## Word of Caution

- **Security**: Ensure that your LeetCode credentials are securely stored in GitHub Secrets. Never hardcode your credentials in the code.
- **LeetCode Terms of Service**: Be aware of LeetCode's terms and conditions regarding automated submissions. Use this script responsibly.

## Personal Take

I don't support the use of these types of tools, but I understand it can be frustrating when you accidentally break a looong streak because you slept early accidently 😅. Use this responsibly and as a backup, not as a replacement for<span style="color:skyblue"> genuine problem-solving practice😎 </span>.

![alt text](image.png)