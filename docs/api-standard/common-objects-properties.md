# Common Objects/Properties

{% table %}

- name
- format
- example

---

- countries
- - Apply ISO 3166-1 alpha-2
- FR

---

- date-time
- - Apply ISO8601<br /> - Always UTC time
- 2017-07-21T17:32:28Z

---

- phone number
- - Country code with '+' sign (+33 for example) <br /> - Number with potential spaces, hyphens or trailing zero(s)
- {<br />    "country_code": "+44",<br />    "number": "1234 567890"<br /> }

{% /table %}
