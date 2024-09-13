## `python:3-windowsservercore`

```console
$ docker pull python@sha256:5d143d9dd3f8c9701beea7303b92d48e2ed9496b06d0a52223e435d518cc1214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `python:3-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull python@sha256:b710cd58e9887fb34d71b945dd81f77e786a937cb6c1410aa332c1b6a33d651f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1522085811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2913d856ab9e5a6e9335e62ce484bfd8e19c76704464592bf496ee768badb71d`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 12 Sep 2024 21:06:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Sep 2024 21:06:34 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 12 Sep 2024 21:06:35 GMT
ENV PYTHON_VERSION=3.12.6
# Thu, 12 Sep 2024 21:07:18 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 12 Sep 2024 21:07:18 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f8ea36f673f903fc05544facc9b2b3296c71593d0b671af83dc6d14d6d5395`  
		Last Modified: Thu, 12 Sep 2024 21:07:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db79783a77ab10864a6ef0306dcf60e37f830c810b2efda94e1ac00eca2b5ef5`  
		Last Modified: Thu, 12 Sep 2024 21:07:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d45bae864db9a2e46e65001ccc7319bc1383edc3f9a5b2f2c8d48a68ef9b14`  
		Last Modified: Thu, 12 Sep 2024 21:07:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f1f25d84c1c61e5dc9106f0acb17a7061fe5607b66371f543b379e5b92ddf3`  
		Last Modified: Thu, 12 Sep 2024 21:07:28 GMT  
		Size: 59.9 MB (59888255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71160605541d49bf382c6763564cccec47ecf1402c694fa421bd3433be4e9c5c`  
		Last Modified: Thu, 12 Sep 2024 21:07:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull python@sha256:2e7408189b1aa7b405da7abc0402ea6c61d7e64bba481435b9d0903dcdd5102d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778521702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca09ee21526ac5c83155fc2302f6f5a7c5f6c6cc1aafadbb816da41dbdaca70`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 12 Sep 2024 21:08:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Sep 2024 21:08:10 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 12 Sep 2024 21:08:10 GMT
ENV PYTHON_VERSION=3.12.6
# Thu, 12 Sep 2024 21:09:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 12 Sep 2024 21:09:22 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a8a3fa39ca74aa60ecd3111a61827b15d11f6220ed097e223019d119e21abc`  
		Last Modified: Thu, 12 Sep 2024 21:09:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360d1a51576275a94cd0dfe8a124e3cd0fa110822e7eb01a0afad14a7e7795e4`  
		Last Modified: Thu, 12 Sep 2024 21:09:26 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0679e2bae2b8b434fde6871c386c1140ab11c61007ddbfbdd60e868ce24186`  
		Last Modified: Thu, 12 Sep 2024 21:09:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b079c6f85c40bb3e514712ee4ac201db9d1df0ad78beabf1ec21f7f4a9cd6ef`  
		Last Modified: Thu, 12 Sep 2024 21:09:31 GMT  
		Size: 58.2 MB (58248193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d93350a2bf1b16dd17176bf472125c26f00d23e340a37c9d0897e27f5ae196e`  
		Last Modified: Thu, 12 Sep 2024 21:09:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
