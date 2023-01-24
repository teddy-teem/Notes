# Windows Notes:
## Multiple SSH Key setup
> 1. Open window cmd/terminal.
> 2. Run `ssh-keygen`
> 3. Output will be like this `Enter file in which to save the key (C:\Users\user/.ssh/id_rsa): `
> 4. Copy location (given) `C:\Users\user/.ssh/id_rsa`
> 5. paste & press enter `Enter file in which to save the key (C:\Users\user/.ssh/id_rsa):C:\Users\user/.ssh/id_rsa`
> 6. Got to `C:\Users\user/.ssh/id_rsa` folder in your computer. 
> 7. Rename `id_rsa.pub` file as you want eg. `id_rsa_personal`, `id_rsa_work` in `C:\Users\user\.ssh`
> 8. repeat multiple time you want & rename it.
> 9. create a file name `config` with no type & write the code like following code in 'config' file.
>     ```
>     Host work
>   		HostName github.com
>   		User git
>   		IdentityFile ~/.ssh/id_rsa_myOrganization
>   
>	 Host personal 
>   		HostName github.com
>   		User git
>   		IdentityFile ~/.ssh/id_rsa_teddy
>     ```
>  10. save it in `C:\Users\user\.ssh`
>  11. use ssh url to clone, write clone command like these `git clone work:user/repo.git`
>  12. go inside the repo & cofigure git user email, git user name with proper hostname. 
>  13. You Done. 

## File name case-sensitive/incase-sensitive
> ***To make file name case-sensitive in a folder use the bellow's command in administrative mode.***
>  ```
>  fsutil.exe file SetCaseSensitiveInfo C:\folder\path enable
>  ```
> ***To make file name case-insensitive in a folder use the bellow's command in administrative mode.***
> ```
> fsutil.exe file SetCaseSensitiveInfo C:\folder\path disable
> ```
>
> ***N.B*** `C:\folder\path` is the file path in which folder you want make above operation
