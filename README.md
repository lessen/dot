# dot

Portable dotfiles.


Problem:

- Runing round re multiple machines
- Want to have a consistent environment on each machine
- But don't want to pollute each machine with dotfiles all over their harddrive

Solution:

- A lot of the tools I use (Emacs, bash, vimm...) accept config files as command line options 
- So write one file contain all my configs which dumps them all /tmp/$USER/...
- And write a little shell that writes the calls to these tools such that those tools are called with those config files 

## Usage

- Download the `dot` file;
- `sh dot`
- To run emacs with the options in the `dot` file, 
     - Use `e filename` 
- To tweak the configs, 
     - edit `dot`
     - type `reload` or restart via control-d then  `sh dot`.

#d# Udpates

There is an `update` function that will download (and overwrite) the local `dot` function. Will wipe any tweeks you've added to `dot`.
Use with care.
