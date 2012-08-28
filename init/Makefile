
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


