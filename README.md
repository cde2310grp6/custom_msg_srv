# CDE2310 custom msgs and srvs
The following are the custom msgs and srvs created for use by the nodes detailed in the other repos.
I will admit, some of them were not quite an appropriate use for a custom msg type, as it was simply just a renaming of an existing msg type.
And it may have even hindered code readability rather than helped it.
The most effective custom message/service types we created was ```ArrayCasualtyPos.msg``` and ```StartCasualtyService.srv```

### ArrayCasualtyPos.msg
stores an array of PoseStamped message types.
used for comms of casualty location between casualty_locate and casualty_save
```
ArrayCasualtyPos.msg
geometry_msgs/PoseStamped[] casualties
```



### StartCasualtyService.srv
stores a string in the service request.
the string would contain info such as "SAVE" or "LOCATE" and is called by mission_control to either casualty_locate or casualty_save respectively.
```
StartCasualtyService.srv

string state
---
```


### CasualtyLocateStatus.msg
```
CasualtyLocateStatus.msg
bool all_casualties_found
```

### CasualtySaveStatus.msg
```
CasualtySaveStatus.msg
bool all_casualties_saved
```

### irRaw.msg
```
irRaw.msg
float64[] ir_data
```
(unused)

