# Vertical Templates: Law Firm, School, Clinic

Max size per client: 30 workers. One shared core, three thin overlays.

## The core (identical for every client)

- Identity: one directory per client, no sharing across clients
- Roles: **Admin** (IT only) / **Manager** / **Staff** / **Guest**
- MFA on every account, including ours
- Audit logs: who opened, changed, shared or deleted what
- Encrypted backups, restore-tested on a schedule
- Offboarding checklist, access reviews (Secure tier)

An **overlay** only changes three things: group names, the folder tree, and the special access rules. That is what we automate later (stage 2).

---

## 1. Law firm (10-30 staff)

**What must stay private:** client files, privileged communication, billing, partner-only matters.

| Core role | Law-firm role |
|---|---|
| Admin | IT (us). Never a fee-earner. |
| Manager | Partners, Head of Chambers |
| Staff | Associates, paralegals, clerks, secretaries |
| Guest | Interns/pupils, external counsel, clients (time-limited) |

**Folder tree**
```
/Firm-Admin          (partners only: finance, HR, payroll)
/Clients
  /<Client-Name>
    /<Matter-Number>  (access = matter team only)
/Templates           (all staff, read-only)
/Library             (all staff, read-only)
/Intern-Shared       (interns: write; supervisors: read)
```

**Special rules**
- Access is **per matter, not per department**: a person sees a matter only if added to its team.
- Conflict-of-interest matters can be walled off from named staff.
- External counsel/clients get expiring links, never accounts that outlive the matter.
- Departing staff keep nothing; matter files stay with the firm.

---

## 2. School (10-30 staff)

**What must stay private:** pupil records, results before release, staff payroll, safeguarding notes, fee debts.

| Core role | School role |
|---|---|
| Admin | IT (us) |
| Manager | Proprietor, Head Teacher/Principal, Bursar |
| Staff | Class teachers, subject teachers, admin office |
| Guest | Visiting teachers, auditors, PTA reps (limited) |

**Folder tree**
```
/Management          (proprietor, head: payroll, contracts)
/Bursary             (bursar + head only: fees, debts)
/Records
  /Pupil-Records     (admin office: write; head: read)
  /Safeguarding      (head + named officer only)
/Academics
  /<Class>
    /Results-Draft   (class teacher: write; head: read)
/Shared-Resources    (all staff)
```

**Special rules**
- Teachers see **only their own classes**; results stay in draft until the head releases them.
- Pupil data is children's data: no personal email/WhatsApp sharing; keep it in the system.
- Safeguarding notes sit in the tightest folder in the school.
- Term-end review: remove access for leavers and temporary staff.

---

## 3. Clinic (10-30 staff)

**What must stay private:** patient records, test results, prescriptions, staff pay.

| Core role | Clinic role |
|---|---|
| Admin | IT (us) |
| Manager | Medical Director, Clinic Manager |
| Staff | Doctors, nurses, lab, pharmacy, front desk |
| Guest | Visiting consultants, locums (time-limited), auditors |

**Folder tree**
```
/Management          (director/manager: finance, payroll)
/Patients
  /Records           (clinical staff only)
  /Lab-Results       (lab: write; treating clinician: read)
  /Billing           (front desk/billing: no clinical notes)
/Pharmacy            (pharmacy + doctors)
/Policies-SOPs       (all staff, read-only)
```

**Special rules**
- **Minimum necessary**: front desk sees billing and appointments, not clinical notes.
- Break-glass access for emergencies must be logged and reviewed.
- Locums get expiring access that ends with their contract.
- Audit logs matter most here: "who viewed this patient's file" must be answerable.

---

## Compliance note (not legal advice)

All three handle personal data and are likely covered by the Nigeria Data Protection Act. Health data and children's data usually get stricter treatment. Have a Nigerian lawyer review the data-handling policy and client agreement before the first paid client.

## Build order

1. Build the **core** once in the lab.
2. Add **one overlay** as the demo (decide which first).
3. Add the other two as variants of the same template.
