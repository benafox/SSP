---
x-trestle-add-props: []
  # Add or modify control properties here
  # Properties may be at the control or part level
  # Add control level properties like this:
  #   - name: ac1_new_prop
  #     value: new property value
  #
  # Add properties to a statement part like this, where "b." is the label of the target statement part
  #   - name: ac1_new_prop
  #     value: new property value
  #     smt-part: b.
  #
x-trestle-set-params:
  # You may set values for parameters in the assembled SSP by adding
  #
  # ssp-values:
  #   - value 1
  #   - value 2
  #
  # below a section of values:
  # The values list refers to the values in the resolved profile catalog, and the ssp-values represent new values
  # to be placed in SetParameters of the SSP.
  #
  ac-02.13_odp.01:
    alt-identifier: ac-2.13_prm_1
    ssp-values:
    - one hour of discovery
    profile-param-value-origin: AC-2(13) implementation statement
  ac-02.13_odp.02:
    alt-identifier: ac-2.13_prm_2
    ssp-values:
    - employees under investigation, terminated for cause, or subject to a law-enforcement report
    profile-param-value-origin: AC-2(13) implementation statement
x-trestle-global:
  profile:
    title: IPS-SRS-001 Tailored Moderate Baseline (AC, AU, IR, CP)
    href: trestle://profiles/ips_srs_abridged/profile.json
  sort-id: ac-02.13
---

# ac-2.13 - \[Access Control\] Disable Accounts for High-risk Individuals

## Control Statement

Disable accounts of individuals within [time period] of discovery of [significant risks].

## Control Assessment Objective

accounts of individuals are disabled within [time period] of discovery of [significant risks].

## Control guidance

Users who pose a significant security and/or privacy risk include individuals for whom reliable evidence indicates either the intention to use authorized access to systems to cause harm or through whom adversaries will cause harm. Such harm includes adverse impacts to organizational operations, organizational assets, individuals, other organizations, or the Nation. Close coordination among system administrators, legal staff, human resource managers, and authorizing officials is essential when disabling system accounts for high-risk individuals.

______________________________________________________________________

## What is the solution and how is it implemented?

<!-- For implementation status enter one of: implemented, partial, planned, alternative, not-applicable -->

<!-- Note that the list of rules under ### Rules: is read-only and changes will not be captured after assembly to JSON -->

### This System

Within one hour of discovery accounts of individuals posing significant security risk will be disabled. The ISSO disables the account manually. Significant risk is identified as any account associated with an employee under investigation, termination for cause, or law-enforcement report. Risk determinations are made by HR through the organizational risk-assessment processes. The ISSO and the CISO are notified directly through email.

#### Implementation Status: implemented
