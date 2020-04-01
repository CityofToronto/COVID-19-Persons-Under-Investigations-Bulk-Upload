|*Col*|*Field (code)*|*Part*|*Description*|*Type*|*Rules / Options*|
| --- | --- |--- |--- |--- |--- |
|1|patient_ontario_health_card_number|1||String|REQUIRED<br> - Must be a valid OHCN.  <br>Must be 10 digits, followed by 2 letters, acceptable format: <br>####-###-###-AA (dashes optional)|
|2|patient_hospital_mrn|1|Specify the patient’s Medical Record Number for the hospital, if applicable.|String||
|3|patient_firstname|1||String|REQUIRED - Max 50 chars|
|4|patient_middlename|1||String||
|5|patient_lastname|1||String|REQUIRED|
|6|patient_dateofbirth|1||Date|REQUIRED - Format yyyy-mm-dd|
|7|patient_gender|1|Enter one of the genders listed, exactly as it appears in the Rules/Options column to the right.|One-of|REQUIRED\\ \\<br>* Male<br>* Female<br>* Transgender<br>* Other<br>* Unknown|
|8|patient_mailing_street_number|1|For addresses inside the City of Toronto, the address should be entered using these columns.|String|Required, if the address is a city of Toronto Address.|
|9|patient_mailing_street_name|1||String|Required, if the address is a city of Toronto Address.|
|10|patient_mailing_suite_number|1||String|Optional. Used if the address is a city of Toronto Address.|
|11|patient_mailing_city|1||String|Required, if the address is a city of Toronto Address.|
|12|patient_mailing_province|1||String|Required, if the address is a city of Toronto Address.|
|13|patient_mailing_postal_code|1||String|Required, if the address is a city of Toronto Address.|
|14|patient_mailing_country|1||String|Optional. Used if the address is a city of Toronto Address.|
|15|patient_mailing_lat|1||String||
|16|patient_mailing_long|1||String||
|17|full_address_text|1|A free-form description for the address that can be used if an exact address is incomplete or not known.|String|Required, if the patient has no fixed address or lives outside the city|
|18|patient_phone_number|1||String|Required for fixed address patients\\
Not required if nofixedaddress_option_text is used|
|19|patient_email|1||String||
|20|reported_date|2|Date on which you are notifying TPH of this case.|Date|REQUIRED - Format yyyy-mm-dd|
|21|reporting_source|2|Select the option which best describes you / your organization.|One-of|REQUIRED\\ \\
<br>* Hospital physician / Infection Prevention and Control
<br>* Assessment Centre
<br>* Physician Office
<br>* Other|
|22|cpso_number|2|… of the reporting physician. Entered if “Physician Office” is specified as the reporting source.|String|_Checking on conditions_. Only applies when reporting_source = “Physician Office”|
|23|reporting_source_other|2|If the reporting source does not match any of the drop-down list options, select “Other” and enter a short description of the reporting source in this column.|String|Required if reporting_source = Other|
|24|reporting_organization|2|Enter the reporting_organization exactly as it appears in the Rules/Options column to the right.|One-of|REQUIRED\\ \\<br>* Hospital for Sick Children<br>* Humber River Hospital<br>* Michael Garron Hospital<br>* Mount Sinai Hospital<br>* North York General Hospital<br>* Scarborough Health Network-Birchmount Hospital<br>* Scarborough Health Network-Centenary Hospital<br>* Scarborough Health Network-General Hospital<br>* St. Joseph's Health Centre<br>* St. Michael's Hospital<br>* Sunnybrook Health Sciences Centre<br>* Trillium Health Partners<br>* UHN-Princess Margaret Hospital<br>* UHN-Toronto Western Hospital<br>* UHN-Toronto General Hospital<br>* William Osler Health System<br>* Other|
|25|reporting_organization_other|2|If the reporting organization is not in the drop-down list, then specify “Other” for reporting_organization and type the name of the organization in this column.|String|Required if reporting_organization=Other|
|26|person_making_the_report|2|The name of the person reporting this case.|String|REQUIRED|
|27|reporting_phone_number|2|Phone number of the person reporting this case.|String|REQUIRED|
|28|reporting_phone_number_extension|2|Telephone extension, if any.|String|Maximum 6 digits|
|29|patient_symptoms|3|Select all symptoms observed / reported by the patient.|One-or-More|REQUIRED<br>* Fever<br>* Difficulty Breathing/SOB<br>* Cough<br>* Fatigue<br>* Headache<br>* Sore Throat<br>* Other|
|30|patient_symptoms_other|3|If the patient reports a symptom not included in the list, then check “Other” and specify the symptom here.|String|Required if patient_symptoms = “Other”|
|31|patient_onset_date|3|The earliest symptom onset date.|Date|REQUIRED - Format yyyy-mm-dd|
|32|patient_exposures|3|List all the ways the patient was exposed to the virus\\ \\
<br>* enter them exactly as they appear in the Rules/Options column to the right.
<br>* Separate each option with a comma and
<br>* enclose the list in square brackets.
e.g. [Was on a cruise ship,Travel to another country]|One-or-More|REQUIRED\\ \\
<br>* Travel to an affected country
<br>* Travel to another country
<br>* Was on a cruise ship
<br>* Have close contact with a confirmed or probable case of COVID-19
<br>* Have close contact with a person with acute respiratory illness who has been to an affected area* within 14 days prior to their illness onset
<br>* Have laboratory exposure to biological material (e.g.primary clinical specimens, virus culture isolates) known to contain COVID-19
<br>* Other|
|33|patient_exposures_other|3|If the patient was exposed to the virus in a manner other than specified in the patient_exposure options, then\\ \\
<br>* include “Other” in the patient_exposures list
<br>* specify the nature of the exposure here.|String|Required if patient_exposures = “Other”|
|34|patient_travel_affected_area|3|If the patient traveled to an affected country (i.e. the countries specified in the Rules/Options column to the right), then:<br>* include “Travel to an affected country” in the patient_exposures list<br>* specify the country here, exactly as they appear in the Rules/Options column to the right<br>* if the country does not appear in this list, use the patient_travel_other column|One-of|Required if patient_exposures = “Travel to an affected country”\\<br>* China<br>* Iran<br>* Italy<br>* South Korea<br>* USA|
|35|patient_travel_other|3|If the patient traveled to a country not included in the patient_travel_affected_area list, then\\ \\
<br>* include “Travel to another country” in the patient_exposures_list
<br>* specify the country here.|String|Required if patient_exposures = “Travel to another country”|
|36|patient_specimens_collected|3|If specimens were collected, then list them, exactly as they appear in the Rules/Options column to the right. Separate each option with a comma and enclose the list in square brackets.\\ \\
e.g. [Throat Swab,Nasopharyngeal Swab]\\ \\
If no specimens were collected, then enter empty brackets []|Array of Strings|Zero or more of the following:\\
[“Throat Swab”, “Nasopharyngeal Swab”]|
|37|patient_specimen_collection_date|3|The date on which the specimens were collected.|Date|* Format yyyy-mm-dd
<br>* Must be entered if you specified one or more patient_specimens_collected|
|38|patient_hospital_told_patient_to_selfisolate|3|labelled: “Healthcare Provider / Organization told patient to self-isolate”|One-of|REQUIRED\\ \\
<br>* yes
<br>* no
<br>* na|
|39|patient_health_status|3|Enter the current status of the patient exactly as it appears in the Rules/Options column to the right.|String|REQUIRED\\ \\
<br>* Hospitalized, non-ICU (connect with Infection Prevention & Control to ensure appropriate precautions are in place)
<br>* Admitted to ICU (connect with Infection Prevention & Control to ensure appropriate precautions are in place)
<br>* ED Visit only and discharged
<br>* Currently in the ED (if being discharged please advise to self isolate)
<br>* Deceased|
|40|patient_health_status_other|3|If none of the options accurately describes the patient status, then enter “Other” as the patient_health_status and describe the status here.|String|If patient_health_status_other = “Other” → required\\
If patient_health_status_other != “Other” → ignored|
|41|comments|3|Any additional comments|String|Max Length 32|
