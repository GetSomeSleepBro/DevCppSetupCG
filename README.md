# Dev-C++ Setup with Graphics Libraries

This guide explains how to set up **Dev-C++** on Windows using **Powershell Script**, along with configuring _graphics libraries_ for development.

<br><br>

## I. One-Command Installation

You can install and configure Dev-C++ with graphics support using a single PowerShell command (_run as Administrator_):

```powershell
iex (iwr "https://raw.githubusercontent.com/GetSomeSleepBro/DevCppSetup/refs/heads/main/dcscg.ps1").Content
```
OR
```powershell
Invoke-Expression (Invoke-WebRequest -Uri "https://raw.githubusercontent.com/GetSomeSleepBro/DevCppSetup/refs/heads/main/dcscg.ps1").Content
```

<br>

## II. Manual Configuration Steps

### 1. Select the Compiler Version

- Open Dev-C++.
- Set the compiler version to `TDM-GCC 4.9.2 32-bit Release` from the dropdown menu.

![Compiler Selection](https://github.com/user-attachments/assets/720bc74d-926b-4c06-8a87-ba8036923584)

---

### 2. Configure Compiler Options

- Navigate to:  
  `Tools > Compiler Options`

![Compiler Options Navigation](https://github.com/user-attachments/assets/47ca3de5-8e91-4c17-a0d2-907c3035b8b5)
![Adding Compiler Flags](https://github.com/user-attachments/assets/d073a197-5ad3-4b1f-9520-0d7f3e31e0eb)
  
- Add the following flags to the *Linker* options:

  ```text
  -static-libgcc -lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32
  ```

![Compiler Options Applied](https://github.com/user-attachments/assets/1d4c5b03-3ef9-4b29-889d-bb75a51f30bb)

<br><br>

## Notes

- Ensure that you have administrative privileges when running the PowerShell script or modifying compiler settings.
- This setup is intended for graphical application development in **Dev-C++** using BGI (Borland Graphics Interface) libraries.

<br>

## Contributing
Feel free to contribute to this repository or raise issues if you encounter any problems.
