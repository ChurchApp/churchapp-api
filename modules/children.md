# Children

[Home](https://github.com/ChurchSuite/churchsuite-api)

The Children module manages all children and youth within ChurchSuite. The following endpoints are available:

## List/search children

* `GET /v1/children/children will return contacts ordered alphabetically
* `GET /v1/children/children?q=sarah` will return contacts whose Name, Address, Email, Telephone, Mobile or Parent Name contains "sarah"
* `GET /v1/children/children?page=2 will return the second page of contacts
* `GET /v1/children/children?page=2&per_page=5 will return the second page of contacts, with each page limited to 5 results

```json
{
  "pagination":{
    "no_results":67,
    "page":1,
    "per_page":2
  },
  "children":[
    {
      "id":"727",
      "name":"Alexander, Becca",
      "first_name":"Becca",
      "last_name":"Alexander",
      "medical_short":"",
      "images": [
      ],
      "type_id":"child_727",
      "site_id":"1",
      "contact_id":null,
      "middle_name":null,
      "formal_name":null,
      "sex":"f",
      "date_of_birth":"2007-01-06",
      "mobile":"09778 787 97969",
      "email":"becca.alexander@gmail.com",
      "telephone":"0115 786 4001",
      "location":{
        "address":"73 Hyde Rise, Nottingham, NG1 1AD",
        "latitude":"52.9570736",
        "longitude":"-1.1527606"
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"",
      "medical":"",
      "special_needs":"",
      "doctor_details":"",
      "parent":{
        "additional_emails":[
          "david.alexander@yahoo.co.uk"
        ],
        "additional_mobiles":[
          "07345 928 726"
        ],
        "primary":{
          "contact_id":false,
          "first_name":"Gemma",
          "last_name":"& David Alexander",
          "sex":"u",
          "relationship":"Daughter",
          "email":"gemma.alexander@gmail.com",
          "mobile":"07775 354 829",
          "telephone":"0115 786 4001",
          "has_email_opt_out":false,
          "has_sms_opt_out":false
        }
      },
      "has_email_opt_out":false,
      "has_sms_opt_out":false
    },
    {
      "id":"765",
      "name":"Alexander, Emma",
      "first_name":"Emma",
      "last_name":"Alexander",
      "medical_short":"",
      "images": [
      ],
      "type_id":"child_765",
      "site_id":"1",
      "contact_id":"141",
      "middle_name":null,
      "formal_name":null,
      "sex":"f",
      "date_of_birth":"2016-05-15",
      "mobile":false,
      "email":"bunnyface@gmail.com",
      "telephone":"0115 786 4002",
      "location":{
        "address":"The Orchards, New Brunswick Avenue, Sherwood, Nottingham, Nottinghamshire, NG3 7EG, United Kingdom",
        "latitude":"52.9595798654589",
        "longitude":"-1.10891811271479"
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"",
      "medical":"",
      "special_needs":"",
      "doctor_details":"",
      "parent":{
        "additional_emails":[
          "test@test.com",
          "test2@test.com"
        ],
        "additional_mobiles":[
          "01234 578 945",
          "09876 543 991"
        ],
        "primary":{
          "contact_id":"141",
          "first_name":"Gemma",
          "last_name":"Alexander",
          "sex":"f",
          "relationship":"Daughter",
          "email":"gemma.alexander@gmail.com",
          "mobile":"07775 354 829",
          "telephone":"0115 786 4002",
          "has_email_opt_out":false,
          "has_sms_opt_out":false
        },
        "secondary":{
          "contact_id":"584",
          "first_name":"Peter",
          "last_name":"Alexander",
          "sex":"u",
          "relationship":"Daughter",
          "email":"pete.alexander123@yahoo.com",
          "mobile":"07973 374 632",
          "telephone":"0115 786 4002",
          "has_email_opt_out":false,
          "has_sms_opt_out":true
        }
      },
      "has_email_opt_out":false,
      "has_sms_opt_out":false
    }
  ]
}
```



## Get a child

* `GET /v1/children/child/1` will return data for a specific child
* `GET /v1/children/child/1?tags=true` will return data for a specific child, including any tags for the child
* `GET /v1/children/child/1?keydates=true` will return data for a specific child, including any key dates for the child

```json
{
  "id":"1",
  "name":"Wright, Micah",
  "first_name":"Micah",
  "last_name":"Wright",
  "medical_short":"",
  "images": [
  ],
  "type_id":"child_1",
  "site_id":"1",
  "contact_id":"2",
  "middle_name":null,
  "formal_name":null,
  "sex":"m",
  "date_of_birth":"2007-05-28",
  "mobile":false,
  "email":"",
  "telephone":"01062 438 661",
  "location":{
    "address":"24 Frederick Crescent, Wollaton, NG5 3DW",
    "latitude":"52.9847116296666",
    "longitude":"-1.15280494914181"
  },
  "consent":{
    "internal":"0",
    "external":"0"
  },
  "school":"Southam St James Primary School",
  "medical":"",
  "special_needs":"",
  "doctor_details":"Netherfield Medical Centre, 2a Forester Street, Netherfield, Nottingham, NG42NJ",
  "parent":{
    "additional_emails":[
      
    ],
    "additional_mobiles":[
      
    ],
    "primary":{
      "contact_id":"2",
      "first_name":"Paula",
      "last_name":"Wright",
      "sex":"f",
      "relationship":"Son",
      "email":"paula.wright@live.com",
      "mobile":"07369 801 623",
      "telephone":"01062 438 661",
      "has_email_opt_out":false,
      "has_sms_opt_out":false
    }
  },
  "has_email_opt_out":false,
  "has_sms_opt_out":false,
  "tags":[
    {
      "id": "1",
      "tag_id": "1",
      "name": "No photo-video consent",
      "description": "",
      "colour": "blue",
      "type": "smart",
      "no_children": 127,
      "tag_no_children": 127
    },
    {
      "id": "2",
      "tag_id": "2",
      "name": "Parents with emails",
      "description": "",
      "colour": "blue",
      "type": "smart",
      "no_children": 126,
      "tag_no_children": 126
    },
    {
      "id": "3",
      "tag_id": "3",
      "name": "Nativity Play - Christmas 2018",
      "description": "",
      "colour": "blue",
      "type": "fixed",
      "no_children": 22,
      "tag_no_children": 22
    }
  ],
  "keydates":[
    {
      "name":"Joined ministry",
      "date":"2016-02-05",
      "description":"Media team"
    },
    {
      "name":"Joined ministry",
      "date":"2016-03-16",
      "description":"Kids"
    }
  ]
}
```

This will return one of the following HTTP codes:

* `200` child data returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` child does not exist

## Get a child's tags

* `GET /v1/children/child/1/tags` will return data for a specific child

```json
{
  "tags":[
    {
      "id": "1",
      "tag_id": "1",
      "name": "No photo-video consent",
      "description": "",
      "colour": "blue",
      "type": "smart",
      "no_children": 127,
      "tag_no_children": 127
    },
    {
      "id": "2",
      "tag_id": "2",
      "name": "Parents with emails",
      "description": "",
      "colour": "blue",
      "type": "smart",
      "no_children": 126,
      "tag_no_children": 126
    },
    {
      "id": "3",
      "tag_id": "3",
      "name": "Nativity Play - Christmas 2018",
      "description": "",
      "colour": "blue",
      "type": "fixed",
      "no_children": 22,
      "tag_no_children": 22
    }
  ]
}
```

This will return one of the following HTTP codes:

* `200` child tags returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` child does not exist

## Get a child's key dates

* `GET /v1/children/child/1/keydates` will return data for a specific child

```json
{
  "keydates":[
    {
      "name":"Confirmation",
      "date":"2015-02-22"
    }
  ]
}
```

This will return one of the following HTTP codes:

* `200` child key dates returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` child does not exist

## Get a child's groups

* `GET /v1/children/child/1/groups` will return data for a specific child

```json
{
  "groups":[
    {
      "id":"4",
      "name":"Fusion",
      "gathering_id":"1",
      "checkin_badges_child":"0",
      "checkin_badges_pickup":"0",
      "checkin_badges_room":"0",
      "checkin_capacity":"15",
      "checkin_ratio":"0"
    },
    {
      "id":"71",
      "name":"Ignite",
      "gathering_id":"10",
      "checkin_badges_child":"1",
      "checkin_badges_pickup":"1",
      "checkin_badges_room":"0",
      "checkin_capacity":"0",
      "checkin_ratio":"0"
    }
  ]
}
```

This will return one of the following HTTP codes:

* `200` child groups returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` child does not exist

## Create a new child

* `POST /v1/children/child` will create a new child in the Address Book

```json
{
  "first_name":"Joe",
  "last_name":"Bloggs",
  "email":"joe@bloggs.com",
  "sex":"m",
  "date_of_birth":"2010-09-21"
}
```

This will return one of the following HTTP codes:

* `201` child created
* `400` some of the data passed through was not valid

This `POST` method returns output in the following format:

```json
{
  "id":"83",
  "contact_id":null,
  "name":"Bloggs, Joe",
  "first_name":"Joe",
  "last_name":"Bloggs",
  "sex":"m",
  "date_of_birth":"2010-09-21",
  "mobile":false,
  "email":"joe@bloggs.com",
  "telephone":"",
  "location":{
    "address":"",
    "latitude":null,
    "longitude":null
  },
  "consent":{
    "internal":"0",
    "external":"0"
  },
  "school":null,
  "medical":null,
  "medical_short":null,
  "special_needs":null,
  "doctor_details":null,
  "images":[
    
  ]
}
```

## Update an existing child's details

* `PUT /v1/children/child/1` will update the details of an existing child in the database

```json
{
  "first_name":"Jane",
  "last_name":"Bloggs",
  "email":"jane.bloggs@gmail.com",
  "sex":"f"
}
```

This will return one of the following HTTP codes:

* `200` child updated
* `400` some of the data passed through was not valid
* `404` child specified to update does not exist

This `PUT` method returns output in the following format:

```json
{
  "id":"83",
  "contact_id":null,
  "name":"Bloggs, Jane",
  "first_name":"Jane",
  "last_name":"Bloggs",
  "sex":"f",
  "date_of_birth":"2010-09-21",
  "mobile":false,
  "email":"jane.bloggs@gmail.com",
  "telephone":"",
  "location":{
    "address":"",
    "latitude":null,
    "longitude":null
  },
  "consent":{
    "internal":"0",
    "external":"0"
  },
  "school":null,
  "medical":null,
  "medical_short":null,
  "special_needs":null,
  "doctor_details":null,
  "images":[
    
  ]
}
```


## Delete a child

* `DELETE /v1/children/child/1` will attempt to delete the specified child

```json

```

This will return one of the following HTTP codes:

* `200` child deleted
* `404` child specified to delete does not exist
 

## List child gatherings

* `GET /v1/children/gatherings` will return data for all child gatherings

```json
{
  "gatherings":[
    {
      "id":"3",
      "name":"DK Groups",
      "groups":[
        {
          "id":"10",
          "name":"Junior",
          "gathering_id":"3",
          "checkin_labels":"1",
          "checkin_capacity":null,
          "checkin_ratio":null
        },
        {
          "id":"9",
          "name":"Senior",
          "gathering_id":"3",
          "checkin_labels":"1",
          "checkin_capacity":"0",
          "checkin_ratio":"0"
        }
      ]
    },
    {
      "id":"1",
      "name":"Sundays",
      "groups":[
        {
          "id":"1",
          "name":"Babies",
          "gathering_id":"1",
          "checkin_labels":"1",
          "checkin_capacity":"10",
          "checkin_ratio":"0"
        },
        {
          "id":"2",
          "name":"Tots",
          "gathering_id":"1",
          "checkin_labels":"1",
          "checkin_capacity":"10",
          "checkin_ratio":"0"
        },
        {
          "id":"3",
          "name":"Impact",
          "gathering_id":"1",
          "checkin_labels":"1",
          "checkin_capacity":"10",
          "checkin_ratio":"0"
        },
        {
          "id":"4",
          "name":"Fusion",
          "gathering_id":"1",
          "checkin_labels":"1",
          "checkin_capacity":"10",
          "checkin_ratio":"0"
        },
        {
          "id":"5",
          "name":"Cohesion",
          "gathering_id":"1",
          "checkin_labels":"1",
          "checkin_capacity":"10",
          "checkin_ratio":"0"
        },
        {
          "id":"11",
          "name":"Adult",
          "gathering_id":"1",
          "checkin_labels":"1",
          "checkin_capacity":"0",
          "checkin_ratio":"0"
        }
      ]
    }
  ]
}
```

## Get a child gathering

* `GET /v1/children/gathering/1` will return data for a specific child gathering

```json
{
  "id":"1",
  "name":"Sundays",
  "groups":[
    {
      "id":"1",
      "name":"Babies",
      "gathering_id":"1",
      "checkin_labels":"1",
      "checkin_capacity":"10",
      "checkin_ratio":"0"
    },
    {
      "id":"2",
      "name":"Tots",
      "gathering_id":"1",
      "checkin_labels":"1",
      "checkin_capacity":"10",
      "checkin_ratio":"0"
    },
    {
      "id":"3",
      "name":"Impact",
      "gathering_id":"1",
      "checkin_labels":"1",
      "checkin_capacity":"10",
      "checkin_ratio":"0"
    },
    {
      "id":"4",
      "name":"Fusion",
      "gathering_id":"1",
      "checkin_labels":"1",
      "checkin_capacity":"10",
      "checkin_ratio":"0"
    },
    {
      "id":"5",
      "name":"Cohesion",
      "gathering_id":"1",
      "checkin_labels":"1",
      "checkin_capacity":"10",
      "checkin_ratio":"0"
    },
    {
      "id":"11",
      "name":"Adult",
      "gathering_id":"1",
      "checkin_labels":"1",
      "checkin_capacity":"0",
      "checkin_ratio":"0"
    }
  ]
}
```

This will return one of the following HTTP codes:

* `200` gathering data returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` gathering does not exist

## Get a child group

* `GET /v1/children/group/1` will return data for a specific child group

```json
{
  "id":"1",
  "name":"Babies",
  "gathering_id":"1",
  "checkin_labels":"1",
  "checkin_capacity":"10",
  "checkin_ratio":"0"
}
```

This will return one of the following HTTP codes:

* `200` group data returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` group does not exist

## Get the attendance data for a child group

* `GET /v1/children/group/1/attendance` will return data for the attendance of a specific child group

```json
{
  "2014-07-17":{
    "0":null,
    "1":"58",
    "total":2
  },
  "2014-07-18":{
    "0":null,
    "1":"58",
    "total":2
  },
  "2014-07-21":{
    "0":"58",
    "total":1
  },
  "2014-07-22":{
    "0":"58",
    "total":1
  },
  "2014-07-29":{
    "0":null,
    "total":1
  },
  "2014-08-08":{
    "0":null,
    "1":null,
    "total":2
  },
  "2014-08-11":{
    "0":null,
    "total":1
  },
  "2014-08-26":{
    "0":null,
    "total":1
  },
  "2014-09-03":{
    "0":null,
    "total":1
  },
  "2014-09-23":{
    "0":"60",
    "1":"66",
    "2":"67",
    "3":"68",
    "total":4
  },
  "2014-10-02":{
    "0":null,
    "1":null,
    "2":"67",
    "total":3
  },
  "2014-10-03":{
    "0":null,
    "1":null,
    "2":null,
    "3":null,
    "total":4
  }
}
```

This will return one of the following HTTP codes:

* `200` group attendance data returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` group does not exist

## Get children in a child group

* `GET /v1/children/group/1/children` will return data for the children in a specific child group

```json
{
  "children":[
    {
      "id":"67",
      "contact_id":"141",
      "name":"Alexander, Emma",
      "first_name":"Emma",
      "last_name":"Alexander",
      "sex":"f",
      "date_of_birth":"2014-01-08",
      "mobile":false,
      "email":"",
      "telephone":"0115 786 4001",
      "location":{
        "address":"",
        "latitude":null,
        "longitude":null
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"",
      "medical":"",
      "medical_short":"",
      "special_needs":"",
      "doctor_details":"",
      "images":[
        
      ]
    },
    {
      "id":"66",
      "contact_id":"65",
      "name":"Marshall, Peter",
      "first_name":"Peter",
      "last_name":"Marshall",
      "sex":"m",
      "date_of_birth":"2014-05-01",
      "mobile":false,
      "email":"",
      "telephone":"01459 409 330",
      "location":{
        "address":"",
        "latitude":null,
        "longitude":null
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"",
      "medical":"",
      "medical_short":"",
      "special_needs":"",
      "doctor_details":"",
      "images":[
        
      ]
    }
  ]
}
```

This will return one of the following HTTP codes:

* `200` group children data returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` group does not exist


## List tags

* `GET /v1/children/tags` will return tags ordered alphabetically

```json
{
  "pagination":{
    "no_results":14,
    "page":1,
    "per_page":14
  },
  "tags":[
  {
      "id": "1439",
      "tag_id": "1439",
      "name": "Age Under 1",
      "description": "",
      "colour": "blue",
      "type": "smart",
      "no_children": 2,
      "tag_no_children": 2
  },
  {
      "id": "1438",
      "tag_id": "1438",
      "name": "All Children",
      "description": "",
      "colour": "blue",
      "type": "smart",
      "no_children": 161,
      "tag_no_children": 161
  },
  {
      "id": "1442",
      "tag_id": "1442",
      "name": "Children 11-18",
      "description": "",
      "colour": "blue",
      "type": "smart",
      "no_children": 59,
      "tag_no_children": 59
  },
  {
      "id": "1417",
      "tag_id": "1417",
      "name": "Consent Outstanding",
      "description": null,
      "colour": "blue",
      "type": "fixed",
      "no_children": 1,
      "tag_no_children": 1
  },
  {
      "id": "896",
      "tag_id": "896",
      "name": "Consent: Granted",
      "description": "",
      "colour": "green",
      "type": "smart",
      "no_children": 11,
      "tag_no_children": 11
  },
  {
      "id": "897",
      "tag_id": "897",
      "name": "Consent: Outstanding",
      "description": "",
      "colour": "red",
      "type": "smart",
      "no_children": 150,
      "tag_no_children": 150
  },
  {
      "id": "26",
      "tag_id": "26",
      "name": "Easter Holiday Club 2019",
      "description": "",
      "colour": "grey",
      "type": "fixed",
      "no_children": 12,
      "tag_no_children": 12
  },
  {
      "id": "1283",
      "tag_id": "1283",
      "name": "Family Fun Day Invites",
      "description": "",
      "colour": "blue",
      "type": "fixed",
      "no_children": 14,
      "tag_no_children": 14
  }
  ]
}
```


## Get a tag

* `GET /v1/children/tag/1` will return data for a specific tag with the ID of 1
* `GET /v1/children/tag/Dance+Team` will return data for a specific tag
* `GET /v1/children/tag/Dance+Team?children=true` will return data for a specific tag, including all children with the tag

Tag names *must be urlencoded*, particularly if they include a space character in them. Failure to correctly encode the tag name could result in a 404 response being returned rather than a 200.

```json
{
  "id": "1283",
  "tag_id": "1283",
  "name": "Family Fun Day Invites",
  "description": "",
  "colour": "blue",
  "type": "fixed",
  "no_children": 14,
  "tag_no_children": 14
}
```

This will return one of the following HTTP codes:

* `200` tag data returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` tag does not exist

## Get a tag's children

* `GET /v1/children/tag/1/children` will return the children for the tag with the ID of 1
* `GET /v1/children/tag/Dance+Team/children` will return the children for the "Dance Team" tag

```json
{
  "pagination":{
    "no_results":6,
    "page":1,
    "per_page":6
  },
  "children":[
    {
      "id":"38",
      "name":"Carter, Naomi",
      "first_name":"Naomi",
      "last_name":"Carter",
      "medical_short":"",
      "images":[
        
      ],
      "contact_id":null,
      "middle_name":null,
      "formal_name":null,
      "sex":"f",
      "date_of_birth":"2005-06-20",
      "mobile":false,
      "email":"",
      "telephone":"01000 083 559",
      "location":{
        "address":"",
        "latitude":null,
        "longitude":null
      },
      "consent":{
        "internal":"0",
        "external":"1"
      },
      "school":"Canon Maggs Junior School",
      "medical":"",
      "special_needs":"",
      "doctor_details":"The Linden Medical Group, Stapleford Care Centre, Church Street, Stapleford, Nottingham, NG98DA"
    },
    {
      "id":"32",
      "name":"Cox, Jackie",
      "first_name":"Jackie",
      "last_name":"Cox",
      "medical_short":"",
      "images":[
        
      ],
      "contact_id":"99",
      "middle_name":null,
      "formal_name":null,
      "sex":"f",
      "date_of_birth":"2000-10-24",
      "mobile":false,
      "email":"",
      "telephone":"01584 395 699",
      "location":{
        "address":"63 Dale Avenue, Sherwood, NG9 6AL",
        "latitude":null,
        "longitude":null
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"Bilton Junior School",
      "medical":"Gluten free",
      "special_needs":"",
      "doctor_details":"Chilwell Meadows Surgery, Ransom Road, Chilwell, Nottingham, NG96DX"
    },
    {
      "id":"22",
      "name":"Day, Julie",
      "first_name":"Julie",
      "last_name":"Day",
      "medical_short":null,
      "images":[
        
      ],
      "contact_id":"69",
      "middle_name":null,
      "formal_name":null,
      "sex":"f",
      "date_of_birth":"1995-11-11",
      "mobile":"07841 478 483",
      "email":"julie.day@sky.com",
      "telephone":"01692 170 889",
      "location":{
        "address":"4 Dovecote Court, Beeston, NG8 1NJ",
        "latitude":null,
        "longitude":null
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"Cubbington Primary School",
      "medical":"",
      "special_needs":"",
      "doctor_details":"St John Street, Mansfield, Nottinghamshire, NG181RH"
    },
    {
      "id":"5",
      "name":"Day, Ruth",
      "first_name":"Ruth",
      "last_name":"Day",
      "medical_short":null,
      "images":[
        
      ],
      "contact_id":"12",
      "middle_name":null,
      "formal_name":null,
      "sex":"f",
      "date_of_birth":"1994-11-02",
      "mobile":"07197 867 555",
      "email":"ruth.day@facebook.com",
      "telephone":"01098 599 657",
      "location":{
        "address":"2 Violet Close, Gedling, NG10 3DX",
        "latitude":null,
        "longitude":null
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"Shottery Primary School",
      "medical":null,
      "special_needs":null,
      "doctor_details":"Belvoir Health Group, Health Centre, Candleby Lane, Cotgrave, NG123JG"
    },
    {
      "id":"18",
      "name":"Day, Ruth",
      "first_name":"Ruth",
      "last_name":"Day",
      "medical_short":"",
      "images":[
        
      ],
      "contact_id":"51",
      "middle_name":null,
      "formal_name":null,
      "sex":"f",
      "date_of_birth":"2002-08-21",
      "mobile":false,
      "email":"",
      "telephone":"01909 353 098",
      "location":{
        "address":"23 Saxon Crescent, Gedling, NG1 4FW",
        "latitude":null,
        "longitude":null
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"Harris School and Sports College",
      "medical":"",
      "special_needs":"",
      "doctor_details":"The Surgery, 112 Watnall Road, Hucknall, Nottingham, NG157JP"
    },
    {
      "id":"19",
      "name":"Gretton, Tracey",
      "first_name":"Tracey",
      "last_name":"Gretton",
      "medical_short":"",
      "images":[
        
      ],
      "contact_id":"58",
      "middle_name":null,
      "formal_name":null,
      "sex":"f",
      "date_of_birth":"2000-09-27",
      "mobile":false,
      "email":"",
      "telephone":"01998 793 321",
      "location":{
        "address":"74 Conway Street, The Meadows, NG5 8JS",
        "latitude":null,
        "longitude":null
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"Foleshill Primary School",
      "medical":"",
      "special_needs":"",
      "doctor_details":"St John Street, Mansfield, Nottinghamshire, NG181RH"
    }
  ]
}
```

This will return one of the following HTTP codes:

* `200` tag children returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` tag does not exist


## List key dates

* `GET /v1/children/keydates` will return key dates ordered alphabetically

```json
{
  "pagination":{
    "no_results":3,
    "page":1,
    "per_page":3
  },
  "keydates":[
    {
      "name":"Confirmation",
      "no_children":"2"
    },
    {
      "name":"Dedicated",
      "no_children":"1"
    },
    {
      "name":"First kids groups attendance",
      "no_children":"0"
    }
  ]
}
```


## Get a key date

* `GET /v1/children/keydate/Confirmation` will return data for a specific key date
* `GET /v1/children/keydate/Confirmation?children=true` will return data for a specific key date, including all children with the key date

Key date names *must be urlencoded*, particularly if they include a space character in them. Failure to correctly encode the key date name could result in a 404 response being returned rather than a 200.

```json
{
  "name":"Confirmation",
  "no_children":"2"
}
```

This will return one of the following HTTP codes:

* `200` key date data returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` key date does not exist

## Get a key date's children

* `GET /v1/children/keydate/Confirmation/children` will return the children for the "Confirmation" key date

```json
{
  "pagination":{
    "no_results":2,
    "page":1,
    "per_page":2
  },
  "children":[
    {
      "id":"59",
      "name":"Baker, Amelia",
      "first_name":"Amelia",
      "last_name":"Baker",
      "medical_short":"",
      "images":[
        
      ],
      "contact_id":"112",
      "middle_name":null,
      "formal_name":null,
      "sex":"f",
      "date_of_birth":"2003-08-07",
      "mobile":"0886 775 2234",
      "email":"",
      "telephone":"0115 123 4567",
      "location":{
        "address":"44 Pruder Street, Thorpe, Nottingham, Nottinghamshire, NG9 2FE, United Kingdom",
        "latitude":null,
        "longitude":null
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"Camberwick Green Secondary School",
      "medical":"",
      "special_needs":"",
      "doctor_details":"",
      "keydates":[
        {
          "name":"Confirmation",
          "date":"2014-09-18"
        }
      ]
    },
    {
      "id":"1",
      "name":"Wright, Micah",
      "first_name":"Micah",
      "last_name":"Wright",
      "medical_short":"",
      "images":[
        
      ],
      "contact_id":"2",
      "middle_name":null,
      "formal_name":null,
      "sex":"m",
      "date_of_birth":"2007-05-28",
      "mobile":false,
      "email":"",
      "telephone":"01062 438 661",
      "location":{
        "address":"24 Frederick Crescent, Wollaton, NG5 3DW",
        "latitude":null,
        "longitude":null
      },
      "consent":{
        "internal":"0",
        "external":"0"
      },
      "school":"Southam St James Primary School",
      "medical":"",
      "special_needs":"",
      "doctor_details":"Netherfield Medical Centre, 2a Forester Street, Netherfield, Nottingham, NG42NJ",
      "keydates":[
        {
          "name":"Confirmation",
          "date":"2015-02-22"
        }
      ]
    }
  ]
}
```

This will return one of the following HTTP codes:

* `200` key date children returned
* `400` some of the data passed through was not valid, e.g. invalid URL
* `404` key date does not exist

