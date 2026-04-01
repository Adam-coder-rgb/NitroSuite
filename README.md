# NitroSuite
# Nitro Suite Resources Folder Structure

## 📁 **Directory Organization**

This folder contains all external resources, scripts, and documentation for the Nitro Suite application.

### **📂 Folder Structure**

```
Resources/
├── 📁 icons/           # Application icons and graphics
│   └── 📄 app.ico       # Main application icon
├── 📁 images/          # Images and graphics
│   └── 📄 logo.png      # Application logo
├── 📁 external/        # External tools and executables
│   └── 📄 nvidia_inspector.exe  # NVIDIA GPU optimization tool
├── 📁 scripts/         # PowerShell and batch scripts
│   ├── 📄 setup_powershell_fixed.ps1     # PowerShell environment setup
│   ├── 📄 instant_executor_fixed.ps1     # Instant command executor
│   ├── 📄 instant_executor.bat           # Batch file access
│   ├── 📄 static_analysis_fixed.ps1       # Pre-build validation
│   └── 📄 wmi_network_query_fixed.ps1    # WMI network queries
├── 📁 documentation/   # Documentation and guides
│   ├── 📄 POWERSHELL_SETUP_COMPLETE.md           # PowerShell setup guide
│   ├── 📄 PRE_BUILD_VALIDATION_PROTOCOL.md       # Build validation protocol
│   └── 📄 WMI_NETWORK_QUERY_SYSTEM.md            # WMI query system docs
└── 📁 temp/            # Temporary/placeholder files
    └── 📄 setup.bat      # Old placeholder script
```

### **🔧 Script Usage**

#### **PowerShell Environment Setup**
```powershell
# Run PowerShell environment configuration
.\Resources\scripts\setup_powershell_fixed.ps1
```

#### **Instant Command Executor**
```powershell
# Interactive mode
.\Resources\scripts\instant_executor_fixed.ps1

# Command execution
.\Resources\scripts\instant_executor_fixed.ps1 -Command "Get-Service" -Description "Service Check"

# Batch file access
.\Resources\scripts\instant_executor.bat
```

#### **Static Analysis (Pre-Build)**
```powershell
# Run validation before build
.\Resources\scripts\static_analysis_fixed.ps1

# Detailed report
.\Resources\scripts\static_analysis_fixed.ps1 -Detailed
```

#### **WMI Network Queries**
```powershell
# Comprehensive network scan
.\Resources\scripts\wmi_network_query_fixed.ps1 -QueryType "All" -Detailed

# Physical adapters only
.\Resources\scripts\wmi_network_query_fixed.ps1 -QueryType "Physical"

# Performance monitoring
.\Resources\scripts\wmi_network_query_fixed.ps1 -QueryType "Performance"

# Troubleshooting
.\Resources\scripts\wmi_network_query_fixed.ps1 -QueryType "Troubleshoot" -Troubleshoot
```

### **📋 File Descriptions**

#### **Icons & Images**
- **app.ico**: Main application icon (placeholder - replace with actual icon)
- **logo.png**: Application logo (placeholder - replace with actual logo)

#### **External Tools**
- **nvidia_inspector.exe**: NVIDIA GPU optimization tool (placeholder - download from guru3d.com)

#### **Scripts**
- **setup_powershell_fixed.ps1**: Configures PowerShell environment for Nitro Suite
- **instant_executor_fixed.ps1**: Provides instant command execution without timeouts
- **instant_executor.bat**: Easy double-click access to instant executor
- **static_analysis_fixed.ps1**: Pre-build validation and static code analysis
- **wmi_network_query_fixed.ps1**: Comprehensive WMI network adapter queries

#### **Documentation**
- **POWERSHELL_SETUP_COMPLETE.md**: Complete PowerShell setup documentation
- **PRE_BUILD_VALIDATION_PROTOCOL.md**: Build validation and No-Error Mandate protocol
- **WMI_NETWORK_QUERY_SYSTEM.md**: WMI network query system documentation

#### **Temporary Files**
- **setup.bat**: Old placeholder script (moved to temp folder)

### **🎯 Integration Notes**

#### **Command Validation**
All scripts are added to `rules/allowed_commands.yml` for security validation:
```yaml
allowed_commands:
  - setup_powershell_fixed.ps1
  - instant_executor_fixed.ps1
  - static_analysis_fixed.ps1
  - wmi_network_query_fixed.ps1
```

#### **Path References**
Update any code references to use the new Resources paths:
```csharp
// Old path
string scriptPath = "setup_powershell_fixed.ps1";

// New path
string scriptPath = Path.Combine("Resources", "scripts", "setup_powershell_fixed.ps1");
```

### **🔐 Security Considerations**

- All scripts are validated against the rules file
- External tools should be verified for authenticity
- Documentation files contain no sensitive information
- Temp folder contains only placeholder files

### **📝 Maintenance**

#### **Adding New Scripts**
1. Place script in appropriate subfolder (scripts/tools)
2. Add to rules/allowed_commands.yml
3. Update this README with usage instructions
4. Test script functionality

#### **Updating Documentation**
1. Update files in documentation folder
2. Keep version information current
3. Update usage examples as needed

#### **Resource Management**
- Replace placeholder files with actual resources
- Keep external tools updated to latest versions
- Remove unused files from temp folder
- Maintain folder structure consistency

### **🚀 Quick Start**

1. **Setup Environment**: Run `Resources\scripts\setup_powershell_fixed.ps1`
2. **Validate Build**: Run `Resources\scripts\static_analysis_fixed.ps1`
3. **Test Network**: Run `Resources\scripts\wmi_network_query_fixed.ps1 -QueryType "All"`
4. **Execute Commands**: Use `Resources\scripts\instant_executor_fixed.ps1`

---

**Last Updated**: March 31, 2026  
**Version**: 1.0  
**Purpose**: Organize Nitro Suite resources for clean project structure
