# Common

This section describes commonly accepted parameters, formats and structures which are used later in individual endpoints overviews.

## Meal Plans

The `mealPlan` valid enum values are:

 Value | Description
---------- | ------- 
0 | no meal plan
1 | breakfast
2 | half board
3 | all inclusive
4 | full board

## Personal Info

The `personalInfo` object:

Name | Format | Description | Mandatory | Comments
---------- | ------- | ------- | ------- | ------- | ------- | -------
`userRemarks` | String | User provided requests to the hotel | Optional |
`names` | <a href="#common-personal-info-guest-general-info">Object[][]</a> | guests information (per room) | Optional |
`info` | <a href="#common-personal-info-main-guest-info">Object</a> | main guest info  | True |

### Main Guest info

The `personalInfo.info` object:

Name | Format | Description | Mandatory | Comments
---------- | ------- | ------- | ------- | ------- | ------- | -------
`country` | <a href="https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes" target="_blank">ISO 3166-1 Alpha-2</a> String | guest nationality | Optional | Recommended for better results
`phoneNumber` | String | Guest phone number | Optional |
`firstName` | String | Guest first name | Optional |
`lastName` | String | Guest last name | Optional |

### Guest GeneralIinfo

The `personalInfo.names` object:

Name | Format | Description | Mandatory | Comments
---------- | ------- | ------- | ------- | ------- | ------- | -------
`title` | <a href="#common-personal-info-guest-title">Enum</a> | guest sex | True |
`age` | Number | Guest age | Optional | Must be provided if guest is a child (under 18)
`firstName` | String | Guest first name | True |
`lastName` | String | Guest last name | True |

### Guest Title

The `personalInfo.names.title` object:

 Value | Description
---------- | ------- 
M | Male
F | Female
C | Child
