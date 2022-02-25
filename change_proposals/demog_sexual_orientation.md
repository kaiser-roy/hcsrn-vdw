# Motivation

This proposal is for an enhancement to the _Demographics_ specification, which should enlarge the set of studies it is possible to do with the VDW.

# Proposed Change

We propose the addition of 3 new variables, all holding information on the indicated patient/member's Sexual Orientation.

|Variable Name|Definition|Type(Len)|Values|Implementation Guidelines|
|-------------|----------|---------|------|-------------------------|
|sexual_orientation[1-3]|One of the patient/member's responses to inquiry into their sexual orientation|char(1)|<dl><dt>B</dt><dd>Bisexual</dd><dt>T</dt><dd>Heterosexual</dd><dt>M</dt><dd>Homosexual</dd><dt>O</dt><dd>Other</dd><dt>D</dt><dd>Patient/member does not know</dd><dt>N</dt><dd>Choose not to disclose</dd><dt>U</dt><dd>Unknown (not asked/no information)</dd></dl>|<p>Null values not allowed.</p><p>Position does not signify temporal ordering, preference, or anything else--it is entirely arbitrary.</p><p>Compatible with both PHINVADS <a href="https://phinvads.cdc.gov/vads/ViewValueSet.action?id=E0004707-45BB-E711-ACE2-0017A477041A">PHVS_SexualOrientation_CDC</a> value set and LOINC code<a href="https://loinc.org/76690-7/">76690-7</a>.</p>|

# Notes

In our original survey of the then-new <abbr title="Sexual Orientation and Gender Identity">SOGI</abbr> data back in 2019, we were originally daunted by Epic Systems' EHR's design, which accomodates multiple values per person, but lacks any indication of e.g., which value was valid at which point in time, or which should be considered current. Because we sometimes see seemingly contradictory responses in raw data for individual patients (e.g., _Straight (not lesbian or gay)_ and _Gay_) it was (and remains) puzzling how these responses can be understood.

Since our 2019 effort to get a handle on SOGI data, we have come to realize that this information is worth adding even given the occasional ambiguous response.  The vast majority of responding patients give a single response.

Because of this ambiguity, we make **no** representation with respect to the ordering of values in the 3 `sexual_orientation` columns.  They may or may not represent an ordering in time of the patient/member's understanding of their orientation. They may or may not represent the patient's relative preference ranking of the orientation descriptions.

Like the rest of the SOGI data in _Demographics_, we expect these variables to be sparsely populated.

# Anticipated Impacts

## On Users

We expect generally positive impacts on users. Applications that will benefit from knowing a persons sexual orientation should be able to use the vast majority of non-missing responses. Other applications will be unaffected.

## On Implementers

Our sense is that the vast majority of information available in HCSRN Organizations' EHRs can be accomodated in this specification, with minimal difficulty.

There are some very small numbers of member/patients who have given more than 3 responses to this question, whose values must be truncated.  That seems a reasonable balance to strike against bloating the table with all or mostly null variables for the tiny proportion of people with more than three responses.

## On The Workgroup

We will need to revise the QA program to add checks and descriptives for the new fields.

# Request For Feedback

## For Scientific Users

1. How do you expect these changes to affect your current program of research?
2. How valuable is this information to you?
3. Are the new variables proposed:
    1. conceptually coherent?
    2. clearly defined?
    3. likely to be useful?

## For Implementers

1. Can you obtain the information needed for the new variables?
1. Do you have other useful, sexual-orientation-relevant information in your source data that would not be well accomodated by the proposed variables?
3. Are the new variables proposed
    1. conceptually coherent?
    1. clearly defined?
    1. likely to be useful?
3. Can you think of a better way of storing this data for research use?