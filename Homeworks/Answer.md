### Group 3 #####


## Homework 1

	- `dpkg -l`							-> rpm -qa	
	- `dpkg -l {package_name}`					-> rpm -qa {package_name}
	- `dpkg -L {package_name}`					-> rpm -ql {package_name}
	- `dpkg -i {package_name}`					-> rpm -i {package_name}
	- `dpkg -r {package_name}`					-> rpm --erase
	- `dpkg -P {package_name}`					-> rpm --erase
	- `dpkg -c {package_name}`					-> rpm -qc {package_name}
	- `dpkg -S {/path/to/file}`					...
	- `dpkg -p {package_name}`					...
	- `dpkg -s {package_name}`					...
	- `dpkg --get-selections`					....


    - `apt policy`						....
    - `add-apt repository {repository_name}`		....
    - `apt list`						-> yum list
    - `apt install {package_name}`				-> yum install {package_name}
    - `apt search {package_name}`				-> yum search {package_name}
    - `apt update`						-> yum check-update
    - `apt upgrade`						-> yum upgrade
    - `apt remove {package_name}`				....
    - `apt purge {package_name}`				....
    - `apt autoremove`					-> yum remove






## Homework 2

	Step1: install alien
	Step2: sudo apt install alien
	Step3: sudo alien bless-0.6.0-1.mga2.x86_64.rpm
	Step4: sudo dpkg -i bless_0.6.0-2_amd64.deb

## Homework 3

```
alias abcdef='ls -lht | head -6'
```

## Homework 4

```
PS1='{$(abc)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
abc(){
    lsb_release -c | awk -F " " '{print $2}'
}
	
```

## Homework 5


```
_qwer() {
	kill $(pgrep -l $1 | awk -F " " '{print $1}')
}

alias kill_all="_qwers"

```

## Homework 6

```
_pull() {
	git pull origin $(git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ \1/')
}
alias gplo="_pull"
```
