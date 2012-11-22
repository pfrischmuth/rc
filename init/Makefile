
default:
	@echo "You can choose, which configs you want to populate"
	@echo "(zsh, vim) !!!Your old config will be deleted!!!"

all: zsh vim ssh
	cd ../rc && make -B all

zsh:
	rm -rf ~/.config/zsh ~/.zshrc
	git clone git://github.com/seebi/zshrc.git ~/.config/zsh
	cd ~/.config/zsh && make -B install

vim:
	rm -rf ~/.vimrc ~/.vim
	git clone git://github.com/seebi/vimrc.git ~/.vim
	cd ~/.vim && git config submodule.bundle/semweb.url "git://github.com/seebi/semweb.vim.git"
	cd ~/.vim && git config submodule.bundle/easychair.url "git://github.com/seebi/easychair.vim.git"
	cd ~/.vim && git submodule init
	cd ~/.vim && git submodule update
	ln -s ~/.vim/vimrc ~/.vimrc
	touch ~/.vim/vimrc.private

ssh:
	mkdir -p ~/.ssh/
	rm -rf ~/.ssh/authorized_keys
	echo "ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAwFqCgkEIJFxeXVCOJzmsx5Hx21KE5JLy7J42B8YG5aoDflg143jqnwCHgj2zPgT3RcRvlvWvd5mir2DnHEhm78fiHR9RIdEAPTDPy8JN3vfd86eu7wld/ZSIviZ8kqP5XKC2hrgLsEd1WtRuK+FEUas/k0vsymdaqnURrNrAacYRy+cepvYhKdCpMMzKQr25uMhsmX6lsDo6MjBAo6U9TdBMHNWurlIDC7hMVVQ2B/GIeTmWU4NkXK5mTtANSM7BzSSJGA3orqHIfnLbJT151QBAruMTZdb3JP7XmZbWlBUEIE3wODe852lQqSg2FkCj0SFG2UO4RjcrmmlBlTo8EQ==" >~/.ssh/authorized_keys
	echo "ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEA0gVJGZHgVsTD6x7CnTKdJr1VM1JHYFxkaMds6qIjyB6qO/hgIutTaN5JSyU4J+t9GKD8MvYC1FTijziNJcymBGkc5RGCZMnqr0Fz9i75Ke6rWwLaTX9yhIIGCQXSdJvCDhPhc7da5BmMI03ktb5V1bD+fLrvbX12zUq8JV+uIKttkbuG5t+fvy0ZkkL1N/132ty9SdeFAb69EV8Fz+K0maQt418Cl34hw/KgOMf09vMTt898rOV/u7gxU1dbG6eJvGKj8syLlKUYVaP588ODr1kTDgaU0mGDtUxTBsUcdFhEZo76bICQBTEM2Q+JYY4PzAC5uo5lvLIYaSM9pm8L0Q==" >~/.ssh/authorized_keys



