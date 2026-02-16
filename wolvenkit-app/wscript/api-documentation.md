# WScript API Documentation

All methods listed on this page are accessible via `wkit.functionName()` without any additional imports.

{% hint style=\"info\" %} The following method list is auto-generated from WolvenKit Source. {% endhint %}

<!-- AUTOGEN_MARKER_START -->
# Overview

## [AppScriptFunctions](#AppScriptFunctions)

TODO.

[SuspendFileWatcher](#AppScriptFunctions-SuspendFileWatcher)          Turn on/off updates to the project tree, useful for when making lots of changes to the project structure.
[SaveToProject](#AppScriptFunctions-SaveToProject)               Add the specified CR2WFile or IGameFile file to the project.
[SaveToRaw](#AppScriptFunctions-SaveToRaw)                   Save the specified text to the specified path in the raw folder.
[SaveToResources](#AppScriptFunctions-SaveToResources)             Save the specified text to the specified path in the resources folder.
[LoadFromResources](#AppScriptFunctions-LoadFromResources)           Loads the content of a text file from resources.
[LoadGameFileFromProject](#AppScriptFunctions-LoadGameFileFromProject)     Loads the specified game file from the project files rather than game archives.
[LoadRawJsonFromProject](#AppScriptFunctions-LoadRawJsonFromProject)      Loads the specified json file from the project raw files rather than game archives.
[GetProjectFiles](#AppScriptFunctions-GetProjectFiles)             Retrieves a list of files from the project.
[ClearExportFileLookup](#AppScriptFunctions-ClearExportFileLookup)       Clears the lookup for exported depot files.
[ExportFiles](#AppScriptFunctions-ExportFiles)                 Exports a list of files as you would with the export tool.
[GetFileFromProject](#AppScriptFunctions-GetFileFromProject)          Loads a file from the project using either a file path or hash.
[GetFile](#AppScriptFunctions-GetFile)                     Loads a file from the project or archive (in this order) using either a file path or hash.
[FileExistsInProject](#AppScriptFunctions-FileExistsInProject)         Check if file exists in the project.
[FileExists](#AppScriptFunctions-FileExists)                  Check if file exists in either the game archives or the project.
[FileExistsInRaw](#AppScriptFunctions-FileExistsInRaw)             Check if file exists in the project Raw folder.
[DeleteFile](#AppScriptFunctions-DeleteFile)                  Deletes a file from the project, if it exists.
[GetRecords](#AppScriptFunctions-GetRecords)                  Loads all records as TweakDBID paths.
[GetFlats](#AppScriptFunctions-GetFlats)                    Loads all flats as TweakDBID paths.
[GetQueries](#AppScriptFunctions-GetQueries)                  Loads all queries as TweakDBID paths.
[GetGroupTags](#AppScriptFunctions-GetGroupTags)                Loads all group tags as TweakDBID paths.
[GetRecord](#AppScriptFunctions-GetRecord)                   Loads a record by its TweakDBID path.
[GetFlat](#AppScriptFunctions-GetFlat)                     Loads a flat by its TweakDBID path.
[GetQuery](#AppScriptFunctions-GetQuery)                    Loads flats of a query by its TweakDBID path.
[GetGroupTag](#AppScriptFunctions-GetGroupTag)                 Loads a group tag by its TweakDBID path.
[HasTDBID](#AppScriptFunctions-HasTDBID)                    Whether TweakDBID path exists as a flat or a record?
[GetTDBIDPath](#AppScriptFunctions-GetTDBIDPath)                Tries to get TweakDBID path from its hash.
[ShowMessageBox](#AppScriptFunctions-ShowMessageBox)              Displays a message box.
[Extract](#AppScriptFunctions-Extract)                     Extracts a file from the base archive and adds it to the project.
[GetActiveDocument](#AppScriptFunctions-GetActiveDocument)           Gets the current active document from the docking manager.
[GetDocuments](#AppScriptFunctions-GetDocuments)                Gets all documents from the docking manager.
[OpenDocument](#AppScriptFunctions-OpenDocument)                Opens a file in  WolvenKit .
[ExportGeometryCacheEntry](#AppScriptFunctions-ExportGeometryCacheEntry)    Exports an geometry_cache entry.
[CreateInstanceAsJSON](#AppScriptFunctions-CreateInstanceAsJSON)        Creates a new instance of the given class, and returns it converted to a JSON string.
[HashString](#AppScriptFunctions-HashString)                  Returns the hashcode for a given string.
[Sleep](#AppScriptFunctions-Sleep)                       Pauses the execution of the script for the specified amount of milliseconds.
[ProgramVersion](#AppScriptFunctions-ProgramVersion)              Returns the current wolvenkit version.
[ShowSettings](#AppScriptFunctions-ShowSettings)                Shows the settings dialog for the supplied data.
[SaveAs](#AppScriptFunctions-SaveAs)                      No description available.
[GetBaseFolder](#AppScriptFunctions-GetBaseFolder)               No description available.
[ParseExportSettings< T >](#AppScriptFunctions-ParseExportSettings-T)    No description available.
[GetGlobalExportArgs](#AppScriptFunctions-GetGlobalExportArgs)         No description available.
[ConvertTDBToPath](#AppScriptFunctions-ConvertTDBToPath)            No description available.
[ConvertTDBToJson](#AppScriptFunctions-ConvertTDBToJson)            No description available.

## [ScriptDocumentWrapper](#ScriptDocumentWrapper)

TODO.

[GetGameFile](#ScriptDocumentWrapper-GetGameFile)    Gets the game file.
[Save](#ScriptDocumentWrapper-Save)           Saves the document.
[Reload](#ScriptDocumentWrapper-Reload)         Reloads the document.
[Close](#ScriptDocumentWrapper-Close)          Closes the document without saving.

## [ScriptFunctions](#ScriptFunctions)

TODO.

[GetArchiveFiles](#ScriptFunctions-GetArchiveFiles)        Gets a list of the files available in the game archives Note to myself: Don't use IEnumerable<T>
[GetFileFromBase](#ScriptFunctions-GetFileFromBase)        DEPRECATED: Please use GetFileFromArchive(path, OpenAs.GameFile) Loads a file from the base archives using either a file path or hash.
[GameFileToJson](#ScriptFunctions-GameFileToJson)         Creates a json representation of the specifed game file.
[JsonToCR2W](#ScriptFunctions-JsonToCR2W)             Creates a CR2W game file from a json.
[ChangeExtension](#ScriptFunctions-ChangeExtension)        Changes the extension of the provided string path.
[GetFileFromArchive](#ScriptFunctions-GetFileFromArchive)     Loads a file from the base archives using either a file path or hash.
[FileExistsInArchive](#ScriptFunctions-FileExistsInArchive)    Check if file exists in the game archives.
[YamlToJson](#ScriptFunctions-YamlToJson)             Converts a YAML string to a JSON string.
[JsonToYaml](#ScriptFunctions-JsonToYaml)             Converts a JSON string to a YAML string.
[ConvertGameFile](#ScriptFunctions-ConvertGameFile)        No description available.

## [UiScriptFunctions](#UiScriptFunctions)

[AddMenuItem](#UiScriptFunctions-AddMenuItem)    No description available.

---

# Detailed Documentation

## AppScriptFunctions

TODO.

### SuspendFileWatcher

> Turn on/off updates to the project tree, useful for when making lots of changes to the project structure.

| Parameter | Description |
|-----------|-------------|
| `suspend` | bool for if updates are suspended |

```csharp
SuspendFileWatcher(suspend: bool) → void
```


### SaveToProject

> Add the specified CR2WFile or IGameFile file to the project.

| Parameter | Description |
|-----------|-------------|
| `path` | The file to write to |
| `file` | CR2WFile or IGameFile to be saved |

```csharp
SaveToProject(path: string, file: object) → void
```


### SaveToRaw

> Save the specified text to the specified path in the raw folder.

| Parameter | Description |
|-----------|-------------|
| `path` | The file to write to |
| `content` | The string to write to the file |

```csharp
SaveToRaw(path: string, content: string) → void
```


### SaveToResources

> Save the specified text to the specified path in the resources folder.

| Parameter | Description |
|-----------|-------------|
| `path` | The file to write to |
| `content` | The string to write to the file |

```csharp
SaveToResources(path: string, content: string) → void
```


### LoadFromResources

> Loads the content of a text file from resources.

| Parameter | Description |
|-----------|-------------|
| `path` | The relative path of the text file |

**Returns:** The content or null

```csharp
LoadFromResources(path: string) → ? string
```


### LoadGameFileFromProject

> Loads the specified game file from the project files rather than game archives.

| Parameter | Description |
|-----------|-------------|
| `path` | The file to open for reading |
| `type` | The type of the object which is returned. Can be "cr2w" or "json" |

```csharp
LoadGameFileFromProject(path: string, type: string) → ? object
```


### LoadRawJsonFromProject

> Loads the specified json file from the project raw files rather than game archives.

| Parameter | Description |
|-----------|-------------|
| `path` | The file to open for reading |
| `type` | The type of the object which is returned. Can be "cr2w" or "json" |

```csharp
LoadRawJsonFromProject(path: string, type: string) → ? object
```


### GetProjectFiles

> Retrieves a list of files from the project.

| Parameter | Description |
|-----------|-------------|
| `folderType` | string parameter folderType = "archive" or "raw" |

```csharp
GetProjectFiles(folderType: string) → List< string >
```


### ClearExportFileLookup

> Clears the lookup for exported depot files.

```csharp
ClearExportFileLookup() → void
```


### ExportFiles

> Exports a list of files as you would with the export tool.

| Parameter | Description |
|-----------|-------------|
| `fileList` | — |
| `defaultSettings` | — |
| `blocking` | — |

```csharp
ExportFiles(fileList: IList, defaultSettings: ScriptObject? = null) → void
```


### GetFileFromProject

> Loads a file from the project using either a file path or hash.

| Parameter | Description |
|-----------|-------------|
| `path` | The path of the file to retrieve |
| `openAs` | The output format (OpenAs.GameFile, OpenAs.CR2W or OpenAs.Json) |

```csharp
GetFileFromProject(path: string, openAs: OpenAs) → ? object
```


### GetFileFromProject

> Loads a file from the project using either a file path or hash.

| Parameter | Description |
|-----------|-------------|
| `hash` | The hash of the file to retrieve |
| `openAs` | The output format (OpenAs.GameFile, OpenAs.CR2W or OpenAs.Json) |

```csharp
GetFileFromProject(hash: ulong, openAs: OpenAs) → ? object
```


### GetFile

> Loads a file from the project or archive (in this order) using either a file path or hash.

| Parameter | Description |
|-----------|-------------|
| `path` | The path of the file to retrieve |
| `openAs` | The output format (OpenAs.GameFile, OpenAs.CR2W or OpenAs.Json) |

```csharp
GetFile(path: string, openAs: OpenAs) → ? object
```


### GetFile

> Loads a file from the project or archive (in this order) using either a file path or hash.

| Parameter | Description |
|-----------|-------------|
| `hash` | The hash of the file to retrieve |
| `openAs` | The output format (OpenAs.GameFile, OpenAs.CR2W or OpenAs.Json) |

```csharp
GetFile(hash: ulong, openAs: OpenAs) → ? object
```


### FileExistsInProject

> Check if file exists in the project.

| Parameter | Description |
|-----------|-------------|
| `path` | file path to check |

```csharp
FileExistsInProject(path: string) → bool
```


### FileExistsInProject

> Check if file exists in the project.

| Parameter | Description |
|-----------|-------------|
| `hash` | hash value to be checked |

```csharp
FileExistsInProject(hash: ulong) → bool
```


### FileExists

> Check if file exists in either the game archives or the project.

| Parameter | Description |
|-----------|-------------|
| `path` | file path to check |

```csharp
FileExists(path: string) → bool
```


### FileExists

> Check if file exists in either the game archives or the project.

| Parameter | Description |
|-----------|-------------|
| `hash` | hash value to be checked |

```csharp
FileExists(hash: ulong) → bool
```


### FileExistsInRaw

> Check if file exists in the project Raw folder.

| Parameter | Description |
|-----------|-------------|
| `filepath` | relative filepath to be checked |

```csharp
FileExistsInRaw(filepath: string) → bool
```


### DeleteFile

> Deletes a file from the project, if it exists.

| Parameter | Description |
|-----------|-------------|
| `filepath` | relative filepath to be deleted |
| `folderType` | project subfolder type (archive\|raw\|resources) |

**Returns:** true if the file was deleted

```csharp
DeleteFile(filepath: string, folderType: string) → bool
```


### GetRecords

> Loads all records as TweakDBID paths.

```csharp
GetRecords() → IEnumerable
```


### GetFlats

> Loads all flats as TweakDBID paths.

```csharp
GetFlats() → IEnumerable
```


### GetQueries

> Loads all queries as TweakDBID paths.

```csharp
GetQueries() → IEnumerable
```


### GetGroupTags

> Loads all group tags as TweakDBID paths.

```csharp
GetGroupTags() → IEnumerable
```


### GetRecord

> Loads a record by its TweakDBID path.

| Parameter | Description |
|-----------|-------------|
| `path` | — |

**Returns:** record as a JSON string, null when not found

```csharp
GetRecord(path: string) → ? string
```


### GetFlat

> Loads a flat by its TweakDBID path.

**Returns:** flat as a JSON string, null when not found

```csharp
GetFlat(path: string) → ? string
```


### GetQuery

> Loads flats of a query by its TweakDBID path.

**Returns:** a list of flats as TweakDBID paths, empty when not found

```csharp
GetQuery(path: string) → IEnumerable
```


### GetGroupTag

> Loads a group tag by its TweakDBID path.

**Returns:** flat as a JSON string, null when not found

```csharp
GetGroupTag(path: string) → ? byte
```


### HasTDBID

> Whether TweakDBID path exists as a flat or a record?

| Parameter | Description |
|-----------|-------------|
| `path` | — |

```csharp
HasTDBID(path: string) → bool
```


### GetTDBIDPath

> Tries to get TweakDBID path from its hash.

| Parameter | Description |
|-----------|-------------|
| `key` | — |

**Returns:** path of the hash, null when undefined

```csharp
GetTDBIDPath(key: ulong) → ? string
```


### ShowMessageBox

> Displays a message box.

| Parameter | Description |
|-----------|-------------|
| `text` | A string that specifies the text to display. |
| `caption` | A string that specifies the title bar caption to display. |
| `image` | A WMessageBoxImage value that specifies the icon to display. |
| `buttons` | A WMessageBoxButtons value that specifies which buttons to display. |

**Returns:** A WMessageBoxResult value that specifies the result the message box button that was clicked by the user returned.

```csharp
ShowMessageBox(text: string, caption: string, image: WMessageBoxImage, buttons: WMessageBoxButtons) → WMessageBoxResult
```


### Extract

> Extracts a file from the base archive and adds it to the project.

| Parameter | Description |
|-----------|-------------|
| `path` | Path of the game file |

```csharp
Extract(path: string) → void
```


### GetActiveDocument

> Gets the current active document from the docking manager.

```csharp
GetActiveDocument() → ?  ScriptDocumentWrapper
```


### GetDocuments

> Gets all documents from the docking manager.

```csharp
GetDocuments() → ? IList<  ScriptDocumentWrapper  >
```


### OpenDocument

> Opens a file in  WolvenKit .

| Parameter | Description |
|-----------|-------------|
| `path` | Path to the file |

**Returns:** Returns true if the file was opened, otherwise it returns false

```csharp
OpenDocument(path: string) → bool
```


### OpenDocument

> Opens an archive game file.

| Parameter | Description |
|-----------|-------------|
| `gameFile` | The game file to open |

```csharp
OpenDocument(gameFile: IGameFile) → void
```


### ExportGeometryCacheEntry

> Exports an geometry_cache entry.

| Parameter | Description |
|-----------|-------------|
| `sectorHashStr` | Sector hash as string |
| `entryHashStr` | Entry hash as string |

```csharp
ExportGeometryCacheEntry(sectorHashStr: string, entryHashStr: string) → ? string
```


### CreateInstanceAsJSON

> Creates a new instance of the given class, and returns it converted to a JSON string.

| Parameter | Description |
|-----------|-------------|
| `className` | Name of the class |

```csharp
CreateInstanceAsJSON(className: string) → ? object
```


### HashString

> Returns the hashcode for a given string.

| Parameter | Description |
|-----------|-------------|
| `data` | String to be hashed |
| `method` | Hash method to use. Can be "fnv1a64" or "default" (Uses the String objects built in hash function) |

```csharp
HashString(data: string, method: string) → ? ulong
```


### Sleep

> Pauses the execution of the script for the specified amount of milliseconds.

| Parameter | Description |
|-----------|-------------|
| `milliseconds` | The number of milliseconds to sleep. |

```csharp
Sleep(milliseconds: int) → void
```


### ProgramVersion

> Returns the current wolvenkit version.

```csharp
ProgramVersion() → string
```


### ShowSettings

> Shows the settings dialog for the supplied data.

| Parameter | Description |
|-----------|-------------|
| `data` | A JavaScript object containing data |

**Returns:** Returns true when the user changed the settings, otherwise it returns false

```csharp
ShowSettings(data: ScriptObject) → bool
```


### SaveAs

```csharp
SaveAs(path: string, action: Action< string >) → void
```


### GetBaseFolder

```csharp
GetBaseFolder(folderType: string) → string?
```


### ParseExportSettings< T >

```csharp
ParseExportSettings< T >(scriptSettingsObject: ScriptObject) → T
```


### GetGlobalExportArgs

```csharp
GetGlobalExportArgs(settings: ScriptObject) → GlobalExportArgs
```


### ConvertTDBToPath

```csharp
ConvertTDBToPath(ids: List< TweakDBID >?) → List< string >
```


### ConvertTDBToJson

```csharp
ConvertTDBToJson(tdb: object?) → string?
```


---


## ScriptDocumentWrapper

TODO.

### GetGameFile

> Gets the game file.

| Parameter | Description |
|-----------|-------------|
| `type` | The output type of the game file ("cr2w" or "json") |

```csharp
GetGameFile(type: string) → object?
```


### Save

> Saves the document.

```csharp
Save() → void
```


### Reload

> Reloads the document.

| Parameter | Description |
|-----------|-------------|
| `force` | If force is true, any unsaved changes will be discarded |

```csharp
Reload(force: bool) → bool
```


### Close

> Closes the document without saving.

```csharp
Close() → void
```


---


## ScriptFunctions

TODO.

### GetArchiveFiles

> Gets a list of the files available in the game archives Note to myself: Don't use IEnumerable<T>

```csharp
GetArchiveFiles() → IEnumerable
```


### GetFileFromBase

> DEPRECATED: Please use GetFileFromArchive(path, OpenAs.GameFile) Loads a file from the base archives using either a file path or hash.

| Parameter | Description |
|-----------|-------------|
| `path` | The path of the file to retrieve |

```csharp
GetFileFromBase(path: string) → ? IGameFile
```


### GetFileFromBase

> DEPRECATED: Please use GetFileFromArchive(hash, OpenAs.GameFile) Loads a file from the base archives using either a file path or hash.

| Parameter | Description |
|-----------|-------------|
| `hash` | The hash of the file to retrieve |

```csharp
GetFileFromBase(hash: ulong) → ? IGameFile
```


### GameFileToJson

> Creates a json representation of the specifed game file.

| Parameter | Description |
|-----------|-------------|
| `gameFile` | The gameFile which should be converted |

```csharp
GameFileToJson(gameFile: IGameFile) → ? string
```


### JsonToCR2W

> Creates a CR2W game file from a json.

| Parameter | Description |
|-----------|-------------|
| `json` | — |

```csharp
JsonToCR2W(json: string) → ? CR2WFile
```


### ChangeExtension

> Changes the extension of the provided string path.

| Parameter | Description |
|-----------|-------------|
| `path` | The path of the file to change |
| `extension` | — |

```csharp
ChangeExtension(path: string, extension: string) → string
```


### GetFileFromArchive

> Loads a file from the base archives using either a file path or hash.

| Parameter | Description |
|-----------|-------------|
| `path` | The path of the file to retrieve |
| `openAs` | The output format (OpenAs.GameFile, OpenAs.CR2W or OpenAs.Json) |

```csharp
GetFileFromArchive(path: string, openAs: OpenAs) → ? object
```


### GetFileFromArchive

> Loads a file from the base archives using either a file path or hash.

| Parameter | Description |
|-----------|-------------|
| `hash` | The hash of the file to retrieve |
| `openAs` | The output format (OpenAs.GameFile, OpenAs.CR2W or OpenAs.Json) |

```csharp
GetFileFromArchive(hash: ulong, openAs: OpenAs) → ? object
```


### FileExistsInArchive

> Check if file exists in the game archives.

| Parameter | Description |
|-----------|-------------|
| `path` | file path to check |

```csharp
FileExistsInArchive(path: string) → bool
```


### FileExistsInArchive

> Check if file exists in the game archives.

| Parameter | Description |
|-----------|-------------|
| `hash` | hash value to be checked |

```csharp
FileExistsInArchive(hash: ulong) → bool
```


### YamlToJson

> Converts a YAML string to a JSON string.

| Parameter | Description |
|-----------|-------------|
| `yamlText` | The YAML string to convert |

**Returns:** The converted JSON string

```csharp
YamlToJson(yamlText: string) → string
```


### JsonToYaml

> Converts a JSON string to a YAML string.

| Parameter | Description |
|-----------|-------------|
| `jsonText` | The JSON string to convert |

**Returns:** The converted YAML string

```csharp
JsonToYaml(jsonText: string) → string
```


### ConvertGameFile

```csharp
ConvertGameFile(gameFile: IGameFile, openAs: OpenAs) → ? object
```


---


## UiScriptFunctions

### AddMenuItem

| Parameter | Description |
|-----------|-------------|
| `target` | — |
| `name` | — |

```csharp
AddMenuItem(target: string, name: string) → ScriptFunctionWrapper
```


### AddMenuItem

| Parameter | Description |
|-----------|-------------|
| `target` | — |
| `name` | — |
| `onClick` | — |

```csharp
AddMenuItem(target: string, name: string, onClick: ScriptObject) → ScriptFunctionWrapper
```


### AddMenuItem

| Parameter | Description |
|-----------|-------------|
| `target` | — |
| `name` | — |
| `onClick` | — |
| `args` | — |

```csharp
AddMenuItem(target: string, name: string, onClick: ScriptObject?, args: params object??[]) → ScriptFunctionWrapper
```


### AddMenuItem

| Parameter | Description |
|-----------|-------------|
| `target` | — |
| `name` | — |
| `onClick` | — |
| `args` | — |

```csharp
AddMenuItem(target: ScriptFunctionWrapper, name: string, onClick: ScriptObject? = null, args: params object??[]) → ScriptFunctionWrapper
```


---

