set nocompatible              " be iMproved, required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required
Plugin 'VundleVim/Vundle.vim'
Plugin 'majutsushi/tagbar'
Plugin 'chriskempson/base16-vim'
Plugin 'https://github.com/nanotech/jellybeans.vim'
Plugin 'morhetz/gruvbox'
Plugin 'https://github.com/sickill/vim-monokai'
Plugin 'https://github.com/python-mode/python-mode'
Plugin 'https://github.com/davidhalter/jedi-vim'
Plugin 'jnurmine/Zenburn'
Plugin 'https://github.com/ajh17/Spacegray.vim'
Plugin 'https://github.com/ctrlpvim/ctrlp.vim'

" All of your Plugins must be added before the following line
call vundle#end()            " required
filetype plugin indent on    " required
" To ignore plugin indent changes, instead use:
"filetype plugin on
"
" Brief help
" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
"
" see :h vundle for more details or wiki for FAQ
" Put your non-Plugin stuff after this line

syntax on
set exrc
set secure
set history=700
set autoread

"pathogen

execute pathogen#infect() 
call pathogen#helptags()

"nastaveni klavesy <leader>
let mapleader=","


"set backspace=2
set nojoinspaces
set ruler
set mouse=a

set showcmd
set showmode
set showmatch
set mat=2

set so=7
set wildmenu
set ruler
set cmdheight=2
set hid

set backspace=eol,start,indent
set whichwrap+=<,>,h,l

set ignorecase
set smartcase
set hlsearch
set incsearch
"nnoremap <esc> :noh<return><esc>

"zde se odstranuji zvuky pri chybach7

set encoding=utf8
set ffs=unix,dos,mac

set nobackup
set nowb
set noswapfile

set smarttab
set expandtab
set shiftwidth=4
set tabstop=4

set lbr
set tw=800

set ai "Auto indent
set si "Smart indent
set wrap "Wrap lines

vnoremap <silent> * :call VisualSelection('f')<CR>
vnoremap <silent> # :call VisualSelection('f')<CR>

"noremap j gj 
noremap k gk

noremap <space> /
noremap <c-space> ?

"nnoremap <C-j> <C-W>j
"nnoremap <C-k> <C-W>k
"nnoremap <C-h> <C-W>h
"nnoremap <C-l> <C-W>l

map <leader>bd :Bclose<cr>

map <leader>ba :1,1000 bd!<cr>

map <leader>tn :tabnew<cr>
map <leader>to :tabonly<cr>
map <leader>tc :tabclose<cr>
map <leader>tm :tabmove

map <leader>te :tabedit <c-r>=expand("%:p:h")<cr>/
map <leader>cd :cd %:p:h<cr>:pwd<cr>

try
    set switchbuf=useopen,usetab,newtab
    set stal=2
catch
endtry

autocmd BufReadPost *
     \ if line("'\"") > 0 && line("'\"") <= line("$") |
     \   exe "normal! g`\"" |
     \ endif     
" Remember info about open buffers on close
set viminfo^=%

" Always show the status line
set laststatus=2
" Format the status line

vmap ,c "+y
imap ,p <esc>"+pa
nmap ,p "+p

"nastavení minimální výšky aktuálního okna 
:set winheight=15

"latex-suite
set grepprg=grep\ -nH\ $*

let g:tex_flavor='latex'
let g:Tex_ViewRule_pdf='okular'
let g:Imap_PlaceHolderStart='<+'
let g:Imap_PlaceHolderEnd='+>'
let g:Tex_DefaultTargetFormat = 'pdf'
let g:Tex_MultipleCompileFormats='pdf, aux'
"xelatex, kdyztak zakomentovat
let g:Tex_CompileRule_pdf = 'xelatex -aux-directory=F:/Vim/my_latex_doc/temp --synctex=-1 -src-specials -interaction=nonstopmode $*'
let g:Tex_BibtexFlavor = 'biber'
inoremap ,e é

nmap ,r :w<cr><leader>ll
nmap ,v <leader>lv

