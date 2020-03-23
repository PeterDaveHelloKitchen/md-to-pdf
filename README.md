# md-to-pdf

A web service for converting markdown to PDF

## Usage

For quick experimentation, you can use the web version at [https://md-to-pdf.herokuapp.com/](https://md-to-pdf.herokuapp.com/).
Just paste your markdown and download the converted PDF.

## API

You can convert markdown by sending a `POST` request to `https://md-to-pdf.herokuapp.com/`.

	curl -X POST -d 'markdown=# Heading 1' -o md-to-pdf.pdf https://md-to-pdf.herokuapp.com/

| Parameter | Required | Description |
| --- | --- | --- |
| `markdown` | Required | The markdown content to convert |
| `css` | Optional | CSS styles to apply |
| `engine` | Optional |The PDF conversion engine, can be `wkhtmltopdf` or `weasyprint`, defaults to `weasyprint` |

## Built with

- [Rocket - a web framework for Rust](https://rocket.rs/)
- [Codemirror - a text editor for the browser](https://codemirror.net/)
- [Pandoc - a universal document converter](https://pandoc.org/)
