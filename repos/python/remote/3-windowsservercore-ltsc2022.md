## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:583561d02f4b17aa7d373e149d246108432284d28447bf6bfe744a85eb37ff79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull python@sha256:332d898731284a3a11d3ab4bc4bfb274dabf49069a950cdc66de41e256888455
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321490563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f522046ebff2318ff1c38ff0e0c54129a9fc0a461cda1e9f64786f30515c5ade`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:40:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:40:29 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Jan 2025 23:40:29 GMT
ENV PYTHON_VERSION=3.13.1
# Tue, 14 Jan 2025 23:40:30 GMT
ENV PYTHON_SHA256=6b33fa9a439a86f553f9f60e538ccabc857d2f308bc77c477c04a46552ade81f
# Tue, 14 Jan 2025 23:41:16 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:41:17 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6eeca0c6777296f5a2ff701e1ca47d39877cea66acfcff29785ac90221974e`  
		Last Modified: Tue, 14 Jan 2025 23:41:23 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948e43b1ed2a0a0147428eb25e98580622f23b76e07631dce002fc91f358673`  
		Last Modified: Tue, 14 Jan 2025 23:41:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5d8730289ec58d71427ff3175ae575f7342b395d1f39450f124edde66097eb`  
		Last Modified: Tue, 14 Jan 2025 23:41:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2498bd05730bdee7c4fd031ea2f40d30ef18edf15cdf09f4bd40c38b960be281`  
		Last Modified: Tue, 14 Jan 2025 23:41:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24eaa89f8578fffb2e4fbd1f5941863060f0ec43cd438c666b6b3ff58a932467`  
		Last Modified: Tue, 14 Jan 2025 23:41:27 GMT  
		Size: 59.1 MB (59098857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e051c54df0b95ce6092efbd200ea4149433db85a5eed8f88c1f64af6f280fa7f`  
		Last Modified: Tue, 14 Jan 2025 23:41:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
