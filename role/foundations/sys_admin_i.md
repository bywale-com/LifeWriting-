Windows System Admin





**@October 1st 2026** ***6:44AM***

### 

### Opening a file from the Terminal ( How do I open a file from the Terminal )



Default app (most common)

Invoke-Item .\\report.pdf

ii .\\report.pdf

(ii is the alias for Invoke-Item — opens with whatever Windows assigned to that file type.)



Explicit program

notepad .\\sys\_admin\_i.txt

Start-Process .\\report.pdf

Start-Process msedge "C:\\full\\path\\file.html"

Open the folder that contains a file

explorer /select,"C:\\Users\\omota\\Downloads\\report.pdf"

Or if you're already in that folder:



explorer .

After a search (full path from results)

ii $\_.FullName

Or pipe:



Get-ChildItem $dl -Filter \*.pdf | Select-Object -First 1 | ForEach-Object { ii $\_.FullName }

Habit: ii for “open this file”; explorer . for “show me this folder.”



























































**@October 1st 2026**



***6:37AM***

### Creating environment variables and functions shortcuts to navigate files and folders.





\- First create the environment variable



$new\_variable = Join-Path $env:'Documents' \*Use this when you're referencing pre-made windows compoartments i.e C:\\ E.T.C



OR 



$new\_variable\_i = C:\\User\\ABSOLUTE\_PATH 



OR



$new\_variable\_ii = $new\_variable '\\sub-directory'



\+ After you've created the variable, call it in a function



\- Search Filtering files, folders and artifacts.



function name = { Set-Location $environment\_variable }



Now you can use it in a command:



+terminal



Get-ChildItem $new\_variable -Filter \*.pdf















































**@October 1st 2026**



***6:37AM***

### \#creating new files



























































**@October 1st 2026**



***6:37AM***

### \#combining environment file/folder shortcuts with additional file destinations and branches.























































**@October 1st 2026**



***6:37AM***

### \#using the tree command





































































### 

### **#SEARCHING FOR THINGS - Looking for things, Finding things, Searching files and folders**





**@October 1st 2026**



***6:37AM***

#### **Combining Filters ( Multiple *Where-Object* arguments e.t.c )**



**In a Where-Object script block you join conditions with -and / -or, and -like patterns must be quoted strings.**



**Wrong (what you had):**



**Where-Object { $\_.LastWriteTime -gt (Get-Date).AddDays(-7), $\_.Name -like \*.pdf }**

**Correct:**



**Get-ChildItem $dl -Recurse -File -ErrorAction SilentlyContinue |**

&#x20; **Where-Object {**

&#x20;   **$\_.LastWriteTime -gt (Get-Date).AddDays(-7) -and**

&#x20;   **$\_.Name -like '\*.pdf'**

&#x20; **}**

**Cheaper first step (extension before date):**



**Get-ChildItem $dl -Recurse -File -Filter \*.pdf -ErrorAction SilentlyContinue |**

&#x20; **Where-Object { $\_.LastWriteTime -gt (Get-Date).AddDays(-7) }**

**Two filters in the pipeline (same idea):**



**Get-ChildItem $dl -Recurse -File -Filter \*.pdf -ErrorAction SilentlyContinue |**

&#x20; **Where-Object LastWriteTime -gt (Get-Date).AddDays(-7)**

**Note: -Filter \*.pdf on -Recurse can behave oddly in some cases; if results look wrong, drop -Filter and use -like '\*.pdf' in Where-Object only.**





***5:30AM***

#### **Intro**



Get-ChildItem $dl -Filter \*.pdf

\# Name starts with 2026

Get-ChildItem $school -Recurse -Filter '2026\*' -ErrorAction SilentlyContinue

\# Name contains "math" (anywhere)

Get-ChildItem $school -Recurse -File -ErrorAction SilentlyContinue |

&#x20; Where-Object { $\_.Name -like '\*math\*' }

\# Name contains COIS and is a PDF

Get-ChildItem $school -Recurse -File -ErrorAction SilentlyContinue |

&#x20; Where-Object { $\_.Name -like '\*COIS\*' -and $\_.Extension -eq '.pdf' }

\# Regex: outline OR syllabus in name

