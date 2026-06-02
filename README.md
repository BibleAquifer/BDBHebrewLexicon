# _Brown-Driver-Briggs Hebrew Lexicon_ Aquifer Resource

This repository (`BDBHebrewLexicon`) contains Aquifer resource data with resource-level metadata, article-level metadata, and content files in JSON and Markdown formats.

## License

This edition of the Brown\-Driver\-Briggs Hebrew Lexicon is licensed with a CC0 license and is in the public domain.

## Structure

The repository is organized by language codes, with each language folder containing subfolders for JSON and Markdown content.

## Documentation

For more information about the Aquifer platform, data, and metadata formats, visit the [Aquifer Documentation repository](https://github.com/BibleAquifer/BDBHebrewLexicon).

## Sources

This edition of the Brown-Driver-Briggs Hebrew and Aramaic Lexicon is derived from three publicly available open-source digitizations. The **primary text** is the HTML edition produced by James Cuénod ([jcuenod/BDB](https://github.com/jcuenod/BDB), maintained at [BN-Content/BDB](https://github.com/BN-Content/BDB)), which traces back to a [University of Texas digitization](https://github.com/jackweinbender/bdb_parse/tree/master/lexicon) and has the clearest open provenance of any available edition. The **OpenScriptures** edition ([openscriptures/HebrewLexicon](https://github.com/openscriptures/HebrewLexicon)) provides XML-structured data used primarily for root-section identification and article alignment. The **unfoldingWord/SIL** edition ([unfoldingWord/Brown-Driver-Briggs-Enhanced](https://github.com/unfoldingWord/Brown-Driver-Briggs-Enhanced)) provides human-reviewed Unicode transcriptions of non-Roman-script words (Arabic, Syriac, Ethiopic, Persian, and Samaritan) that were rendered as images in the primary source. Several other digital editions were considered and excluded because their provenance points to a BibleSoft-licensed edition that carries a copyright claim.

Each of these sources present accuracy problems as encoding of mixed left-to-right and right-to-left languages is a complicated matter. When the languages involved are non-Roman-script, the complications multiply. There are typos and other textual shortcomings in this material, but what is released here is judged to be on the whole relatively accurate and useful.

## Improvements Applied

Several improvements were applied to the primary text during production of this edition. Headwords were cross-checked across all three sources: where OpenScriptures and the unfoldingWord/SIL edition agree on a consonant skeleton that differs from the primary source, the OpenScriptures headword is substituted. Words in Arabic, Syriac, Ethiopic, Persian, and Samaritan script — originally present only as images in the primary sources — have been replaced with Unicode text using transcriptions reviewed by SIL personnel. Internal *vide* ("see") cross-references have been resolved and linked to their target entries using a three-level lookup (page number, normalized headword, consonant skeleton). Bible references carry machine-readable `data-verses` encoding for use by Aquifer consumers. BDB abbreviations are tagged with `<abbr>` elements keyed to the lexicon's own abbreviation list, and Strong's numbers are formatted as superscript references.

## Known Limitations

A number of areas remain for future improvement. A small number of foreign-script substitutions were skipped where the consonant skeleton of the transcription diverged too far from the primary source text; these are logged for manual review. Articles present only in OpenScriptures or **unfoldingWord/SIL** (i.e., not found in the primary source) have been excluded from this edition pending human review to confirm article identity. Finally, the provenance of the **unfoldingWord/SIL** edition is not fully documented, and it may share a textual ancestor with the BibleSoft-licensed edition; content derived from it (foreign-script transcriptions and limited headword influence) has been treated conservatively for this reason.

## Reporting Issues

If you find an issue with this edition, please report it by opening an issue in the repository. It is best to report issues and make PRs with the JSON format of the files as the other formats (markdown, PDF, etc.) are generated from the JSON.
