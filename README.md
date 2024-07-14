# Xbox 360 XEX Building Fix for Visual Studio 2022

## Issue
Visual Studio 2022 may incorrectly report a build failure even when the XEX file is successfully created for Xbox 360 projects.

## Solution
Replace the default .targets file with a custom version:

1. Navigate to:
   `C:\Program Files (x86)\MSBuild\Microsoft.Cpp\v4.0\Platforms\Xbox 360\PlatformToolsets\2010-01`

2. Locate the existing .targets file (likely named `Microsoft.Cpp.Xbox360.2010-01.targets`).

3. Back up the original file.

4. Replace it with your custom .targets file.

## Note
After applying this fix, the project should build successfully. However, Visual Studio may still display a "failed" message. This is a known issue and can be safely ignored if the XEX file is generated correctly.
