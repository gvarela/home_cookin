Install
=======
        ruby < <( curl https://github.com/gvarela/home_cookin/raw/master/install-homecookin )

Usage
=====
Run your default configuration (~/.cook)
        sudo cook

Run an ad hoc dna.json
        sudo cook node.json

Rerun cook without re-downloading cookbooks (usefull for debugging cookbooks)
        sudo cook node.json --rerun

.cook
======
The default configuration installs homebrew and git through homebrew. To add recipes add them to the recipe list.

e.g.

        {
          "cookbooks": ["https://github.com/gvarela/osx-cookbooks/tarball/master"]
          "recipes": ["homebrew", "git", "mysql", "imagemagick"]  
        }
