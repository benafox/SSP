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
  ac-1_prm_1:
    aggregates:
    - ac-01_odp.01
    - ac-01_odp.02
  ac-01_odp.01:
    profile-param-value-origin: AC-1 implementation statement
    ssp-values:
    - all IPS employees
  ac-01_odp.02:
    profile-param-value-origin: AC-1 implementation statement
    ssp-values:
    - all IPS employees
  ac-01_odp.03:
    alt-identifier: ac-1_prm_2
    profile-param-value-origin: AC-1 (inherits organization-wide policy)
    ssp-values:
    - organization-level
  ac-01_odp.04:
    alt-identifier: ac-1_prm_3
    profile-param-value-origin: AC-1 implementation statement
    ssp-values:
    - Chief Information Security Officer
  ac-01_odp.05:
    alt-identifier: ac-1_prm_4
    profile-param-value-origin: AC-1 implementation statement
    ssp-values:
    - every three years
  ac-01_odp.06:
    alt-identifier: ac-1_prm_5
    profile-param-value-origin: AC-1 implementation statement
    ssp-values:
    - a security breach, a change in applicable law, a significant system change, or a major system assessment finding
  ac-01_odp.07:
    alt-identifier: ac-1_prm_6
    profile-param-value-origin: AC-1 implementation statement
    ssp-values:
    - annually
  ac-01_odp.08:
    alt-identifier: ac-1_prm_7
    profile-param-value-origin: AC-1 implementation statement
    ssp-values:
    - a security breach, a change in applicable law, a significant system change, or a major system assessment finding
x-trestle-global:
  profile:
    title: IPS-SRS-001 Tailored Moderate Baseline (AC, AU, IR, CP)
    href: trestle://profiles/ips_srs_abridged/profile.json
  sort-id: ac-01
---

# ac-1 - \[Access Control\] Policy and Procedures

## Control Statement

- \[a.\] Develop, document, and disseminate to [organization-defined personnel or roles]:

  - \[1.\] [Selection (one or more): organization-level; mission/business process-level; system-level] access control policy that:

    - \[(a)\] Addresses purpose, scope, roles, responsibilities, management commitment, coordination among organizational entities, and compliance; and
    - \[(b)\] Is consistent with applicable laws, executive orders, directives, regulations, policies, standards, and guidelines; and

  - \[2.\] Procedures to facilitate the implementation of the access control policy and the associated access controls;

- \[b.\] Designate an [official] to manage the development, documentation, and dissemination of the access control policy and procedures; and

- \[c.\] Review and update the current access control:

  - \[1.\] Policy [frequency] and following [events] ; and
  - \[2.\] Procedures [frequency] and following [events].

## Control Assessment Objective

- \[AC-01a.\]

  - \[AC-01a.[01]\] an access control policy is developed and documented;
  - \[AC-01a.[02]\] the access control policy is disseminated to [personnel or roles];
  - \[AC-01a.[03]\] access control procedures to facilitate the implementation of the access control policy and associated controls are developed and documented;
  - \[AC-01a.[04]\] the access control procedures are disseminated to [personnel or roles];
  - \[AC-01a.01\]

    - \[AC-01a.01(a)\]

      - \[AC-01a.01(a)[01]\] the [Selection (one or more): organization-level; mission/business process-level; system-level] access control policy addresses purpose;
      - \[AC-01a.01(a)[02]\] the [Selection (one or more): organization-level; mission/business process-level; system-level] access control policy addresses scope;
      - \[AC-01a.01(a)[03]\] the [Selection (one or more): organization-level; mission/business process-level; system-level] access control policy addresses roles;
      - \[AC-01a.01(a)[04]\] the [Selection (one or more): organization-level; mission/business process-level; system-level] access control policy addresses responsibilities;
      - \[AC-01a.01(a)[05]\] the [Selection (one or more): organization-level; mission/business process-level; system-level] access control policy addresses management commitment;
      - \[AC-01a.01(a)[06]\] the [Selection (one or more): organization-level; mission/business process-level; system-level] access control policy addresses coordination among organizational entities;
      - \[AC-01a.01(a)[07]\] the [Selection (one or more): organization-level; mission/business process-level; system-level] access control policy addresses compliance;

    - \[AC-01a.01(b)\] the [Selection (one or more): organization-level; mission/business process-level; system-level] access control policy is consistent with applicable laws, Executive Orders, directives, regulations, policies, standards, and guidelines;

- \[AC-01b.\] the [official] is designated to manage the development, documentation, and dissemination of the access control policy and procedures;

- \[AC-01c.\]

  - \[AC-01c.01\]

    - \[AC-01c.01[01]\] the current access control policy is reviewed and updated [frequency];
    - \[AC-01c.01[02]\] the current access control policy is reviewed and updated following [events];

  - \[AC-01c.02\]

    - \[AC-01c.02[01]\] the current access control procedures are reviewed and updated [frequency];
    - \[AC-01c.02[02]\] the current access control procedures are reviewed and updated following [events].

## Control guidance

Access control policy and procedures address the controls in the AC family that are implemented within systems and organizations. The risk management strategy is an important factor in establishing such policies and procedures. Policies and procedures contribute to security and privacy assurance. Therefore, it is important that security and privacy programs collaborate on the development of access control policy and procedures. Security and privacy program policies and procedures at the organization level are preferable, in general, and may obviate the need for mission- or system-specific policies and procedures. The policy can be included as part of the general security and privacy policy or be represented by multiple policies reflecting the complex nature of organizations. Procedures can be established for security and privacy programs, for mission or business processes, and for systems, if needed. Procedures describe how the policies or controls are implemented and can be directed at the individual or role that is the object of the procedure. Procedures can be documented in system security and privacy plans or in one or more separate documents. Events that may precipitate an update to access control policy and procedures include assessment or audit findings, security incidents or breaches, or changes in laws, executive orders, directives, regulations, policies, standards, and guidelines. Simply restating controls does not constitute an organizational policy or procedure.

______________________________________________________________________

## What is the solution and how is it implemented?

<!-- For implementation status enter one of: implemented, partial, planned, alternative, not-applicable -->

<!-- Note that the list of rules under ### Rules: is read-only and changes will not be captured after assembly to JSON -->

### This System

Access control policy for IPS-SRS-001 starts with the IPS Common Control Policy where all information security policies are drafted according to laws, regulations, and operational requirements. The IPS Common Control Policy addresses purpose, scope, roles and responsibilities, management commitment, coordination among organizational entities, and compliance. Policy is updated at least every three years and procedures are updated every year. Upon a breach in the security objectives of the system, change in laws, significant system change, or major system assessment finding the policies and procedures are updated according to the event.

The IPS Chief Information Security Officer is responsible for ensuring all employees are familiar with the policies and to test their implementation. Policy and procedures at the system level are implemented by the Information System Security Officer for the system. The CISO oversees the ISSO by approving the specific implementations of the policies and procedures.

Documentation for the policy, procedures, and the associated AC controls that fall within the responsibility of IPS is found separately on the organization intranet.

#### Implementation Status: implemented
