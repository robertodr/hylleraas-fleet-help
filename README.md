# The Hylleraas fleet
In December 2019 the centre acquired 2 new machines. The machines were obtained with the idea of having local resources with immediate availability for debuggin and testing on high-end hardware.
## The machines

Both machines are running [Debian 10](https://www.debian.org).

`woolf` (named after [Virginia Woolf](https://en.wikipedia.org/wiki/Virginia_Woolf)) is an Intel machine:
- Intel [Xeon W2295](https://ark.intel.com/content/www/us/en/ark/products/198011/intel-xeon-w-2295-processor-24-75m-cache-3-00-ghz.html) CPU
- 128 GB of DDR4 2666 MHz RAM
- Nvidia [Quadro RTX4000](https://www.nvidia.com/en-us/design-visualization/quadro/rtx-4000/) GPU
- 1 TB SSD (`/scratch` partition)
- 10 TB HDD

`sandel` (named after [Cora Sandel](https://no.wikipedia.org/wiki/Cora_Sandel)) is an AMD machine:
- AMD [Ryzen Threadripper 2990WX](https://www.amd.com/en/products/cpu/amd-ryzen-threadripper-2990wx) CPU
- 64 GB of DDR4 2933 MHz RAM
- Nvidia [Quadro RTX4000](https://www.nvidia.com/en-us/design-visualization/quadro/rtx-4000/) GPU
- 1 TB SSD (`/scratch` partition)
- 6 TB HDD

## Packages
### The AOCC compiler
Do the following to use the AOCC compiler in `sandel`
 ```
 $ source /opt/AMD/aocc-compiler-2.1.0/setenv_AOCC.sh
 ```

## Registering an account
In order to register an account, we ask you to fill this [Google form](https://docs.google.com/forms/d/e/1FAIpQLSc6PJvJRLYuoJs_PdA0GNmKgFBLkUyVdez2LoeJtVtd5wNhog/viewform?usp=sf_link) with your contact information and desired username. You will be contacted with further instructions. 

## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/robertodr/hylleraas-fleet-help/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/robertodr/hylleraas-fleet-help/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
