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
  ac-6.1_prm_2:
    aggregates:
    - ac-06.01_odp.02
    - ac-06.01_odp.03
    - ac-06.01_odp.04
  ac-06.01_odp.01:
    alt-identifier: ac-6.1_prm_1
    ssp-values:
    - the ISSO and system administrators
    profile-param-value-origin: AC-6(1) implementation statement
  ac-06.01_odp.02:
    ssp-values:
    - patch deployment, firewall rule changes, security group rule changes, security service configuration, and access control list modification
    profile-param-value-origin: AC-6(1) implementation statement
  ac-06.01_odp.03:
    ssp-values:
    - audit and log data review, access compliance review, and emergency account deactivation
    profile-param-value-origin: AC-6(1) implementation statement
  ac-06.01_odp.04:
    ssp-values:
    - the ISSO and system administrators
    profile-param-value-origin: AC-6(1) implementation statement
  ac-06.01_odp.05:
    alt-identifier: ac-6.1_prm_3
    ssp-values:
    - audit logs, access compliance data, and security service configuration
    profile-param-value-origin: AC-6(1) implementation statement
x-trestle-global:
  profile:
    title: IPS-SRS-001 Tailored Moderate Baseline (AC, AU, IR, CP)
    href: trestle://profiles/ips_srs_abridged/profile.json
  sort-id: ac-06.01
---

# ac-6.1 - \[Access Control\] Authorize Access to Security Functions

## Control Statement

Authorize access for [individuals and roles] to:

- \[(a)\] [organization-defined security functions (deployed in hardware, software, and firmware)] ; and

- \[(b)\] [security-relevant information].

## Control Assessment Objective

- \[AC-06(01)(a)\]

  - \[AC-06(01)(a)[01]\] access is authorized for [individuals and roles] to [security functions (deployed in hardware)];
  - \[AC-06(01)(a)[02]\] access is authorized for [individuals and roles] to [security functions (deployed in software)];
  - \[AC-06(01)(a)[03]\] access is authorized for [individuals and roles] to [security functions (deployed in firmware)];

- \[AC-06(01)(b)\] access is authorized for [individuals and roles] to [security-relevant information].

## Control guidance

Security functions include establishing system accounts, configuring access authorizations (i.e., permissions, privileges), configuring settings for events to be audited, and establishing intrusion detection parameters. Security-relevant information includes filtering rules for routers or firewalls, configuration parameters for security services, cryptographic key management information, and access control lists. Authorized personnel include security administrators, system administrators, system security officers, system programmers, and other privileged users.

______________________________________________________________________

## What is the solution and how is it implemented?

<!-- For implementation status enter one of: implemented, partial, planned, alternative, not-applicable -->

<!-- Note that the list of rules under ### Rules: is read-only and changes will not be captured after assembly to JSON -->

### This System

The ISSO and system administrators are two roles that are authorized to access security functions. Audit and log data and access compliance are reviewed by the ISSO. Emergency account deactivation is handled by the ISSO.

System administrators deploy patches, modify and implement firewall rules, modify and implement security group rules, configure parameters for security services, and modify access control lists.

Non-privileged users, parents, teachers, and school administrators, have no access to security relevant information, or functions available to the ISSO and system administrator.

#### Implementation Status: implemented
