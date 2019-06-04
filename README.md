# Corpus BlackLab Metadata Config

Corpus specific metadata configuration for the corpora used in the Bridging the Gap project.

We use the [index-safar BlackLab format](https://github.com/arabic-digital-humanities/index-safar) for indexing our documents.
The files in this repository are used to make configure the metadata fields shown in the user interface.

## Usage

In order to use them, the yaml files in this repository need to be merged with the index-safar yaml files. The [adhtools](https://github.com/arabic-digital-humanities/adhtools) contain a workflow for doing this. Example usage:

```
cwltool ~/cwl-working-dir/index-corpus-specific.cwl --generic_yaml path/to/index-safar/safar-[analyzer|stemmer].blf.yaml --in_dir /path/to/input/data/safar/xml/with/metadata --index_format safar-[analyzer|stemmer] --index_name corpus --specific_yaml /path/to/corpus-blacklab-metadata-config/[fiqh|dawa].yaml --xmx 10G --yaml_name safar-[analyzer|stemmer].blf.yaml
```

## License

[![License: CC BY 4.0](https://i.creativecommons.org/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)

The data in this repository is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
