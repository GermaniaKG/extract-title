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
$ extract-title [options] *.pdf
$ extract-title [options] <file> [ <file> … ]
```

### Options

Option | Description
:-----|:------------
-p, --png | Create a PNG file as well
-w, --webp | Create a WEBP file as well. Requires *cweb* to be installed, will be ignored otherwise.
-q, --quality *int* | Output quality, defaults to 90
--force | Overwrite existing files

### Examples

Create JPEG, PNG and WEBP with lower quality.
If a matching JPG/PNG/WEBP output file exists, this conversion will be skipped.

```bash
$ extract-title -pw --quality 50 *.pdf
```

Like above, but with forced output, i.e. any existing file will be overridden:

```bash
$ extract-title -pw -q 50 --force *.pdf
```


