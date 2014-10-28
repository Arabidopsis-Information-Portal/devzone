## BAR expressologs_by_locus_v0.1

Function: Given a locus, return all homologous genes that exhibit similar expression patterns in equivalent tissues in other plant species.
GitHub: https://github.com/Arabidopsis-Information-Portal/bar_webservices_demos/tree/master/expressologsByLocus

Usage
```
curl -skL -H "Authorization: Bearer $TOKEN" -X GET https://api.araport.org/community/v0.3/aip/expressologs_by_locus_v0.1/search?locus=AT2G39730
```

Parameters
* locus: any valid AGI identifier

## BAR efp_by_locus_v0.1

Function: Given a locus and data source, return an eFP image depicting its expression pattern in that data source
GitHub: https://github.com/Arabidopsis-Information-Portal/bar_webservices_demos/tree/master/efpByLocus

Usage
```
curl -skL -H "Authorization: Bearer $TOKEN" -X GET https://api.araport.org/community/v0.3/aip/efp_by_locus_v0.1/search?locus=AT2G39730&source=Seed
```

Parameters
* locus: any valid AGI identifier
* source: member of 'Abiotic_Stress','Biotic_Stress','Chemical','Developmental_Map','Guard_Cell','Hormone','Light_Series','Natural_Variation','Seed','Tissue_Specific'

## ATTED atted_coexpressed_by_locus_v0.1

Function: Given a locus and a method/threshold for measuring similarity, return all Arabidopsis loci that are coexpressed with the query locus. Makes use of the ATTED-II v2 and the AIP synonym_to_locus APIs. 

 Usage
 ```
curl -skL -H "Authorization: Bearer $TOKEN" -X GET "https://api.araport.org/community/v0.3/aip/atted_coexpressed_by_locus_v0.1/search?locus=AT2G39730&relationship_type=correlation_coefficient&threshold=0.85"
```

Parameters
* locus: Valid AGI locus identifier
* relationship_type: correlation_coefficient | mutual_rank
* threshold : float
* database_version (optional): An ATTED-II database version

## AIP locus_gene_report_v0.1

Function: Given a locus, return curatorDescription, briefDescription, name, and computationalDescription in AIP-conformant JSON. 
Github: https://github.com/Arabidopsis-Information-Portal/aip_thalemine_webservices/tree/master/locus_gene_report

Usage
```
curl -skL -H "Authorization: Bearer $TOKEN" -X GET "https://api.araport.org/community/v0.3/aip/locus_gene_report_v0.1/search?locus=AT2G39730" 
```

Parameters
* locus: any valid AGI identifier


## AIP intermine/v0.4

Function: Provides computational access to all Intermine web services. 
GitHub: Not applicabel

Usage: Unlike APIs served from the /community endpoint, Intermine APIs at present do not require (or accept) authentication though we expect this to change in the 0.5 release of the service. The APIs supported by Intermine are documented at a [central dashboard](http://iodocs.labs.intermine.org/) where we expect Thalemine to appear soon. For now, you will need to use your imagination a bit to map the API URLs from the iodocs pages to a working invocation of the Thalemine API. 

Here's an example service call to YeastMine which will fetch its data model:
```
curl -skL -X GET "http://yeastmine.yeastgenome.org/yeastmine/service/model?format=json"
```

The cognate call for Thalemine is:
```
curl -skL "https://api.araport.org/intermine/v0.4/model?format=json"
```

