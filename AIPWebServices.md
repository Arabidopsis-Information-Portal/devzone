## BAR expressologs_by_locus_v0.1

Function: Given a locus, return all homologous genes that exhibit similar expression patterns in equivalent tissues in other plant species

Source: https://github.com/Arabidopsis-Information-Portal/bar_webservices_demos/tree/master/expressologsByLocus

Usage
```
curl -skL -H "Authorization: Bearer $TOKEN" -X GET https://api.araport.org/community/v0.3/aip/expressologs_by_locus_v0.1/search?locus=AT2G39730
```

Parameters
* locus: any valid AGI identifier

## BAR efp_by_locus_v0.1

Function: Given a locus and data source, return an eFP image depicting its expression pattern in that data source
Source: https://github.com/Arabidopsis-Information-Portal/bar_webservices_demos/tree/master/efpByLocus

Usage
```
curl -skL -H "Authorization: Bearer $TOKEN" -X GET https://api.araport.org/community/v0.3/aip/efp_by_locus_v0.1/search?locus=AT2G39730&source=Seed
```

Parameters
* locus: any valid AGI identifier
* source: member of 'Abiotic_Stress','Biotic_Stress','Chemical','Developmental_Map','Guard_Cell','Hormone','Light_Series','Natural_Variation','Seed','Tissue_Specific'

## ATTED atted_coexpressed_by_locus_v0.1

Function: Given a locus and a method/threshold for measuring similarity, return all Arabidopsis loci that are coexpressed with the query locus. Makes use of the ATTED-II v2 and the AIP synonym_to_locus APIs. 

Source: https://github.com/Arabidopsis-Information-Portal/atted_webservices

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

Function: Given a locus, return curatorDescription, briefDescription, name, and computationalDescription in AIP-conformant JSON

Source: https://github.com/Arabidopsis-Information-Portal/aip_thalemine_webservices/tree/master/locus_gene_report

Usage
```
curl -skL -H "Authorization: Bearer $TOKEN" -X GET "https://api.araport.org/community/v0.3/aip/locus_gene_report_v0.1/search?locus=AT2G39730" 
```

Parameters
* locus: any valid AGI identifier

## AIP synonymResolver

Function: Provides lightning-fast mapping of synonyms, aliases, and database identifiers to and from Arabidopsis AGI locus identifiers. 

Source: https://github.com/Arabidopsis-Information-Portal/aip_SynonymResolver

### resolver_fetch_synonyms_by_locus_v0.1

Function: List the supported synonym namespaces

Usage
```
curl -skL -X GET -H "Authorization: Bearer $TOKEN" "https://api.araport.org/community/v0.3/aip/resolver_synonym_kinds_v0.1/list"
```

Parameters
* None

### resolver_fetch_locus_by_synonym_v0.2

Function: Lookup an AGI locus identifier from its synonym

Usage
```
curl -skL -X GET -H "Authorization: Bearer $TOKEN" "https://api.araport.org/community/v0.3/aip/resolver_fetch_locus_by_synonym_v0.2/search?identifier=FWA"
```

Parameters
* identifier : Any reasonable synonym, alias, or database identifer. If we can't find it you'll get back an empty result

### resolver_fetch_synonyms_by_locus_v0.1

Function: Return all synonyms, etc. for a given AGI locus identifier

Usage
```
curl -skL -X GET -H "Authorization: Bearer $TOKEN" "https://api.araport.org/community/v0.3/aip/resolver_fetch_synonyms_by_locus_v0.1/search?locus=AT4G25530"
```

Parameters
* locus : any valid AGI identifier

## AIP agave/v2

Function: Provides foundational support for AIP and other projects, including authentication & authorization, file handling & transfer, job execution & management, events & notifications, monitoring, and user profile management

Source: https://bitbucket.org/taccaci/agave

Usage: Documented extensively at the [Agave API Developer Portal](http://agaveapi.co/). Interaction with the Araport-specific instance of Agave is via the [Araport API Manager](https://api.araport.org/store/).

## AIP intermine/v0.4

Function: Provides computational access to all ThaleMine web services.

ThaleMine is an implementation of the [InterMine](http://intermine.org) biological data warehouse.

Source: [http://iodocs.labs.intermine.org/thalemine/docs](http://iodocs.labs.intermine.org/thalemine/docs)

Usage: Unlike APIs served from the `/community` endpoint, ThaleMine APIs at present do not require (or accept) authentication, though we expect this to change in the 0.5 release of the service. The APIs supported by various implementations of InterMine are documented at a [central dashboard](http://iodocs.labs.intermine.org/).

The cognate call for ThaleMine is:
```
curl -skL -X GET "https://api.araport.org/intermine/v0.4/model?format=json"
```