## `references/protocols/`

For Omics data, protocols are the metadata that document the processes, tools and standards used to generate sequencing data. Protocols are important to complete, as the information will be needed for future analysis, pipelines or workflows with the data.

Arcus documents the protocol information in structured yaml files. The YAML structure and information captured depends on the sequencing method (such as High-Throughput sequencing, Microarray or Metabolics) and the file type (like FASTQ, CRAM, VCF, etc.). High-Throughput sequencing data includes whole genome sequencing, whole exome sequencing and RNA-seq data. Microarrays include SNP data. A new yaml file should be created whenever the process, tools or standards are different for a set of files. The protocol yaml is linked to the files in the (file_manifest.csv)[manifests/file_manifest.csv] file.
## Admin Notes

This sub-directory is optional. For studies containing sequencing data, this sub-directory is required. 
