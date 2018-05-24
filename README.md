# search_generator
A generic Splunk search generator

A generic search load generation script will reach from a search_file setup with searches that should be run:

File Needs to be formatted with the following syntax specifically with the search to be run in square brackets

normal = ["earliest=-24h@h "INFO" index=_internal | stats count"]

sparse = ["earliest=-24h@h "WARN" index=_internal | stats count"]

dense = ["earliest=-24h@h "ERROR" index=_internal | stats count"]

supersparse = ["earliest=-24h@h "SUPER sparse!" index=_internal | stats count"]

The goal being to help with the even distribution of different kinds of searches for synthetic testing
