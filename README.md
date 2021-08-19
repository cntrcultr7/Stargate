# healthrecords


---
### Short description

Logs every event associated with the creation of an "Episode" (ep) in Electronic Health Records (EHR) in SaaS.
(1) User can create an ep. associated with a booking or outside of a booking
(2) User can create + edit eps. on both mobile app & desktop

*An ep. can be imported, need to account for this distinction b/t episodes created in saas.
*IF an ep. created outside of booking THEN eventid IS NULL


---
### Columns
- **Id** (int)<br>
PK. Unique id per episode<br>
- Date (datetime)<br>

- **Status** (0 / 1 / 2)<br>
0 = Draft (mobile only)
1 = Saved (default value for desktop regardless if save button actively saved)<br>
2 = Deleted<br>
*Draft logic deprecated in desktop and is live in mobile (as of 13-08-2021)*<br>
- **EventId** (int)<br>
Id of booking if episode created from booking origin.<br>
- **UserId** (int)<br>
Id of user who created episode<br>
- **Comments** (string)<br>
[Deprecated] Old feature logic (as of 13-08-2021)<br>
- **Diagnosis** (string)<br>
[Deprecated] Old feature logic (as of 13-08-2021)<br>
- **Medication** (string)<br>
[Deprecated] Old feature logic (as of 13-08-2021)<br>
- **PatientId** (int)<br>
ID of patient episode is linked to.<br>

---
### Owner/contact person
product analytics
