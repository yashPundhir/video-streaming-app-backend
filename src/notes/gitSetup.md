## this entire process is useful when u have been using git and github on some other system nd due to some reasons, u have to use git and github on some other system but for the same github account.

- So, i was using git on my acer laptop and bcz of that i have set up local git username nd email on my acer laptop and i have created a personal github account which i use to push my local projects to that remote github account.

- I have another HP laptop for job related work and thus it uses some other local git username nd email into that system and job related github account to push my local project into that remote github account.

- Now, due to some reasons, I have to use my HP laptop to perform some work which i otherwise would be doing using my acer laptop. i.e. i have a personal project which i need to push to my personal github account using the HP laptop. But the problem is that I was not able to push the code to my remote personal GIthub Repo from my HP laptop.

- So, to solve this issue, the following things needs to be done:

  - in my HP laptop, reset the global username and email using the following code:

  ```bash
    git config --global user.name "newUserName"
    git config --global user.email "newUserEmailId@domain.com"
  ```

  - The next step is to either create a new Personal Access Token from the personal github account or use the existing Personal Access Token from the personal github account.

  - Then run the following code in the git bash terminal before running the command to push the code.

  ```bash
    git remote set-url origin https://<token>@github.com/<username>/<repo>

    For Exmaple: git remote set-url origin https://ghp_supersecrettoken@github.com/GitHubUser/AwesomeRepo
  ```

  - Then run the command to push the code:

  ```bash
    git push -u origin main
  ```
