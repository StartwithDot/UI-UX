## P1.1: Find What the Brief Does Not Answer

### Question 1
**What is the maximum file size and format supported for document uploads on the portal?**
* **Source / Role to answer:** Lead Systems Engineer
* **Time estimate:** 2 hours
* **Why it changes the design:** If the website doesn't give a specific file format or size the user's application might get canceled/declined after submiting the application without the applicant knowing. This led to calls to office frequently

---

### Question 2
**Can an applicant edit or withdraw their application before or after the final submission deadline?**
* **Source / Role to answer:** PSC Rules & Policy Officer / Department Secretary
* **Time estimate:** 3 to 5 business days (requires administrative policy clarification)
* **Why it changes the design:** Add a section double check the info they have given and rewrite it if the information given is wrong

---

### Question 3
**What happens if an applicant drops off halfway through, does the system auto-save as a draft on the server or locally on the device?**
* **Source / Role to answer:** Technical Lead / Backend Architect
* **Time estimate:** 1 business day (reviewing session management and database schemas)
* **Why it changes the design:** Determines whether to build a multi-step progress bar with an explicit "Save Draft" button and draft recovery card, or design for single-session completion with session-expiry warnings.