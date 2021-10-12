---
title: Configuring Zotero & Zotfile for cross-device PDF sync
date: 2021-10-12
draft: false
featured: false
authors:
  - admin
tags:
  - academia
  - zotero
  - windows
  - mac
  - linux
  - android
  - dropbox
  - pdf
image:
  filename: ""
  focal_point: ""
  preview_only: false
---

🚩 Problem: How to synchronise PDF files from Zotero library across multiple devices (with or without Zotero installed)

Note I wanted to sync the *actual* PDF files, as opposed to copies of the published PDFs +- synced annotations, because I use a [Microsoft Surface](https://www.microsoft.com/en-gb/surface) with [Drawboard](https://www.drawboard.com/) to scribble all over papers. This can result in quite large file sizes and thus my library is already well over the [300 MB free limit of Zotero Storage](https://www.zotero.org/storage) (the recommended file sync solution, of course). I do however have plenty of available cloud storage with other providers such as [Dropbox](https://www.dropbox.com/), [OneDrive](https://onedrive.live.com/) etc. which I would like to make use of.

A naive solution would be to sync the folder containing the Zotero library, e.g. via dropbox. However this is explicitly discouraged by Zotero (see link for details).

> [Storing your Zotero data directory in a cloud storage folder (Dropbox, Google Drive, OneDrive, etc) is extremely likely to corrupt your database and shouldn't be done.](https://www.zotero.org/support/kb/data_directory_in_cloud_storage_folder)

🚩 Looking at the Zotero library folder also reveals a secondary issue - the **filesystem naming and structuring convention is completely unreadable!** This might be fine if you go 'all in' on Zotero but I prefer the redundancy of knowing that even if a product should be depreciated/taken over/no longer free I can still navigate my files.

There's quite a lot of discussion on the internet about how best to achieve this seemingly trivial task but I didn't find any explanation to be particularly clear and think this could dissuade a lot of people from using Zotero in the first place. Hence I share my solution.


💡 Solution = use linked files + ZotFile

1. Create folder for your Zotero library at a location of your choice, e.g. within dropbox  
2. Add this folder path within Zotero at `Edit/Preferences/Advanced/Files & Folders/Linked Attachment Base Directory
3. Install the [ZotFile](http://zotfile.com/) extension (see instructions on website)
4. Add Zotero library path within ZotFile at `Tools/Zotfile Preferences/` under `Source Folder for Attaching New Files` and set `Location of Files: Custom Location`
5. Existing files in your library need to be manually marked for 'automatic' (!) renaming by right clicking on the PDF in Zotero and selecting `Manage Attachments/Rename Attachments` which will choose an appropriately readable file name e.g. `Author_Year_Title.pdf` (can specify this in ZotFile preferences)

If you want to access your files on another computer you can configure Zotero in exactly the same fashion and it works. I've been using this for over a year now without a single issue (I believe behind the scenes the operation differs from the Zotero default in that Zotero is actually storing a *link to the PDF*, rather than the PDF, and then these links are made relative to the directory you specify, hence working across devices.)

Importantly for a tablet/other computer you can also just open the PDFs manually as they're all now in a single folder and named sensibly!

Hope this is of use to someone and saves a headache or two. No doubt there's other/easier ways but this worked for me.
