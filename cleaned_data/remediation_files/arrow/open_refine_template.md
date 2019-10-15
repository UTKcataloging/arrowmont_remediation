# OpenRefine Template for The Arrow

---

## Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```

## Row Template

```
<mods>
<identifier type="pid">{{cells['PID'].value}}</identifier>
<identifier type="filename">{{cells['filename'].value}}</identifier>
{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>')}}
{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells['tableOfContents'].value), '', '<tableOfContents>' + cells['tableOfContents'].value + '</tableOfContents>')}}
{{if(isBlank(cells['Names 1'].value), '', '<name><namePart>' + cells['Names 1'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['Names 2'].value), '', '<name><namePart>' + cells['Names 2'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['Names 3'].value), '', '<name><namePart>' + cells['Names 3'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['Names 4'].value), '', '<name><namePart>' + cells['Names 4'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['Names 5'].value), '', '<name><namePart>' + cells['Names 5'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['Names 6'].value), '', '<name><namePart>' + cells['Names 6'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['Names 7'].value), '', '<name><namePart>' + cells['Names 7'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['Names 8'].value), '', '<name><namePart>' + cells['Names 8'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['Names 9'].value), '', '<name><namePart>' + cells['Names 9'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['Names 10'].value), '', '<name><namePart>' + cells['Names 10'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['Names 11'].value), '', '<name><namePart>' + cells['Names 11'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['dateIssued'].value), '', '<originInfo><dateIssued' + if(isBlank(cells['date_qualifier'].value), '', ' qualifier="approximate"') + '>' + cells['dateIssued'].value + '</dateIssued><dateIssued encoding="edtf" keyDate="yes"' + if(isBlank(cells['date_qualifier'].value), '', ' qualifier="approximate"') + '>' + cells['dateIssued_edtf'].value + '</dateIssued><publisher>Pi Beta Phi</publisher></originInfo>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells['extent'].value}}</extent></physicalDescription>
{{if(isBlank(cells['subject_temporal'].value), '', '<subject><temporal>' + cells['subject_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['mods.subject.1topic'].value), '', '<subject' + if(isBlank(cells['mods.subject.1topic_URI'].value), '', ' authority="lcsh" valueURI="' + cells['mods.subject.1topic_URI'].value + '"') + '><topic>' + cells['mods.subject.1topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['mods.subject.2topic'].value), '', '<subject' + if(isBlank(cells['mods.subject.2topic_URI'].value), '', ' authority="lcsh" valueURI="' + cells['mods.subject.2topic_URI'].value + '"') + '><topic>' + cells['mods.subject.2topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['mods.subject.3topic'].value), '', '<subject' + if(isBlank(cells['mods.subject.3topic_URI'].value), '', ' authority="lcsh" valueURI="' + cells['mods.subject.3topic_URI'].value + '"') + '><topic>' + cells['mods.subject.3topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['mods.subject.4topic'].value), '', '<subject' + if(isBlank(cells['mods.subject.4topic_URI'].value), '', ' authority="lcsh" valueURI="' + cells['mods.subject.4topic_URI'].value + '"') + '><topic>' + cells['mods.subject.4topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['mods.subject.1name'].value), '', '<subject' + if(isBlank(cells['mods.subject.1name_URI'].value), '', ' authority="naf" valueURI="' + cells['mods.subject.1name_URI'].value + '"') + '><name><namePart>' + cells['mods.subject.1name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['mods.subject.2name'].value), '', '<subject' + if(isBlank(cells['mods.subject.2name_URI'].value), '', ' authority="naf" valueURI="' + cells['mods.subject.2name_URI'].value + '"') + '><name><namePart>' + cells['mods.subject.2name'].value + '</namePart></name></subject>')}}
<subject authority="naf" valueURI="http://id.loc.gov/authorities/names/n80040520"><geographic>Gatlinburg (Tenn.)</geographic></subject>
<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh85057008"><geographic>Great Smoky Mountains (N.C. and Tenn.)</geographic></subject>
{{if(isBlank(cells['genre'].value), '', '<genre authority="lcgft" valueURI="' + cells['genre_URI'].value + '">' + cells['genre'].value + '</genre>')}}
<language><languageTerm authority="iso639-2b" type="text">English</languageTerm></language>
<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>
<relatedItem type="host" displayLabel="Project"><titleInfo><title>From Pi Beta Phi to Arrowmont</title></titleInfo></relatedItem>
<relatedItem displayLabel="Project Part" type="host"><titleInfo><title>The Arrow of Pi Beta Phi</title></titleInfo></relatedItem>
<relatedItem displayLabel="Bibliographic Citation" type="host"><titleInfo><title>{{cells['volume_title'].value}}</title></titleInfo></relatedItem>
<location><physicalLocation>Pi Beta Phi Fraternity</physicalLocation>
<physicalLocation displayLabel="Address">1154 Town and Country Commons Drive, Town and Country, Missouri 63017</physicalLocation><shelfLocator>{{cells['shelfLocator'].value}}</shelfLocator></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource><recordOrigin>Created and edited in general conformance to MODS Guidelines (Version 3.5).</recordOrigin></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>
```

## Row Separator

**LEAVE BLANK**

## Suffix

```
</modsCollection>
```