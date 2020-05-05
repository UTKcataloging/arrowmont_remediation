**Prefix:**

<?xml version="1.0" encoding="UTF-8"?> <modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">



**Body:**

<mods>

<identifier type="pid">{{cells["headeridentifier"].value}}</identifier>

<titleInfo><title>{{cells["title"].value}}</title></titleInfo>

{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}

{{if(isBlank(cells['namePart'].value), '', '<name'+ if(isBlank(cells['name.URI'].value), '', ' authority="naf" valueURI="' + cells['name.URI'].value + '"') + '><namePart>' + cells['namePart'].value + '</namePart>' + if(isBlank(cells['roleTerm'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role_URI'].value + '">' + cells['roleTerm'].value + '</roleTerm></role>') + '</name>')}}

<originInfo> {{if(isBlank(cells["humanReadableDate"].value),'','<dateCreated>' + cells['humanReadableDate'].value + '</dateCreated>')}}{{if(isBlank(cells["dateCreated_edtf"].value),'','<dateCreated encoding="edtf">' + cells['dateCreated_edtf'].value + '</dateCreated>')}}</originInfo>

<language><languageTerm authority="iso639-2b" type="text">English</languageTerm></language>

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells['extent'].value}}</extent></physicalDescription>

{{if(isBlank(cells['physicalDescription_form2'].value),'','<physicalDescription><form authority="aat" valueURI="' + cells['form_URI2'].value + '">' + cells['form2'].value + '</form></physicalDescription>')}}

{{if(isBlank(cells['subject.0geographic_loc'].value), '', '<subject' + if(isBlank(cells['subject.geographic_loc_URI'].value), '>', ' authority="naf" valueURI="' + cells['subject.geographic_loc_URI'].value + '">') + '<geographic>' + cells['subject.geographic_loc'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject.1geographic'].value), '', '<subject' + if(isBlank(cells['subject.1geographic_URI'].value), '>', ' authority="naf" valueURI="' + cells['subject.1geographic_URI'].value + '">') + '<geographic>' + cells['subject.1geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject.0topic'].value), '', '<subject' + if(isBlank(cells['subject.0topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.0topic_URI'].value + '">') + '<topic>' + cells['subject.0topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject.1topic'].value), '', '<subject' + if(isBlank(cells['subject.1topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.1topic_URI'].value + '">') + '<topic>' + cells['subject.1topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject.2topic'].value), '', '<subject' + if(isBlank(cells['subject.2topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.2topic_URI'].value + '">') + '<topic>' + cells['subject.2topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject.3topic'].value), '', '<subject' + if(isBlank(cells['subject.3topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.3topic_URI'].value + '">') + '<topic>' + cells['subject.3topic'].value + '</topic></subject>')}}

<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>

<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['relatedItem'].value}}</title></titleInfo></relatedItem>

<location><physicalLocation valueURI="{{cells['physicalLocation_uri'].value}}">{{cells['physicalLocation.1text'].value}}</physicalLocation><shelfLocator>{{cells['physicalLocation.2text'].value}}</shelfLocator></location>

<recordInfo><recordContentSource valueURI="{{cells['source_URI'].value}}">{{cells['source'].value}}</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['Copyright_URI'].value}}">{{cells['Copyright'].value}}</accessCondition> 

</mods>



**Suffix:**

</modsCollection>