* Drop this into you .gitconfig file at C:/Users/YOURNAME/.gitconfiig
* Save, restart your git console
* Enjoy!

```
[alias]
[alias]
	s = status
	f = reset head --hard
	cm = checkout master
	cd = checkout development
	ac = !git add . && git commit -am
	
	#pretty printing
	lm = log-magic
	log-magic = log -20 --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
	
	#list all branches
	super-b = branch --all --format='%(refname:short)'
	
	# list aliases
    la = "!git config -l | grep alias | cut -c 7-"
```

# Explanations

* s - status
* f - flush or 'fuck this', depending on your mood :)
* ct/cm - chekcout to the source branch
* lm/logmagic - pretty prints your log output