# S3 Versioning

* Once versioning is turned on it **cannot be removed**. It can only be suspended. To remove versioning, you have to create a new bucket and transfer all files from old to new
* For newer version of an object, you still have to set permissions to allow access. It is disabled by default even if previous version is public
* All versions of the file add up to the storage. Hence for larger objects, ensure that there is some lifecycle versioning in place
* Version deleted cannot be restored
* Object deleted can be restored – Delete the Delete marker
* Versioning is a good backup tool
* For versioning, **MFA can be setup** for Delete capability for object / bucket – Complicated setup



