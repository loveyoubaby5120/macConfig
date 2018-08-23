* TERMINAL
    * [HOMEBREW](#HOMEBREW)
    * [NPM](#NPM)
    * [VIM CONFIG](#VIMCONFIG)
    * [VIM KEYBOARD SHORTCUTS](#VIMKEYBOARDSHORTCUTS)

# <a name="HOMEBREW">HOMEBREW</a>

```bash
# 搜索引擎  elasticsearch
# https://www.elastic.co/products/elasticsearch
brew install elasticsearch

# 搜索引擎管理界面  kibana
# https://www.elastic.co/products/kibana
brew install kibana

# Logstash是一个开放源码的服务器端数据处理流水线，可同时从众多来源获取数据，并将其转换为您最喜爱的“收藏”（我们的自然是弹性搜索）。  logstash
# https://www.elastic.co/products/logstash
brew install logstash

# 文件夹跳转  j ***
# https://github.com/wting/autojump
brew install autojump

# VIM  vim *.*
brew install vim

# libsodium 是一种现代化，易于使用的软件库，用于加密，解密，签名，密码散列等
# https://download.libsodium.org/doc/libsodium_users/
brew install libsodium

# 文件搜索  fzf ***
# https://github.com/junegunn/fzf
brew install fzf

# 内容匹配  ag ***
# https://github.com/ggreer/the_silver_searcher
brew install the_silver_searcher

# 终端命令矫正 fuck
# https://github.com/nvbn/thefuck
brew install thefuck

# terminal 浏览器 w3m url
# http://w3m.sourceforge.net/
brew install w3m

# 文件夹结构显示 tree
# http://mama.indstate.edu/users/ice/tree/
brew install tree

# 文件传输工具 wormhole send || wormhole receive
# https://github.com/warner/magic-wormhole
brew install magic-wormhole

# 监视文件和记录，或者在更改时触发操作 watchman watch ***
brew install watchman

# 抓包工具 mitmproxy -b 192.168.1.107 -p 8888
# https://mitmproxy.org/
brew install mitmproxy

# 终端执行命令监控 gosuv start-server
# https://github.com/codeskyblue/gosuv
brew install gosuv

# javascript 静态类型检查器
# https://flow.org/en/docs/getting-started/
brew install flow

# shadowsocks 转换 http/https polipo socksParentProxy=localhost:1080
# https://www.irif.fr/~jch/software/polipo/
brew install polipo

# json 查询工具
# https://github.com/stedolan/jq
brew install jq

# 快捷键提示工具
# https://www.cheatsheetapp.com/CheatSheet/
brew cask install cheatsheet

# Mac PrefPane来管理您所有的Homebrew安装的服务
# https://github.com/jimbojsb/launchrocket
brew cask install launchrocket

# 跟踪程序使用情况
# https://www.mediaatelier.com/Usage/
brew cask install usage

# 分屏工具
# https://www.irradiatedsoftware.com/sizeup/
brew cask install sizeup

```

# <a name="NPM">NPM</a>

```bash
# 活动监视器 vtop
# https://github.com/MrRio/vtop
npm install -g vtop

# 可视化依赖关系图 dependency-cruiser
# https://github.com/sverweij/dependency-cruiser
npm install dependency-cruiser

```

# <a name="VIMCONFIG">VIMCONFIG</a>
```bash
set nocompatible              " be iMproved, required
filetype off                  " required

set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

Plugin 'gmarik/Vundle.vim'

" plugins
Plugin 'scrooloose/nerdtree'
Plugin 'vim-airline/vim-airline'
Plugin 'vim-airline/vim-airline-themes'
Plugin 'vim-scripts/taglist.vim'
Plugin 'majutsushi/tagbar'
Plugin 'godlygeek/tabular'
Plugin 'Shougo/neocomplete.vim'
Plugin 'kien/ctrlp.vim'
Plugin 'terryma/vim-multiple-cursors'
Plugin 'jiangmiao/auto-pairs'
Plugin 'tomasr/molokai'
Plugin 'tpope/vim-fugitive'
Plugin 'scrooloose/syntastic'
Plugin 'fatih/vim-go'
Plugin 'rizzatti/dash.vim'
"Plugin 'wakatime/vim-wakatime'
" Plugin 'tpope/vim-commentary'
Plugin 'Yggdroot/indentLine'
" Plugin 'mattn/emmet-vim'
" Plugin 'jQuery'
Plugin 'plasticboy/vim-markdown'
Plugin 'suan/vim-instant-markdown'
Plugin 'kien/rainbow_parentheses.vim'
" Plugin 'nathanaelkane/vim-indent-guides'
Plugin 'mhinz/vim-signify'
Plugin 'elzr/vim-json'
Plugin 'zaiste/tmux.vim'
Plugin 'rking/ag.vim'
Plugin 'sjl/gundo.vim'
Plugin 'dag/vim-fish'

call vundle#end()            " required
filetype plugin indent on    " required

" settings
syntax enable " 语法开启
syntax on
let mapleader=',' " comma as <leader>
" jk is escape
inoremap jk <esc>
let g:molokai_original = 1
let g:rehash256 = 1
set t_Co=256
colorscheme molokai
set background=dark
" set termguicolors " 支持真彩色
highlight Normal ctermfg=252 ctermbg=none
set termencoding=utf-8
set encoding=utf8
set fileencodings=utf8,ucs-bom,gbk,cp936,gb2312,gb18030
set cul
set laststatus=2
set statusline+=%{fugitive#statusline()}
set number     " 显示行号
set noshowmode " 左下角的状态栏不显示--INSERT--之类的信息
set tabstop=4 " number of visual spaces per TAB
set shiftwidth=4
set softtabstop=4 " number of spaces in tab when editing
set expandtab " tabs are spaces
set smarttab
set autoindent " 自动缩进
set smartindent
set ruler " 右下角显示状态栏
set ignorecase "搜索时忽略大小写
set smartcase
set hls
set foldmethod=indent
" set foldlevel=99
set showcmd " show command in bottom bar
set splitright
set splitbelow
set hidden
set nocursorline
set nocursorcolumn


" backup
set nobackup
set nowb
set noswapfile

" search
set hlsearch " 高亮搜索
set incsearch " search as characters are entered
" turn off search highlight
nnoremap <leader><space> :nohlsearch<CR> 

" backspace
set backspace=eol,start,indent "退格键删除字符
set whichwrap+=<,>,h,l
set nowrap

" autocmd InsertLeave * se nocul " 用浅色高亮当前行
" autocmd InsertEnter * se cul"

set confirm
"set guifont=Droid\ Sans\ Mono\ for\ Powerline:h16 " 设置GUI的VIM的字体为Droid Sans Mono for Powerline和大小为16"

set wildmenu " visual autocomplete for command menu
set showmatch " highlight matching [{()}]

" move
" nnoremap j gj
" nnoremap k gk
nnoremap B ^
nnoremap E $
nnoremap <leader>w :w<CR>
nnoremap <Leader>q :q<CR>


" nerdtree settings
" autocmd vimenter * NERDTree
autocmd StdinReadPre * let s:std_in=1
autocmd VimEnter * if argc() == 0 && !exists("s:std_in") | NERDTree | endif
map <silent> <F2> :NERDTreeToggle<CR>
autocmd bufenter * if (winnr("$") == 1 && exists("b:NERDTreeType") && b:NERDTreeType == "primary") | q | endif

" airline settings
let g:airline_powerline_fonts = 1
let g:airline_theme='powerlineish'
let g:Powerline_symbols = 'fancy'
let Powerline_symbols = 'compatible'
let g:airline#extensions#tabline#enabled = 1
let g:airline#extensions#tabline#left_sep = ' '
let g:airline#extensions#tabline#left_alt_sep = '>'
let g:airline#extensions#tabline#buffer_nr_show = 1
" let g:airline#extensions#tabline#show_buffers = 1
" let g:airline#extensions#tabline#show_tab_nr = 1
" let g:airline#extension#tabline#show_tab_type = 1
let g:airline#extensions#whitespace#enabled = 0
let g:airline#extensions#whitespace#symbol = '|'
nnoremap <F1> :bn<CR>
nnoremap <F3> :bp<CR>
" :bd " close the buffer(what I think of a tab)
" let g:airline_section_b = '%{getcwd()}'
let g:airline_section_b = '%{fugitive#statusline()}'
" let g:airline_section_c = '%{fugitive#statusline()}'
let g:airline_section_c = '%{strftime("%T")}'
" let g:airline_section_gutter = airline#section#create(['BN: %{bufnr("%")}','%='])
" let g:airline_section_c = '%<%f%m %#__accent_red#%{airline#util#wrap(airline#parts#readonly(),0)}%#__restore__#'
" let g:airline_section_c = airline#section#create_right(['%f'])
" let g:airline_section_x = airline#section#create_right(['branch', 'ffenc'])
" let g:airline_section_y = '%Y'
let g:airline#extensions#branch#enabled = 1
let g:airline#extensions#hunks#enabled = 0
let g:airline#extensions#branch#empty_message = ''
let g:airline#extensions#branch#vcs_priority = ["git", "mercurial"]
if !exists('g:airline_symbols')
      let g:airline_symbols = {}
  endif
let g:airline_symbols.space = "\ua0"
function! s:tagbar_integration()
    " statusline tells you what function you are in!
endfunction


" ctags settings
let Tlist_Ctags_Cmd ='/usr/local/Cellar/ctags/5.8_1/bin/ctags'  "这里比较重要了，设置ctags的位置，不是指向MacOS自带的那个，而是我们用homebrew安装的那个，Centos下配置注销这行即可。

" taglist settings
let Tlist_Use_Right_Window = 1        " 让taglist窗口出现在Vim的右边
let Tlist_File_Fold_Auto_Close = 1    " 当同时显示多个文件中的tag时，设置为1，可使taglist只显示当前文件tag，其它文件的tag都被折叠起来。
let Tlist_Show_One_File = 1           " 只显示一个文件中的tag，默认为显示多个
let Tlist_Sort_Type ='name'           " Tag的排序规则，以名字排序。默认是以在文件中出现的顺序排序
let Tlist_GainFocus_On_ToggleOpen = 1 " Taglist窗口打开时，立刻切换为有焦点状态
let Tlist_Exit_OnlyWindow = 1         " 如果taglist窗口是最后一个窗口，则退出vim
let Tlist_WinWidth = 32               " 设置窗体宽度为32，可以根据自己喜好设置
map <silent> <F9> :TlistToggle <CR>

" tagbar settings
nmap <F8> :TagbarToggle<CR>
let g:tagbar_autofocus=1
let g:tagbar_width = 32 " 设置窗口宽度。默认为40
let g:tagbar_left = 1
let g:tagbar_show_linenumbers = 1
let g:tagbar_type_go = {
    \ 'ctagstype' : 'go',
    \ 'kinds'     : [
        \ 'p:package',
        \ 'i:imports:1',
        \ 'c:constants',
        \ 'v:variables',
        \ 't:types',
        \ 'n:interfaces',
        \ 'w:fields',
        \ 'e:embedded',
        \ 'm:methods',
        \ 'r:constructor',
        \ 'f:functions'
    \ ],
    \ 'sro' : '.',
    \ 'kind2scope' : {
        \ 't' : 'ctype',
        \ 'n' : 'ntype'
    \ },
    \ 'scope2kind' : {
        \ 'ctype' : 't',
        \ 'ntype' : 'n'
    \ },
    \ 'ctagsbin'  : 'gotags',
    \ 'ctagsargs' : '-sort -silent'
\ }

" Dash settings
nmap <F5> :Dash<CR>
" nmap <silent> <F5> <Plug>DashSearch


autocmd FileType css setlocal omnifunc=csscomplete#CompleteCSS
" autocmd FileType html,markdown setlocal omnifunc=htmlcomplete#CompleteTags
autocmd FileType python setlocal omnifunc=pythoncomplete#Complete
autocmd FileType xml setlocal omnifunc=xmlcomplete#CompleteTags

" ctrlp settings
if executable('ag')
    " use ag over grep
    set grepprg=ag\ --nogroup\ --nocolor\ --ignore-case\ --column
    set grepformat=%f:%l:%c:%m,%f:%l:%m
    " use ag in ctrlp for listing files
    let g:ctrlp_user_command = 'ag %s -l --nocolor -g ""'
    " ag is fast enough that ctrlp doesn't need to cache
    let g:ctrlp_use_caching = 0
endif
let g:ctrlp_map = '<c-p>'
let g:ctrlp_cmd = 'CtrlP'

let g:ctrlp_working_path_mode = 'ra'
set wildignore+=*/tmp/*,*.so,*.swp,*.zip     " Linux/MacOSX
" let g:ctrlp_user_command = 'find %s -type f'        " MacOSX/Linux


" syntastic settings
set statusline+=%#warningmsg#
set statusline+=%{SyntasticStatuslineFlag()}
set statusline+=%*

let g:syntastic_always_populate_loc_list = 1
let g:syntastic_auto_loc_list = 1
let g:syntastic_check_on_open = 0 " 是否在打开文件时检查
let g:syntastic_check_on_wq = 1 " 是否在保存文件后检查

" vim-go settings 
let g:go_highlight_functions = 1
let g:go_highlight_methods   = 1
let g:go_highlight_fields    = 1
let g:go_highlight_types     = 1
let g:go_highlight_operators = 1
let g:go_highlight_build_constraints = 1
let g:go_highlight_extra_types = 1
let g:go_highlight_generate_tags = 1

let g:go_fmt_command = "goimports"
let g:go_autodetect_gopath = 1
" let g:syntastic_go_checkers = ['golint', 'govet', 'errcheck', 'gofmt']
"let g:syntastic_mode_map = {'mode': 'active', 'passive_filetypes': ['go']}
let g:syntastic_go_checkers = ['govet', 'errcheck', 'go']
let g:go_list_type = "quickfix"

" open :GoDeclsDir with ctrl-d
nmap <C-d> :GoDeclsDir<cr>
imap <C-d> <esc>:<C-u>GoDeclsDir<cr>

" neocomplete settings 
" Disable AutoComplPop.
 let g:acp_enableAtStartup = 0
 " Use neocomplete.
 let g:neocomplete#enable_at_startup = 1
 " Use smartcase.
 let g:neocomplete#enable_smart_case = 1
 " Set minimum syntax keyword length.
 let g:neocomplete#sources#syntax#min_keyword_length = 3

 " Plugin key-mappings.
 inoremap <expr><C-g>     neocomplete#undo_completion()
 inoremap <expr><C-l>     neocomplete#complete_common_string()

 " Recommended key-mappings.
 " <CR>: close popup and save indent.
 inoremap <silent> <CR> <C-r>=<SID>my_cr_function()<CR>
 function! s:my_cr_function()
     return neocomplete#close_popup() . "\<CR>"
 endfunction
 " <TAB>: completion.
 inoremap <expr><TAB>  pumvisible() ? "\<C-n>" : "\<TAB>"
 " <C-h>, <BS>: close popup and delete backword char.
 inoremap <expr><C-h> neocomplete#smart_close_popup()."\<C-h>"
 inoremap <expr><BS> neocomplete#smart_close_popup()."\<C-h>"
 inoremap <expr><C-y>  neocomplete#close_popup()
 inoremap <expr><C-e>  neocomplete#cancel_popup()

 " Go related mappings
 au FileType go nmap <Leader>i <Plug>(go-info)
 au FileType go nmap <Leader>gd <Plug>(go-doc)
 au FileType go nmap <Leader>r <Plug>(go-run)
 au FileType go nmap <Leader>b <Plug>(go-build)
 au FileType go nmap <Leader>t <Plug>(go-test)
 au FileType go nmap gd <Plug>(go-def-tab)

" vim-markdown settings
au BufRead, BufNewFile *.{md, markdown, mkd} set filetype=markdown
let g:vim_markdown_folding_disabled = 1
let g:vim_markdown_math = 1
let g:vim_markdown_new_list_item_indent = 4
let g:vim_markdown_conceal = 0
let g:vim_markdown_frontmatter = 1
let g:vim_markdown_json_frontmatter = 1
" vim-instant-markdown settings
let g:instant_markdown_autostart = 0
let g:markdown_fenced_languages = ['html', 'python', 'javascript', 'vim', 'sh']
set shell=/bin/bash

" rainbow settings
let g:rbpt_colorpairs = [
    \ ['brown',       'RoyalBlue3'],
    \ ['Darkblue',    'SeaGreen3'],
    \ ['darkgray',    'DarkOrchid3'],
    \ ['darkgreen',   'firebrick3'],
    \ ['darkcyan',    'RoyalBlue3'],
    \ ['darkred',     'SeaGreen3'],
    \ ['darkmagenta', 'DarkOrchid3'],
    \ ['brown',       'firebrick3'],
    \ ['gray',        'RoyalBlue3'],
    \ ['black',       'SeaGreen3'],
    \ ['darkmagenta', 'DarkOrchid3'],
    \ ['Darkblue',    'firebrick3'],
    \ ['darkgreen',   'RoyalBlue3'],
    \ ['darkcyan',    'SeaGreen3'],
    \ ['darkred',     'DarkOrchid3'],
    \ ['red',         'firebrick3'],
    \ ]
let g:rbpt_max = 16
" always on
au VimEnter * RainbowParenthesesToggle
au syntax * RainbowParenthesesLoadRound
au syntax * RainbowParenthesesLoadSquare
au syntax * RainbowParenthesesLoadBraces

" indentLine settings
set list lcs=tab:\|\ " 这里有个空格

" vim-signify settings
let g:signify_vcs_list = ['git', 'hg']
nmap <leader>sn <plug>(signify-next-hunk)
nmap <leader>sp <plug>(signify-prev-hunk)
highlight DiffAdd           cterm=bold ctermbg=none ctermfg=119
highlight DiffDelete        cterm=bold ctermbg=none ctermfg=167
highlight DiffChange        cterm=bold ctermbg=none ctermfg=227
highlight SignifySignAdd    cterm=bold ctermbg=237  ctermfg=119
highlight SignifySignDelete cterm=bold ctermbg=237  ctermfg=167
highlight SignifySignChange cterm=bold ctermbg=237  ctermfg=227

" ag.vim settings
" 在搜索代码时不默认直接打开搜索的第一个结果
" nmap <c-t> :Ag! ""<left>.Ag! 
nnoremap <leader>a :Ag!<SPACE>

" gundo.vim settings
nnoremap <leader>u :GundoToggle<CR>

" multiple-cursors settings
" default mapping
" let g:multiple_cursor_use_default_mapping=1
" let g:multiple_cursor_next_key='<C-n>'
" let g:multiple_cursor_prev_key='<C-p>'
" let g:multiple_cursor_skip_key='<C-x>'
" let g:multiple_cursor_quit_key='<Esc>'

" vim-fish settings

" vim-json settings
nmap <leader>jt :%!python -m json.tool<CR>

```

# <a name="VIMKEYBOARDSHORTCUTS">VIM KEYBOARD SHORTCUTS</a>
```bash
    z + R   (依次按无需同时按) 
```
