PAVAN CHAITANYA WORKTRACK v0.8 — TASK & TIME INTEGRATION

Changes:
- Time entries can be linked to a Project and a specific Task.
- The Time Logger has a Create Task shortcut.
- Start Timer now asks for activity, project and linked task.
- Stopping the timer saves a time entry linked to the selected task/project.
- Task list shows total time logged per task.
- Project list shows total time logged per project.
- Task and Project deletion are available with confirmation.
- Deleting a task keeps its historical time entries but removes their task link.
- Deleting a project keeps tasks, time entries and engineering records, detaching them from the deleted project.
- Drawings/BOM, Materials/PRS-MRS, ECR and Vendor records have individual Delete actions.
- Cloud read now preserves the Drive updatedAt timestamp.
- Initial cloud sync prioritizes non-empty cloud data when the local browser cache is empty, preventing an empty local cache from replacing existing Drive records.

DEPLOYMENT:
1. Back up your current GitHub repository and export a WorkTrack JSON backup before replacing files.
2. Upload the files inside worktrack-main/ to the root of your GitHub Pages repository, replacing the existing files.
3. In Apps Script, update Code.gs with the supplied Code.gs file from this package (or add the updatedAt property to the JSONP success response).
4. Save Code.gs, then Deploy > Manage deployments > Edit > New version > Deploy. Keep the existing /exec URL.
5. Open WorkTrack and hard refresh with Ctrl+F5.
6. Use Settings > Update Now to sync. If local storage is empty and Drive has records, the app should download the Drive records.

DATA SAFETY:
- No Drive records are included in this package or modified by it.
- Delete actions require confirmation.
- Deleting a project detaches linked records rather than cascading deletion.
- Deleting a task leaves time records in history, but unlinks them from the deleted task.
- Always export a backup before deploying.


VISUAL UPDATE v0.8.1:
- Updated the overall interface to a clean navy/blue neutral palette.
- Assigned a distinct colour identity to Dashboard, Tasks, Time Logger, Projects, Drawings & BOM, Materials, ECR, Vendors, Reports and Settings.
- Added distinct colours for open, in-progress, waiting, completed and overdue status labels.
- Updated the PWA browser theme and service-worker cache version.
