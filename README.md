# VSProjectGuids
<!--- 
declare @typeGuids as table(name varchar(max), guid varchar(max));

insert into @typeGuids
select distinct name, upper(guid) guid
from (values 
 ('ASP.NET 5', '{8BB2217D-0F2D-49D1-97BC-3654ED321F3B}')
,('ASP.NET MVC 1', '{603C0E0B-DB56-11DC-BE95-000D561079B0}')
,('ASP.NET MVC 2', '{F85E285D-A4E0-4152-9332-AB1D724D3325}')
,('ASP.NET MVC 3', '{E53F8FEA-EAE0-44A6-8774-FFD645390401}')
,('ASP.NET MVC 4', '{E3E379DF-F4C6-4180-9B81-6769533ABE47}')
,('ASP.NET MVC 5', '{349C5851-65DF-11DA-9384-00065B846F21}')
,('C#', '{FAE04EC0-301F-11D3-BF4B-00C04F79EFBC}')
,('C++', '{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}')
,('Database', '{A9ACE9BB-CECE-4E62-9AA4-C7E7C5BD2124}')
,('Database (other project types)', '{4F174C21-8C12-11D0-8340-0000F80270F8}')
,('Deployment Cab', '{3EA9E505-35AC-4774-B492-AD1749C4943A}')
,('Deployment Merge Module', '{06A35CCD-C46D-44D5-987B-CF40FF872267}')
,('Deployment Setup', '{978C614F-708E-4E1A-B201-565925725DBA}')
,('Deployment Smart Device Cab', '{AB322303-2255-48EF-A496-5904EB18DA55}')
,('Distributed System', '{F135691A-BF7E-435D-8960-F99683D2D49C}')
,('Dynamics 2012 AX C# in AOT', '{BF6F8E12-879D-49E7-ADF0-5503146B24B8}')
,('F#', '{F2A71F9B-5D33-465A-A702-920D77279786}')
,('J#', '{E6FDF86B-F3D1-11D4-8576-0002A516ECE8}')
,('Legacy (2003) Smart Device (C#)', '{20D4826A-C6FA-45DB-90F4-C717570B9F32}')
,('Legacy (2003) Smart Device (VB.NET)', '{CB4CE8C6-1BDB-4DC7-A4D3-65A1999772F8}')
,('Micro Framework', '{b69e3092-b931-443c-abe7-7e7b65f2a37f}')
,('Model-View-Controller v2 (MVC 2)', '{F85E285D-A4E0-4152-9332-AB1D724D3325}')
,('Model-View-Controller v3 (MVC 3)', '{E53F8FEA-EAE0-44A6-8774-FFD645390401}')
,('Model-View-Controller v4 (MVC 4)', '{E3E379DF-F4C6-4180-9B81-6769533ABE47}')
,('Model-View-Controller v5 (MVC 5)', '{349C5851-65DF-11DA-9384-00065B846F21}')
,('Mono for Android', '{EFBA0AD7-5A72-4C68-AF49-83D382785DCF}')
,('MonoTouch', '{6BC8ED88-2882-458C-8E55-DFD12B67127B}')
,('MonoTouch Binding', '{F5B4F3BC-B597-4E2B-B552-EF5D8A32436F}')
,('Portable Class Library', '{786C830F-07A1-408B-BD7F-6EE04809D6DB}')
,('Project Folders', '{66A26720-8FB5-11D2-AA7E-00C04F688DDE}')
,('Report Project', '{F14B399A-7131-4C87-9E4B-1186C45EF12D}')
,('SharePoint (C#)', '{593B0543-81F6-4436-BA1E-4747859CAAE2}')
,('SharePoint (VB.NET)', '{EC05E597-79D4-47f3-ADA0-324C4F7C7484}')
,('SharePoint Workflow', '{F8810EC1-6754-47FC-A15F-DFABD2E3FA90}')
,('Silverlight', '{A1591282-1198-4647-A2B1-27E5FF5F6F3B}')
,('Smart Device (C#)', '{4D628B5B-2FBC-4AA6-8C16-197242AEB884}')
,('Smart Device (VB.NET)', '{68B1623D-7FB9-47D8-8664-7ECEA3297D4F}')
,('Solution Folder', '{2150E333-8FDC-42A3-9474-1A3956D46DE8}')
,('Test', '{3AC096D0-A1C2-E12C-1390-A8335801FDAB}')
,('Universal Windows Class Library', '{A5A43C5B-DE2A-4C0C-9213-0A381AF9435A}')
,('VB.NET', '{F184B08F-C81C-45F6-A57F-5ABD9991F28F}')
,('Visual Database Tools', '{C252FEB5-A946-4202-B1D4-9916A0590387}')
,('Visual Studio 2015 Installer Project Extension', '{54435603-DBB4-11D2-8724-00A0C9A8B90C}')
,('Visual Studio Tools for Applications (VSTA)', '{A860303F-1F3F-4691-B57E-529FC101A107}')
,('Visual Studio Tools for Office (VSTO)', '{BAA0C2D2-18E2-41B9-852F-F413020CAA33}')
,('Web Application', '{349C5851-65DF-11DA-9384-00065B846F21}')
,('Web Site', '{E24C65DC-7377-472B-9ABA-BC803B73C61A}')
,('Windows (C#)', '{FAE04EC0-301F-11D3-BF4B-00C04F79EFBC}')
,('Windows (VB.NET)', '{F184B08F-C81C-45F6-A57F-5ABD9991F28F}')
,('Windows (Visual C++)', '{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}')
,('Windows Communication Foundation (WCF)', '{3D9AD99F-2412-4246-B90B-4EAA41C64699}')
,('Windows Phone 8/8.1 Blank/Hub/Webview App', '{76F1466A-8B6D-4E39-A767-685A06062A39}')
,('Windows Phone 8/8.1 App (C#)', '{C089C8C0-30E0-4E22-80C0-CE093F111A43}')
,('Windows Phone 8/8.1 App (VB.NET)', '{DB03555F-0C8B-43BE-9FF9-57896B3C5E56}')
,('Windows Presentation Foundation (WPF)', '{60DC8134-EBA5-43B8-BCC9-BB4BC16C2548}')
,('Windows Store (Metro) Apps & Components', '{BC8A1FFA-BEE3-4634-8014-F334798102B3}')
,('Workflow (C#)', '{14822709-B5A1-4724-98CA-57A101D1B079}')
,('Workflow (VB.NET)', '{D59BE175-2ED0-4C54-BE3D-CDAA9F3214C8}')
,('Workflow Foundation', '{32F31D43-81CC-4C15-9DE6-3FC5453562B6}')
,('Xamarin.Android', '{EFBA0AD7-5A72-4C68-AF49-83D382785DCF}')
,('Xamarin.iOS', '{6BC8ED88-2882-458C-8E55-DFD12B67127B}')
,('XNA (Windows)', '{6D335F3A-9D43-41b4-9D22-F6F17C4BE596}')
,('XNA (XBox)', '{2DF5C3F4-5A5F-47a9-8E94-23B4456F55E2}')
,('XNA (Zune)', '{D399B71A-8929-442a-A9AC-8BEC78BB2433}')
,('Platform Toolset v120', '{8DB26A54-E6C6-494F-9B32-ACBB256CD3A5}')
,('Platform Toolset v141', '{C2CAFE0E-DCE1-4D03-BBF6-18283CF86E48}')
,('SSIS', '{159641d6-6404-4a2a-ae62-294de0fe8301}')
,('C# (.Net Core)', '{9A19103F-16F7-4668-BE54-9A1E7A4F7556}')
,('MonoDevelop Addin projects', '{86F6BF2A-E449-4B3E-813B-9ACC37E5545F}')
,('Workflow Visual C# Project', '{9D2881F7-F482-416C-8D64-CA83326250B9}')
,('VB Web MVC Project Templates', '{141DA93E-88A7-45D5-B15B-89117F514D64}')
,('WPF Project Flavor CSharp Templates', '{b3bae735-386c-4030-8329-ef48eeda4036}')
,('C# Web MVC Project Templates', '{141DA93E-88A7-45D5-B15B-89117F514D64}')
,('Workflow Project', '{AAFFDC1E-A1C7-47BC-B3DC-9E685DF3959B}')
,('Web Application Project Factory', '{349C5850-65DF-11DA-9384-00065B846F21}')
insert into @typeGuids
select distinct *
from (values 
 ('Deployment Merge Module', '{06A35CCD-C46D-44D5-987B-CF40FF872267}')
,('C# Web MVC Project Templates', '{141DA93E-88A7-45D5-B15B-89117F514D64}')
,('VB Web MVC Project Templates', '{141DA93E-88A7-45D5-B15B-89117F514D64}')
,('Web MVC 301 Project Factory (Compatibility)', '{141DA93E-88A7-45D5-B15B-89117F514D64}')
,('Web MVC 4 Project Factory (Compatibility)', '{141DA93E-88A7-45D5-B15B-89117F514D64}')
,('Workflow (C#)', '{14822709-B5A1-4724-98CA-57A101D1B079}')
,('SSIS', '{159641d6-6404-4a2a-ae62-294de0fe8301}')
,('Legacy (2003) Smart Device (C#)', '{20D4826A-C6FA-45DB-90F4-C717570B9F32}')
,('Solution Folder', '{2150E333-8FDC-42A3-9474-1A3956D46DE8}')
,('XNA (XBox)', '{2DF5C3F4-5A5F-47a9-8E94-23B4456F55E2}')
,('Workflow Foundation', '{32F31D43-81CC-4C15-9DE6-3FC5453562B6}')
,('VB Web Application Project Templates', '{349C5850-65DF-11DA-9384-00065B846F21}')
,('Web Application Project Factory', '{349C5850-65DF-11DA-9384-00065B846F21}')
,('C# Web Application Project Templates', '{349C5850-65DF-11DA-9384-00065B846F21}')
,('ASP.NET MVC 5', '{349C5851-65DF-11DA-9384-00065B846F21}')
,('Model-View-Controller v5 (MVC 5)', '{349C5851-65DF-11DA-9384-00065B846F21}')
,('Web Application', '{349C5851-65DF-11DA-9384-00065B846F21}')
,('Test', '{3AC096D0-A1C2-E12C-1390-A8335801FDAB}')
,('Windows Communication Foundation (WCF)', '{3D9AD99F-2412-4246-B90B-4EAA41C64699}')
,('Deployment Cab', '{3EA9E505-35AC-4774-B492-AD1749C4943A}')
,('Smart Device (C#)', '{4D628B5B-2FBC-4AA6-8C16-197242AEB884}')
,('Database (other project types)', '{4F174C21-8C12-11D0-8340-0000F80270F8}')
,('CSharp Test Project', '{52CBD135-1F97-2580-011F-C7CD052E44DE}')
,('VisualBasic Test Project', '{52CBD135-1F97-2580-011F-C7CD052E44DE}')
,('Visucal C++ Test Project', '{52CBD135-1F97-2580-011F-C7CD052E44DE}')
,('Visual Studio 2015 Installer Project Extension', '{54435603-DBB4-11D2-8724-00A0C9A8B90C}')
,('SharePoint (C#)', '{593B0543-81F6-4436-BA1E-4747859CAAE2}')
,('ASP.NET MVC 1', '{603C0E0B-DB56-11DC-BE95-000D561079B0}')
,('Windows Presentation Foundation (WPF)', '{60DC8134-EBA5-43B8-BCC9-BB4BC16C2548}')
,('Project Folders', '{66A26720-8FB5-11D2-AA7E-00C04F688DDE}')
,('Smart Device (VB.NET)', '{68B1623D-7FB9-47D8-8664-7ECEA3297D4F}')
,('MonoTouch', '{6BC8ED88-2882-458C-8E55-DFD12B67127B}')
,('Xamarin.iOS', '{6BC8ED88-2882-458C-8E55-DFD12B67127B}')
,('XNA (Windows)', '{6D335F3A-9D43-41b4-9D22-F6F17C4BE596}')
,('Windows Phone 8/8.1 Blank/Hub/Webview App', '{76F1466A-8B6D-4E39-A767-685A06062A39}')
,('Portable Class Library', '{786C830F-07A1-408B-BD7F-6EE04809D6DB}')
,('MonoDevelop Addin projects', '{86F6BF2A-E449-4B3E-813B-9ACC37E5545F}')
,('ASP.NET 5', '{8BB2217D-0F2D-49D1-97BC-3654ED321F3B}')
,('C++', '{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}')
,('Windows (Visual C++)', '{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}')
,('Platform Toolset v120', '{8DB26A54-E6C6-494F-9B32-ACBB256CD3A5}')
,('Deployment Setup', '{978C614F-708E-4E1A-B201-565925725DBA}')
,('C# (.Net Core)', '{9A19103F-16F7-4668-BE54-9A1E7A4F7556}')
,('Workflow Visual Basic Project', '{9D2881F7-F482-416C-8D64-CA83326250B9}')
,('Workflow Visual C# Project', '{9D2881F7-F482-416C-8D64-CA83326250B9}')
,('Silverlight', '{A1591282-1198-4647-A2B1-27E5FF5F6F3B}')
,('Universal Windows Class Library', '{A5A43C5B-DE2A-4C0C-9213-0A381AF9435A}')
,('Visual Studio Tools for Applications (VSTA)', '{A860303F-1F3F-4691-B57E-529FC101A107}')
,('Database', '{A9ACE9BB-CECE-4E62-9AA4-C7E7C5BD2124}')
,('Workflow Project', '{AAFFDC1E-A1C7-47BC-B3DC-9E685DF3959B}')
,('Deployment Smart Device Cab', '{AB322303-2255-48EF-A496-5904EB18DA55}')
,('WPF Project Flavor CSharp Templates', '{b3bae735-386c-4030-8329-ef48eeda4036}')
,('WPF Project Flavor Visual Basic Templates', '{b3bae735-386c-4030-8329-ef48eeda4036}')
,('Micro Framework', '{b69e3092-b931-443c-abe7-7e7b65f2a37f}')
,('Visual Studio Tools for Office (VSTO)', '{BAA0C2D2-18E2-41B9-852F-F413020CAA33}')
,('Windows Store (Metro) Apps & Components', '{BC8A1FFA-BEE3-4634-8014-F334798102B3}')
,('Dynamics 2012 AX C# in AOT', '{BF6F8E12-879D-49E7-ADF0-5503146B24B8}')
,('Windows Phone 8/8.1 App (C#)', '{C089C8C0-30E0-4E22-80C0-CE093F111A43}')
,('Visual Database Tools', '{C252FEB5-A946-4202-B1D4-9916A0590387}')
,('Platform Toolset v141', '{C2CAFE0E-DCE1-4D03-BBF6-18283CF86E48}')
,('VB Silverlight Project Templates', '{CB22EE0E-4072-4ae7-96E2-90FCCF879544}')
,('Microsoft Silverlight Project Factory', '{CB22EE0E-4072-4ae7-96E2-90FCCF879544}')
,('C# Silverlight Project Templates', '{CB22EE0E-4072-4ae7-96E2-90FCCF879544}')
,('Legacy (2003) Smart Device (VB.NET)', '{CB4CE8C6-1BDB-4DC7-A4D3-65A1999772F8}')
,('XNA (Zune)', '{D399B71A-8929-442a-A9AC-8BEC78BB2433}')
,('Workflow (VB.NET)', '{D59BE175-2ED0-4C54-BE3D-CDAA9F3214C8}')
,('Windows Phone 8/8.1 App (VB.NET)', '{DB03555F-0C8B-43BE-9FF9-57896B3C5E56}')
,('Web Site', '{E24C65DC-7377-472B-9ABA-BC803B73C61A}')
,('Model-View-Controller v4 (MVC 4)', '{E3E379DF-F4C6-4180-9B81-6769533ABE47}')
,('ASP.NET MVC 4', '{E3E379DF-F4C6-4180-9B81-6769533ABE47}')
,('ASP.NET MVC 3', '{E53F8FEA-EAE0-44A6-8774-FFD645390401}')
,('Model-View-Controller v3 (MVC 3)', '{E53F8FEA-EAE0-44A6-8774-FFD645390401}')
,('J#', '{E6FDF86B-F3D1-11D4-8576-0002A516ECE8}')
,('SharePoint (VB.NET)', '{EC05E597-79D4-47f3-ADA0-324C4F7C7484}')
,('Mono for Android', '{EFBA0AD7-5A72-4C68-AF49-83D382785DCF}')
,('Xamarin.Android', '{EFBA0AD7-5A72-4C68-AF49-83D382785DCF}')
,('Distributed System', '{F135691A-BF7E-435D-8960-F99683D2D49C}')
,('Report Project', '{F14B399A-7131-4C87-9E4B-1186C45EF12D}')
,('Windows (VB.NET)', '{F184B08F-C81C-45F6-A57F-5ABD9991F28F}')
,('VB.NET', '{F184B08F-C81C-45F6-A57F-5ABD9991F28F}')
,('F#', '{F2A71F9B-5D33-465A-A702-920D77279786}')
,('MonoTouch Binding', '{F5B4F3BC-B597-4E2B-B552-EF5D8A32436F}')
,('Model-View-Controller v2 (MVC 2)', '{F85E285D-A4E0-4152-9332-AB1D724D3325}')
,('ASP.NET MVC 2', '{F85E285D-A4E0-4152-9332-AB1D724D3325}')
,('SharePoint Workflow', '{F8810EC1-6754-47FC-A15F-DFABD2E3FA90}')
,('Windows (C#)', '{FAE04EC0-301F-11D3-BF4B-00C04F79EFBC}')
,('C#', '{FAE04EC0-301F-11D3-BF4B-00C04F79EFBC}')
)a(name, guid);

declare @by varchar(50) = 'By Description' ;

select case when ROW_NUMBER() over (order by case when @by = 'By Description' then Name else guid end) = 1 then '**'+ @by +'** <br />' + '<table> '
	+ '<thead><tr><th>' + case when @by = 'By Description' then 'Description' else 'Guid' end + '</th>'+
	+ '<th>' + case when @by = 'By Description' then 'Guid' else 'Description' end + '</th></tr></thead><tbody>'
	else '' end + '<tr><td>'  + 
	case when @by = 'By Description' then Name else guid end + '</td><td>' + 
	case when @by = 'By Description' then guid else name end + '</td></tr>' + 
	case when  lead(name) over (order by case when @by = 'By Description' then Name else guid end) is null then '</tbody></table>'	 else '' end, *
from @typeGuids

--->

**By Description** <br /><table> <thead><tr><th>Description</th><th>Guid</th></tr></thead><tbody><tr><td>ASP.NET 5</td><td>{8BB2217D-0F2D-49D1-97BC-3654ED321F3B}</td></tr>
<tr><td>ASP.NET MVC 1</td><td>{603C0E0B-DB56-11DC-BE95-000D561079B0}</td></tr>
<tr><td>ASP.NET MVC 2</td><td>{F85E285D-A4E0-4152-9332-AB1D724D3325}</td></tr>
<tr><td>ASP.NET MVC 3</td><td>{E53F8FEA-EAE0-44A6-8774-FFD645390401}</td></tr>
<tr><td>ASP.NET MVC 4</td><td>{E3E379DF-F4C6-4180-9B81-6769533ABE47}</td></tr>
<tr><td>ASP.NET MVC 5</td><td>{349C5851-65DF-11DA-9384-00065B846F21}</td></tr>
<tr><td>C#</td><td>{FAE04EC0-301F-11D3-BF4B-00C04F79EFBC}</td></tr>
<tr><td>C# (.Net Core)</td><td>{9A19103F-16F7-4668-BE54-9A1E7A4F7556}</td></tr>
<tr><td>C# Silverlight Project Templates</td><td>{CB22EE0E-4072-4ae7-96E2-90FCCF879544}</td></tr>
<tr><td>C# Web Application Project Templates</td><td>{349C5850-65DF-11DA-9384-00065B846F21}</td></tr>
<tr><td>C# Web MVC Project Templates</td><td>{141DA93E-88A7-45D5-B15B-89117F514D64}</td></tr>
<tr><td>C++</td><td>{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}</td></tr>
<tr><td>CSharp Test Project</td><td>{52CBD135-1F97-2580-011F-C7CD052E44DE}</td></tr>
<tr><td>Database</td><td>{A9ACE9BB-CECE-4E62-9AA4-C7E7C5BD2124}</td></tr>
<tr><td>Database (other project types)</td><td>{4F174C21-8C12-11D0-8340-0000F80270F8}</td></tr>
<tr><td>Deployment Cab</td><td>{3EA9E505-35AC-4774-B492-AD1749C4943A}</td></tr>
<tr><td>Deployment Merge Module</td><td>{06A35CCD-C46D-44D5-987B-CF40FF872267}</td></tr>
<tr><td>Deployment Setup</td><td>{978C614F-708E-4E1A-B201-565925725DBA}</td></tr>
<tr><td>Deployment Smart Device Cab</td><td>{AB322303-2255-48EF-A496-5904EB18DA55}</td></tr>
<tr><td>Distributed System</td><td>{F135691A-BF7E-435D-8960-F99683D2D49C}</td></tr>
<tr><td>Dynamics 2012 AX C# in AOT</td><td>{BF6F8E12-879D-49E7-ADF0-5503146B24B8}</td></tr>
<tr><td>F#</td><td>{F2A71F9B-5D33-465A-A702-920D77279786}</td></tr>
<tr><td>J#</td><td>{E6FDF86B-F3D1-11D4-8576-0002A516ECE8}</td></tr>
<tr><td>Legacy (2003) Smart Device (C#)</td><td>{20D4826A-C6FA-45DB-90F4-C717570B9F32}</td></tr>
<tr><td>Legacy (2003) Smart Device (VB.NET)</td><td>{CB4CE8C6-1BDB-4DC7-A4D3-65A1999772F8}</td></tr>
<tr><td>Micro Framework</td><td>{b69e3092-b931-443c-abe7-7e7b65f2a37f}</td></tr>
<tr><td>Microsoft Silverlight Project Factory</td><td>{CB22EE0E-4072-4ae7-96E2-90FCCF879544}</td></tr>
<tr><td>Model-View-Controller v2 (MVC 2)</td><td>{F85E285D-A4E0-4152-9332-AB1D724D3325}</td></tr>
<tr><td>Model-View-Controller v3 (MVC 3)</td><td>{E53F8FEA-EAE0-44A6-8774-FFD645390401}</td></tr>
<tr><td>Model-View-Controller v4 (MVC 4)</td><td>{E3E379DF-F4C6-4180-9B81-6769533ABE47}</td></tr>
<tr><td>Model-View-Controller v5 (MVC 5)</td><td>{349C5851-65DF-11DA-9384-00065B846F21}</td></tr>
<tr><td>Mono for Android</td><td>{EFBA0AD7-5A72-4C68-AF49-83D382785DCF}</td></tr>
<tr><td>MonoDevelop Addin projects</td><td>{86F6BF2A-E449-4B3E-813B-9ACC37E5545F}</td></tr>
<tr><td>MonoTouch</td><td>{6BC8ED88-2882-458C-8E55-DFD12B67127B}</td></tr>
<tr><td>MonoTouch Binding</td><td>{F5B4F3BC-B597-4E2B-B552-EF5D8A32436F}</td></tr>
<tr><td>Platform Toolset v120</td><td>{8DB26A54-E6C6-494F-9B32-ACBB256CD3A5}</td></tr>
<tr><td>Platform Toolset v141</td><td>{C2CAFE0E-DCE1-4D03-BBF6-18283CF86E48}</td></tr>
<tr><td>Portable Class Library</td><td>{786C830F-07A1-408B-BD7F-6EE04809D6DB}</td></tr>
<tr><td>Project Folders</td><td>{66A26720-8FB5-11D2-AA7E-00C04F688DDE}</td></tr>
<tr><td>Report Project</td><td>{F14B399A-7131-4C87-9E4B-1186C45EF12D}</td></tr>
<tr><td>SharePoint (C#)</td><td>{593B0543-81F6-4436-BA1E-4747859CAAE2}</td></tr>
<tr><td>SharePoint (VB.NET)</td><td>{EC05E597-79D4-47f3-ADA0-324C4F7C7484}</td></tr>
<tr><td>SharePoint Workflow</td><td>{F8810EC1-6754-47FC-A15F-DFABD2E3FA90}</td></tr>
<tr><td>Silverlight</td><td>{A1591282-1198-4647-A2B1-27E5FF5F6F3B}</td></tr>
<tr><td>Smart Device (C#)</td><td>{4D628B5B-2FBC-4AA6-8C16-197242AEB884}</td></tr>
<tr><td>Smart Device (VB.NET)</td><td>{68B1623D-7FB9-47D8-8664-7ECEA3297D4F}</td></tr>
<tr><td>Solution Folder</td><td>{2150E333-8FDC-42A3-9474-1A3956D46DE8}</td></tr>
<tr><td>SSIS</td><td>{159641d6-6404-4a2a-ae62-294de0fe8301}</td></tr>
<tr><td>Test</td><td>{3AC096D0-A1C2-E12C-1390-A8335801FDAB}</td></tr>
<tr><td>Universal Windows Class Library</td><td>{A5A43C5B-DE2A-4C0C-9213-0A381AF9435A}</td></tr>
<tr><td>VB Silverlight Project Templates</td><td>{CB22EE0E-4072-4ae7-96E2-90FCCF879544}</td></tr>
<tr><td>VB Web Application Project Templates</td><td>{349C5850-65DF-11DA-9384-00065B846F21}</td></tr>
<tr><td>VB Web MVC Project Templates</td><td>{141DA93E-88A7-45D5-B15B-89117F514D64}</td></tr>
<tr><td>VB.NET</td><td>{F184B08F-C81C-45F6-A57F-5ABD9991F28F}</td></tr>
<tr><td>Visual Database Tools</td><td>{C252FEB5-A946-4202-B1D4-9916A0590387}</td></tr>
<tr><td>Visual Studio 2015 Installer Project Extension</td><td>{54435603-DBB4-11D2-8724-00A0C9A8B90C}</td></tr>
<tr><td>Visual Studio Tools for Applications (VSTA)</td><td>{A860303F-1F3F-4691-B57E-529FC101A107}</td></tr>
<tr><td>Visual Studio Tools for Office (VSTO)</td><td>{BAA0C2D2-18E2-41B9-852F-F413020CAA33}</td></tr>
<tr><td>VisualBasic Test Project</td><td>{52CBD135-1F97-2580-011F-C7CD052E44DE}</td></tr>
<tr><td>Visucal C++ Test Project</td><td>{52CBD135-1F97-2580-011F-C7CD052E44DE}</td></tr>
<tr><td>Web Application</td><td>{349C5851-65DF-11DA-9384-00065B846F21}</td></tr>
<tr><td>Web Application Project Factory</td><td>{349C5850-65DF-11DA-9384-00065B846F21}</td></tr>
<tr><td>Web MVC 301 Project Factory (Compatibility)</td><td>{141DA93E-88A7-45D5-B15B-89117F514D64}</td></tr>
<tr><td>Web MVC 4 Project Factory (Compatibility)</td><td>{141DA93E-88A7-45D5-B15B-89117F514D64}</td></tr>
<tr><td>Web Site</td><td>{E24C65DC-7377-472B-9ABA-BC803B73C61A}</td></tr>
<tr><td>Windows (C#)</td><td>{FAE04EC0-301F-11D3-BF4B-00C04F79EFBC}</td></tr>
<tr><td>Windows (VB.NET)</td><td>{F184B08F-C81C-45F6-A57F-5ABD9991F28F}</td></tr>
<tr><td>Windows (Visual C++)</td><td>{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}</td></tr>
<tr><td>Windows Communication Foundation (WCF)</td><td>{3D9AD99F-2412-4246-B90B-4EAA41C64699}</td></tr>
<tr><td>Windows Phone 8/8.1 App (C#)</td><td>{C089C8C0-30E0-4E22-80C0-CE093F111A43}</td></tr>
<tr><td>Windows Phone 8/8.1 App (VB.NET)</td><td>{DB03555F-0C8B-43BE-9FF9-57896B3C5E56}</td></tr>
<tr><td>Windows Phone 8/8.1 Blank/Hub/Webview App</td><td>{76F1466A-8B6D-4E39-A767-685A06062A39}</td></tr>
<tr><td>Windows Presentation Foundation (WPF)</td><td>{60DC8134-EBA5-43B8-BCC9-BB4BC16C2548}</td></tr>
<tr><td>Windows Store (Metro) Apps & Components</td><td>{BC8A1FFA-BEE3-4634-8014-F334798102B3}</td></tr>
<tr><td>Workflow (C#)</td><td>{14822709-B5A1-4724-98CA-57A101D1B079}</td></tr>
<tr><td>Workflow (VB.NET)</td><td>{D59BE175-2ED0-4C54-BE3D-CDAA9F3214C8}</td></tr>
<tr><td>Workflow Foundation</td><td>{32F31D43-81CC-4C15-9DE6-3FC5453562B6}</td></tr>
<tr><td>Workflow Project</td><td>{AAFFDC1E-A1C7-47BC-B3DC-9E685DF3959B}</td></tr>
<tr><td>Workflow Visual Basic Project</td><td>{9D2881F7-F482-416C-8D64-CA83326250B9}</td></tr>
<tr><td>Workflow Visual C# Project</td><td>{9D2881F7-F482-416C-8D64-CA83326250B9}</td></tr>
<tr><td>WPF Project Flavor CSharp Templates</td><td>{b3bae735-386c-4030-8329-ef48eeda4036}</td></tr>
<tr><td>WPF Project Flavor Visual Basic Templates</td><td>{b3bae735-386c-4030-8329-ef48eeda4036}</td></tr>
<tr><td>Xamarin.Android</td><td>{EFBA0AD7-5A72-4C68-AF49-83D382785DCF}</td></tr>
<tr><td>Xamarin.iOS</td><td>{6BC8ED88-2882-458C-8E55-DFD12B67127B}</td></tr>
<tr><td>XNA (Windows)</td><td>{6D335F3A-9D43-41b4-9D22-F6F17C4BE596}</td></tr>
<tr><td>XNA (XBox)</td><td>{2DF5C3F4-5A5F-47a9-8E94-23B4456F55E2}</td></tr>
<tr><td>XNA (Zune)</td><td>{D399B71A-8929-442a-A9AC-8BEC78BB2433}</td></tr></tbody></table>

**By Guid** <br /><table> <thead><tr><th>Guid</th><th>Description</th></tr></thead><tbody><tr><td>{06A35CCD-C46D-44D5-987B-CF40FF872267}</td><td>Deployment Merge Module</td></tr>
<tr><td>{141DA93E-88A7-45D5-B15B-89117F514D64}</td><td>C# Web MVC Project Templates</td></tr>
<tr><td>{141DA93E-88A7-45D5-B15B-89117F514D64}</td><td>VB Web MVC Project Templates</td></tr>
<tr><td>{141DA93E-88A7-45D5-B15B-89117F514D64}</td><td>Web MVC 301 Project Factory (Compatibility)</td></tr>
<tr><td>{141DA93E-88A7-45D5-B15B-89117F514D64}</td><td>Web MVC 4 Project Factory (Compatibility)</td></tr>
<tr><td>{14822709-B5A1-4724-98CA-57A101D1B079}</td><td>Workflow (C#)</td></tr>
<tr><td>{159641d6-6404-4a2a-ae62-294de0fe8301}</td><td>SSIS</td></tr>
<tr><td>{20D4826A-C6FA-45DB-90F4-C717570B9F32}</td><td>Legacy (2003) Smart Device (C#)</td></tr>
<tr><td>{2150E333-8FDC-42A3-9474-1A3956D46DE8}</td><td>Solution Folder</td></tr>
<tr><td>{2DF5C3F4-5A5F-47a9-8E94-23B4456F55E2}</td><td>XNA (XBox)</td></tr>
<tr><td>{32F31D43-81CC-4C15-9DE6-3FC5453562B6}</td><td>Workflow Foundation</td></tr>
<tr><td>{349C5850-65DF-11DA-9384-00065B846F21}</td><td>VB Web Application Project Templates</td></tr>
<tr><td>{349C5850-65DF-11DA-9384-00065B846F21}</td><td>Web Application Project Factory</td></tr>
<tr><td>{349C5850-65DF-11DA-9384-00065B846F21}</td><td>C# Web Application Project Templates</td></tr>
<tr><td>{349C5851-65DF-11DA-9384-00065B846F21}</td><td>ASP.NET MVC 5</td></tr>
<tr><td>{349C5851-65DF-11DA-9384-00065B846F21}</td><td>Model-View-Controller v5 (MVC 5)</td></tr>
<tr><td>{349C5851-65DF-11DA-9384-00065B846F21}</td><td>Web Application</td></tr>
<tr><td>{3AC096D0-A1C2-E12C-1390-A8335801FDAB}</td><td>Test</td></tr>
<tr><td>{3D9AD99F-2412-4246-B90B-4EAA41C64699}</td><td>Windows Communication Foundation (WCF)</td></tr>
<tr><td>{3EA9E505-35AC-4774-B492-AD1749C4943A}</td><td>Deployment Cab</td></tr>
<tr><td>{4D628B5B-2FBC-4AA6-8C16-197242AEB884}</td><td>Smart Device (C#)</td></tr>
<tr><td>{4F174C21-8C12-11D0-8340-0000F80270F8}</td><td>Database (other project types)</td></tr>
<tr><td>{52CBD135-1F97-2580-011F-C7CD052E44DE}</td><td>CSharp Test Project</td></tr>
<tr><td>{52CBD135-1F97-2580-011F-C7CD052E44DE}</td><td>VisualBasic Test Project</td></tr>
<tr><td>{52CBD135-1F97-2580-011F-C7CD052E44DE}</td><td>Visucal C++ Test Project</td></tr>
<tr><td>{54435603-DBB4-11D2-8724-00A0C9A8B90C}</td><td>Visual Studio 2015 Installer Project Extension</td></tr>
<tr><td>{593B0543-81F6-4436-BA1E-4747859CAAE2}</td><td>SharePoint (C#)</td></tr>
<tr><td>{603C0E0B-DB56-11DC-BE95-000D561079B0}</td><td>ASP.NET MVC 1</td></tr>
<tr><td>{60DC8134-EBA5-43B8-BCC9-BB4BC16C2548}</td><td>Windows Presentation Foundation (WPF)</td></tr>
<tr><td>{66A26720-8FB5-11D2-AA7E-00C04F688DDE}</td><td>Project Folders</td></tr>
<tr><td>{68B1623D-7FB9-47D8-8664-7ECEA3297D4F}</td><td>Smart Device (VB.NET)</td></tr>
<tr><td>{6BC8ED88-2882-458C-8E55-DFD12B67127B}</td><td>MonoTouch</td></tr>
<tr><td>{6BC8ED88-2882-458C-8E55-DFD12B67127B}</td><td>Xamarin.iOS</td></tr>
<tr><td>{6D335F3A-9D43-41b4-9D22-F6F17C4BE596}</td><td>XNA (Windows)</td></tr>
<tr><td>{76F1466A-8B6D-4E39-A767-685A06062A39}</td><td>Windows Phone 8/8.1 Blank/Hub/Webview App</td></tr>
<tr><td>{786C830F-07A1-408B-BD7F-6EE04809D6DB}</td><td>Portable Class Library</td></tr>
<tr><td>{86F6BF2A-E449-4B3E-813B-9ACC37E5545F}</td><td>MonoDevelop Addin projects</td></tr>
<tr><td>{8BB2217D-0F2D-49D1-97BC-3654ED321F3B}</td><td>ASP.NET 5</td></tr>
<tr><td>{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}</td><td>C++</td></tr>
<tr><td>{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}</td><td>Windows (Visual C++)</td></tr>
<tr><td>{8DB26A54-E6C6-494F-9B32-ACBB256CD3A5}</td><td>Platform Toolset v120</td></tr>
<tr><td>{978C614F-708E-4E1A-B201-565925725DBA}</td><td>Deployment Setup</td></tr>
<tr><td>{9A19103F-16F7-4668-BE54-9A1E7A4F7556}</td><td>C# (.Net Core)</td></tr>
<tr><td>{9D2881F7-F482-416C-8D64-CA83326250B9}</td><td>Workflow Visual Basic Project</td></tr>
<tr><td>{9D2881F7-F482-416C-8D64-CA83326250B9}</td><td>Workflow Visual C# Project</td></tr>
<tr><td>{A1591282-1198-4647-A2B1-27E5FF5F6F3B}</td><td>Silverlight</td></tr>
<tr><td>{A5A43C5B-DE2A-4C0C-9213-0A381AF9435A}</td><td>Universal Windows Class Library</td></tr>
<tr><td>{A860303F-1F3F-4691-B57E-529FC101A107}</td><td>Visual Studio Tools for Applications (VSTA)</td></tr>
<tr><td>{A9ACE9BB-CECE-4E62-9AA4-C7E7C5BD2124}</td><td>Database</td></tr>
<tr><td>{AAFFDC1E-A1C7-47BC-B3DC-9E685DF3959B}</td><td>Workflow Project</td></tr>
<tr><td>{AB322303-2255-48EF-A496-5904EB18DA55}</td><td>Deployment Smart Device Cab</td></tr>
<tr><td>{b3bae735-386c-4030-8329-ef48eeda4036}</td><td>WPF Project Flavor CSharp Templates</td></tr>
<tr><td>{b3bae735-386c-4030-8329-ef48eeda4036}</td><td>WPF Project Flavor Visual Basic Templates</td></tr>
<tr><td>{b69e3092-b931-443c-abe7-7e7b65f2a37f}</td><td>Micro Framework</td></tr>
<tr><td>{BAA0C2D2-18E2-41B9-852F-F413020CAA33}</td><td>Visual Studio Tools for Office (VSTO)</td></tr>
<tr><td>{BC8A1FFA-BEE3-4634-8014-F334798102B3}</td><td>Windows Store (Metro) Apps & Components</td></tr>
<tr><td>{BF6F8E12-879D-49E7-ADF0-5503146B24B8}</td><td>Dynamics 2012 AX C# in AOT</td></tr>
<tr><td>{C089C8C0-30E0-4E22-80C0-CE093F111A43}</td><td>Windows Phone 8/8.1 App (C#)</td></tr>
<tr><td>{C252FEB5-A946-4202-B1D4-9916A0590387}</td><td>Visual Database Tools</td></tr>
<tr><td>{C2CAFE0E-DCE1-4D03-BBF6-18283CF86E48}</td><td>Platform Toolset v141</td></tr>
<tr><td>{CB22EE0E-4072-4ae7-96E2-90FCCF879544}</td><td>VB Silverlight Project Templates</td></tr>
<tr><td>{CB22EE0E-4072-4ae7-96E2-90FCCF879544}</td><td>Microsoft Silverlight Project Factory</td></tr>
<tr><td>{CB22EE0E-4072-4ae7-96E2-90FCCF879544}</td><td>C# Silverlight Project Templates</td></tr>
<tr><td>{CB4CE8C6-1BDB-4DC7-A4D3-65A1999772F8}</td><td>Legacy (2003) Smart Device (VB.NET)</td></tr>
<tr><td>{D399B71A-8929-442a-A9AC-8BEC78BB2433}</td><td>XNA (Zune)</td></tr>
<tr><td>{D59BE175-2ED0-4C54-BE3D-CDAA9F3214C8}</td><td>Workflow (VB.NET)</td></tr>
<tr><td>{DB03555F-0C8B-43BE-9FF9-57896B3C5E56}</td><td>Windows Phone 8/8.1 App (VB.NET)</td></tr>
<tr><td>{E24C65DC-7377-472B-9ABA-BC803B73C61A}</td><td>Web Site</td></tr>
<tr><td>{E3E379DF-F4C6-4180-9B81-6769533ABE47}</td><td>Model-View-Controller v4 (MVC 4)</td></tr>
<tr><td>{E3E379DF-F4C6-4180-9B81-6769533ABE47}</td><td>ASP.NET MVC 4</td></tr>
<tr><td>{E53F8FEA-EAE0-44A6-8774-FFD645390401}</td><td>ASP.NET MVC 3</td></tr>
<tr><td>{E53F8FEA-EAE0-44A6-8774-FFD645390401}</td><td>Model-View-Controller v3 (MVC 3)</td></tr>
<tr><td>{E6FDF86B-F3D1-11D4-8576-0002A516ECE8}</td><td>J#</td></tr>
<tr><td>{EC05E597-79D4-47f3-ADA0-324C4F7C7484}</td><td>SharePoint (VB.NET)</td></tr>
<tr><td>{EFBA0AD7-5A72-4C68-AF49-83D382785DCF}</td><td>Mono for Android</td></tr>
<tr><td>{EFBA0AD7-5A72-4C68-AF49-83D382785DCF}</td><td>Xamarin.Android</td></tr>
<tr><td>{F135691A-BF7E-435D-8960-F99683D2D49C}</td><td>Distributed System</td></tr>
<tr><td>{F14B399A-7131-4C87-9E4B-1186C45EF12D}</td><td>Report Project</td></tr>
<tr><td>{F184B08F-C81C-45F6-A57F-5ABD9991F28F}</td><td>Windows (VB.NET)</td></tr>
<tr><td>{F184B08F-C81C-45F6-A57F-5ABD9991F28F}</td><td>VB.NET</td></tr>
<tr><td>{F2A71F9B-5D33-465A-A702-920D77279786}</td><td>F#</td></tr>
<tr><td>{F5B4F3BC-B597-4E2B-B552-EF5D8A32436F}</td><td>MonoTouch Binding</td></tr>
<tr><td>{F85E285D-A4E0-4152-9332-AB1D724D3325}</td><td>Model-View-Controller v2 (MVC 2)</td></tr>
<tr><td>{F85E285D-A4E0-4152-9332-AB1D724D3325}</td><td>ASP.NET MVC 2</td></tr>
<tr><td>{F8810EC1-6754-47FC-A15F-DFABD2E3FA90}</td><td>SharePoint Workflow</td></tr>
<tr><td>{FAE04EC0-301F-11D3-BF4B-00C04F79EFBC}</td><td>Windows (C#)</td></tr>
<tr><td>{FAE04EC0-301F-11D3-BF4B-00C04F79EFBC}</td><td>C#</td></tr></tbody></table>
