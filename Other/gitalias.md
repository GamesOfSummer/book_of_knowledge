* Drop this into you .gitconfig file at C:/Users/YOURNAME/.gitconfiig
* Save, restart your git console
* Enjoy!

```
[alias]
	s = status
	f = reset head --hard
	cm = checkout master
	cd = checkout development
	lm = log-magic
	log-magic = log -20 --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
```

# Explanations

* s - status
* f - flush or 'fuck this', depending on your mood :)
* ct/cm - chekcout to the source branch
* lm/logmagic - pretty prints your log output