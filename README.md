Squarespace Multilingual Website
----------------------------------
_Make your squarespace website multilingual by following steps below_


#### Create Files For New Language

Make a copy of every `.region` file for new language and give them different name for example `urdu.region`
Then navigate to blocks folder and and make copy of navigation file for example: `urdu-navigation.block`


#### Define Tempaltes For New Language

Open the template.conf file and navigate to the `layouts` section.
```json
"layouts" : { "default" : { "name" : "default", "regions" : [ "site"] } }
```

Add this code:
```json
"urdu" : { "name" : "Urdu Template", "regions" : [ "urdu"] }
```


#### Define Navigation For New Language

Open the template.conf file and navigate to the `Navigations` section.
```json 
navigations" : [ { "title" : "Main Navigation", "name" : "mainNav" } ]
```

Add this code:
```json 
{ "title" : "Urdu Navigation", "name" : "urduNav" }
```


#### Include Your Newly Created Navigation In New Template

To include new navigation in your new template, use the Squarespace navigation tag with same navigation id and template name you added in `template.conf` for new navigation:

```json
<squarespace:navigation navigationId="urduNav" template="urdu-navigation" />
```


#### Add Language Switching Buttons

