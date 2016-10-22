# GetFilesFromFolderInBundle
For Swift 3. A class that when used will return files from a parent folder containing children folders. It will not find folders that are contained within a child folder. 

The following example will work. A parent folder called 'Images' that is in the application bundle which has subfolders with files in them.

/Images<br />
  /Social<br />
    facebook.png<br />
    twitter.png<br />
  /Other<br />
    dog.png<br />
    sun.png<br />
  ...<br />
  
Calling the class is as easy as:

```
ImageAssetManager().loadFileURLSFromFolderInBundle(parentFolder: "<YourParentFolderName>") { (result, status) in
            
            guard status == .success else {
              return
             }  
             
             // Do Stuff
             // result is [Data]
           }

```
