# Open Refine Template for The Art of Arrowmont

## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="filename">{{cells["identifier"].value}}</identifier>
<identifier type="pid">{{cells["PID"].value}}</identifier>
<titleInfo><title>{{cells['title'].value}}</title></titleInfo>
<abstract>{{cells['abstract'].value}}</abstract>
<abstract>{{cells['abstract_grant'].value}}</abstract>
{{if(isBlank(cells['creator'].value), '', '<name type="personal"' + if(isBlank(cells['creator_URI'].value), '', ' authority="naf" valueURI="' + cells['creator_URI'].value + '"') + '><namePart>' + cells['creator'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/art">Artist</roleTerm></role></name>')}}
<physicalDescription>
{{if(isBlank(cells['form_broad'].value), '', '<form authority="aat" valueURI="' + cells['form_broad_URI'].value + '">' + cells['form_broad'].value + '</form>')}}
{{if(isBlank(cells['form_aat'].value), '', '<form authority="aat" valueURI="' + cells['form_aat_URI'].value + '">' + cells['form_aat'].value + '</form>')}}
{{if(isBlank(cells['form_aat_2'].value), '', '<form authority="aat" valueURI="' + cells['form_aat_2_URI'].value + '">' + cells['form_aat_2'].value + '</form>')}}
{{if(isBlank(cells['form_aat_3'].value), '', '<form authority="aat" valueURI="' + cells['form_aat_3_URI'].value + '">' + cells['form_aat_3'].value + '</form>')}}
<extent>{{cells['extent'].value}}</extent>
</physicalDescription>
<originInfo><dateCreated>{{cells['dateCreated'].value}}</dateCreated><dateCreated encoding="edtf" keyDate="yes">{{cells['dateCreated'].value}}</dateCreated><place><placeTerm valueURI="http://id.loc.gov/authorities/names/no2001080757">Arrowmont School of Arts and Crafts</placeTerm></place></originInfo>
{{if(isBlank(cells['subject_lcsh'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_URI'].value + '"><topic>' + cells['subject_lcsh'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_lcsh_2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_2_URI'].value + '"><topic>' + cells['subject_lcsh_2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_lcsh_3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_3_URI'].value + '"><topic>' + cells['subject_lcsh_3'].value + '</topic></subject>')}}
<typeOfResource>three dimensional object</typeOfResource>
<language><languageTerm type="text" authority="iso639-2b">No linguistic content</languageTerm></language>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Art of Arrowmont</title></titleInfo></relatedItem>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource><languageOfCataloging><languageTerm type="text" authority="iso639-2b">English</languageTerm></languageOfCataloging><recordOrigin>
Created and edited in general conformance to MODS Guidelines (Version 3.5).
</recordOrigin></recordInfo>
<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/CNE/1.0/">Copyright Not Evaluated</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```