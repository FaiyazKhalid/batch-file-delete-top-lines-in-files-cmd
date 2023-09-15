# batch-file-delete-top-lines-in-files-cmd
Use this Command line in CMD

Steps:
One CMD
type this command:
CD c:\folder\

paste this code

@echo off
for %%F in ("*.html") do (
  more +39 "%%F" >"%%F.html"
  move /y "%%F.html" "%%F" >nul
  echo %%F
)
msg * Done!
exit /b
