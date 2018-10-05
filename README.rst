Publication approval
--------------------

This plugin adds curation functionality to Girder, allowing content to be
assembled and approved prior to publication. Admin users can activate curation
for any folder, and users who are then granted permission can compose content
under that folder. The users can request publication of the content when it is
ready, which admins may approve or reject. The plugin provides a UI along with
workflow management, notification, and permission support for these actions.

The standard curation workflow works as follows, with any operations affecting
privacy or permissions being applied to the folder and all of its descendant
folders.

- Site admins can enable curation for any folder, which changes the folder to
  Private.
- Users with write access can populate the folder with data.
- When ready, a user can request approval from the admin. The folder becomes
  read-only at this point for any user or group with write access, to avoid
  further changes being made while the admin is reviewing.
- The admin can approve or reject the folder contents.
- If approved, the folder becomes Public.
- If rejected, the folder becomes writeable again by any user or group with read
  access, enabling users to make changes and resubmit for approval.

The curation dialog is accessible from the Folder actions menu and shows the
following information.

- Whether curation is enabled or disabled for the folder.
- The current curation status: construction, requested, or approved.
- A timeline of status changes, who performed them and when.
- Context-dependent action buttons to perform state transitions.
