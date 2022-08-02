# termux-bashit
Style your Termux without changing your shell. OH-MY-ZSH alternative.

# Requirements
1. *Termux App* from Fdroid
2. *Termux Styling* from Fdroid

<image src="images/Imagepipe_49.jpg" alt="termux-bashit">

**Note-01:** From Froid because App on Play Store does not get any Latest Updates.

**Note-02:** This is a guide how to use [bash-it](https://github.com/Bash-it/bash-it) framework to make your termux look good and easy to use.

# Steps

1. Basic Styling using Termux Style addon:
  - Change Color : Nancy
    **Steps:** 
    1. Long Press anywhere on Termux
    2. Select `more`
    3. Then `style`
    4. Finally `choose color`
   
  - Change Font : VictorMono
    **Steps:** 
    1. Long Press anywhere on Termux
    2. Select `more`
    3. Then `style`
    4. Finally `choose font`

<image src="images/Imagepipe_54.jpg" alt="termux-bashit">

2. Clone and Install Bash-it framework
```bash
git clone --depth=1 https://github.com/Bash-it/bash-it.git ~/.bash_it
~/.bash_it/install.sh
```

3. Change Theme to agnoster as in the image in line 14

```bash
source ~/.bashrc
nano -l .bashrc
```

<image src="images/Imagepipe_50.jpg" alt="termux-bashit">

4. Append LOGNAME variable into theme file.
  - You can find theme files under `~/.bash_it/themes/` directory
  - I had used `anything` as my LOGNAME in the sample picture above. 
  - You can use anything as a logname by replacing `$anything` in below code.
  ```bash
  echo LOGNAME=$anything >> ~/.bash_it/themes/agnoster/agnoster.theme.bash
  ```
  - If you want to use your real LOGNAME which you can find using command `logname`. Use this following code instead.
  ```bash
  echo LOGNAME=$(LOGNAME) >> ~/.bash_it/themes/agnoster/agnoster.theme.bash
  ```
 
5. Enable the Theme

```bash
source ~/.bashrc
exec bash
```

**That's it you can play with bash-it.**