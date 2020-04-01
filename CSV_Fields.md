## Field list

**REQUIRED fields are bolded.**

|*Col*|*Field (code)*|*Part*|*Description*|*Type*|
| --- | --- | --- | --- | --- |
|1|**patient_ontario_health_card_number**|1|Must be a valid OHCN.Must be 10 digits, followed by 2 letters, acceptable format: ####-###-###-AA (dashes optional)|String|
|2|patient_hospital_mrn|1|Specify the patient’s Medical Record Number for the hospital, if applicable.|String|
|3|**patient_firstname**|1|Max 50 chars|String|
|4|patient_middlename|1||String|
|5|**patient_lastname**|1||String|
|6|**patient_dateofbirth**|1||Date|
|7|**patient_gender**|1|Enter one of the genders listed, exactly as it appears in the Rules/Options column to the right.|One-of|
|8|**patient_mailing_street_number**|1|For addresses inside the City of Toronto, the address should be entered using these columns. Required, if the address is a city of Toronto Address.|String|
|9|**patient_mailing_street_name**|1||String|
|10|**patient_mailing_suite_number**|1||String|
|11|**patient_mailing_city**|1||String|
|12|**patient_mailing_province**|1||String|
|13|**patient_mailing_postal_code**|1||String|
|14|patient_mailing_country|1||String|
|15|patient_mailing_lat|1||String|
|16|patient_mailing_long|1||String|
|17|**full_address_text**|1|A free-form description for the address that can be used if an exact address is incomplete or not known. Required, if the patient has no fixed address or lives outside the city.|String|
|18|**patient_phone_number**|1|Required for fixed address patientsNot required if full_address_text is used|String|
|19|patient_email|1||String|
|20|**reported_date**|2|Date on which you are notifying TPH of this case. Format is yyyy-mm-dd|Date|
|21|**reporting_source**|2|Select the option which best describes you / your organization.|One-of|
|22|cpso_number|2|… of the reporting physician. Entered if “Physician Office” is specified as the reporting source.Only applies when reporting_source = “Physician Office”|String|
|23|reporting_source_other|2|If the reporting source does not match any of the drop-down list options, select “Other” and enter a short description of the reporting source in this column. Required if reporting_source = Other|String|
|24|reporting_organization|2|Enter the reporting_organization exactly as it appears in the Rules/Options column to the right.|One-of|
|25|reporting_organization_other|2|If the reporting organization is not in the drop-down list, then specify “Other” for reporting_organization and type the name of the organization in this column. Required if reporting_organization=Other|String|
|26|**person_making_the_report**|2|The name of the person reporting this case.|String|
|27|**reporting_phone_number**|2|Phone number of the person reporting this case.|String|
|28|reporting_phone_number_extension|2|Telephone extension, if any. Maximum 6 digits|String|
|29|**patient_symptoms**|3|Select all symptoms observed / reported by the patient.|One-or-More|
|30|patient_symptoms_other|3|If the patient reports a symptom not included in the list, then check “Other” and specify the symptom here. Required if patient_symptoms = “Other”|String|
|31|**patient_onset_date**|3|The earliest symptom onset date. Format yyyy-mm-dd|Date|
|32|**patient_exposures**|3|List all the ways the patient was exposed to the virus * enter them exactly as they appear in the Rules/Options column to the right.* Separate each option with a comma and * enclose the list in square brackets.e.g. [Was on a cruise ship,Travel to another country]|One-or-More|
|33|patient_exposures_other|3|If the patient was exposed to the virus in a manner other than specified in the patient_exposure options, then\\ \\* include “Other” in the patient_exposures list* specify the nature of the exposure here. Required if patient_exposures = “Other” |String|
|34|patient_travel_affected_area|3|If the patient traveled to an affected country (i.e. the countries specified in the Rules/Options column to the right), then:\\ \\* include “Travel to an affected country” in the patient_exposures list* specify the country here, exactly as they appear in the Rules/Options column to the right* if the country does not appear in this list, use the patient_travel_other column.<br>Required if patient_exposures = “Travel to an affected country” |One-of|
|35|patient_travel_other|3|If the patient traveled to a country not included in the patient_travel_affected_area list, then<br>* include “Travel to another country” in the patient_exposures_list<br>* specify the country here.<br>Required if patient_exposures = “Travel to another country”|String|
|36|**patient_specimens_collected**|3|If specimens were collected, then list them, exactly as they appear in the Rules/Options column to the right. Separate each option with a comma and enclose the list in square brackets.<br>e.g. [Throat Swab,Nasopharyngeal Swab] If no specimens were collected, then enter empty brackets []<br>Zero or more of the following:[“Throat Swab”, “Nasopharyngeal Swab”]|Array of Strings|
|37|patient_specimen_collection_date|3|The date on which the specimens were collected.<br>Format yyyy-mm-dd.<br>Must be entered if you specified one or more patient_specimens_collected|Date|
|38|**patient_hospital_told_patient_to_selfisolate**|3|labelled: “Healthcare Provider / Organization told patient to self-isolate”.<br>Options are:<br>yes<br>no<br>na|One-of|
|39|**patient_health_status**|3|Enter the current status of the patient exactly as it appears in the Rules/Options column to the right.|String|
|40|patient_health_status_other|3|If none of the options accurately describes the patient status, then enter “Other” as the patient_health_status and describe the status here.<br>If patient_health_status_other = “Other” → requiredIf patient_health_status_other != “Other” → ignored|String|
|41|comments|3|Any additional comments. Max Length 32767|String|

## Field multi-choice options

### 7. patient_gender 

1. Male
1. Female
1. Transgender
1. Other
1. Unknown

