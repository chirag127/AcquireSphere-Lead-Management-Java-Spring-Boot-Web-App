# 🚀 Pull Request Template: Apex Velocity Review

**Repository:** AcquireSphere-Lead-Management-Java-Spring-Boot-Web-App
**Author:** @chirag127

---

## 🎯 1. Summary & Intent (BLUF)

<!-- Please provide a concise, one-sentence summary of what this PR accomplishes. -->

[ ] **Feature:** Adds new functionality.
[ ] **Bugfix:** Corrects existing behavior.
[ ] **Refactor:** Improves internal structure without changing external behavior.
[ ] **Documentation:** Updates documentation only.
[ ] **Chore:** Maintenance/build process changes.

**High-Level Description:**

---

## ⚙️ 2. Architectural & Technical Details

<!-- Detail the scope of the change, referencing specific files or modules impacted. Ensure adherence to SOLID principles. -->

### Affected Components (Java/Spring):

*   (e.g., `LeadService.java`, `CustomerController.java`, `pom.xml`)
*   

### Design Rationale:

<!-- Why was this approach chosen over alternatives? Reference the Apex standards where applicable (e.g., DRY, YAGNI adherence). -->

### Security/Performance Note:

<!-- Mention any new dependencies, database queries, or API calls that required security review or performance consideration. -->

---

## ✅ 3. Verification Checklist

<!-- Self-test before requesting a review. Ensure all mandatory criteria are met. -->

### Developer Verification:

*   [ ] Local build successful (`mvn clean install`).
*   [ ] All new unit tests pass (`mvn test`).
*   [ ] Relevant integration tests executed.
*   [ ] Code adheres to Java formatting standards (checked via IDE/Ruff equivalent for Java ecosystem).
*   [ ] Documentation (Javadoc/README updates) included if external contract changed.
*   [ ] No unnecessary logging/debugging statements remain.

### Architectural Compliance:

*   [ ] Follows Hexagonal principles where applicable (clear separation between Domain and Infrastructure).
*   [ ] Data persistence layer abstraction is maintained.
*   [ ] Dependency Injection configuration verified.

---

## 🐛 4. Related Issues / References

<!-- Link to any associated Jira tickets or GitHub issues. -->

Closes #[Issue Number]
See also #[Related Issue Number]

---

**Note to Reviewer:** Please focus verification on Section 2, specifically around the business logic implementation in `[Specific File]`. Thank you for maintaining the zero-defect standard.