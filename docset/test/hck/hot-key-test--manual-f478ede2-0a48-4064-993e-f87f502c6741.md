---
author: joshbax-msft
title: Hot Key Test (Manual)
description: Hot Key Test (Manual)
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 4376e0a0-e1ef-443f-83ce-81b31e738793
---

# Hot Key Test (Manual)


This test verifies that the computer uses the expected API to implement application command features. This ensures compatibility with any applications that handle these messages.

For information about the WM\_APPCOMMAND API notifications, see [WM\_APPCOMMAND message](http://go.microsoft.com/fwlink/?LinkId=236362).

## Test details


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Associated requirements</strong></p></td>
<td><p>Device.Input.Keyboard.BrowserMultimediaKeysUseMSApis Device.Input.Keyboard.HotKeyFunctionAPI Device.Input.Keyboard.LogoFlagKey Device.Input.Keyboard.ScanCode</p>
<p>[See the device hardware requirements.](http://go.microsoft.com/fwlink/p/?linkid=254483)</p></td>
</tr>
<tr class="even">
<td><p><strong>Platforms</strong></p></td>
<td><p>Windows 7 (x64) Windows 7 (x86) Windows 8 (x64) Windows 8 (x86) Windows Server 2012 (x64) Windows Server 2003 x64 Windows Server 2003 x86Windows Server 2008 R2 (x64) Windows Server 2008 x64 Windows Server 2008 x86Windows 8.1 x64Windows 8.1 x86Windows Server 2012 R2 Windows Vista Client x64 Windows Vista Client x86</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expected run time</strong></p></td>
<td><p>~2 minutes</p></td>
</tr>
<tr class="even">
<td><p><strong>Categories</strong></p></td>
<td><p>Certification</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Manual</p></td>
</tr>
</tbody>
</table>

 

## Running the test


Before you run the test, complete the test setup as described in the test requirements: [Keyboard Testing Prerequisites](keyboard-testing-prerequisites.md).

## Troubleshooting


For troubleshooting information, see [Troubleshooting Device.Input Testing](troubleshooting-deviceinput-testing.md).

If the test application is not receiving some notifications, make sure that the keyboard sends the expected scan code. Also, make sure that any other software that listens for WM\_APPCOMMAND notifications is not running.

## More information


The test has two views: setup view and execution view. In the setup view, select the application command keys that your keyboard has implemented. In the execution view, you're prompted to press keys that correspond to each command. If the computer receives the expected API notification, the appropriate result displays **Pass** and the color changes from yellow to green. When all results are green, the keyboard has passed the test. To complete the test, click **Submit Results**. You can reset the test at any time by clicking **Reset Test**.

### Command syntax

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>InputTest.exe /hotkey</strong></p></td>
<td><p>Runs the test, providing the user with the selection of one of three tests.</p></td>
</tr>
<tr class="even">
<td><p><strong>/hotkey</strong></p></td>
<td><p>Starts the application with the Hot Key test selected.</p></td>
</tr>
</tbody>
</table>

 

### File list

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>File</th>
<th>Location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Hook.dll</p></td>
<td><p><em>&lt;testbinroot&gt;</em>\</p></td>
</tr>
<tr class="even">
<td><p>InputTest.exe</p></td>
<td><p><em>&lt;testbinroot&gt;</em>\</p></td>
</tr>
<tr class="odd">
<td><p>WttLoggerWrapper.dll</p></td>
<td><p><em>&lt;testbinroot&gt;</em>\</p></td>
</tr>
</tbody>
</table>

 

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bp_hck\p_hck%5D:%20Hot%20Key%20Test%20%28Manual%29%20%20RELEASE:%20%284/27/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")



