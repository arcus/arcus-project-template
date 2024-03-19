## `manifests/`

Storage location for structured metadata about all `data/` files and participants in a research effort. Contents of this directory include an inventory of all raw and endpoint data, an inventory of all participants and their related cohorts/samples/family roles (as applicable), an association between IDs and all data files, and documentation of relationships between files in pipelines/workflows.

### Required files

* [participant\_manifest.csv](participant_manifest.csv) matches participants/patients to cohorts and biosample IDs. Ideally, `biosample_id` links to the CHOP biobank. When you cannot link the the biobank, treat `biosample_id` as the IDs you use for samples taken from participants. If you deal with only one sample type, you might use the participant ID. If you run a treatment/control experiment, you might use `{participantID}_treat` and `{participantID}_control` as as a biosample ID scheme. If you work with different tissue samples from participants, you might use `{participantID}_{tissue}` as a biosample ID scheme. See [participant data dictionary](data_dicts/participant_manifest.csv) for definitions of each column. 
* [file\_manifest.csv](file_manifest.csv) matches biosample IDs to data files and experimental protocols, described in yaml files. Many files might share the same experimental protocol. These yaml protocol files describe experiment and data processing details. See [file data dictionary](data_dicts/file_manifest.csv) for definitions of each column. See the [omics-protocol repository](https://github.research.chop.edu/arcus/omics-protocols) (this is a CHOP enterprise website) for detailed information about the templates.
* [participant-crosswalk.txt](participant-crosswalk.txt) is a tab delimited file with no header that links `local_participant_id` in `PARTICIPANT_MANIFEST` to MRNs. See [crosswalk data dictionary](data_dicts/participant_crosswalk.csv) for definitions of each column.

### Optional files depending on data
* [file\_derivation.csv](file_derivation.csv) describes the relationships between files in a pipeline or workflow. See [derivation data dictionary](data_dicts/file_derivation.csv) for definitions of each column.
* [env\_manifest.csv](env_manifest.csv)Environment files are necessary for all scripts and machine models, and document the environment in which it was created and run. The environment_manifest.csv links the script or machine model and the environment file stored within the configs directory.


## Admin Notes

This sub-directory is required. 

