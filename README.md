# NTUA Typst Essay Template

A clean and professional Typst template designed for assignments and reports at the National Technical University of Athens (NTUA).

## Features

- **Custom Title Page**: Includes university logo, institute details, course/assignment title, and a team members table.
- **Greek Language Support**: Pre-configured for Greek (`lang: "el"`) using the **GFS Neohellenic** font family.
- **Headers & Footers**: Automatic headers with author information and assignment title.
- **Math & Equations**: Section-based equation numbering (e.g., 1.1, 1.2) and specialized math fonts.
- **Code Highlighting**: Custom font support for raw code blocks.
- **Integrated Packages**: Pre-configured with `unify` for SI units and `CeTZ` for plotting/drawing.

## Prerequisites

To use this template as intended, you should have the following fonts installed on your system:

- **GFS Neohellenic**: Main text font.
- **GFS Neohellenic Math**: Math font for equations.
- **Comic Code**: (Optional) Used for raw code blocks. You can change this in `conf.typ` if desired.

## Getting Started

1. Clone this repository or copy the files to your project directory.
2. Ensure you have the required fonts installed.
3. Edit `main.typ` to fill in your assignment details:

```typst
#import "conf.typ": *

#show: doc => conf(
  title: "Τίτλος Εργασίας",
  short-title: "Σύντομος Τίτλος",
  subtitle: "Μάθημα / Τύπος Εργασίας",
  author: "Ονοματεπώνυμο",
  institute: "ΕΘΝΙΚΟ ΜΕΤΣΟΒΕΙΟ ΠΟΛΥΤΕΧΝΕΙΟ ΣΧΟΛΗ ...",
  logo: "./pyro.svg",
  team-members: (
    ("Όνομα 1", "ΑΜ"),
    ("Όνομα 2", "ΑΜ"),
  ),
  doc,
)

= Εισαγωγή
Το κείμενό σας εδώ...
```

## Project Structure

- `main.typ`: Your main document file where you write your content.
- `conf.typ`: The template configuration and layout logic.
- `pyro.svg`: The NTUA logo (replace if necessary).

## Usage with Typst

Compile your document using the Typst CLI. It is recommended to use the `a-2b` PDF standard for better compatibility with archival requirements (often required for university submissions):

```bash
typst compile --pdf-standard a-2b main.typ
```

Or watch for changes:

```bash
typst watch main.typ
```

## License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.
