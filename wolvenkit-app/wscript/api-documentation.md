# WScript API Documentation

All methods listed on this page are accessible via `wkit.functionName()` without any additional imports.

{% hint style=\"info\" %} The following method list is auto-generated from WolvenKit Source. {% endhint %}

<!-- AUTOGEN_MARKER_START -->
# Overview

## <a href="api-documentation.md#appscriptfunctions">AppScriptFunctions</a>

TODO.

<table>
<tr><td width="300"><b>Method</b></td><td><b>Description</b></td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-suspendfilewatcher">SuspendFileWatcher</a></code></td><td>Turn on/off updates to the project tree, useful for when making lots of changes to the project structure.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-savetoproject">SaveToProject</a></code></td><td>Add the specified CR2WFile or IGameFile file to the project.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-savetoraw">SaveToRaw</a></code></td><td>Save the specified text to the specified path in the raw folder.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-savetoresources">SaveToResources</a></code></td><td>Save the specified text to the specified path in the resources folder.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-loadfromresources">LoadFromResources</a></code></td><td>Loads the content of a text file from resources.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-loadgamefilefromproject">LoadGameFileFromProject</a></code></td><td>Loads the specified game file from the project files rather than game archives.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-loadrawjsonfromproject">LoadRawJsonFromProject</a></code></td><td>Loads the specified json file from the project raw files rather than game archives.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getprojectfiles">GetProjectFiles</a></code></td><td>Retrieves a list of files from the project.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-clearexportfilelookup">ClearExportFileLookup</a></code></td><td>Clears the lookup for exported depot files.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-exportfiles">ExportFiles</a></code></td><td>Exports a list of files as you would with the export tool.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getfilefromproject">GetFileFromProject</a></code></td><td>Loads a file from the project using either a file path or hash.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getfile">GetFile</a></code></td><td>Loads a file from the project or archive (in this order) using either a file path or hash.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-fileexistsinproject">FileExistsInProject</a></code></td><td>Check if file exists in the project.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-fileexists">FileExists</a></code></td><td>Check if file exists in either the game archives or the project.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-fileexistsinraw">FileExistsInRaw</a></code></td><td>Check if file exists in the project Raw folder.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-deletefile">DeleteFile</a></code></td><td>Deletes a file from the project, if it exists.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getrecords">GetRecords</a></code></td><td>Loads all records as TweakDBID paths.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getflats">GetFlats</a></code></td><td>Loads all flats as TweakDBID paths.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getqueries">GetQueries</a></code></td><td>Loads all queries as TweakDBID paths.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getgrouptags">GetGroupTags</a></code></td><td>Loads all group tags as TweakDBID paths.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getrecord">GetRecord</a></code></td><td>Loads a record by its TweakDBID path.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getflat">GetFlat</a></code></td><td>Loads a flat by its TweakDBID path.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getquery">GetQuery</a></code></td><td>Loads flats of a query by its TweakDBID path.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getgrouptag">GetGroupTag</a></code></td><td>Loads a group tag by its TweakDBID path.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-hastdbid">HasTDBID</a></code></td><td>Whether TweakDBID path exists as a flat or a record?</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-gettdbidpath">GetTDBIDPath</a></code></td><td>Tries to get TweakDBID path from its hash.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-showmessagebox">ShowMessageBox</a></code></td><td>Displays a message box.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-extract">Extract</a></code></td><td>Extracts a file from the base archive and adds it to the project.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getactivedocument">GetActiveDocument</a></code></td><td>Gets the current active document from the docking manager.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getdocuments">GetDocuments</a></code></td><td>Gets all documents from the docking manager.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-opendocument">OpenDocument</a></code></td><td>Opens a file in  WolvenKit .</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-exportgeometrycacheentry">ExportGeometryCacheEntry</a></code></td><td>Exports an geometry_cache entry.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-createinstanceasjson">CreateInstanceAsJSON</a></code></td><td>Creates a new instance of the given class, and returns it converted to a JSON string.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-hashstring">HashString</a></code></td><td>Returns the hashcode for a given string.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-sleep">Sleep</a></code></td><td>Pauses the execution of the script for the specified amount of milliseconds.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-programversion">ProgramVersion</a></code></td><td>Returns the current wolvenkit version.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-showsettings">ShowSettings</a></code></td><td>Shows the settings dialog for the supplied data.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-saveas">SaveAs</a></code></td><td>No description available.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getbasefolder">GetBaseFolder</a></code></td><td>No description available.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-parseexportsettings-t">ParseExportSettings< T ></a></code></td><td>No description available.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-getglobalexportargs">GetGlobalExportArgs</a></code></td><td>No description available.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-converttdbtopath">ConvertTDBToPath</a></code></td><td>No description available.</td></tr>
<tr><td><code><a href="api-documentation.md#appscriptfunctions-converttdbtojson">ConvertTDBToJson</a></code></td><td>No description available.</td></tr>
</table>

## <a href="api-documentation.md#scriptdocumentwrapper">ScriptDocumentWrapper</a>

TODO.

<table>
<tr><td width="300"><b>Method</b></td><td><b>Description</b></td></tr>
<tr><td><code><a href="api-documentation.md#scriptdocumentwrapper-getgamefile">GetGameFile</a></code></td><td>Gets the game file.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptdocumentwrapper-save">Save</a></code></td><td>Saves the document.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptdocumentwrapper-reload">Reload</a></code></td><td>Reloads the document.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptdocumentwrapper-close">Close</a></code></td><td>Closes the document without saving.</td></tr>
</table>

## <a href="api-documentation.md#scriptfunctions">ScriptFunctions</a>

TODO.

<table>
<tr><td width="300"><b>Method</b></td><td><b>Description</b></td></tr>
<tr><td><code><a href="api-documentation.md#scriptfunctions-getarchivefiles">GetArchiveFiles</a></code></td><td>Gets a list of the files available in the game archives Note to myself: Don't use IEnumerable<T></td></tr>
<tr><td><code><a href="api-documentation.md#scriptfunctions-getfilefrombase">GetFileFromBase</a></code></td><td>DEPRECATED: Please use GetFileFromArchive(path, OpenAs.GameFile) Loads a file from the base archives using either a file path or hash.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptfunctions-gamefiletojson">GameFileToJson</a></code></td><td>Creates a json representation of the specifed game file.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptfunctions-jsontocr2w">JsonToCR2W</a></code></td><td>Creates a CR2W game file from a json.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptfunctions-changeextension">ChangeExtension</a></code></td><td>Changes the extension of the provided string path.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptfunctions-getfilefromarchive">GetFileFromArchive</a></code></td><td>Loads a file from the base archives using either a file path or hash.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptfunctions-fileexistsinarchive">FileExistsInArchive</a></code></td><td>Check if file exists in the game archives.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptfunctions-yamltojson">YamlToJson</a></code></td><td>Converts a YAML string to a JSON string.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptfunctions-jsontoyaml">JsonToYaml</a></code></td><td>Converts a JSON string to a YAML string.</td></tr>
<tr><td><code><a href="api-documentation.md#scriptfunctions-convertgamefile">ConvertGameFile</a></code></td><td>No description available.</td></tr>
</table>

## <a href="api-documentation.md#uiscriptfunctions">UiScriptFunctions</a>

<table>
<tr><td width="300"><b>Method</b></td><td><b>Description</b></td></tr>
<tr><td><code><a href="api-documentation.md#uiscriptfunctions-addmenuitem">AddMenuItem</a></code></td><td>No description available.</td></tr>
</table>

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

