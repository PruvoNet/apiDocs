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

> Body

```json-doc
{
  "userRemarks": "adjacent rooms",
  "info": {
    "country": "ES",
    "phoneNumber": "+1-32-1234567",
    "firstName": "Bob",
    "lastName": "Saget"
  },
  "names": [
    [
      {
        "title": "M",
        "firstName": "john",
        "lastName": "smith"
      },
      {
        "title": "F",
        "firstName": "barbara",
        "lastName": "smith"
      },
      {
        "title": "C",
        "firstName": "sandy",
        "lastName": "smith",
        "age": 8
      }
    ],
    [
      {
        "title": "M",
        "firstName": "don",
        "lastName": "page"
      },
      {
        "title": "F",
        "firstName": "keren",
        "lastName": "page"
      },
      {
        "title": "C",
        "firstName": "mira",
        "lastName": "page",
        "age": 12
      }
    ]
  ]
}
```

The `personalInfo` object:

Name | Format | Description | Mandatory | Comments
---------- | ------- | ------- | ------- | ------- | ------- | -------
`userRemarks` | String | User provided requests to the hotel | Optional |
`info` | <a href="#common-personal-info-main-guest-info">Object</a> | main guest info  | True |
`names` | <a href="#common-personal-info-guest-general-info">Object[][]</a> | guests information (per room) | Optional |

### Main Guest info

> Body

```json-doc
{
  "country": "ES",
  "phoneNumber": "+1-32-1234567",
  "firstName": "Bob",
  "lastName": "Saget"
}
```

The `personalInfo.info` object:

Name | Format | Description | Mandatory | Comments
---------- | ------- | ------- | ------- | ------- | ------- | -------
`country` | <a href="https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes" target="_blank">ISO 3166-1 Alpha-2</a> String | guest nationality | Optional | Recommended for better results
`phoneNumber` | String | Guest phone number | Optional |
`firstName` | String | Guest first name | Optional |
`lastName` | String | Guest last name | Optional |

### Guest General Info

> Body

```json-doc
{
  "title": "C",
  "firstName": "mira",
  "lastName": "page",
  "age": 12
}
```

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
