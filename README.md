# Edvard Munchs tekster
Website: [emunch.no](https://www.emunch.no/)

The website has been developed at the Munch Museum. It is a digital archive of material taken from the Munch collection in the Munch Museum. Essentially, the content consists of texts written by Edvard Munch and letters to and from Edvard Munch.

The collection of letters includes 4262 letters and drafts. We hope to include all of these in the NorKorr data set.

Unfortunately, the metadata for Munch’s texts currently exist in conflicting versions.

The register files at the website have not been updated for almost two years because the website needs a technical update before it is possible to publish again.

Some of the offline register files have been updated (but not published) anticipating an update of the website. 
Metadata in the collection database are updated when new data are found. We are aware of differences between the metadata in the register files and those in the collection database. 

Currently, the museum is working with the dating of all letters and letter drafts from Munch, revising dates where necessary and dating previously undated letters where possible. The result of this work is for practical reasons temporarily registered in an Excel sheet but will be transferred to the collection database once the work is completed.

Obviously, we want to have only one version of the metadata, and we want that to be registered in the collection database. From there the metadata can be published via an API to the new version of emunch.no.

We are planning to collect all metadata in the collection database when we have the necessary in-house resources to do so, but until then we have a confusing metadata situation and the metadata themselves are inconsistent.

## Files from the emunch project

### Register files

#### register_tei.xml
All texts by Munch, no matter what text type they are, are listed in this file. Metadata are not up to date.

#### correspondence.xml
All letters received by Munch are listed in this file. Metadata are not up to date.

#### Placenames
ID_sted-verdier.xlsx contains a list of all registered placenames.

#### Kronologi_Munchs_brev_20220831.xlsx
This file is not publicly available because it represents a snapshot of the current status of the ongoing work revising the dating of Munch’s letters.

### Letter files
XML text files are placed in xml-filer.zip. The zip file contains all types of texts and probably not all letters that are registered in register_tei.xml. It does not contain any of the letters registered in correspondence.xml.

The files are not the newest versions. The files are organised in-house in a folder structure on SharePoint and presently it was not possible to download them in one operation. However, if there are place data in a letter it should be encoded in these file versions already.

#### Structure of files
Each letter is comprised of at least two files, a main (parent) file and a page (child) file. When there is more than one page in a letter there are as many page files as there are pages. Postcard images and illustrations, drawings and envelopes also get their own files.

#### Identifying letters by inventory numbers
The inventory number of the letter is part of the <title> tag in each page file, see example here:

```
<teiHeader><fileDesc><titleStmt><title>No-MM_N0033-01.jpg</title>
```

#### Finding placenames in letters
Placenames can be found in page files as <placeName> tags inside <dateline> tags, see example:

```
<dateline><placeName key="pl155">S. Cloud</placeName> <date when="1889">1889</date></dateline>
```

