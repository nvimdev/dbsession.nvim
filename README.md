# dbsession.nvim

A simple small and powerful session plugin for neovim

# Install

- Lazy.nvim

```lua
require('lazy').setup({
    {'glepnir/dbsession.nvim', cmd = { 'SessionSave', 'SessionDelete', 'SessionLoad'},
      opts = { --config --}
    }
})
```

- packer.nvim

```lua
use({'glepnir/dbsession.nvim', cmd = { 'SessionSave', 'SessionDelete', 'SessionLoad'},
    config = function() require('dbsession').setup({}) end
})
```

# Options

- `dir` the session store dir default is `stdpath(cache)/nvim/session`
- `auto_save_on_exit` auto save session when quit neovim

# Commands

- `SessionSave name?` you can set a special name for session if not set will use default name it
  generate according cwd and time

- `SessionLoad |TAB` load a session by select from complete list

- `SessionDelete |TAB` delete a session

# LICENSE MIT
