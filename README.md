# personal config files for freeBSD

Change "quaterly" to "latest" in line 11:

    mkdir -p /usr/local/etc/pkg/repos
    cp /etc/pkg/FreeBSD.conf /usr/local/etc/pkg/repos/FreeBSD.conf
    vi /usr/local/etc/pkg/repos/FreeBSD.conf

Update system and etc.:

    freebsd-update fetch install
    portsnap fetch extract
    pkg update
    
Install packages:

    pkg install sudo zsh vim git xorg firefox
    
    git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim 
    
Set zsh to default:
    
    chsh -s $(which zsh)

xorg dpi setting:
- in ~/.Xresources:
    
        Xft.dpi: 192

    



Firefox settings (if srcolling not smooth):

    in: about:config
  
    set: layers.acceleration.force-enabled true
