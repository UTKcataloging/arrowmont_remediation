**Open Refine Template for Arrsimple Collection**



**Prefix**

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```



**Body**

```
<mods>
<identifier type="pid">{{cells["PID"].value}}</identifier>
<identifier type="local">{{cells["identifier"].value}}</identifier>
{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>')}} 
<abstract>{{cells["abstract"].value}}</abstract>
{{if(isBlank(cells['dateCreated'].value), '', '<originInfo><dateCreated encoding="edtf">' + cells['dateCreated'].value + '</dateCreated></originInfo>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><form authority="aat" valueURI="{{cells['form2_URI'].value}}">{{cells['form2'].value}}</form><extent>{{cells["extent"].value}}</extent></physicalDescription>
{{if(isBlank(cells['subject_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '"><topic>' + cells['subject_topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_2_URI'].value + '"><topic>' + cells['subject_topic_2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_4_URI'].value + '"><topic>' + cells['subject_topic_4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_3_URI'].value + '"><topic>' + cells['subject_topic_3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject authority="wikidata" valueURI="' + cells['subject_name_URI'].value + '"><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name_2'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_2_URI'].value + '"><name><namePart>' + cells['subject_name_2'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name_3'].value), '', '<subject authority="wikidata" valueURI="' + cells['subject_name_3_URI'].value + '"><name><namePart>' + cells['subject_name_3'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_2_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_2_name_URI'].value + '"><name><namePart>' + cells['subject_2_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_2_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_2_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_2_geographic'].value, '', '<subject authority="naf" valueURI="' + cells['subject_2_geographic_URI'].value + '"><geographic>' + cells['subject_2_geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_3_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_3_name_URI'].value + '"><name><namePart>' + cells['subject_3_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_3_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_3_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_4_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_4_name_URI'].value + '"><name><namePart>' + cells['subject_4_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_4_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_4_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_5_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_5_name_URI'].value + '"><name><namePart>' + cells['subject_5_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_5_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_5_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_6_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_6_name_URI'].value + '"><name><namePart>' + cells['subject_6_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_6_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_6_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_7_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_7_name_URI'].value + '"><name><namePart>' + cells['subject_7_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_7_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_7_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_8_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_8_name_URI'].value + '"><name><namePart>' + cells['subject_8_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_9_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_9_name_URI'].value + '"><name><namePart>' + cells['subject_9_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_10_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_10_name_URI'].value + '"><name><namePart>' + cells['subject_10_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_11_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_11_name_URI'].value + '"><name><namePart>' + cells['subject_11_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_12_name'].value), '', '<subject authority="local" valueURI="' + cells['subject_12_name_URI'].value + '"><name><namePart>' + cells['subject_12_name'].value + '</namePart></name></subject>')}}

<subject authority="naf" valueURI="{{cells['subject_geographic_URI'].value}}"><geographic>{{cells['subject_geographic'].value}}</geographic><cartographics><coordinates>{{cells['coordinates'].value}}</coordinates></cartographics></subject>
<language>
<languageTerm type="text" authority="iso639-2b">English</languageTerm>
</language>
<typeOfResource>text</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['accessCondition_URI'].value}}">{{cells['accessCondition'].value}}</accessCondition>
</mods>
```



**Suffix**

```
</modsCollection>
```

