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
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form></physicalDescription>

{{if(isBlank(cells['subject_0_topic'].value), '', '<subject authority="local"><topic>' + cells['subject_0_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_1_topic'].value), '', '<subject authority="local"><topic>' + cells['subject_1_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_2_topic'].value), '', '<subject authority="local"><topic>' + cells['subject_2_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_2_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_2_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_2_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_2_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_2_geographic'].value), '', '<subject' + if(isBlank(cells['subject_2_geographic_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_2_geographic_URI'].value + '"') + '><geographic>' + cells['subject_2_geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_3_topic'].value), '', '<subject authority="local"><topic>' + cells['subject_3_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_3_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_3_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_3_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_3_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_3_geographic'].value), '', '<subject' + if(isBlank(cells['subject_3_geographic_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_3_geographic_URI'].value + '"') + '><geographic>' + cells['subject_3_geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_4_topic'].value), '', '<subject authority="local"><topic>' + cells['subject_4_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_4_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_4_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_4_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_4_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_4_geographic'].value), '', '<subject' + if(isBlank(cells['subject_4_geographic_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_4_geographic_URI'].value + '"') + '><geographic>' + cells['subject_4_geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_5_topic'].value), '', '<subject authority="local"><topic>' + cells['subject_5_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_5_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_5_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_5_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_5_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_5_geographic'].value), '', '<subject' + if(isBlank(cells['subject_5_geographic_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_5_geographic_URI'].value + '"') + '><geographic>' + cells['subject_5_geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_6_topic'].value), '', '<subject authority="local"><topic>' + cells['subject_6_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_6_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_6_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_6_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_6_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_6_geographic'].value), '', '<subject' + if(isBlank(cells['subject_6_geographic_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_6_geographic_URI'].value + '"') + '><geographic>' + cells['subject_6_geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_7_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_7_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_7_temporal'].value), '', '<subject authority="local"><temporal>' + cells['subject_7_temporal'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_7_geographic'].value), '', '<subject' + if(isBlank(cells['subject_7_geographic_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_7_geographic_URI'].value + '"') + '><geographic>' + cells['subject_7_geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_8_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_8_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_9_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_9_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_10_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_10_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_11_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_11_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_12_name'].value), '', '<subject authority="local"><name><namePart>' + cells['subject_12_name'].value + '</namePart></name></subject>')}}

<language>
<languageTerm type="text" authority="iso639-2b">English</languageTerm>
</language>
<typeOfResource>still image</typeOfResource>
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

