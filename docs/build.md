



# CAA TCK TOOLS

=== "V5"

### step1
"C:\Program Files\Dassault Systemes\T27\win_b64\code\command\tck_init.bat"

### step2	
	cmd输入
	tck_list
	会显示一下结果

	SCM_adm_V5_6R2017_B27 tckDevTools_V5_6R2017_B27 SCM_adm_V5_6R2017_B27
	V5_6R2017_B27 Mkmk_V5_6R2017_B27 tckDevTools_V5_6R2017_B27 CSC_V5_6R2017_B27
	V6R2021x_B423 Mkmk_V6R2021x_B423 tckDevTools_V6R2021x_B423 CSC_V6R2021x_B423

### step3	
	cmd输入
	Tck_list V5_6R2017_B27 -all
	会显示一下结果

	SCM_adm_V5_6R2017_B27 user 2023/03/07-19:30:34 local
	Type = Official
	tckDevTools_V5_6R2017_B27 2023/03/07-19:30:34 local
		Windows NT: C:\Program Files\Dassault Systemes\T27\win_b64\code\command\tckDevTools_init.bat
	SCM_adm_V5_6R2017_B27 2023/03/07-19:30:34 local
		Windows NT: C:\Program Files\Dassault Systemes\T27\win_b64\code\command\admin\adl_profile_adm.bat
	V5_6R2017_B27 user 2023/03/07-19:30:34 local
	Type = Official
	Mkmk_V5_6R2017_B27 2023/03/07-19:30:34 local
		Windows NT: C:\Program Files\Dassault Systemes\T27\win_b64\code\command\mkinit.bat
	tckDevTools_V5_6R2017_B27 2023/03/07-19:30:34 local
		Windows NT: C:\Program Files\Dassault Systemes\T27\win_b64\code\command\tckDevTools_init.bat
	CSC_V5_6R2017_B27 2023/03/07-19:30:34 local
		Windows NT: C:\Program Files\Dassault Systemes\T27\win_b64\code\command\mkcsinit.bat


### step4

ADD:

	```batch
	tck_update_local V5_6R2017_B27 -tool Mkmk_V5_6R2017_B27 -profile "C:\Program Files\Dassault Systemes\T22\win_b64\code\command\mkinit.bat"
	tck_update_local V5_6R2017_B27 -tool tckDevTools_V5_6R2017_B27 -profile "C:\Program Files\Dassault Systemes\T22\win_b64\code\command\tckDevTools_init.bat"
	tck_update_local V5_6R2017_B27 -tool CSC_V5_6R2017_B27 -profile "C:\Program Files\Dassault Systemes\T22\win_b64\code\command\mkcsinit.bat"
	```

REMOVE:

	```batch

	tck_update_local V5_6R2017_B27 -tool Mkmk_V5_6R2017_B27 -remove  "C:\Program Files\Dassault Systemes\T27\win_b64\code\command\mkinit.bat"
	tck_update_local V5_6R2017_B27 -tool tckDevTools_V5_6R2017_B27 -remove "C:\Program Files\Dassault Systemes\T27\win_b64\code\command\tckDevTools_init.bat"
	tck_update_local V5_6R2017_B27 -tool CSC_V5_6R2017_B27 -remove  "C:\Program Files\Dassault Systemes\T27\win_b64\code\command\mkcsinit.bat"

	```

'*******************************************************************************************

### Tool help

	```batch

	C:\Users\user>tck_update_local
	Running command: tck_update_local
	#ERR# ADLBC - 0004: tck_update_local requires one argument
	Usage: tck_update_local TCK [-tool Tool] [-profile profile | -remove] [-os] [-h|-help|-?]
		tck_update_local TCK -tool Tool [-profile profile]
		tck_update_local TCK -tool Tool -remove
		tck_update_local TCK -remove

	```

	Tck_list V6R2021x_B423 -all,会显示一下结果

'*******************************************************************************************

### step1
```batch
"C:\dev\T423\win_b64\code\command\tck_init.bat"
```
### step2

#### add

	```batch

	tck_update_local V6R2021x_B423 -tool tckDevTools_V5_6R2017_B27 -profile "C:\dev\T423\win_b64\code\command\tckDevTools_init.bat"
	tck_update_local V6R2021x_B423 -tool SCM_adm_V5_6R2017_B27 -profile "C:\dev\T423\win_b64\code\command\admin\adl_profile_adm.bat"
	tck_update_local V6R2021x_B423 -tool Mkmk_V6R2021x_B423 -profile  "C:\dev\T423\win_b64\code\command\mkinit.bat"
	tck_update_local V6R2021x_B423 -tool tckDevTools_V6R2021x_B423 -profile "C:\dev\T423\win_b64\code\command\tckDevTools_init.bat"
	tck_update_local V6R2021x_B423 -tool CSC_V6R2021x_B423 -profile  "C:\dev\T423\win_b64\code\command\mkcsinit.bat"
	tck_update_local V6R2021x_B423 -profile

	```

#### remove

	```batch

	tck_update_local V6R2021x_B423 -tool tckDevTools_V5_6R2017_B27 -remove "C:\dev\T423\win_b64\code\command\tckDevTools_init.bat"
	tck_update_local V6R2021x_B423 -tool SCM_adm_V5_6R2017_B27 -remove "C:\dev\T423\win_b64\code\command\admin\adl_profile_adm.bat"
	tck_update_local V6R2021x_B423 -tool Mkmk_V6R2021x_B423 -remove  "C:\dev\T423\win_b64\code\command\mkinit.bat"
	tck_update_local V6R2021x_B423 -tool tckDevTools_V6R2021x_B423 -remove "C:\dev\T423\win_b64\code\command\tckDevTools_init.bat"
	tck_update_local V6R2021x_B423 -tool CSC_V6R2021x_B423 -remove  "C:\dev\T423\win_b64\code\command\mkcsinit.bat"
	tck_update_local V6R2021x_B423 -remove

	```

	

