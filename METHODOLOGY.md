# NSVRC All Points Broadband Availability Dataset

## First Public Release

September 2026

## Executive Summary

This repository contains an address level dataset and supporting analysis of publicly funded broadband locations across the Northern Shenandoah Valley Regional Commission (NSVRC) region of Virginia.

Broadband access is no longer a luxury. Reliable high speed internet is essential for education, employment, telehealth, agriculture, business development, government services, emergency communications, and participation in modern society. Despite significant public investment intended to expand broadband access, many residents throughout the region continue to report limited, unavailable, or uncertain service options.

This project was created to provide an independent, transparent, and reproducible view of broadband availability at publicly funded locations. The underlying work is publicly funded, the underlying source data is publicly available, and the resulting dataset is being released for public use to support transparency, accountability, journalism, research, mapping, verification, and future analysis.

One of the challenges facing residents, local governments, journalists, and researchers is that information related to broadband deployment is often distributed across multiple datasets, funding programs, public records, GIS systems, maps, and service qualification tools. This project brings those sources together into a single address level dataset using a consistent methodology.

The resulting dataset contains 51,080 publicly funded broadband locations across eight counties and preserves funding provenance, geographic attribution, address validation information, availability results, and supporting metadata necessary for independent review.

## Why This Matters

The NSVRC regional broadband initiative represents one of the largest broadband deployment efforts in Virginia.

Thousands of locations throughout the region were identified through VATI and BEAD funding programs because reliable broadband service was unavailable, inadequate, or underserved.

The objective of this repository is not to advocate for any particular outcome. The objective is to provide a transparent and independently verifiable dataset that allows residents, journalists, local governments, researchers, and other interested parties to evaluate publicly funded broadband deployment using a common set of data and methods.

This repository exists because transparency is important whenever public funds are used to build public infrastructure.

## Regional Overview

The dataset covers the following Northern Shenandoah Valley Regional Commission counties:

* Augusta County
* Clarke County
* Fauquier County
* Frederick County
* Page County
* Rappahannock County
* Rockingham County
* Warren County

The project combines authoritative statewide GIS data, public broadband funding records, and publicly observable availability results into a single regional dataset.

## Key Statistics

Current funded addresses:

51,080

Current orderable addresses:

9,172

Current not orderable addresses:

41,753

Current unresolved addresses:

155

Current regional orderable rate:

18.01%

## Data Sources

This project incorporates publicly available information from:

Virginia Geographic Information Network (VGIN)

https://vgin.vdem.virginia.gov

Virginia Statewide Address Points (2026 Q2)

Virginia Administrative Boundary Dataset (2025)

Virginia Telecommunication Initiative (VATI)

VATI 2022

VATI 2023

VATI 2024

Virginia Broadband Equity, Access, and Deployment Program (BEAD)

Post Challenge Eligible Locations

Virginia Department of Housing and Community Development

https://www.dhcd.virginia.gov/broadband

Virginia Broadband Map

https://vast.virginia.gov

Northern Shenandoah Valley Regional Commission

https://www.nsvregion.org

Public All Points Broadband availability and service qualification systems

https://allpointsbroadband.com

Additional source information is provided in SOURCES.md.

## Methodology Overview

No single public dataset contained all funded broadband locations.

The dataset was constructed by combining statewide address points, administrative boundaries, VATI locations, BEAD locations, and public availability results into a unified address level database.

Records were standardized, geographically validated, deduplicated, and merged while preserving source attribution and funding provenance.

Addresses associated with multiple funding programs were consolidated into a single address level record while retaining source history and funding relationships.

Where multiple datasets referenced the same physical location, those relationships were preserved rather than discarded.

## Address Matching and Reconciliation

One of the most significant technical challenges involved reconciling multiple datasets that were created for different purposes.

Examples included:

* Multiple funding records associated with the same physical address
* Different address formatting conventions between datasets
* Rural route and roadway naming differences
* Funding records without complete address information
* Address numbering inconsistencies
* Geographic coordinate differences between source datasets
* Locations appearing in both VATI and BEAD datasets

Rather than selecting a preferred source and discarding alternatives, the project preserves funding provenance and source relationships whenever possible.

## County Boundary and Geographic Challenges

County assignment is not always straightforward.

Challenges encountered during processing included:

* Addresses located near county boundaries
* Postal city names that do not align with county borders
* Funding coordinates located near neighboring jurisdictions
* Different county assignments across source datasets
* Provider address suggestions associated with neighboring counties
* Geographic coordinate discrepancies between datasets

Because of these issues, county names alone were not considered sufficient for validation.

Spatial validation, geographic coordinates, county boundaries, and match distances were used together to evaluate records.

Where geographic conflicts occurred, those relationships were preserved for review rather than silently discarded.

## Availability Evaluation Method

Each address was evaluated through the public All Points Broadband service qualification workflow.

The objective was to determine whether an address appeared publicly orderable at the time of evaluation.

The analysis evaluates publicly observable availability results.

