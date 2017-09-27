# Germania KG · extract-title

**Extract the first page of a PDF into a JPEG or PNG or WebP file.**

## Requirements

- This tool requires **ImageMagick's** *convert* tool. See [project page](https://www.imagemagick.org/script/index.php) or [brew formula.](http://formulae.brew.sh/formula/imagemagick) 
- When you aim at **WebP** images, ImageMagick is required to work with Google's *cwebp* image compressor. See [project page](https://developers.google.com/speed/webp/docs/cwebp) or [brew formula.](http://formulae.brew.sh/formula/webp)

## Installation


**Homebrew/MacOS:** extract-title is available via Germania's [homebrew-images](https://github.com/GermaniaKG/homebrew-images) tap.

```bash
$ brew install germaniakg/images/extract-title
```

**Linux:** Clone the repo somewhere. Do not forget to add the **extract-title** directory to your local *PATH* variable or add a symlink to your *bin* directory.

```bash
$ git clone https://github.com/GermaniaKG/extract-title.git extract-title
```

## Usage

Pass one or more PDF file or a wildcard argument. Optionally, control output with command line options.

```bash
$ extract-title [options] *.pdf
$ extract-title [options] <file> [ <file> … ]
```

### Options

Option | Description
:-----|:------------
-p, --png | Create a PNG file as well
-w, --webp | Create a WebP file as well. Requires *ImageMagick* to work with *cweb*, will be ignored otherwise.
-q *int*, --quality *int* | Output quality as integer, defaults to 90
--size *int* | Pixel length on longer side; defaults to 1200 
--force | Overwrite existing files


### Examples

Create JPEG and additionally PNG and WebP. Create with lower quality than usual 90% quality.
If a matching output file exists, skip conversion for this file format.

```bash
$ extract-title -pw --quality 50 *.pdf
```

Like above, but with forced output, i.e. any existing file will be overridden:

```bash
$ extract-title -pw -q 50 --force *.pdf
```


