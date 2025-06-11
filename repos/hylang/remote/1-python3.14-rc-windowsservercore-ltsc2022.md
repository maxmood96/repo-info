## `hylang:1-python3.14-rc-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:53d9ce8a6f3123044068938bf0f8f05156697ca9773dfb79df1f0b024b14731a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `hylang:1-python3.14-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull hylang@sha256:960ea3bb6431a5be6c1600651e7081cb811bc158e21c619ad27c463dbc0fdb7b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349751788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d98c9ad16787ba69b617b12554db27ce3ffc2cd5244f24ebd84c1fe84a3587`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:34:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:34:14 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 10 Jun 2025 21:34:15 GMT
ENV PYTHON_VERSION=3.14.0b2
# Tue, 10 Jun 2025 21:34:16 GMT
ENV PYTHON_SHA256=279b1d0e2b1b6cece6f03e49218aacccfd10367e07b785edeb1d4135507434c1
# Tue, 10 Jun 2025 21:34:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:35:00 GMT
CMD ["python"]
# Tue, 10 Jun 2025 22:13:21 GMT
ENV HY_VERSION=1.1.0
# Tue, 10 Jun 2025 22:13:22 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 10 Jun 2025 22:13:54 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 10 Jun 2025 22:13:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cca587f28ebf4d9feda2a212619caf7b13fe722ee34d8951557c96e30f4ee88`  
		Last Modified: Tue, 10 Jun 2025 22:09:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610228a20e4ad3405b8e957069ec8d0dc27e7118e2e7f953536cde1e5a27fc52`  
		Last Modified: Tue, 10 Jun 2025 22:09:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3562303e4b5bc00d0728bebc520a3f433ebf55eb31cedd24a82e991343c0024`  
		Last Modified: Tue, 10 Jun 2025 22:09:08 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7940dddcc05a8ce3ed351160fb4061d5f3a27b750457f3dd0ab4fc3c817d4d58`  
		Last Modified: Tue, 10 Jun 2025 22:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a564cbfed04b696715f0ea191da09fdb504654a9f3e23187e1e3c6d8b810333`  
		Last Modified: Tue, 10 Jun 2025 22:09:16 GMT  
		Size: 61.0 MB (60968985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122393cae925036f14a18bdf60c0cbd117203ca256287741a0739016cbb3c817`  
		Last Modified: Tue, 10 Jun 2025 22:09:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6049bac7016748ee36145038e31c2f19abc083dfad451bd64d045076fd0f78`  
		Last Modified: Tue, 10 Jun 2025 22:14:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce9bceb510b0a84418742bc6fb734cd45eb8dae974c6bd6b56fbf40a32a7371`  
		Last Modified: Tue, 10 Jun 2025 22:14:20 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9808e0edaf1308a27dd33d08210d6a287f858b5e26506d78bbc5cf5823608165`  
		Last Modified: Tue, 10 Jun 2025 22:14:21 GMT  
		Size: 8.5 MB (8520959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207d09ec6b71ad1be48415fa9c293283ec48c03bf1073a9bf15fee4b27e2544d`  
		Last Modified: Tue, 10 Jun 2025 22:14:20 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
