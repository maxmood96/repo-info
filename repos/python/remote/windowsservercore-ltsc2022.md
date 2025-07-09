## `python:windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:ce7589d83a47711703788b095c0c08b99f321423e0b51dd4ca9967c3bb1419d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `python:windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull python@sha256:a1dea822f5ade175f3640a0c7b5372cc967c364b936018d3befe553cecb66785
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2339724833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4250eca2e9ee1cd2cdb98f8a5f00f11c3967b420cfd8f58f4f6113521200acf5`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:18:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:18:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Jul 2025 18:18:47 GMT
ENV PYTHON_VERSION=3.13.5
# Wed, 09 Jul 2025 18:18:48 GMT
ENV PYTHON_SHA256=c1cb40978b28f696b111c36034a1bdeda17d25e35c74a08ef5e5ff405a63fc20
# Wed, 09 Jul 2025 18:19:53 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:19:57 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1711877ca996bed7e85f73e15f121a6332e31b065e5ca18b8c7556e85f754fb3`  
		Last Modified: Wed, 09 Jul 2025 19:08:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3a63d25932d061554da048646ec64b6451f40ad4e9b6a4cf8257eedda3100f`  
		Last Modified: Wed, 09 Jul 2025 19:08:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4e2ebdbde9a04823c5dd4edd57d79e3653e3f77d3c9cd48e3ceb44b6a764a8`  
		Last Modified: Wed, 09 Jul 2025 19:08:21 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4e0f04648b13befdf1765c65192056c1b6a99c114f8c5e052fd59b065fb69`  
		Last Modified: Wed, 09 Jul 2025 19:08:21 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9352a6fe37ddffc06d405e31eaf9fe6c11a0242d4a6eb10e4b9bc176654985`  
		Last Modified: Wed, 09 Jul 2025 19:08:27 GMT  
		Size: 59.1 MB (59114909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c061fadb8aefeb1d15ddb13adeb0183be5b8b68b9c48e6cf390c1c26dfa38f`  
		Last Modified: Wed, 09 Jul 2025 19:08:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
