# Suggested setup when using AAP CLI

Example .vimrc file to make vi or vim "yaml ready"
```
set autoindent
set tabstop=2
set shiftwidth=2
autocmd FileType yaml setlocal ai ts=2 sw=2 et cursorcolumn
autocmd FileType yml setlocal ai ts=2 sw=2 et cursorcolumn

let &t_SI .= "\<Esc>[?2004h"
let &t_EI .= "\<Esc>[?2004l"

inoremap <special> <expr> <Esc>[200~ XTermPasteBegin()

function! XTermPasteBegin()
  set pastetoggle=<Esc>[201~
  set paste
  return ""
endfunction
```

Ansible short cuts for your BASH shell (.bashrc)
```
alias a=ansible
alias ad=ansible-doc
alias ag=ansible-galaxy
alias ai=ansible-inventory
alias al=ansible-lint
alias ap=ansible-playbook
alias an=ansible-navigator
alias ap=ansible-galaxy
alias av=ansible-vault
```
