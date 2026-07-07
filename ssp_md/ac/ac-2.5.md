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
  ac-02.05_odp:
    alt-identifier: ac-2.5_prm_1
    ssp-values:
    - 15 minutes of inactivity (5 minutes for privileged sessions)
    profile-param-value-origin: AC-2(5) implementation statement
x-trestle-global:
  profile:
    title: IPS-SRS-001 Tailored Moderate Baseline (AC, AU, IR, CP)
    href: trestle://profiles/ips_srs_abridged/profile.json
  sort-id: ac-02.05
---

# ac-2.5 - \[Access Control\] Inactivity Logout

## Control Statement

Require that users log out when [time period of expected inactivity or description of when to log out].

## Control Assessment Objective

users are required to log out when [time period of expected inactivity or description of when to log out].

## Control guidance

Inactivity logout is behavior- or policy-based and requires users to take physical action to log out when they are expecting inactivity longer than the defined period. Automatic enforcement of inactivity logout is addressed by [AC-11](#ac-11).

______________________________________________________________________

## What is the solution and how is it implemented?

<!-- For implementation status enter one of: implemented, partial, planned, alternative, not-applicable -->

<!-- Note that the list of rules under ### Rules: is read-only and changes will not be captured after assembly to JSON -->

### This System

Users are required to log out when expecting to have an inactivity period of 15 minutes or more. Privileged session users are expected to log out whenever they are expecting a period of inactivity of 5 minutes or longer. Automatic enforcement is detailed in AC-12.

#### Implementation Status: implemented
