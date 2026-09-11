# Data portability

## Shared Markdown files

Choose a folder to edit existing UTF-8 `.md` files directly. Files stay in place when you disconnect the folder or stop using Wavebreak. Existing directories are listed as relative file paths, with a search field to help find notes. Other compatible tools can open the same files.

Current limits: 1 MB per note, up to 20 folder levels and 20,000 scanned entries. Hidden folders, links and non-Markdown files are excluded. Obsidian plugins, rendered attachments, folder creation, rename and delete are not provided by this editor.

Use Refresh files for the list and Reload from disk for an open note. There is no automatic filesystem watching or synchronization. Save drafts before leaving or closing the tab; automatic crash recovery is not implemented.

The editor checks whether a file changed before replacing it and retains a previous revision in local application backups. Independent apps do not share a transactional lock, so a narrow simultaneous-save race remains. Avoid editing the same file simultaneously in several apps and keep your own backup. Application note backups currently accumulate without automatic retention management.

## Local Daily notes

These are separate from a connected Markdown folder. Use the workspace's JSON export for a portable backup and the supported notes import for a copy. Choosing a folder does not migrate local notes or connect the standalone notes application's internal storage automatically.

## Browser data

The alpha includes supported JSON bookmark/settings import and export. It does not import browser passwords or read other browsers' credential stores. Do not assume complete migration of browser profiles, extensions or every data type.
