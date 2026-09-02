# Virginia Publicly Funded Broadband Availability Dataset

## Overview

This repository contains a regional dataset of publicly funded broadband locations across Virginia along with supporting documentation, methodology, maps, and analysis.

The project combines multiple public datasets into a single address-level database and evaluates broadband availability using publicly accessible service qualification information.

The primary goals are transparency, reproducibility, and independent verification of publicly funded broadband deployment progress.

## Dataset Summary

The current dataset contains 51,080 publicly funded broadband locations.

Source programs include:

* Virginia Telecommunication Initiative (VATI) 2022
* Virginia Telecommunication Initiative (VATI) 2023
* Virginia Telecommunication Initiative (VATI) 2024
* Virginia Broadband Equity, Access, and Deployment (BEAD) locations

The analysis currently covers:

* Augusta County
* Clarke County
* Fauquier County
* Frederick County
* Page County
* Rappahannock County
* Rockingham County
* Warren County

## Data Sources

Virginia Geographic Information Network (VGIN)

https://vgin.vdem.virginia.gov

Virginia Office of Broadband

https://www.dhcd.virginia.gov/broadband

Virginia Broadband Availability Map

https://vast.virginia.gov

DHCD City and County Broadband Profiles

https://www.dhcd.virginia.gov/city-county-broadband-profiles

Northern Shenandoah Valley Regional Commission

https://www.nsvregion.org

Rappahannock Broadband Authority Project Resources

https://rappbroadband.org/about-the-project/

## Methodology

No single public dataset contained all funded locations.

The dataset was constructed by combining statewide address points, administrative boundaries, VATI locations, and BEAD locations into a unified address database.

Records were standardized, deduplicated, geographically validated, and merged while preserving source attribution and funding provenance.

Each address was evaluated using the public All Points Broadband ordering system and assigned an availability classification.

## Availability Classifications

The primary availability field is:

`CURRENT_APB_RESULT`

Possible values include:

| Value | Description |
|---------|---------|
| yes | Address appeared orderable |
| no | Address did not appear orderable |
| unknown_no_suggestion | No address suggestion returned |
| unknown_bad_resolution | Address resolved incorrectly |
| unknown_error | Technical error prevented evaluation |
| not_checked | Evaluation not yet completed |

Unknown and unresolved records are retained rather than discarded to preserve transparency.

## Example Fields

The dataset contains hundreds of fields. Commonly referenced fields include:

* ADDRESS
* CITY
* COUNTY
* STATE
* ZIP
* LATITUDE
* LONGITUDE
* FUNDING_TYPE
* SOURCE_DATASET
* VATI_INCLUDED
* BEAD_INCLUDED
* CURRENT_APB_RESULT
* APB_V2_RESULT
* APB_can_apb_service_address
* APB_lookup_status
* APB_match_quality
* APB_lookup_type
* APB_available_bundle_count
* APB_available_bundle_names
* APB_lookup_timestamp

## Data Quality

Several data quality challenges were encountered during construction:

* Duplicate locations appearing in multiple funding programs
* Inconsistent address formatting between source datasets
* Address normalization differences
* County assignment conflicts
* Incorrect address resolutions
* Addresses resolving outside the expected locality
* Unmatched or incomplete source records

Rather than removing problematic records, unresolved cases were preserved and classified separately.

## Limitations

This dataset reflects observations derived from public data sources and publicly accessible service qualification systems.

The dataset does not independently verify:

* Construction completion
* Fiber installation status
* Engineering completion
* Customer activation status
* Future deployment plans
* Internal provider records

Results should therefore be interpreted as a documented snapshot of publicly observable broadband availability at the time the evaluation was performed.

## Transparency

All findings originate from address-level records.

Unknown values remain classified as unknown.

Dataset versions are preserved.

Methodology changes are documented.

Source attribution is retained whenever possible.

The intent is to support independent review, validation, and further research by residents, journalists, researchers, local governments, and other stakeholders.
