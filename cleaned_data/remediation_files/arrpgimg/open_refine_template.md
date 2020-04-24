# OpenRefine Template for Arrowmont Simple Images

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
{{if(isBlank(cells['supplied_title'].value), '', '<titleInfo supplied="yes"><title>' + cells["supplied_title"].value + '</title></titleInfo>')}}
{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
<name><namePart>{{cells['creator'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre">Creator</roleTerm></role></name>
{{'<originInfo>' + if(isBlank(cells['date'].value), '', '<dateCreated>' + cells['date'].value + '</dateCreated>') + if(isBlank(cells['date_end'].value), '<dateCreated encoding="edtf" keyDate="yes">' + cells['date_start'].value + '</dateCreated>', '<dateCreated encoding="edtf" keyDate="yes" point="start">' + cells['date_start'].value + '</dateCreated><dateCreated encoding="edtf" keyDate="yes" point="end">' + cells['date_end'].value + '</dateCreated>') + '</originInfo>'}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_aat_URI'].value}}">{{cells['form_aat'].value}}</form></physicalDescription>
{{if(isBlank(cells['subject_topic'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_URI'].value + '"><topic>' + cells['subject_topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_2'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_2_URI'].value + '"><topic>' + cells['subject_topic_2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_3'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_3_URI'].value + '"><topic>' + cells['subject_topic_3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_4'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_4_URI'].value + '"><topic>' + cells['subject_topic_4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_5'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_5_URI'].value + '"><topic>' + cells['subject_topic_5'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_6'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_6_URI'].value + '"><topic>' + cells['subject_topic_6'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_7'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_7_URI'].value + '"><topic>' + cells['subject_topic_7'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_8'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_8_URI'].value + '"><topic>' + cells['subject_topic_8'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_9'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_9_URI'].value + '"><topic>' + cells['subject_topic_9'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_10'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_10_URI'].value + '"><topic>' + cells['subject_topic_10'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_geo_lcsh'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_geo_lcsh_URI'].value + '"><geographic>' + cells['subject_geo_lcsh'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geo_lcsh_2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_geo_lcsh_2_URI'].value + '"><geographic>' + cells['subject_geo_lcsh_2'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_name_Geo'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_Geo_URI'].value + '"><geographic>' + cells['subject_name_Geo'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_name_Geo_2'].value), '', '<subject' + if(isBlank(cells['subject_name_Geo_2_auth'].value), '', ' authority="' + cells['subject_name_Geo_2_auth'].value + '" valueURI="' + cells['subject_name_Geo_2_URI'].value + '"') + '><geographic>' + cells['subject_name_Geo_2'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_name_Geo_3'].value), '', '<subject' + if(isBlank(cells['subject_name_Geo_3_URI'].value), '', ' authority="geonames" valueURI="' + cells['subject_name_Geo_3_URI'].value + '"') + '><geographic>' + cells['subject_name_Geo_3'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_name_Geo_4'].value), '', '<subject' + if(isBlank(cells['subject_name_Geo_4_URI'].value), '', ' authority="geonames" valueURI="' + cells['subject_name_Geo_4_URI'].value + '"') + '><geographic>' + cells['subject_name_Geo_4'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject' + if(isBlank(cells['subject_name_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name_URI'].value + '"') + '><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name2'].value), '', '<subject' + if(isBlank(cells['subject_name2_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name2_URI'].value + '"') + '><name><namePart>' + cells['subject_name2'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name3'].value), '', '<subject' + if(isBlank(cells['subject_name3_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name3_URI'].value + '"') + '><name><namePart>' + cells['subject_name3'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name4'].value), '', '<subject' + if(isBlank(cells['subject_name4_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name4_URI'].value + '"') + '><name><namePart>' + cells['subject_name4'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name5'].value), '', '<subject><name><namePart>' + cells['subject_name5'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name6'].value), '', '<subject><name><namePart>' + cells['subject_name6'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name7'].value), '', '<subject><name><namePart>' + cells['subject_name7'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name8'].value), '', '<subject><name><namePart>' + cells['subject_name8'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name9'].value), '', '<subject><name><namePart>' + cells['subject_name9'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name10'].value), '', '<subject><name><namePart>' + cells['subject_name10'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name11'].value), '', '<subject><name><namePart>' + cells['subject_name11'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name12'].value), '', '<subject><name><namePart>' + cells['subject_name12'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name13'].value), '', '<subject><name><namePart>' + cells['subject_name13'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name14'].value), '', '<subject><name><namePart>' + cells['subject_name14'].value + '</namePart></name></subject>')}}
<typeOfResource>still image</typeOfResource>
<relatedItem type="otherVersion"><titleInfo><title>{{cells['scrapbook'].value}}</title></titleInfo><location><url>{{cells['scrapbook_URI'].value}}</url></location></relatedItem>
<relatedItem displayLabel="Project Part" type="host"><titleInfo><title>Arrowmont Simple Images from Scrapbooks</title></titleInfo></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2001080757">Arrowmont School of Arts and Crafts</physicalLocation></location>
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