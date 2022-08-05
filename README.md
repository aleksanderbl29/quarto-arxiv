# ArXiv Template

This is a Quarto template that assists you in creating PDF outputs which closely match the arXiv template for the rticles package (which is itself derived from [kourgeorge/arxiv-style](https://github.com/kourgeorge/arxiv-style)). If you are intending to publish your article on arXiv, it is highly recommended you upload your TeX files (and supporting files) directly. However, this template supports rendering decent looking PDFs for upload to other repositories either before or instead of submission to arXiv itself. The TeX generated from the default `.qmd` template also passes arxiv's pre-submission build process and checks, and so preprints generated from this template _may_ be able to be submitted to arXiv without any alterations.

There are currently a few differences between the PDFs generated by this template and those generated by the arXiv rticles template:

1. The fonts and spacings are not a perfect match. PRs to fix this are more than welcome.
2. References and links are not currently hyperlinked. PRs to fix this also more than welcome.
3. ORCiD IDs will be rendered as clickable logos next to author names. This is an intentional change.
4. Emails will be displayed as hyperlinks, and not in monospaced font. This is also intentional.

Any other differences are unintentional bugs -- please open an issue about anything you encounter!

## Creating a New Article

You can use this as a template to create a new article. To do this, use the following command:

```bash
quarto use template mikemahoney218/quarto-arxiv
```

This will install the extension and create an example qmd file and bibiography that you can use as a starting place for your article.

## Installation For Existing Document

You may also use this format with an existing Quarto project or document. From the quarto project or document directory, run the following command to install this format:

```bash
quarto install extension mikemahoney218/quarto-arxiv
```

## Usage

To use the format, you can use the format names `arxiv-pdf` and `arxiv-html`. For example:

```bash
quarto render article.qmd --to arxiv-pdf
```

or in your document yaml

```yaml
format:
  pdf: default
  arxiv-pdf:
    keep-tex: true    
```

You can view a preview of the rendered template at <https://mike.quarto.pub/quarto-arxiv-template/>.
