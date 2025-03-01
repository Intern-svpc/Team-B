System Description: HR, Student, and Admin Panel

Roles and Responsibilities:
1. HR Panel:
   - HR can add Job Descriptions (JD).
   - HR can view ongoing JDs.
   - HR can close JDs.
   
2. Admin Panel:
   - Admin receives JD requests when HR submits them.
   - Admin can approve JD requests.
   - Approved JDs update in the HR ongoing section and are visible to students.
   - Admin can see the number of job opportunities and HRs.

3. Student Panel:
   - Students can view job opportunities once approved by the admin.
   - When HR closes a JD, it is removed from the student portal.


Data Flow:
1. HR Login:
   - HR login details are stored in the `hrs` table.

2. Adding JD:
   - When HR adds a JD, it is stored in the `jds` table.
   - The JD is linked to the HR using `hrid`.
   - The initial status of the JD is set to `2` (Pending).

3. Admin Approval:
   - The JD request is sent to the Admin.
   - If the Admin approves the JD:
     - The status of the JD changes to `1` (Ongoing).
     - The JD appears in the HR's ongoing section.
     - The JD becomes visible in the Student Panel.

4. Closing JD:
   - If HR closes the JD:
     - The status changes to `0` (Closed).
     - The JD is removed from the Student Portal.

