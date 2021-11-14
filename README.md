# typora2tex

Quick terminal application that takes my typora markdown notes and converts them into tex. 

You should be able to convert it to a tex file (with the same name, flags available below) 
```bash
typora2tex mymarkdown.md
```

The default behaviour assumes all images are stored in the images folder in the same directory as the markdown file. This is needed so that all `.svg` files can be converted to `.eps` files. If you are not using .svg files, this doesn't matter. 

Feel free to use this! But I have made this for my personal workflow, so your mileage may vary. 

## Features

I'll focus on a limited set of features important to me. It should be able to change:

- `#` to the appropriate `\section{header}`
- bullet points to `\begin{itemize} ... \end{itemize}`
- dragged and dropped figures into `\includegraphics{..../..}`
- ` `` ` marks will become inline `\texttt{...}`for now. 

##### Future features:

- multiline code blocks for Julia, python, C++ and bash
- numbered points to `\begin{enumerate} ... \end{enumerate}`

## How to install



## Options

#### Output File

One can set the output file explicitly. Default is a file with the same name as the markdown in the same folder as the markdown

```bash
typora2tex mymarkdown.md -o ./path/to/final.tex
```

```bash
typora2tex mymarkdown.md --outputfile=./path/to/final.tex  #or as an optional parameter
```

#### Templates

You should be able to give your own template if needed

```bash
typora2tex mymarkdown.md -t ./path/to/mytemplate.tex
```

You should be able to give the name of a default template if needed
```bash
typora2tex mymarkdown.md --template=article
```

#### Images from svg to eps

You specify the directory with all the images:

And it wil convert all `svg` files into `eps` files using `inkscape`  and change the extension in the links in the resultant tex file. 

```ba
typora2tex mymarkdown.md --imagefolder=./images
```

#### Author

You can also set the author

```bash
typora2tex mymarkdown.md --author="Asad Hussain"
```

#### Help

For help you can just use the `--help` command:

```bash
typora2tex --help
```

