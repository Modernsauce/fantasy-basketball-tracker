\# Fantasy Basketball Draft Agent — Startup Guide



Use this checklist whenever you want to work on the project.



\## Project location



```text

C:\\Users\\Liam Bhu Hammond\\Documents\\GitHub\\fantasy-basketball-tracker

```



\## Start a work session



\### 1. Open PowerShell



Open \*\*PowerShell\*\* from the Start menu.



\### 2. Move into the project folder



```powershell

cd "C:\\Users\\Liam Bhu Hammond\\Documents\\GitHub\\fantasy-basketball-tracker"

```



\### 3. Activate the Python virtual environment



```powershell

.\\.venv\\Scripts\\Activate.ps1

```



A successful activation changes the beginning of the terminal prompt to:



```text

(.venv) PS C:\\Users\\Liam Bhu Hammond\\Documents\\GitHub\\fantasy-basketball-tracker>

```



If `(.venv)` does not appear, do \*\*not\*\* install packages or run the project yet.



\### 4. Open the project in VS Code



```powershell

code .

```



If that command does not work, open VS Code manually and select:



```text

File → Open Folder → fantasy-basketball-tracker

```



\### 5. Start the Streamlit application



From the same PowerShell terminal, run:



```powershell

python -m streamlit run app.py

```



Streamlit will print a local address, usually:



```text

http://localhost:8501

```



Open that address in a browser if it does not open automatically.



\## While working



\- Keep the PowerShell window running while the Streamlit app is open.

\- Save changes in VS Code with `Ctrl + S`.

\- Streamlit usually refreshes the browser automatically after a saved Python-file change.

\- If the page does not update, click \*\*Rerun\*\* in the Streamlit browser page or refresh the browser.

\- Do not create a new virtual environment each time. The existing `.venv` folder is reused.

\- Do not install packages outside the activated `(.venv)` environment.



\## Stop the app



In the PowerShell window that is running Streamlit, press:



```text

Ctrl + C

```



Then close PowerShell if you are finished.



\## Commit changes with GitHub Desktop



1\. Open \*\*GitHub Desktop\*\*.

2\. Select the `fantasy-basketball-tracker` repository.

3\. Review the changed files.

4\. Confirm `.venv` is \*\*not\*\* listed.

5\. Write a concise summary of the change.

6\. Click \*\*Commit to main\*\*.

7\. Click \*\*Push origin\*\*.



\## If something goes wrong



\### PowerShell says activation scripts are disabled



Run this once:



```powershell

Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

```



Close and reopen PowerShell, return to the project folder, and retry:



```powershell

.\\.venv\\Scripts\\Activate.ps1

```



\### PowerShell cannot find `Activate.ps1`



First make sure you are in the project folder:



```powershell

cd "C:\\Users\\Liam Bhu Hammond\\Documents\\GitHub\\fantasy-basketball-tracker"

```



Then check that the file exists:



```powershell

Test-Path .\\.venv\\Scripts\\Activate.ps1

```



Expected result:



```text

True

```



\### Streamlit is not recognized



Make sure `(.venv)` appears in the terminal prompt, then use:



```powershell

python -m streamlit run app.py

```



Do not rely on just:



```powershell

streamlit run app.py

```



because `python -m streamlit` reliably uses the Streamlit installation associated with the active project environment.



\### Port 8501 is already in use



This usually means another Streamlit session is already running. Find the old PowerShell window and stop it with `Ctrl + C`.



Or run the app on a different port:



```powershell

python -m streamlit run app.py --server.port 8502

```



Then open:



```text

http://localhost:8502

```

