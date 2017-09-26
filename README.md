# Germania KG · extract-title

**Extract the first page of a PDF into a JPEG file.**

## Requirements

This tool requires **ImageMagick:** [Project page](https://www.imagemagick.org/script/index.php) · [brew formula](http://formulae.brew.sh/formula/imagemagick)

## Installation


**Homebrew/OSX:** extract-title is available via Germania's [homebrew-images](https://github.com/GermaniaKG/homebrew-images) tap.

```bash
$ brew install germaniakg/images/extract-title
```

**Linux:** Clone the repo somewhere. Do not forget to add the **extract-title** directory to your local **$PATH** variable.

```bash
$ git clone https://github.com/GermaniaKG/extract-title.git extract-title
```

## Usage

Pass one or more PDF file or a wildcard argument:

```bash
$ extract-title *.pdf
$ extract-title <file> [ <file> … ]
```