imap ,r <esc>:w<cr><leader>ll
imap ,v <esc><leader>lv

"cislovani
set nu

function! NumberToggle() 
  if(&relativenumber == 1)
	set nornu
  else
	set rnu
  endif
endfunc

nnoremap <C-n> :call NumberToggle()<cr>


au FocusLost * :set nornu
au FocusGained * :set rnu

autocmd InsertEnter * :set nornu
autocmd InsertLeave * :set rnu

"nerdtree
"map ,f :NERDTreeFind<CR>
map <C-k> :NERDTreeToggle %<CR>

"ctrp
"set runtimepath^=~/.vim/bundle/ctrlp.vim

"mapping na přecházení mezi chybami
"nnoremap ,ln :lne<cr>
"nnoremap ,lp :lp<cr>
"inoremap ,ln <esc>:lne<cr>i
"inoremap ,lp <esc>:lp<cr>i

"https://github.com/colbycheeze/dotfiles/blob/master/vimrc
"zmena velikosti aktualniho okna (pri split atd.)
nnoremap <silent> <Right> :vertical resize +5<cr>
nnoremap <silent> <Left> :vertical resize -5<cr>
nnoremap <silent> <Up> :resize +5<cr>
nnoremap <silent> <Down> :resize -5<cr>
""Use tab to jump between blocks, because it's easier
"nnoremap <tab> %
"vnoremap <tab> %
" Always use vertical diffs
set diffopt+=vertical
inoremap jj <Esc>
"vnoremap jj <Esc> "nelze se pohybovat dolu

" give us 256 color schemes!
"set term=screen-256color
"set t_Co=256

colorscheme gruvbox
set background=dark
"set background=light
"colorscheme zenburn
"rusi pozadi daneho colorscheme
highlight Normal ctermbg=NONE
highlight nonText ctermbg=NONE

set spell spelllang=cs,en
highlight clear SpellBad
highlight SpellBad term=standout ctermfg=1 term=underline cterm=underline
highlight clear SpellCap
highlight SpellCap term=underline cterm=underline
highlight clear SpellRare
highlight SpellRare term=underline cterm=underline
highlight clear SpellLocal
highlight SpellLocal term=underline cterm=underline

"ukládání fold
augroup remember_folds
  autocmd!
  autocmd BufWinLeave *.* mkview
  autocmd BufWinEnter *.* loadview
augroup END

nnoremap ,cd :cd %:p:h<CR>:pwd<CR>

"nastaveni splitu dolu a napravo
set splitbelow
set splitright

"tagbar
nmap <F8> :TagbarToggle<CR>

set shell=/bin/bash

"notetaking
let g:notes_directories = ['~/Documents/Notes', '~/Dropbox/Notes']
let g:notes_suffix = '.txt'
let g:notes_word_boundaries = 1
"let g:notes_smart_quotes = 0 "chytre nahrazovani v insert modu
let g:notes_tab_indents = 0

"changing cursor in insert mode (in urxvt)
let &t_SI = "\<Esc>[6 q"
let &t_SR = "\<Esc>[4 q"
let &t_EI = "\<Esc>[2 q"

"nastaveni slovniku (podle filetype); NEFUNGUJE
"au FileType * execute 'setlocal dict+=~/.vim/dictionaries/'.&filetype.'.txt'

"slovniky jednoduseji
set dict+=~/.vim/dictionaries/py.txt

"pymode
let g:pymode_rope = 0

"folding
"set foldmethod=syntax   
"set foldmethod=indent
set foldmethod=manual
"set foldnestmax=10
"set nofoldenable
"set foldlevel=2

"conflict between pymode a nd jedi-vim
" Load rope plugin
let g:pymode_rope = 0
let g:jedi#show_call_signatures = 0

" R Markdown
autocmd Filetype rmd map <F5> :!echo<space>"require(rmarkdown);<space>render('<c-r>%')"<space>\|<space>R<space>--vanilla<enter>
