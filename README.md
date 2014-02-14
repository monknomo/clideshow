clide
=====

Clideshow is a command line slideshow.  The name is a combination of cli (command line interface) and slideshows.
Clideshow allows you create a text slide deck, and display 'slides' sequentially on the command line whenever you type
'slide'.

Installation
------------
Clone this repository.  $HOME/.clideshow is a good location for the scripts to live
```
git clone git://github.com/monknomo/clideshow.git $HOME/.clideshow
```
Assuming you installed the scripts to the above path, make them executable and add them to your path
```
sudo chmod a+x $HOME/.clideshow/clideshow
sudo chmoe a+x $HOME/.clideshow/slide
echo 'export PATH="$HOME/.clideshow:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
Non-Ubuntu users may wish to change .bashrc to .bash_profile

Type 'clideshow -h' for this list of commands:
```
slideshow - Create and edit command line slideshows

positional arguments:
  dst                   The filesystem location of a slideshow

optional arguments:
  -h, --help            show this help message and exit
  --switch              Sets the slideshow dst to the current slideshow
  --start-at INDEX      Sets the starting slide using 0 based indexing
                        therefore the first slide is at position 0. Changes
                        dst slideshow, defaults to current
  --new-slide [NEW_SLIDE [NEW_SLIDE ...]]
                        Adds N new slides with text 'NEW_SLIDE' to the
                        slideshow 'dst', space delimited. Use quotes to
                        separate slides
  --new                 Create a new slideshow at dst. Overwrites existing
                        files.
  --clear               sets the dst slideshow to clear before displaying a
                        slide
  --noclear             sets the dst slideshow to not clear before displaying
                        a slide
  --show                Shows the entire slideshow at dst, defaults to the
                        current slideshow
  --save                Saves the current slideshow to dst

```

Usage
-----

After you have created a new slideshow with --new and added a few slides to it with --new-slide "my slide text" use the command slide (just imagine you are yelling at a projector assistant) and you should see the text from your first slide appear in the console.


