## `hylang:python3.13-rc-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:6d37c7b2718c36c47b708b94f026df614feadd708ce317fd2f21f4dbc9cf036d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `hylang:python3.13-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull hylang@sha256:cc10dd654b4526d82b92d7473246e5f311fe3a12462f00a9eaa64e2f05669cdc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1530125973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb9b613cb0da81088fe3f4ef49cc84572692760abffe35fc4eceb38d65953c0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 12 Sep 2024 21:08:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Sep 2024 21:08:21 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 12 Sep 2024 21:08:22 GMT
ENV PYTHON_VERSION=3.13.0rc2
# Thu, 12 Sep 2024 21:09:33 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 12 Sep 2024 21:09:33 GMT
CMD ["python"]
# Tue, 24 Sep 2024 01:03:03 GMT
ENV HY_VERSION=1.0.0
# Tue, 24 Sep 2024 01:03:04 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 24 Sep 2024 01:04:05 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 24 Sep 2024 01:04:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fb02669e1c7a7c5c299e3860b307a51f514d4607cccb978a00ed5a89f9f8f0`  
		Last Modified: Thu, 12 Sep 2024 21:09:36 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76f2596d1965bedcc8f6f1cec27181875a54b0cd1ecbc515a8452e204c78727`  
		Last Modified: Thu, 12 Sep 2024 21:09:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df128227eb9d381fd2041cd713db2074be7cde2f15426b5aea816418c4a446e`  
		Last Modified: Thu, 12 Sep 2024 21:09:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1868a18ba69e19b7aac03f63288067a759a29ec4a363b4dff734300d94f33242`  
		Last Modified: Thu, 12 Sep 2024 21:09:40 GMT  
		Size: 59.1 MB (59066041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbc747e898cfb45be2a972b2ea5d8c227822126bef3d2224a47fb4a77ce26a3`  
		Last Modified: Thu, 12 Sep 2024 21:09:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5428141648305c4c70913eff4ac7411c1aa60a23cd720d6646718270ef90635`  
		Last Modified: Tue, 24 Sep 2024 01:04:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d3cef2376250b66471154604fcae7cd3829b7438696825fcbc2c0fa5754379`  
		Last Modified: Tue, 24 Sep 2024 01:04:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9f79a31d0fa3c3a6f610e370c62f2612d942793e6d58a0443d0796f3949c22`  
		Last Modified: Tue, 24 Sep 2024 01:04:11 GMT  
		Size: 8.9 MB (8858504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccad436a2a915d482b98ec66b4a109ca126871bc0fa8d6c02aa7a1e24a29a9dd`  
		Last Modified: Tue, 24 Sep 2024 01:04:09 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
