Track-R-cmd
===========

A paper thin CLI wrapper around [Track-R](http://github.com/jfgomez86/Track-R).


Installing
----------

No fancy-pants gem packaging yet:

    git clone git://github.com/heisters/track-r-cmd.git
    vi track-r-cmd/track-r-cmd # add your token on TOKEN
    cd <a directory that's in your $PATH>
    ln -s <the directory you cloned to>/track-r-cmd/track-r-cmd

Usage
-----

    track-r-cmd projects # lists all projects
    track-r-cmd project foobar stories # lists all stories for the project "foobar"
    track-r-cmd project foo stories # same, as long as you don't have any other projects that match /foo/
    track-r-cmd project foo stories owned_by Jorge # filters stories where the owned_by field matches /Jorge/
    track-r-cmd stories foo owned_by Jorge # same. The project selection is implicit
    track-r-cmd # load an IRB session with all the helpers defined
    track-r-cmd "puts t.projects.map(&:url)" # eval some arbitrary code in the defined environment
