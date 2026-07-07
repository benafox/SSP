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
  ac-02.02_odp.01:
    alt-identifier: ac-2.2_prm_1
    ssp-values:
    - disable
    profile-param-value-origin: AC-2(2) implementation statement
  ac-02.02_odp.02:
    alt-identifier: ac-2.2_prm_2
    ssp-values:
    - 96 hours
    profile-param-value-origin: AC-2(2) implementation statement
x-trestle-global:
  profile:
    title: IPS-SRS-001 Tailored Moderate Baseline (AC, AU, IR, CP)
    href: trestle://profiles/ips_srs_abridged/profile.json
  sort-id: ac-02.02
---

# ac-2.2 - \[Access Control\] Automated Temporary and Emergency Account Management

## Control Statement

Automatically [Selection: remove; disable] temporary and emergency accounts after [time period].

## Control Assessment Objective

temporary and emergency accounts are automatically [Selection: remove; disable] after [time period].

## Control guidance

Management of temporary and emergency accounts includes the removal or disabling of such accounts automatically after a predefined time period rather than at the convenience of the system administrator. Automatic removal or disabling of accounts provides a more consistent implementation.

______________________________________________________________________

## What is the solution and how is it implemented?

<!-- For implementation status enter one of: implemented, partial, planned, alternative, not-applicable -->

<!-- Note that the list of rules under ### Rules: is read-only and changes will not be captured after assembly to JSON -->

### This System

In an emergency situation like AWS/District IdP provider going down an emergency account may be provisioned. Any emergency account is automatically disabled after a period of 96 hours from creation.

Temporary accounts are not used in this system. The baseline control implements an 8 hour interval for account creation, modification, and termination that would be documented through HR and used for short-duration staff like a substitute school administrator or teacher.

#### Implementation Status: implemented