The analysis does not independently verify:

* Construction completion
* Fiber construction status
* Installation scheduling
* Subscriber activation
* Service installation
* Internal provider records
* Future deployment plans

Results should therefore be interpreted as a documented snapshot of publicly observable availability at the time of evaluation.

## Availability Classifications

The primary availability field is:

CURRENT_APB_RESULT

Possible values include:

yes

Address appeared publicly orderable.

no

Address did not appear publicly orderable.

unknown_no_suggestion

No address suggestion was returned.

unknown_bad_resolution

The address resolved to an apparently incorrect location.

unknown_error

A technical issue prevented evaluation.

not_checked

Evaluation was not completed.

Unknown and unresolved records are retained rather than reassigned through assumption.

## Quality Assurance

Multiple validation processes were used during dataset construction.

These included:

* County boundary validation
* Geographic coordinate validation
* Address normalization
* Duplicate detection
* Funding source reconciliation
* Match distance analysis
* Resolution validation
* Manual review of unusual geographic results

Rather than removing problematic records, unresolved records were preserved and classified separately.

The objective was to ensure that every funded location remained accounted for.

## Dataset Contents

The current dataset contains:

* Address information
* Geographic coordinates
* County assignments
* Funding associations
* VATI participation indicators
* BEAD participation indicators
* Source attribution
* Availability results
* Match quality information
* Validation fields
* Lookup provenance fields

## Important Fields

Frequently used fields include:

* ADDRESS
* CITY
* COUNTY
* STATE
* ZIP
* VGIN_LATITUDE
* VGIN_LONGITUDE
* CURRENT_APB_RESULT
* VATI_INCLUDED
* BEAD_INCLUDED
* FUNDING_CATEGORY
* SOURCE_PROGRAMS
* SOURCE_YEARS
* SOURCE_FILES
* MATCH_DISTANCE_FEET
* APB_LOOKUP_STATUS
* APB_MATCH_QUALITY
* APB_LOOKUP_TYPE
* APB_LOOKUP_TIMESTAMP

Field names are documented exactly as they appear in the dataset and are intentionally preserved without modification.

## Regional Summary

| Metric | Value |
|----------|----------:|
| Funded Addresses | 51,080 |
| Orderable | 9,172 |
| Not Orderable | 41,753 |
| Not Checked | 78 |
| Unknown No Suggestion | 45 |
| Unknown Bad Resolution | 30 |
| Unknown Error | 2 |
| Total Unresolved | 155 |
| Regional Orderable Rate | 18.01% |

## County Summary

| County | Funded Addresses | Orderable | Not Orderable | Unresolved | Orderable Rate |
|----------|----------:|----------:|----------:|----------:|----------:|
| Augusta | 8,252 | 4,444 | 3,806 | 2 | 53.85% |
| Clarke | 3,197 | 130 | 3,066 | 1 | 4.07% |
| Fauquier | 11,008 | 338 | 10,607 | 63 | 3.09% |
| Frederick | 8,312 | 411 | 7,897 | 4 | 4.95% |
| Page | 4,712 | 368 | 4,329 | 15 | 7.83% |
| Rappahannock | 2,505 | 721 | 1,781 | 3 | 28.81% |
| Rockingham | 10,181 | 2,669 | 7,505 | 7 | 26.23% |
| Warren | 2,913 | 91 | 2,762 | 60 | 3.19% |
| NSVRC Total | 51,080 | 9,172 | 41,753 | 155 | 18.01% |

## VATI Associated Summary

VATI associated locations include both VATI_ONLY and VATI_AND_BEAD records.

| County | VATI Associated Addresses | Orderable | Not Orderable | Unresolved | Orderable Rate |
|----------|----------:|----------:|----------:|----------:|----------:|
| Augusta | 4,779 | 4,210 | 568 | 1 | 88.11% |
| Clarke | 2,112 | 129 | 1,983 | 0 | 6.11% |
| Fauquier | 8,710 | 332 | 8,326 | 52 | 3.83% |
| Frederick | 3,954 | 398 | 3,556 | 0 | 10.07% |
| Page | 2,939 | 346 | 2,585 | 8 | 11.80% |
| Rappahannock | 712 | 344 | 368 | 0 | 48.31% |
| Rockingham | 5,798 | 2,500 | 3,297 | 1 | 43.13% |
| Warren | 1,164 | 87 | 1,055 | 22 | 7.62% |

## Public Use and Licensing

This repository is built from publicly available datasets and evaluates infrastructure associated with publicly funded broadband programs.

Consistent with the public nature of both the underlying data and the public funding involved, the datasets, methodology, documentation, and analysis contained within this repository are being released publicly for use by residents, journalists, researchers, local governments, and other interested parties.

See LICENSE for additional information.

## Version History

First Public Release

September 2026

Regional funded addresses:

51,080

Status classifications:

yes
no
unknown_no_suggestion
unknown_bad_resolution
unknown_error
not_checked

## Sources and References

Complete source documentation is available in SOURCES.md.