Get-ChildItem $docs -Recurse -File -ErrorAction SilentlyContinue |

&#x20; Where-Object { $\_.Name -match 'outline|syllabus' }

\# Limit depth (don't dig forever)

Get-ChildItem $wale -Recurse -Depth 4 -File -ErrorAction SilentlyContinue |

&#x20; Where-Object { $\_.Name -like '\*sys\_admin\*' }

\# Folders only, name contains "role"

Get-ChildItem $wale -Recurse -Directory -ErrorAction SilentlyContinue |

&#x20; Where-Object { $\_.Name -like '\*role\*' }

\# Modified in last 7 days, Downloads

Get-ChildItem $dl -File |

&#x20; Where-Object { $\_.LastWriteTime -gt (Get-Date).AddDays(-7) }

\# Big files over 50 MB under School

Get-ChildItem $school -Recurse -File -ErrorAction SilentlyContinue |

&#x20; Where-Object { $\_.Length -gt 50MB } |

&#x20; Sort-Object Length -Descending

\# Show full path (easier to copy)

Get-ChildItem $dl -Recurse -File -ErrorAction SilentlyContinue |

&#x20; Where-Object { $\_.Name -like '\*OSAP\*' } |

&#x20; Select-Object -ExpandProperty FullName

\# Search text inside files (e.g. .txt, .py, .md)

Select-String -Path (Join-Path $school '\*') -Pattern 'shippingCost' -Recurse -ErrorAction SilentlyContinue

\# Content search with file-type filter

Get-ChildItem $school -Recurse -Include \*.py,\*.txt,\*.md -File -ErrorAction SilentlyContinue |

&#x20; Select-String -Pattern 'def test\_'

\# From current folder only (after you cd somewhere)

Get-ChildItem . -Recurse -File -ErrorAction SilentlyContinue |

&#x20; Where-Object { $\_.Name -like '\*foundation\*' }

\# Explorer-style: everything under profile with "assessment" in name (slower)

Get-ChildItem $env:USERPROFILE -Recurse -File -ErrorAction SilentlyContinue |

&#x20; Where-Object { $\_.Name -like '\*assessment\*' } |

&#x20; Select-Object FullName, LastWriteTime





u







































**@October 1st 2026**



***6:37AM***

### \#copying and moving items between folders



\+ one nifty tip is this. You can be in the folder where you want the files moved ( when destination folder is working folder ), and simply move the file with no target destination; it will place it in your working folder.



like so:

&#x20;      

PS C:\\Users\\omota\\Documents\\Wale Omotayo\\School> Move-Item C:\\Users\\omota\\Downloads\\assignment1.pdf



\* This command will move the pdf file into my current working folder in .../school



Copy vs move

Intent	Cmdlet	Source after

Keep original

Copy-Item

Still there

Relocate

Move-Item

Gone from source

Basic patterns (PowerShell)

Copy one file into current folder:



Copy-Item "$dl\\report.pdf" .

Copy into a specific folder:



Copy-Item "$dl\\report.pdf" $school\\2026FALL\\

Move instead:



Move-Item "$dl\\report.pdf" $school\\2026FALL\\

Rename while moving (same folder, new name):



Move-Item .\\old-name.pdf .\\new-name.pdf

Copy a whole folder:



Copy-Item "$dl\\SomeFolder" $school\\ -Recurse

After you cd (relative paths)

cd $school\\2026FALL

Copy-Item "$dl\\report.pdf" .

Move-Item .\\draft.pdf .\\archive\\

Useful flags

Copy-Item $src $dest -Force          # overwrite existing dest

Move-Item $src $dest -Force

New-Item -ItemType Directory -Path $dest -Force   # ensure folder exists first

Quick check

Test-Path $dest\\report.pdf

Get-Item $dest\\report.pdf

Classic cmd (optional)

copy "%USERPROFILE%\\Downloads\\report.pdf" "C:\\path\\to\\School\\2026FALL\\"

move "%USERPROFILE%\\Downloads\\report.pdf" "C:\\path\\to\\School\\2026FALL\\"

Stick with Copy-Item / Move-Item in PowerShell — same quoting rules as your $dl, $school, and $wale shortcuts.







































































