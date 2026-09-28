# Android-APK-Static-Analysis
Static security analysis of an Android APK using Kali Linux, APKTool, AndroidManifest and Smali code review.
# Android APK Static Analysis

This project contains a static security analysis of an Android APK performed in a Kali Linux environment.

The objective of this project was to inspect the APK structure, review application metadata, analyze the AndroidManifest.xml file, examine the decoded Smali code, and identify any obvious security or malicious indicators.

## Tools Used

- Kali Linux
- APKTool
- unzip
- file
- sha256sum
- grep
- AndroidManifest.xml analysis
- Smali code inspection

## Analysis Performed

The following steps were performed during the analysis:

- Identified the APK file type
- Calculated the SHA-256 hash
- Inspected the internal APK structure
- Extracted APK contents
- Decoded the APK using APKTool
- Reviewed application metadata
- Inspected signing-related files
- Reviewed AndroidManifest.xml
- Examined Smali code
- Checked for suspicious URLs, secrets, and network indicators

## Key Findings

- Package name: `com.browserstack.addnumber`
- Version: `1.0`
- Version Code: `1`
- Minimum SDK: `19`
- Target SDK: `23`
- No sensitive Android permissions were identified
- No obvious suspicious network URLs or API endpoints were found
- No additional native payloads or suspicious executables were identified
- Application-specific code primarily performs a simple numeric addition operation
- The APK is signed using an Android Debug certificate
- `android:debuggable="true"` was observed
- `android:allowBackup="true"` was observed

The debugging and backup settings may represent security-hardening concerns if the application were intended for production use. However, these settings alone do not indicate malicious behavior.

## Conclusion

Based on the static analysis performed, no clear malicious indicators were identified in the APK.

The application appears to perform a simple addition-related function and does not request sensitive permissions or contain obvious suspicious network behavior.

This conclusion is limited to static analysis. Additional dynamic analysis and reputation scanning would be required for a more complete security assessment.

## Report

The complete analysis report is available in the `Report` folder.

## Screenshots

Evidence collected during the analysis is available in the `Screenshots` folder.

## Disclaimer

This project was created for educational and cybersecurity learning purposes. The analysis was performed only on an APK provided for authorized academic practice.
