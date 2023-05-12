# Sample of git config file 
- Example: .gitconfig 
- Place them in $XDG_CONFIG_HOME/git

## ~/.gitconfig
```
[user]
	name     = Estefanio N Santos
	email    = estefanions@gmail.com
	username = estefanionsantos
[core]
	editor = vim
```

# Multiple gitconfig settings on same OS user
you can create several gitconfig (.gitconfig-n1, .gitconfig-n2, etc...)
for several different accounts and here in the example we will create for only two

## ~/.gitconfig-n1
```
[user]
	name  = Lorem Santos
	email = lorem.santos-n1@example.com
```

## ~/.gitconfig-n2
```
[user]
	name  = Lorem Santos
	email = lorem.santos-n2@example.com
```

## Including settings in global ~/.gitconfig

```
[includeIf "gitdir:/directory/path/company-n1/"]
  path = ~/.gitconfig-n1
[includeIf "gitdir:/directory/path/company-n2/"]
  path = ~/.gitconfig-n2
```

