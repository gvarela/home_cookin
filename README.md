Install
=======
        bash < <( curl https://github.com/gvarela/home_cookin/raw/master/install-homecookin )

Usage
=====
Run your default configuration (~/.cook)

        sudo cook

Run an ad hoc dna.json

        sudo cook node.json

Rerun chef-solo without re-downloading cookbooks (usefull for debugging cookbooks)

        sudo cook node.json --rerun

Reset the home_cookin environment, which reinstalls chef and removes all cache directories

        sudo cook node.json --reset-env

Run chef-solo with verbose output (debug log level)

        sudo cook node.json --verbose

Help

        cook -h

.cook
======
The default configuration installs homebrew and git through homebrew. To add recipes add them to the recipe list.

e.g.

        {
          "cookbooks": ["https://github.com/gvarela/osx-cookbooks/tarball/master"]
          "recipes": ["homebrew", "git", "mysql", "imagemagick"]  
        }

To create a default developer image see this gist https://gist.github.com/720515

Thanks
=====
To Josh Peek for the osx-cookbooks and the original cook gist https://gist.github.com/655000
