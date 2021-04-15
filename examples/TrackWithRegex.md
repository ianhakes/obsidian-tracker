# Track Text with Regular Expression

**Important**!!
1. Use single quotes to wrap the regular expression, or use double quotes with all back slashes (escape characters) duplicated.
2. Make your own expression, or find a suitable one from website like [regex101](https://regex101.com).
3. Use a named group "(?\<value\>XXXXXX)" in your expression if you need values be retrieved from text.

## Count Occurencies (No Value)
### Occurencies of Email
[Regex for searching simple emails](https://regex101.com/library/mF3pK7)
``` tracker
searchType: text
searchTarget: '.+\@.+\..+'
folder: diary
startDate: 2021-01-01
endDate: 2021-01-31
line:
    title: Email Occurencies
    yAxisLabel: Count
    lineColor: yellow
```

``` tracker
searchType: text
searchTarget: '.+\@.+\..+'
folder: diary
startDate: 2021-01-01
endDate: 2021-01-31
summary:
    template: "Total number of emails found: {{sum}}"
    style: "font-size:20px;color:red;margin-left: 50px;margin-top:00px;"
```

## Count Values
### Weightlifting Tracker 
Track text in format "weightlifting: 10".
[Regex for searching value-attached texts](https://regex101.com/r/eCWpgS/2)
``` tracker
searchType: text
searchTarget: 'weightlifting: (?<value>[\-]?[0-9]+[\.][0-9]+|[\-]?[0-9]+)'
folder: diary
startDate: 2021-01-01
endDate: 2021-01-31
line:
    title: Weight Lifting
    yAxisLabel: Count
    lineColor: yellow
```

Please also check those search targets in markdown files under folder 'diary'.