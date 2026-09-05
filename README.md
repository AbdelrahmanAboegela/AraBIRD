# AraBIRD

**AraBIRD: A Modern Standard Arabic Adaptation of BIRD for Text-to-SQL
over English Schemas**

AraBIRD is a Modern Standard Arabic (MSA) adaptation of the BIRD
Text-to-SQL benchmark. It enables evaluation of Arabic Text-to-SQL
systems where users ask questions in Arabic while database schemas,
identifiers, stored values, and SQL remain in English.

The dataset focuses on cross-lingual schema grounding without
translating the underlying databases.

## Dataset

AraBIRD contains:

-   **8,375 training examples**
-   **1,469 development examples**

Each example includes:

-   Arabic question
-   Arabic evidence
-   Original BIRD database identifier
-   Gold SQL query
-   Original English schema/database context

Repository structure:

    AraBIRD/
    ├── train.json
    ├── dev.json
    └── README.md

## Task

Given:

    Arabic Question + Evidence + English Database Schema

the goal is to generate the correct SQL query.

Evaluation is performed using SQL execution accuracy on the target
databases.

## Construction

AraBIRD was created through:

-   SQL-aware MSA translation
-   Preservation of schema identifiers and database values
-   Automatic consistency checks
-   Native Arabic speaker auditing

Gold SQL was used only during dataset construction and auditing, not as
model input during evaluation.

## Citation

If you use AraBIRD, please cite:

``` bibtex
@inproceedings{alshames2026arabird,
  title={AraBIRD: A Modern Standard Arabic Adaptation of BIRD for Text-to-SQL over English Schemas},
  author={Alshames, Abdelrahman A. and Abdelmotteleb, Ibrahim and Sameh, Maya and Salem, Zeyad M. and Farrag, Shehab and Morcos, Gina and Alashry, Salma A. and Zaky, Ahmed B.},
  booktitle={2026 IEEE 8th Novel Intelligent and Leading Emerging Sciences Conference (NILES)},
  year={2026}
}
```

## Authors

-   Abdelrahman A. Alshames
-   Ibrahim Abdelmotteleb
-   Maya Sameh
-   Zeyad M. Salem
-   Shehab Farrag
-   Gina Morcos
-   Salma A. Alashry
-   Ahmed B. Zaky

## License

For research use. Please follow the original BIRD benchmark terms for
any inherited database resources.
