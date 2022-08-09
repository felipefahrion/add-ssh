# Add SSH

```
ssh-keygen -t ed25519 -C "<your_email@any.com>"

```

```
eval "$(ssh-agent -s)"
```

```
open ~/.ssh/config
```

Add into config file:
```
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519
```

```
ssh-add -K ~/.ssh/id_ed25519
```


```
pbcopy < ~/.ssh/id_ed25519.pub
```

Follow this link to add into Github page: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

